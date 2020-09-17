# tabBarController-operation (Swift 5.0)
Take notes for tabBarController

  
## Remove tabBar item from tabBarController
     //remove tabBar item 2
     let indexToRemove = 2
     if indexToRemove < self.tabBarController!.viewControllers!.count {
       var viewControllers = self.tabBarController!.viewControllers
       viewControllers?.remove(at: indexToRemove)
       tabBarController!.viewControllers = viewControllers
     }
   
## Enable and disable tabBar item within tabBarController
      
     let tabItems = self.tabBarController?.tabBar.items
     for i in 0..<tabItems!.count {
         if tabItems![i].title == "Setup" {
               tabItems![i].isEnabled = true
                    self.tabBarController?.selectedIndex = i
                }else {
                    tabItems![i].isEnabled = false
                }
          }
      }
      
## Hide All tabBar
      
    self.tabBarController?.tabBar.isHidden = true
      
      
