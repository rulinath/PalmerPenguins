# PalmerPenguins
code for textbook ch 1

Code for 1.2
install.packages("tidyverse")  
library(tidyverse)  
library(palmerpenguins)  
library(ggthemes)  
penguins  
glimpse(penguins)  
ggplot(
  data = penguins,
  mapping = aes(x = flipper_length_mm, y = body_mass_g, color = species)
) +
  geom_point(mapping = aes(color = species, shape = species)) +
  geom_smooth(method = "lm") +
  labs(
    title = "Body mass and flipper length",
    subtitle = "Dimensions for Adelie, Chinstrap, and Gentoo Penguins",
    x = "Flipper length (mm)", y = "Body mass (g)",
    color = "Species", shape = "Species"
  ) +
  scale_color_colorblind()  

  Code for 1.4.1  
ggplot (penguins, aes(x = fct_infreq(species))) + geom_bar()

Code for l.4.2
ggplot(penguins, aes(x = body_mass_g)) +
  geom_histogram(binwidth = 200)
