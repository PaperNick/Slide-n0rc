## Info about this fork

This fork contains a modification of Slide that allows changing the Client ID of the app.
This modification was necessary to deal with Reddit's API changes from July 1, 2023.

To get Slide working again follow these steps:

1. Go to https://www.reddit.com/prefs/apps → create app
2. Choose a name and **installed app**
3. Insert any **redirect uri**, e.g. http://127.0.0.1
4. Copy the Client ID of your newly created app (shown below the words "installed app" below your app name)
5. Start Slide
6. Choose *Change Client ID* from the drawer menu
7. Paste the Client ID from step 4
8. Insert the Redirect URL from step 3
9. Save and restart Slide

## Local rebuild instructions

1. Install Java 11 (openjdk 11.0.20 2023-07-18) from SDKMAN:

```
sdk install java 11.0.20-tem
```

2. Install Android SDK (Android Studio Giraffe | 2022.3.1):

http://developer.android.com/sdk/index.html#Other

Alternatively, check sdkmanager (use version 29, 30 or 34):

https://developer.android.com/tools/sdkmanager

3. Build the project by specifying the Android SDK root folder:

```
ANDROID_SDK_ROOT="$HOME/Android/Sdk" ./gradlew assemble lint{With,No}GPlay{Debug,Release} test{With,No}GPlay{Debug,Release}UnitTest
```

4. If some of the unit tests fail, that's fine

5. If the build process is successful, you will find an APK file in directory: `app/build/outputs/apk/noGPlay/debug`

6. Copy `app-noGPlay-debug.apk` file to your phone

7. Install the app

8. Enter your Client ID from the previous section

## Current project status

This project will be on indefinite hiatus for the foreseeable future, and may not be maintained.
Updates are not guaranteed.
See [here](https://github.com/Haptic-Apps/Slide/issues/3449) for details.

You may continue to use Slide if you so wish.
However, with this said, it would be recommended to consider migrating to another (more stable) Reddit client.

Some other open-source (and internally ad-free) Reddit clients include:
- [Infinity For Reddit](https://github.com/Docile-Alligator/Infinity-For-Reddit)
- [RedReader](https://github.com/QuantumBadger/RedReader)
- [Dawn](https://github.com/Tunous/Dawn)

# Slide

<img src="app/src/main/res/drawable/ic_launcher.png"
    align="left" width="180" hspace="10" vspace="10">

Slide is an open-source, ad-free Reddit browser for Android.
It is based around the [Java Reddit API Wrapper](https://github.com/mattbdean/JRAW).

Slide is available on the Google Play Store and F-Droid.

<a href="https://play.google.com/store/apps/details?id=me.ccrama.redditslide">
    <img alt="Get it on Google Play"
        height="80"
        src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" />
</a>
<a href="https://f-droid.org/app/me.ccrama.redditslide">
    <img alt="Get it on F-Droid"
        height="80"
        src="https://fdroid.gitlab.io/artwork/badge/get-it-on.png" />
</a>

There is an active community for Slide on the
[/r/slideforreddit](https://www.reddit.com/r/slideforreddit) subreddit,
which anybody is welcome to join.

There is also a [Discord](https://discord.gg/hVWAY8A).

## Sponsors

Thank you to our awesome Github Sponsors, who help keep the Slide project going.

|  | GitHub profile |
| --------- | ------------- |
| **KevinNThomas** | https://github.com/KevinNThomas |
| **andrewkdinh** | https://github.com/andrewkdinh |

If you're interested in sponsoring our work, check out the sponsor slots for Slide contributors on the right-hand **Sponsorship** menu.

## Contributing

### Issues

In any project it's likely that a few bugs will slip through the cracks, so it
helps greatly if people document any bugs they find to ensure that they get
fixed promptly.

You can view a list of known issues and feature requests using [the issue tracker](https://github.com/Haptic-Apps/Slide/issues).
If you don't see your issue (or you aren't sure), feel free to [submit it!](https://github.com/Haptic-Apps/Slide/issues/new).

Where appropriate, a screenshot works wonders to help us see exactly what the issue is.
You can upload screenshots directly using the GitHub issue tracker or
by attaching a link (to Imgur, for example), whichever is easier for you.

### Translations

If you are able to contribute a translation into a language missing from Slide,
or spot any room for improvement in an existing translation, we greatly
appreciate anything you can assist with!

[The project uses Crowdin](https://crowdin.com/project/slide-for-reddit),
a platform that allows anybody to contribute to translating the app with as many words at a time as they want.
Crowdin provides a nice interface for translating, and no knowledge of the code is needed.

### Code

If you are a developer and wish to contribute to the app, please fork the project
and submit a pull request.

If you have any questions, feel free to
[ask in the `#android-dev` Discord channel](https://discord.gg/HeShMsX) or
[drop me a message](https://www.reddit.com/message/compose/?to=ccrama) on Reddit.

If this is your first time contributing to the project and want to tackle an
easy issue, take a look at the issues labelled [`Good First Issue`](https://github.com/Haptic-Apps/Slide/issues?q=is%3Aopen+is%3Aissue+label%3A%22Good+First+Issue%22).
These issues have been marked as such because we believe they are easier to fix than other issues.

## Changelog

The file [CHANGELOG.md](CHANGELOG.md) provides an overview of the changes for a
release; for a more detailed look at changes to the app, [view individual commits](https://github.com/Haptic-Apps/Slide/commits/master).

## Licensing

Slide is licensed under the [GNU v3 Public License](LICENSE.txt).
