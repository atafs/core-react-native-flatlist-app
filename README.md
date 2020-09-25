# core-react-native-flatlist-app
This pet project has a network capacity to make HTTP request and a UI layer to display the data retrieved from the endpoints in a flatlist at a mobile app!!

## Snapshots
![ezgif com-gif-maker (1)](https://user-images.githubusercontent.com/7454154/94228267-7a90b280-fef4-11ea-8019-6fd13f7dce05.gif)

## Description about the project, folder system and reasoning behind it:
- In the **api** folder I am using the apisauce library. It is essentially a wrapper around axios but with error handling addded to it!! I am defining a client and using an endpoints object to store and use them.
-  In the **assets** folder I have the spinner from lottie library! There are plenty of amazing option there from free to payed activity indicators.
- At the **components** folder  the **ActivityIndicator** is using the spinner from lotties when making the api request and waiting for the promise to be resolved. The **Button** is used when there is an error like not network connection or something. That will give the user a retry option. The **Screen** is an interesting one!! So, to avoid having to add SafeAreaView to a screen every time we create a new one (which can be quite often), this wrapper around a view that shows all the components we pass to them by using the children props is very handy!! A very good reusable component with the intent to increase productivity when writing code!! There is also a **Card** component to show the data retrieved from the endpoints. And last but not least a very interesting reusable Text component. To which we can pass additional other props to add specific properties depending when it is being used. As well as additional styles. They have snapshot tests that can be extended to more relevant tests that will validate the quality of them!!
- A **config** folder to have a simpler and more consistent way of keeping in one place the theme of the app. And as such, a simple way to change in one place and have an effect in all the app.
- The **helper** folder is where I added the function to handle the logic around getting the names of the genres. There is room for improvements to add a more single line javascript approach. 
- The **hooks** folder has another great reusable hook to make api requests. Handling the data, error and loading states. 
- At last, the **screen** folder has the FlatList where we render our data. As well as the cases of something going wrong with the request or the app still making the request.

## In future iterations...
- Would be nice to have the cards as touchable components to navigate (from react navigation) to another screen. To display additional information about the movies.
- To use swipeable components (from react native swipeable) to have additional functionality to the FlatList like to delete an element. But instead of taking space in the screen, the swipeable gesture could give us access to those icons in more modern way!!
- Handling authentication and authorization for the login and register screens. The form could be written in Formik and Yup.
- Handling push notifications is always a plus to create more engagement from the user.
