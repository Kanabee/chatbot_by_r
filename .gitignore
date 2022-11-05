sizelist <- c("M","R","L")
location <- c("hachioji","hino","takao")
pizza <- data.frame(
  pizza_menu =c("1.CHEESE FANTASY QUATTRO","2.CHEESE FANTASY DOMINO DELUXE","3.CHEESE FANTASY AMERICAN","4.CHEESE FANTASY GARLIC MASTER"),

  M_size =c(3000,3000,3000,3000),
  R_size =c(3599,3599,3599,3599),
  L_size =c(4200,4200,4200,4200)
)
side_menu<- data.frame(
sidemenu_list = c("1. OVEN BAKED POTATO WEDGES ",
                      "2. NUGGETS",
                      "3. JAPANESE FRIED CHICKEN",
                      "4. SALAD"),
sidemenu_price_list = c(450,399,599,450)
)
drink_menu <- data.frame(
  drink_list= c("1.COLA","2.COFFEE","3.ORANGE JUICE"),
  drink_price = c(300,300,300)
)
#print(pizza)
##print(drink_menu)
cart_list <- list(
                  item =c(),
                  price =c()
                  )

 

delivery<- function(){
  print("You choose Delivery")
  print("please put your name")
  name<-readLines("stdin" ,n=1)
  print("please put your address")
  address<-readLines("stdin" ,n=1)
  print("phone :")
  phone<-readLines("stdin" ,n=1)
  print(paste(name,address,phone))
  print("please check your information submit please press 1 ")
  check<-as.integer(readLines("stdin" ,n=1) )
  if(check == 1){
    print("30 minute wait !!")
  }else{
    print("information error please do again!")
  }
  
}
#order pizza
order_pizza <- function(){
  print("Please choose pizza")
  print(pizza$pizza_menu)
  pizza_id <- as.integer(readLines("stdin" ,n=1))
  print("please choose pizza size")
  print("1. M size 2.R size 3.L size")
  size_id<- as.integer(readLines("stdin" ,n=1))
  item <- pizza$pizza_menu[pizza_id]
  price <- pizza[pizza_id,size_id+1]
  return(list(item,price))
}

order_sidemenu <- function(){
  print("Please choose sidemenu")
  print(side_menu$sidemenu_list)
  sidemenu_id<-as.integer(readLines("stdin" ,n=1))
  item<- side_menu$sidemenu_list[sidemenu_id]
  price <-side_menu[sidemenu_id,'sidemenu_price_list']
  return(list(item,price))
}

order_drink <-function(){
  print("Please choose drink")
  print(drink_menu$drink_list)
  drinkmenu_id<-as.integer(readLines("stdin" ,n=1))
  item <-drink_menu$drink_list[drinkmenu_id]
  price <-drink_menu[drinkmenu_id,'drink_price']
  return(list(item,price))
}  

#collect in cart 
cart<- function(list){
  item = list[[1]]
  price = list[[2]]
  cart_list$item<- c(cart_list$item,item)
  cart_list$price <- c(cart_list$price,price)  
  return(cart_list)
}

 

  
print("Welcome to Pizza chat bot")
print("what do u want to do ?")
print("1.order Pizza 2. read promotion 3.comment")

action<-as.integer(readLines('stdin', n=1))
if(action==1){
  print("Do u want to buy pizza ? Y/N")
  need_pizza <- tolower(readLines('stdin', n=1))
  while(need_pizza =='y'){
    cart_list <-cart(order_pizza())
    print("do u want more? Y/N")
    need_pizza <- tolower(readLines('stdin', n=1))
  }
  print("Do u want sidemenu ? Y/N")
  need_sidemenu <- tolower(readLines('stdin', n=1))
  while (need_sidemenu == 'y'){
    cart_list <- cart(order_sidemenu())
    print('do u want more? (Y/N)')
    need_sidemenu<- tolower(readLines('stdin', n=1))
  }
  print("Do u want drink ? Y/N")
  need_drink<- tolower(readLines('stdin', n=1))
  while (need_drink == 'y'){    
    cart_list <- cart(order_drink())
    print('do u want more? (Y/N)')
    need_drink<- tolower(readLines('stdin', n=1))
  }
}
print("please check your order !")
cart_list <- data.frame(cart_list)
cart_list

total_amount <- sum(cart_list$price)
print(paste("total :", total_amount,"Yen"))
print('1:Carry Out, 2:Delivery ')
buy <- as.integer(readLines('stdin', n=1))
  if(buy == 1){
    print("you choose Carry Out !")
    print("please choose location ")
    print("1.hachioji 2.hino 3.takao")
    location <- as.integer(readLines('stdin', n=1))
    print(location)
    print("your code number")
    random_code <- (sample.int(9999, 1, replace = TRUE))
    print(paste("code-number:",random_code,"-",loc[[location]]))
    print("Thank you !)
    
  }else{
    delivery()
  }
}else if(action ==2){
  print("promotion pizza")
  print("XXX")
  
}else if(action==3){
  print("commnt :")
  comment <- (readLines('stdin', n=1)
  print(commnt)
}
