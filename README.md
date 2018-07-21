[![Build Status](https://app.bitrise.io/app/30780cbfc9482ff6/status.svg?token=q24RvGeSG3hQiDJi_GQyFQ&branch=master)](https://app.bitrise.io/app/30780cbfc9482ff6)

# VaderSharp. The best sentiment analysis tool. In C#.

**NOTE:** This is a fork of [codingupastorm](https://github.com/codingupastorm)'s excellent [VaderSharp library](https://github.com/codingupastorm/vadersharp).

"VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media."

Previously VADER was only available in python (https://github.com/cjhutto/vaderSentiment). I wanted to use it in C# so ported it over.

# Getting Started

VaderSharp supports:

- .NET Core
- ~.NET Framework 3.5 and above~
- Mono & Xamarin
- UWP

To install VaderSharp, run the following command in the Package Manager Console:

```
Install-Package Dids.VaderSharp
```

# Usage

Import the package at the top of the page:

```c#
using VaderSharp;
```

Then just initialize an instance of SentimentIntensityAnalyzer and call it's PolarityScores method:

```c#
SentimentIntensityAnalyzer analyzer = new SentimentIntensityAnalyzer();

var results = analyzer.PolarityScores("Wow, this package is amazingly easy to use");

Console.WriteLine("Positive score: " + results.Positive);
Console.WriteLine("Negative score: " + results.Negative);
Console.WriteLine("Neutral score: " + results.Neutral);
Console.WriteLine("Compound score: " + results.Compound);
```
