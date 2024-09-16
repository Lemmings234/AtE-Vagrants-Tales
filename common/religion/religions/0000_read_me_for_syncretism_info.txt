# Hi! This is Mygavolt, the dev largely responsible for ATE's complex doctrine and syncretism setup
# I'm writing this read me for future devs or enterprising submodders so they know how to set up their faith so syncretism functions correctly
# In order for faiths with a Syncretism tenet that sets to Astray to function correctly, you need to give that faith its corresponding invisible doctrine
# These doctrines can be found in 000_syncretism_related_doctrines, as the syncretism_override_doctrine and americanist_syncretism_variation doctrine sets
# Custom faiths made over the course of the game will get these doctrines naturally in the faith_creation on_action - for starting faiths, you need to add them manually
# That will look like the following example from Anglican:

# doctrine = doctrine_catholic_syncretism
# doctrine = catholic_override_doctrine

# You will also need to do this with Inter-Faith Services, La Mano de Dios, and Las Veinte Verdades. That will be discussed after the syncretism stuff

# This is necessary for the following syncretic tenets. Americanism is a unique case, and will be addressed later
# Catholic Syncretism
# Protestant Syncretism
# Latter Day Saints Syncretism
# Eastern Christian Syncretism
# Reawakened Syncretism
# Divina Patriota Syncretism
# Veteranic Syncretism
# Afro-Diasporic Syncretism
# Rasta Syncretism

# Harmonic Syncretism

# Americanist Syncretism IF THE SYNCRETIC FAITH IS ANACHRONOUS, WITH ADDITIONAL STIPULATIONS
# Industrialist Syncretism IF THE SYNCRETIC FAITH IS ANACHRONOUS
# Capitalist Syncretism IF THE SYNCRETIC FAITH IS ANACHRONOUS
# Idiosyncratic Syncretism IF THE SYNCRETIC FAITH IS ANACHRONOUS
# Modernist Syncretism IF THE SYNCRETIC FAITH IS ANACHRONOUS

# For Americanist Syncretic faiths, regardless of whether they have the override doctrine or not, they also need a syncretism variation doctrine
# If you want the faith to have the President as their Head of Faith, give them Hail to the Chief and the following line of code:
# religious_head = k_presidency

# For NON-ANACHRONIST faiths that you want to be "presidential" but not see the President as their Head of Faith, give them Freedom of Religion
# Freedom of Religion is redundant to americanist_override_doctrine on Anachronists, so don't give them Freedom of Religion, give them Americana

# For faiths you want to be "non-presidential", give them Americana
# For Anachronists, if you set things up correctly they will have americanist_override_doctrine alongside special_doctrine_americana
# This means their syncretism will be naturally upgraded to Astray rather than Hostile

# the Inter-Faith Services, La Mano de Dios, and Las Veinte Verdades override doctrines are written in 0000_hostility_groups, in the ifs_override_doctrine_group & hand_of_god_twenty_truths_doctrine_group sets

# For faiths with Inter-Faith Services, you need to add the "ifs_override_doctrine" to the faith with IFS
# This will render any other doctrine or tenet they have a receptor doctrine, being something for other doctrines to scan for regarding overrides
# That will look like the following example from Quaker:

# doctrine = tenet_inter_faith_services
# doctrine = ifs_override_doctrine

# For faiths with La Mano de Dios, you need to add the "hand_of_god_override_doctrine" to the faith with La Mano de Dios
# This will mean they always see Peronists as Evil, regardless of any lower-order doctrines below them
# That will look like the following example from Heromaquia:

# doctrine = tenet_the_hand_of_god
# doctrine = hand_of_god_override_doctrine

# Similarly, for faiths with Las Veinte Verdades, you need to add the "twenty_truths_override_doctrine" to the faith
# This will mean they always see Heroic faiths as Evil, regardless of any lower-order doctrines below them
# That will look like the following example from Justicialista:

# doctrine = tenet_las_veinte_verdades
# doctrine = twenty_truths_override_doctrine 