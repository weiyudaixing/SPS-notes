# Symbols, Patterns and Signals

## A6. Probabilistic Data Modelling

With a deterministic model, we don’t model any uncertainties or ‘randomness’ in the data. In some applications this is not a problem, but in others, we can benefit from using a *probabilistic model*.

Now, instead of modelling <img src="tex/d12d945985b54186e47b52d15438b151.svg?invert_in_darkmode&sanitize=true" align=middle width=146.972925pt height=22.063469999999988pt/>, we account for error with <img src="tex/68dd132c118c879031afc40cc18d69f3.svg?invert_in_darkmode&sanitize=true" align=middle width=174.7185pt height=22.063469999999988pt/>, where <img src="tex/8cd34385ed61aca950a6b06d09fb50ac.svg?invert_in_darkmode&sanitize=true" align=middle width=7.9764465000000095pt height=13.387440000000009pt/> is a random number, usually close to zero. This says that, if we have a large number of samples, on average, we expect to see a linear relationship between weight and length.

‘Random’ does not mean <img src="tex/8cd34385ed61aca950a6b06d09fb50ac.svg?invert_in_darkmode&sanitize=true" align=middle width=7.9764465000000095pt height=13.387440000000009pt/> can take on arbitrary values at any time. It simply means we are uncertain as to what value it will have at any given time, and we build that uncertainty into our model. We do this formally with **random variables** and **probability theory**.

For example, we could model the length of a species as being distributed around the average length with a certain spread, i.e. length = average length + <img src="tex/8cd34385ed61aca950a6b06d09fb50ac.svg?invert_in_darkmode&sanitize=true" align=middle width=7.9764465000000095pt height=13.387440000000009pt/>. If we only take one sample, it’s hard to estimate what the average is, so we need lots of data to use the model.

### Continuous random variables

<p align="center"><img src="tex/720a5b5576f0f1507079a57e66153a97.svg?invert_in_darkmode&sanitize=true" align=middle width=194.0136pt height=41.27887499999999pt/></p>
<p align="center"><img src="tex/cae57eae8983308d9d42b8f6a5c6b045.svg?invert_in_darkmode&sanitize=true" align=middle width=234.4419pt height=39.61221pt/></p>

#### Normal distribution

<p align="center"><img src="tex/c2d268812a5ab2872ca0246c248ddda5.svg?invert_in_darkmode&sanitize=true" align=middle width=99.17985pt height=18.312359999999998pt/></p>
<p align="center"><img src="tex/2c730eea83158095420d965fbd4a27ba.svg?invert_in_darkmode&sanitize=true" align=middle width=205.81605pt height=39.789089999999995pt/></p>

##### Vector normal

<p align="center"><img src="tex/796895e15022c9d1123603f4b7661394.svg?invert_in_darkmode&sanitize=true" align=middle width=307.8768pt height=39.45249pt/></p>

### Marginal distribution

For a vector (multi-dimensional) distribution, we can find the marginal distribution of one dimension, i.e. the distribution of one variable without assumption of the others, by summing/integrating over all the others:

For 2D continuous: <img src="tex/56c79c8ef85bfc677e63fe5b4f2fef69.svg?invert_in_darkmode&sanitize=true" align=middle width=341.6688pt height=45.81357pt/>

For independent dimensions, <img src="tex/d96e2a29a773f4a08bcf30bf75be0497.svg?invert_in_darkmode&sanitize=true" align=middle width=118.40729999999999pt height=23.890019999999986pt/>

### Probabilistic line fitting

<p align="center"><img src="tex/2b901397a6e8e33087d5878b8834fc4b.svg?invert_in_darkmode&sanitize=true" align=middle width=174.40664999999998pt height=14.611871999999998pt/></p>

Assume that <img src="tex/3454df22382541cf6ff82f66ff974486.svg?invert_in_darkmode&sanitize=true" align=middle width=95.59605pt height=27.177810000000004pt/>. Use **Maximum Likelihood** estimation:

<p align="center"><img src="tex/9089f0d09d53eb4efb42e99137b7f64f.svg?invert_in_darkmode&sanitize=true" align=middle width=268.80809999999997pt height=16.438356pt/></p>
<p align="center"><img src="tex/354e0d230f3b43d9b6d9c06bf5c4bdd2.svg?invert_in_darkmode&sanitize=true" align=middle width=170.9037pt height=22.19184pt/></p>

Assume that all the measurements are independent: <img src="tex/e162625f55a30198f65e22edd597908f.svg?invert_in_darkmode&sanitize=true" align=middle width=182.93384999999998pt height=56.15642999999997pt/>.

Since <img src="tex/3454df22382541cf6ff82f66ff974486.svg?invert_in_darkmode&sanitize=true" align=middle width=95.59605pt height=27.177810000000004pt/> in <img src="tex/2a063846d27e5a2005b4a988e6f83357.svg?invert_in_darkmode&sanitize=true" align=middle width=76.72995pt height=18.41036999999999pt/>, we get <img src="tex/9b69b50c35ce9d5fc911459cef00022f.svg?invert_in_darkmode&sanitize=true" align=middle width=182.41740000000001pt height=27.177810000000004pt/>.

<p align="center"><img src="tex/282e06b7d769ac49b38ed60c8ef27bf4.svg?invert_in_darkmode&sanitize=true" align=middle width=361.3203pt height=39.789089999999995pt/></p>
<p align="center"><img src="tex/068fc0653a43340fb868b78b076af64e.svg?invert_in_darkmode&sanitize=true" align=middle width=327.69989999999996pt height=43.8966pt/></p>
<p align="center"><img src="tex/b3b27c12ddaa3707f784ddea2552b1c9.svg?invert_in_darkmode&sanitize=true" align=middle width=210.4608pt height=36.655409999999996pt/></p>
<p align="center"><img src="tex/527f3486024ec87a07cc02b91f7320ef.svg?invert_in_darkmode&sanitize=true" align=middle width=110.153175pt height=39.878685pt/></p>

This gives the same results as with deterministic model.
