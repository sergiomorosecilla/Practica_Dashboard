## ATP Tennis Rankings, Results, and Stats


FUENTE: https://github.com/JeffSackmann/tennis_atp.git

This contains my master ATP player file, historical rankings, results, and match stats.

There are some tour-level matches with missing stats. Some are missing because ATP doesn't have them. Others I've deleted because they didn't pass some sanity check (loser won 60% of points, or match time was under 20 minutes, etc). Also, Davis Cup matches are included in the tour-level files, but there are no stats for Davis Cup matches until the last few seasons.


# Attention

Please read, understand, and abide by the license below. It seems like a reasonable thing to ask, given the hundreds of hours I've put into amassing and maintaining this dataset. Unfortunately, a few bad apples have violated the license, and when people do that, it makes me considerably less motivated to continue updating.

Also, if you're using this for academic/research purposes (great!), take a minute and cite it properly. It's not that hard, it helps others find a useful resource, and let's face it, you should be doing it anyway.

# License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Dataset" property="dct:title" rel="dct:type">Tennis databases, files, and algorithms</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://www.tennisabstract.com/" property="cc:attributionName" rel="cc:attributionURL">Jeff Sackmann / Tennis Abstract</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/JeffSackmann" rel="dct:source">https://github.com/JeffSackmann</a>.

In other words: Attribution is required. Non-commercial use only. 









* Many of the columns in the 'matches' files are self-explanatory, or are very similar to previous columns.

tourney_id
- a unique identifier for each tournament, such as 2020-888. The exact formats are borrowed from several different sources, so while the first four characters are always the year, the rest of the ID doesn't follow a predictable structure.

tourney_name
surface
draw_size
- number of players in the draw, often rounded up to the nearest power of 2. (For instance, a tournament with 28 players may be shown as 32.)

tourney_level
- For men: 'G' = Grand Slams, 'M' = Masters 1000s, 'A' = other tour-level events, 'C' = Challengers, 'S' = Satellites/ITFs, 'F' = Tour finals and other season-ending events, and 'D' = Davis Cup 
- For women, there are several additional tourney_level codes, including 'P' = Premier, 'PM' = Premier Mandatory, and 'I' = International. The various levels of ITFs are given by the prize money (in thousands), such as '15' = ITF $15,000. Other codes, such as 'T1' for Tier I (and so on) are used for older WTA tournament designations. 'D' is used for Federation/Fed/Billie Jean King Cup, and also for Wightman Cup and Bonne Bell Cup.

- Others, eventually for both genders: 'E' = exhibition (events not sanctioned by the tour, though the definitions can be ambiguous), 'J' = juniors, and 'T' = team tennis, which does yet appear anywhere in the dataset but will at some point.

tourney_date
- eight digits, YYYYMMDD, usually the Monday of the tournament week.

match_num
- a match-specific identifier. Often starting from 1, sometimes counting down from 300, and sometimes arbitrary. 

winner_id
- the player_id used in this repo for the winner of the match

winner_seed
winner_entry
- 'WC' = wild card, 'Q' = qualifier, 'LL' = lucky loser, 'PR' = protected ranking, 'ITF' = ITF entry, and there are a few others that are occasionally used.

winner_name
winner_hand
- R = right, L = left, U = unknown. For ambidextrous players, this is their serving hand.
winner_ht
- height in centimeters, where available

winner_ioc
- three-character country code

winner_age
- age, in years, as of the tourney_date

loser_id
loser_seed
loser_entry
loser_name
loser_hand
loser_ht
loser_ioc
loser_age
score
best_of
- '3' or '5', indicating the the number of sets for this match

round
minutes
- match length, where available

w_ace
- winner's number of aces
w_df
- winner's number of doubles faults
w_svpt
- winner's number of serve points
w_1stIn
- winner's number of first serves made
w_1stWon
- winner's number of first-serve points won
w_2ndWon
- winner's number of second-serve points won
w_SvGms
- winner's number of serve games
w_bpSaved
- winner's number of break points saved
w_bpFaced
- winner's number of break points faced

l_ace
l_df
l_svpt
l_1stIn
l_1stWon
l_2ndWon
l_SvGms
l_bpSaved
l_bpFaced

winner_rank
- winner's ATP or WTA rank, as of the tourney_date, or the most recent ranking date before the tourney_date
winner_rank_points
- number of ranking points, where available
loser_rank
loser_rank_points

* _doubles_ files notes

The matches_doubles files have similar columns, though not all in the same order.

The identifying information for each player refers to 'winner1', 'winner2', 'loser1', and 'loser2'. The labels 1 and 2 are not assigned for any particular reason.

In general, the tournament IDs for doubles results are the same as for singles results (so, for instance, you can see which players entered both draws at the same event), though this is not guaranteed for every single tournament, since some of the data came from different sources.

The stats columns ('w_ace' etc) are per *team*, not per player. That's a function of how tennis stats are typically recorded, not a decision on my part.
