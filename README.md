# shopify_geolocation_cart
A script i made that adds geolocation functionality to shopify carts for gps delivery for businesses.

The following code is what took me a couple of months to make. Mostly just trial and error. The gist of it is that you need to create a product in your shopify store call it “Gps coordinates”. Then you need to get the Id of that product. Paste the code snippet below to your cart-template.liquid. Then modify the jquery to add the gps coordinates to the Gps coordinates product Id to the cart and thats it.

The customer will check out and then when you get the order you will the customers gps goordinates and a google map link in the order, so you can send someone to deliver. Before hand, you will need to add a pin svg to your shopify store, so the pin will be synced with the map, other than that, it works pretty well! I made this map because where i live, i work in a desert area where making local deliveries was near impossible because google maps hasn’t mapped most of the desert. There are no street names, so people go by landmarks here.

So with this map, i could get their exact geolocation where they are, and i get a map that takes me or the delivery driver to them. Also, to make this work you will need your own google api key. For the future i was planning to use openstreetmap api, and this was going to be the basis of one django app that im currently building. I hope this helps, it was a royal pain to figure all this out from scratch. This currently works with shopify only. Ill paste some images of the script working and the website where it currently is applied on. If you need help installing this in your shopify store, we can work out an arrangement. Contact me at pointperks@gmail.com. This code is under Attribution 4.0 International (CC BY 4.0) https://creativecommons.org/licenses/by/4.0/

If you want to see pictures of code working in action vistit website https://www.pointperks.net/shopify-geolocation-addon-for-cart/ to see pictures and in the website page i will provide link to the actual website where i implemented the code, so you can see that it is functioning.

                                  .--===-:.                                           
                               .+*########**+:                                        
                              =*#############*=                                       
                             +################*.                                      
                            .*################*=                                      
                             .+*++++****######*+.                                     
                              .===-==++****##**+:                                     
                               -===+********#**+.                                     
                               .+*=*+++=++******:                                     
                                :--+++==+********+.                                   
                                 -=+**++****##*###*=-:.                               
                                  :=+****##########*****+=-.                          
                                    =++*#####**####*********+-.                       
                                 .=+***#******#####************=-                     
                               :+####*###+++*####**#*************+.                   
                            .-+*######*##*=*####**#******###******+.                  
                           -*#**##**#***##*###***#***##*###********=                  
                         .-**#####******####****#****#####*#*******+.                 
                      -+**########****#*##**=**##***######***#*****+.                 
                    -+**##########***####***:+**#*#######***##*****+.                 
                   =****##########***###*******#########***##******+.                 
                 :=**#########%###***###********########**##*******+.                 
                :=++*####%%%%%%###***###*******########***##**##***=                  
                -++*###%#%%%%%%##*######*******########**######*#**-                  
                -++*######+=----*#########****#########****#####***.                  
                -++*##*=:       -####*#*******##################***.                  
                :=+**:          :*###*********##########******##***.                  
              .-=++*=           .*#####*#****###########*+***###***:                  
             :-==+**-            +#####****############+==+**###***:                  
            .--=++**.            :*###################+==+***###*#*:                  
            .--==+#+              +##################+=++****####**-                  
             :=-+*+.              -#################+=++**#*#####**-                  
              .-::.               .*###############+++***########**+                  
                -.                 +#############*++***##########**+.                 
                :.                 =############++***##########*#***:                 
  ......::-:....----::.:--::...    +##########*=++**##########*###**-                 
 .::.:-:::::----===+******++++=+-:=++*+***##*+++***###############**=                 
  .. ::....:....:-=+**=-+*++++==+++=**-=**===++***################**+                 
 :=+=-::.:........--+**==**=++++++*=+**++====***##################**+                 
 -==++*+=--.:.: :.:-=+*+=+*==+++==*==+*+=++=+*+*#*###############***=                 
   .:-=+++++==-:-::=-+*==+*==+*==+*==+++*#=+*=+****##############***-                 
       .:-==+++++++***#*###*########*****+=*+=*+**-. .-=+*#####***=.                  
          ...::::::::::::.........          .....         .:-=+***.                   
                                                                ..                    
