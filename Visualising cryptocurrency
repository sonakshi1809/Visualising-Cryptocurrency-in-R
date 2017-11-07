#install package coinmarketcapr and load it into the library
install.packages("coinmarketcapr")
library(coinmarketcapr)
#plot the top 5 currencies 
plot_top_5_currencies()
#To extract Global Market Cap of Leading Cryptocurrencies
market_today <- get_marketcap_ticker_all()
head(market_today[,1:8])
#subset the data with top 10 currencies to analyse 
Top_10<- market_today[0:10, ]
#plotting the percent change in price of the top 10 cryptocurrencies over time
ggplot(data =  Top_10) + 
  geom_point(mapping = aes(x = Top_10$name, y = Top_10$percent_change_1h), color = "blue")+
  geom_point(mapping = aes(x = Top_10$name, y = Top_10$percent_change_24h), color = "red")+
  geom_point(mapping = aes(x = Top_10$name, y = Top_10$percent_change_7d), color = "green")+
  xlab('Cryptocurrency') +
  ylab('Percent Change in Price over time')+
  ggtitle('Change in Price of top 10 cryptocurrencies over time')
