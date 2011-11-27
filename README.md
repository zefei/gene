This is a very (could be overly) simple simulation of the wipeout gene described <a href="http://www.scientificamerican.com/article.cfm?id=the-wipeout-gene">here</a>.
It is discussed <a href="http://www.reddit.com/r/science/comments/mq9jh/the_wipeout_gene_a_new_breed_of_genetically/">here</a> on Reddit,
and the source of is page is hosted <a href="http://github.com/zefei/gene">here</a> on Github.

The simple model used here assumes that at every iteration,
an uninfected pair of mosquitos produces some uninfected offsprings.<br />
The number of healthy offsprings (of each sex) for each pair is a function of the current total number of that sex,
the original number of that sex, and a resilience coefficient (in [0, 1]).<br />
The function is MIN((original_total / current_total) ^ resilience, 1000),
implying that the nature has an inertia to restore any changes.<br />
Also, an infected pair of mosquitos produces some infected male offsprings,
the number of which also follows the resilience function.
