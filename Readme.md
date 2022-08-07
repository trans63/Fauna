# Fauna
Live and Let Live - Using AI and Crowdsourcing to stop animal attacks.

Submission - [Devpost](https://devpost.com/software/fauna-glc25a)
## Inspiration
Animals are everywhere, right? Even in the Bay Area, where we have everything from snakes to mountain lions to bobcats. Though some animals are a man's best friend, like your very own dog, some are the best enemies as well. Humans and nature are always at conflict.

Now, the mess gets worse. Humans have snatched the shelter of animals and animals are forced to live closer and closer to humans. Every year, people die due to interactions with dangerous animals. Animals too suffer, as interactions with humans can injure them or have them put down. In rural and countryside areas it's considered **common** to die due to animal attacks. Many people die each year due to unexpected animal attacks worldwide. Injuries, too, cost a lot to treat and manage, and in the US alone, treatment of animal injuries cost as much as $2 billion.

My solution was an app that would be community-driven and that would crowdsource information on animal encounters to allow people to avoid wild animals.

We called it: **Fauna**

## What it does

The goal of my app is twofold:

- Allow users to see where wild animals have been spotted
- Allow users to add photos and location of the wild animal, they've spotted

My app allows users to provide photos of wild animals they saw or encountered and add them to a geographic database that other users can see. I made a mobile app where users can log in, submit photos (and even take them through the app) and then immediately use computer vision and object recognition to identify the animal and add the encounter to our database. I also use Google maps to provide an interactive, location-based viewer for encounters and alerts when you might be getting close.

**Summarised workflow** - After successfully logging in, the app fetches your location. While reporting an animal you upload an image of that animal and the app immediately recognizes the animal. The location of the animal is posted on the map. All other users within a 5km radius are notified about the animal, they can see its picture and the time spotted. Henceforth they will get alerted and take precautions.

## How I built it

Tech stack relied heavily on Google's Cloud Platform.

- API runs on **Google App Engine** 
- Images are stored in **Google Cloud Storage**
- Animal Detection is done through **Google Vision** 
- I use **Google Maps** for location data.
- Front-end is built with **Flutter** 
- Languages used are **python** and **dart**

I also used **CockroachDB** for our database. I utilized their spatial functions in order to create `GEOGRAPHY` entries where I could add locations. My **Flask** API uses SQLAlchemy to interact with the database and update values.

I use Flutter for the frontend in order to build for both iOS and Android. For a project like this one, more users are essential, so we need as many platforms as possible as well, Flutter communicates to our API, which communicates to our database to read and write encounters.

## Challenges I ran into

Ahhh, there were a LOT of challenges. Most of them were in the front-end, where I ran into issues with not deciding on a framework fast enough. I also ran into issues with dependencies conflicts with Flutter, and the setup was painful as well :( .

I also ran into issues when dealing with HEIF files. Though I did find a way to convert HEIF to PNG and to do it fast, Google Cloud Platform makes it very difficult to use the `libheif` library.

Uhfff, Most constrictive of all was probably time. I had very little time to style the application though I definitely landed a good job with it. It's been a tough journey, with quite a few setbacks, but I finally did it. 

## Accomplishments and what I've learned

This has been an amazing project to work on. I successfully wrote a complete app with a full REST API that uses Google Cloud Vision components. Every bit of this project has been an accomplishment, from the tricky and time-crunched front-end to the complicated and involved back-end. I've gotten a lot better at working with Google's Cloud Platform, learned a lot about databases with CockroachDB, and I've built something brand new that is fresh and interesting to all of us.

Things I've learned or gotten better at:

- Google Cloud Platform
- SQL
- Spatial Databases
- Flutter
- Flask

## What's next for Fauna

So, where to? Wherever I go from here, my app will help us avoid any dangerous animals :D.

My next steps are probably to work on styling. The back-end is fast, reliable, and scalable, thanks to Google Cloud and CockroachDB, but the front-end could use some touch-ups to make it just that much smoother. I have high hopes that with some more time and effort, and some focused clean-up of code and UI, I did be able to make this an app that wouldn't just be useful and valuable, but life-saving as well for both humans and animals.

## Conclusions

Thanks for checking out Fauna! I've put a lot of time and effort into this, so I'm really excited to get some feedback. The app is fully functional!!. Check out the Android and iOS installer files at the links below, or view our code on [Github]() Thanks!
