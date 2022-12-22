# Cross Currency Option Valuation

A cross currency option is a currency translated option of the type foreign equity option struck in domestic currency, which is a call or put on a foreign asset with a strike price set in domestic currency and payoff measured in domestic currency.

The spot underlying price in foreign currency is converted into an amount in domestic currency using the spot exchange rate.  This amount is then adjusted by the current value of predicted future discrete dividends, measured in domestic currency.

Let   be the stock price measured in a foreign currency.  Let   be the exchange rate, quoted in domestic currency per one unit of foreign currency.  A non-quanto cross currency European vanilla call option has a payoff at the maturity T

					 						(1)

where K is the strike measured in domestic currency.  The payoff is also measured in domestic currency.  For an Asian call option, the payoff is

					 						(2)

where   are the average dates and  .

Since there are two sources of uncertainties involved in the option, one resulting from underlying price changes and the other resulting from changes in the exchange rate, this option is non-quanto.  The holder of the option bears the risk caused by the fluctuation of the exchange rate between the underlying currency and the payoff currency.  

The domestic risk-neutral processes for   and   are

					 						(3)		

And

					 			(4)

where r is the domestic risk free interest rate,   is the foreign risk free interest rate, q is the dividend yield,   is the volatility of the underlying stock,   is the volatility of the exchange rate, and   is the correlation coefficient between the rate of return of the foreign underlying stock and the exchange rate.  Also

					 							(5)
					 						(6)

And

					 .						(7)

Here   is two-dimensional standard Brownian motion under the risk-neutral measure Q.  

Appling Ito’s Lemma, we have

					 .				(8) 

Substituting (3) to (7) into (8), we obtain

					 .			(9)

Thus,   is log-normal, with a drift of domestic risk free rate r minus dividend yield q, and a volatility of

	 .						(10)

The values of vanilla European call/put options can be calculated by using the closed form Black-Scholes formula.  For Asian options of European style, either Monte Carlo simulation or the Michael Curran’s approximation can be employed for pricing.  Instead of using  , the composite volatility   must be used in these pricing formulae.

As to the discrete dividends, since they are a riskless component in the stock price dynamic, the spot stock price should be reduced by the present value of all the dividends during the life of the option.  Let   be the current value date.   Taking the predicted discrete dividends of the underlying stock into account, the translated stock price at time zero is given by

					  						(11)

where m is the number of dividends paid during the option period,   is the dividend payment date,   is the forward exchange rate corresponding to the dividend payment date  ,   is the domestic risk free interest rate (ref. https://finpricing.com/lib/IrCurveIntroduction.html) corresponding to .

The aforementioned options are actually currency translated options of the type foreign equity option struck in domestic currency, which is a call or put on a foreign asset with a strike price set in domestic currency and payoff measured in domestic currency.

