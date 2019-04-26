#
# This is a Shiny web application. You can run the application by clicking
# the 'Run App' button above.
#
# Find out more about building applications with Shiny here:
#
#    http://shiny.rstudio.com/
#

library(shiny)

# Define UI for application that draws a histogram
ui <- fluidPage(
   
   # Application title
   titlePanel("Shiny Megawork"),
   
   # Sidebar with a slider input for number of bins 
   sidebarLayout(
      sidebarPanel(
        radioButtons("type", "Burial Type",
                     choices = list("Megalith with mound" = 1,
                                    "Megalith without mound" = 2,
                                    "Gallery Grave" = 3,
                                    "Stone circle or menhire" = 4,
                                    "Enclosure" = 5),
                     selected = 1),
        
        # Only show this panel if the plot type is a histogram
        conditionalPanel(
          condition = "input.type == 1",
          radioButtons(
            "mound_shape", "Mound Shape",
            choices = list("Round mound" = 1,
                           "Semicircle Mound" = 2,
                           "Long mound" = 3),
            selected = 1),
          conditionalPanel(
            condition = "input.mound_shape == 1",
            numericInput("radius","Mound Radius (in m)", value=0) 
            ))
      ),
      
      # Show a plot of the generated distribution
      mainPanel(
         p("output goes here")
      )
   ),
   # WHERE YOUR FOOTER GOES
   hr(),
   p("based on Müller 1990")
)

# Define server logic required to draw a histogram
server <- function(input, output) {
 
  # logic goes here
}

# Run the application 
shinyApp(ui = ui, server = server)

