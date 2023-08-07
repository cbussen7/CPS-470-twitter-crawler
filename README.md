# Author: Christopher Bussen (bussenc1)
# Date: November 10, 2022

Instructions: 
I tested and compiled/ran this code using Google Colab - simply click the run button within Colab. For this project, Colab was using Python version 3.7.15. Additionally, it is important to note that in order to run this code, you must be able to enter valid credentials for an elevated Twitter Developer account (I had these files saved in a txt file that I would upload each time I ran the program). NOTE: I wasn't sure whether to submit the .ipynb file or the .py file so I included both of them.

The main functionalities of this program is to retrieve basic information about a list of Twitter users using Tweepy. For each user, it will show the user name, screen name, user ID, location, description, number of followers/following/tweets, and the URL. Additionally, it will show a list of each user's (bidirectional) friends as well as their first 20 followers. It will also collect the first 50 tweets containing the keywords 'Ohio' and 'weather', as well as the first 50 tweets originating from the Dayton region. Finally, it will deliver a feed of 25 tweets about Dayton basketball if it is 4 PM EST on a day where the Dayton Flyers Men's Basketball team plays.

EXAMPLE OUTPUT: 
    Saving twkeys.txt to twkeys.txt
    verification successful!

    User name:  Nick
    Screen name:  Nickloaf_
    User ID:  1123259995603263488
    Location:  
    User description:  
    Number of followers:  46
    Number of following:  28
    Number of tweets:  39
    User URL:  None
    Nickloaf_ has 46 followers (5000 means method hit max).
    Nickloaf_ has 28 following.
    Number of friends and screen names (based on set of intersection of followers and following):4
    Moloney414
    avi_rajurkar
    siravofficial
    SliimeyKamm
    First 20 followers: 
    ManyPenzero
    ChristabelClay3
    AutumnSimoson
    StovallVerlie
    MafaldaOgata
    RodenburgYusra
    YerBurgees
    MezydloShirley
    LonzoElara
    LilianaMagowan
    GemaLemasters
    FreyaNanke
    BeatrixLeek
    VictoryEsme
    MarleneScofiel1
    MckensieTemika
    IndiRood
    AyaCalcutt
    DeniceTsiatsos
    marton_winnie

    User name:  Christopher Bussen
    Screen name:  chrisbus7
    User ID:  3278738520
    Location:  
    User description:  Luke Ridnour Stan
    Number of followers:  52
    Number of following:  373
    Number of tweets:  103
    User URL:  None
    chrisbus7 has 52 followers (5000 means method hit max).
    chrisbus7 has 373 following.
    Number of friends and screen names (based on set of intersection of followers and following):5
    JackHanaway
    SnellSZN
    dannoe19
    yungben_
    UDClubBaseball
    First 20 followers: 
    GracejaWallace
    NicoleeaVaughan
    jculbertson7
    melinda77yi
    AdamCrutt13
    jspiegel208
    LocalDingus
    henrymay313
    ZacharyRudich10
    dannoe19
    UDClubBaseball
    jayraythomas1
    nick5_5_
    norailouis
    sarahbarah53
    erinmcgraw_
    yungben_
    BoninoConnor
    PaulFraser__
    Caitlin60437878

    User name:  GeeksforGeeks
    Screen name:  geeksforgeeks
    User ID:  57741058
    Location:  India
    User description:  Here to share resources, spread knowledge and have some fun! 💻 Founder and CEO @sandeep_jain
    Number of followers:  49340
    Number of following:  96
    Number of tweets:  18478
    User URL:  https://t.co/EWO31dEMUP
    geeksforgeeks has 5000 followers (5000 means method hit max).
    geeksforgeeks has 96 following.
    Number of friends and screen names (based on set of intersection of followers and following):1
    rass_aa
    First 20 followers: 
    maha_sphs2402
    nitish200899
    im_manawariqbal
    MunawarKh4n
    tigroviylev
    AnantIsha
    eorivi
    AfzalKhan_safi
    HabiburTanim
    Ajuffejay
    OyeChaudhary_
    anxirex
    Brijesh39326073
    gondmanyu
    uday_mukhija
    DiegoJSteele
    asphaltx24
    nilesh_smart1
    Aakash828673241
    _hustle_master

    User name:  Twitter
    Screen name:  Twitter
    User ID:  783214
    Location:  everywhere
    User description:  What's happening?!
    Number of followers:  64864149
    Number of following:  6
    Number of tweets:  15043
    User URL:  https://t.co/DAtOo6uuHk
    Twitter has 5000 followers (5000 means method hit max).
    Twitter has 6 following.
    Number of friends and screen names (based on set of intersection of followers and following):0
    First 20 followers: 
    maricwtt
    GrubmanAaron
    NagiHussein
    AnnamariaHaxto3
    gamberini_lorna
    QingtianDeng4
    josephpierrot3
    BALopezOfficial
    Lyndon50959110
    Ortiz6Mil
    BrentonShaneela
    sjdisdabest
    BarclayRobina
    GONZALO05771354
    Holly_Tee23
    convtble_bert
    Knightj28048521
    quinnme91112736
    aliensw59264565
    ErhartZahida

    User name:  GitHub
    Screen name:  github
    User ID:  13334762
    Location:  San Francisco, CA
    User description:  The complete developer platform to build, scale, and deliver secure software.
    Number of followers:  2403808
    Number of following:  336
    Number of tweets:  7603
    User URL:  https://t.co/bbJgfyhBlh
    github has 5000 followers (5000 means method hit max).
    github has 336 following.
    Number of friends and screen names (based on set of intersection of followers and following):0
    First 20 followers: 
    RowanGDurrant
    forensic_matt
    ryanbooker
    trisselyur
    unknxwnname
    oharenas
    MrTiagoSanV1
    ansidion
    JHamizi
    John73014818
    yarafahadd
    van_Onkruit
    morteza1978
    wlcfriends2
    pakistanitester
    errer_exe
    devAsadUllah
    FrankLeeGangLi
    Amin_am66
    MichealDeaigns
    Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in… https://t.co/8LnV5lPgsf 

    Tropical Storm Nicole has made landfall on Florida and will soon begin turning north. Rainfall from Nicole will mov… https://t.co/QhlpsNFFe2 

    The weather Ohio State fans think their offense is playing in today https://t.co/UrhHIiEvuS 

    RT @TheRickWilson: Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in fron… 

    Hey Ohio!! Hope you made the best of the weather!! 🌞 🍻 🌭 🍔 Winter here we come!! 🥶 ❄️ @MillerLite https://t.co/FzY8UIJEjY 

    RT @TheRickWilson: Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in fron… 

    RT @TheRickWilson: Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in fron… 

    RT @TheRickWilson: Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in fron… 

    RT @TheRickWilson: Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in fron… 

    RT @TheRickWilson: Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in fron… 

    RT @KatieMcGrawx: GET READY: This is what the radar is expected to look like tomorrow! Widespread heavy rain is likely. PLUS, temperatures… 

    @AngelWa33017557 Cool
    Very nice. 
    Nice weather here in Ohio as well. 

    RT @TheRickWilson: Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in fron… 

    @john_k_mathues @weather_history @Josh_oknefski Wow. I visited Nashville in 1998 from Ohio, and we were on the I-40… https://t.co/QcnUBuEhJY 

    RT @TheRickWilson: Protip for Kevin McCarthy today:

    Don't have coffee with Elise, stand near a window with Gaetz, walk down stairs in fron… 

    RT @jbook37: At this point I don't know what Ohio State is going to do? They cannot throw in this weather and because you can't run the foo… 

    @chiwizardry @Birm This team can beat only on turf in domes .. just not a weather team which is ironic because they are a OHIO team 

    RT @jbook37: At this point I don't know what Ohio State is going to do? They cannot throw in this weather and because you can't run the foo… 

    Northwestern has been moving the ball just fine. It's not all about the weather. Ohio State is flat out getting outplayed. 

    Ohio St offense is extremely soft....the weather today requires you to line up, overpower them at the line of scrim… https://t.co/mQNDupL5ol 

    RT @jbook37: At this point I don't know what Ohio State is going to do? They cannot throw in this weather and because you can't run the foo… 

    When playing in weather like this....   Play Big Ten Football.   I or wishbone formation, and run the %*%&amp;^ Ball st… https://t.co/xVASyVuFxJ 

    Northwestern is one of the worst teams in the Power 5. No weather excuses for Ohio State when they can't even run t… https://t.co/FMNkZv9PNO 

    I can’t believe I’m about to send this tweet.

    But Ohio State may not score in the first half. Against Northwestern… https://t.co/kQkSgUnkDS 

    Ohio State players don't like to play in weather. 

    RT @jbook37: At this point I don't know what Ohio State is going to do? They cannot throw in this weather and because you can't run the foo… 

    Ohio State having real problems with this weather. They can’t get anything on the ground, making it really difficul… https://t.co/uJcQYhYc2F 

    @theblockspot Pretty sure Purple Vandy is playing in the same weather. Maybe Ohio St just isn’t very good? 

    @bluebyninety If the weather for The Game is like it is today in Chicago, Ohio has NO chance.  😁 

    RT @GriffinStrom3: Bad weather or not, this is the third straight ugly start for the Ohio State offense since returning from the bye week. 

    Give Ohio State a little bad weather and they're complete shit. You would think they would have figured out how to… https://t.co/LBPP6MsUEc 

    At this point I don't know what Ohio State is going to do? They cannot throw in this weather and because you can't… https://t.co/e5zGXAwD65 

    This Ohio State game got all the signs of upset alert. Early game, bad weather, NW 1-7 

    RT @KyleRowland: I don’t want to see a single excuse about the weather from Ohio State. Northwestern is AWFUL. If you can’t just line up an… 

    RT @KyleRowland: I don’t want to see a single excuse about the weather from Ohio State. Northwestern is AWFUL. If you can’t just line up an… 

    RT @KyleRowland: I don’t want to see a single excuse about the weather from Ohio State. Northwestern is AWFUL. If you can’t just line up an… 

    The Northwestern / Ohio State game is about to get wet &amp; wild. Severe warning event for the stadium, but no lightni… https://t.co/JFE575OCTk 

    Ohio state players look so disinterested on their bench. The color analysts are blaming the weather for why Ohio st… https://t.co/0tzYTtTQEm 

    RT @WolverineCorner: Ohio State's lack of running game and not being able to play in any sort of bad weather is legitimately funny and shou… 

    The weather is the real mvp for Northwestern so far against Ohio State. Wind gusts strong enough to push people bac… https://t.co/0DJQZ7YjXe 

    Honestly this Ohio State team is pathetic today. Obviously the weather isn’t helping but between today and last yea… https://t.co/cj0NxE4pMx 

    I know the weather is horrendous at Northwestern but Ohio state is still sucking 😂 

    @barstoolsports Ohio state just remember that northwestern is playing in the same weather with a bunch of 2 star recruits as well 

    Want to beat ohio state? Just hope there's any sort of weather whatsoever at all. 

    This Ohio State team under Day cannot handle weather. Look at UM last year and this mess as evidence. #OSUvsNW 

    Ohio State can’t play in bad weather games 

    RT @KyleRowland: I don’t want to see a single excuse about the weather from Ohio State. Northwestern is AWFUL. If you can’t just line up an… 

    Ohio State cannot run the ball. They better pray for perfect weather conditions in three weeks. 

    Man starting to think Ohio St may not be a top tier team this year. The weather is bad this game, but their defense… https://t.co/w0ovsJPUWx 

    Ohio State has a huge problem of looking ahead of some teams.

    They also have an inability to play in bad weather. 

    i’m not a rose kind of girl my favorite flowers are more beautiful 

    Here’s another example of ignorance people point of view, and not able to comprehend the meaning of equality for al… https://t.co/LZNUBbnYg9 

    @ashleyjjwhite Folks.

    Or yinz. 

    You already know what time it is. It’s the semi-annual Kayla Siegel Robins Green photo dump!! 💕 

    You make everythi… https://t.co/buQPOwhMqs 

    @jaceutd_ @Lacazetteeeee @ManUtd 😂 

    Wank https://t.co/inGEqDsPH7 

    We need some 😤🤣 https://t.co/2PP8fgKrI4 

    @tylerbowyer @Peoples_Pundit There are lawyers down there, right?
    How do they protect "chain of custody" (ballot in… https://t.co/yW0rNePgB2 

    @WalterBlake1 And yet Trump is walking around free 

    @rnbadley Dude this one’s a BOP! Each one keeps getting better and better! I’m pumped af for the album 🙌🔥🙌 

    #Anipoke Who will win the World Coronation Series? 

    @golfbobski @AdamRintala @AngelaBelcamino Ask Amy Klobuchar about her "hot dish." 

    I tooted three times on Mastodon today. 

    Like always, I blamed it on the dog. Habits are hard to break. 

    MOVING ON! Bulldogs beat Ashland on PK’s to advance in NCAA Tourney! https://t.co/gdSFJAKqrq 

    Yeah, I'm not sure anyone can play Ozzy, famous or not. Besides, he's gonna outlive us all anyways. He is The Princ… https://t.co/r5xHghmsjA 

    Join the Kettering Health team! See our latest job openings here: https://t.co/bLkR4Neqkz https://t.co/k2JVOKujWK… https://t.co/EcHWamFBwa 

    Wordle 509 4/6

    ⬜🟨⬜🟨🟨
    ⬜⬜🟨🟨🟨
    🟨🟨🟨🟨⬜
    🟩🟩🟩🟩🟩 

    @JACKPOSTJUICER Is that mikaela that’s getting kicked out for STILL trying to go?! 👀 

    IF the USA dissolves into civil war... so what?

    KBR has nothing to do with it... YOU ARE A - - PRIVATE - - DEFENSE… https://t.co/eLpj7rmDqR 

    @HeelWillMahoney I gave it two years a week or so ago when it was announced that Musk purchased it. At this point g… https://t.co/r6GiSVooWF 

    @FesterBesterte3 @sisterinferior Not trying to endorse or dissuade, just being honest 🤷🏻‍♂️ 

    @ashraf_elmansy يابختي♥️ 

    @Joe79451714 @laurenboebert We have AOC chill 

    @NoahSherry4 @937Elegy I love Great Lakes! Not a big fan of porters though. 

    I’m going out of help but think of paint of my time falling asleep and then to night, I don’t want to not really needs fed, 

    @deepknight @CurryTony @historyinmemes 🤣🤣🤣😭😭😭😭😭 

    @coreyacj09w @my_name_a_pete @jonmalexander not Dorset, it's a QB that overthrew, lol, pay attention, open your eyes 

    @elonmusk Lmao 

    @CallofDutyUK 🧼 

    Pantry stocked https://t.co/py5DqEYWTE 

    @t_taimae 泰志おはよぉぉ！！！☀️ 

    @LogicalHeathen Well... I can tell you, our reason for reading the bible is slightly different than why we read Harry Potter. 😉 

    @tina1128 @NatetheLawyer On my phone I switched to desktop  website and back then they started showing up. 

    This #Finance job might be a great fit for you. Click the link in our bio to see it and more. Inventory Crew Member… https://t.co/GQwrISF7EA 

    @bria_110 Nope I'm good ha 

    @lgm_hiroki23_46 ひろきおはがたぁぁぁあ！！☀️ 

    Lmao sure they are https://t.co/2DgdGaD0hd 

    @TAKECHA13386207 たけちゃんおはぁぁぁ！！☀️ 

    @jonmalexander lmao, oh gawd, smfh 

    🌈⚡️☄️🌪🥂🍝 https://t.co/UOME9nV9Iu https://t.co/1ZUti3tACZ 

    @NFLRookieWatxh @HollywoodxKev Udfa btw 

    @videosdroles_ Guette leur chef d'état aussi https://t.co/FPtOSLILFo 

    @ohisama_mikuni がわおはがたぁぁぁぁあああ🌱✨ 

    @DakotaDropDead @JACKPOSTJUICER https://t.co/QG6kjJb95g 

    @elonmusk you’re soooooooooo fucking stupid, man LOL 

    @toyonchu_tykz とよんちゅおはよぉぉ！！！！☀️ 

    @MaoYugenVT https://t.co/9UxYFax5AU 

    @CeeHawk But you will never convince me that the biker shorts were good, because they were awful 

    The Rose Croix, the Rose Line... I'm it

    17 hours. 

    @shibayuu46 ゆースケおはよぉ！！！🌱✨ 
