# LIBOR Rate Model Introduction

LIBOR Rate Model is used for pricing Libor-rate based derivative securities. The model is applied, primarily, to value instruments that settle at a Libor-rate reset point.  In order to value instruments that settle at points intermediate to Libor resets, we calculate the numeraire value at the settlement time by interpolating the numeraire at bracketing Libor reset points. 

Libor rate model is very useful to price callable exotics. Many derivatives have callable features. Callable exotics are among the most challenging derivatives to price. These products are loosely defined by the provision that gives the holder or issuer the right to call the product after a lock-out period (more details at https://finpricing.com/lib/EqCallable.html).

Let   denote a Libor rate that sets at time   for an accrual period  .  A European caplet on   is an option with payoff at   of the form
 .
Similarly, a floorlet has payoff of the form
 .

Consider a European option on a fixed-for-floating-rate swap specified by
•	forward start time,  ,
•	set of future resets,  , where  ,
•	floating-leg payments of   at  where   denotes the spot Libor at   for the accrual period  .
A European payer swaption has payoff at   of the form
 
where
 
is the spot swap rate at time  .  A European receiver swaption has payoff at   of the form
 .

Consider a set of future Libor reset dates,  , where  .  Let   denote the forward Libor rate, as seen at time  , which sets at time   for the accrual period  .     We seek to model Libor rates under the spot Libor measure, which has numeraire process,
 ,
where   denotes the price at time   of a zero coupon bond with maturity of  .  

Let   denote the integer,  , such that  .  Under the spot Libor measure, WM assumes that
	           		(3.1)

for  , where
•	   is a vector of uncorrelated, standard Brownian motions,
•	  is a time deterministic volatility vector, which we define below.

We primarily consider interest rate derivatives that depend on the set of Libor rates above,  , and that settle at one of the reset times above,  .  Consider, for example, a payoff,  , at time  .  This payoff then has value 
 .

A volatility vector is of the form
 .
Here
 

Furthermore
 
where
 

Here
 
denotes a Chebyshev polynomial of the first kind.

In the above, the parameters   and   are determined from calibration.


