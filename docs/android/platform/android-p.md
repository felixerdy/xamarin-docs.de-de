---
title: Android-P-Vorschau
description: Informationen zum Einstieg in Xamarin.Android zum Entwickeln von apps für die neueste Version von Android.
ms.prod: xamarin
ms.assetid: 6575DD32-9DC8-44E6-85EF-1F8BD07D3780
ms.technology: xamarin-android
author: mgmclemore
ms.author: mamcle
ms.date: 07/27/2018
ms.openlocfilehash: a3eef6f2537a4b09f603787d7cdbf70a173fca80
ms.sourcegitcommit: aa9b9b203ab4cd6a6b4fd51e27d865e2abf582c1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2018
ms.locfileid: "39351920"
---
# <a name="android-p-preview"></a>Android-P-Vorschau

_Informationen zum Einstieg in Xamarin.Android zum Entwickeln von apps für die neueste Version von Android._

![](~/media/shared/preview.png)

Die [Android P Developer Preview](https://developer.android.com/preview/) ist jetzt von Google verfügbar. Eine Reihe von neuen Funktionen und APIs in dieser Version vorgenommen werden, und viele davon sind erforderlich, in der neuesten Android-Geräte der neuen Hardwarefunktionen nutzen.

![Android-P-Hero-Bild](android-p-images/01-android-p-logo.png)

In diesem Artikel ist strukturiert, um Ihnen den Einstieg in die Entwicklung von Xamarin.Android-apps für die Android-P-Vorschau unterstützen. Es wird erläutert, wie die erforderlichen Updates zu installieren, konfigurieren Sie das SDK und bereiten Sie vor einem Emulator oder Gerät zu Testzwecken. Außerdem bietet einen Überblick über die neuen Features in Android P und enthält Beispiel-Quellcode, das veranschaulicht, wie Sie einige der wichtigsten Features Android P verwenden.


## <a name="requirements"></a>Anforderungen

Folgendes ist erforderlich, um Android-P-Funktionen in Xamarin basierenden apps zu verwenden:

-   **Visual Studio** &ndash; bei Verwendung von Windows Version 15,8 Preview 5 oder höher von Visual Studio ist erforderlich.  Wenn Sie einen Mac verwenden, ist die aktuelle Betaversion von Visual Studio für Mac oder höher erforderlich.

-   **Xamarin.Android** &ndash; Xamarin.Android 9.0.0.17 oder höher muss installiert sein, mit Visual Studio.

-   **Java Developer Kit** &ndash; Entwicklung mit Xamarin Android 9.0 erfordert [JDK 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) (oder Sie können versuchen, die Vorschau von Microsoft Verteilung der [OpenJDK](~/android/get-started/installation/openjdk.md)).

-   **Android SDK** &ndash; Android SDK-API-28 oder höher muss über den Android SDK Manager installiert werden.

## <a name="getting-started"></a>Erste Schritte

Zum Einstieg anhand von Android-P, die mit Xamarin.Android, müssen Sie herunterladen und die neuesten Tools und SDK-Pakete installieren, bevor Sie Ihr erste Android P-Projekt erstellen können:

1. Aktualisieren Sie auf Visual Studio 15.8 Preview 5 oder höher. Wenn Sie Visual Studio für Mac verwenden, wechseln Sie zu Visual Studio für Mac [Beta](https://docs.microsoft.com/visualstudio/mac/update) Kanal.

2. Installieren Sie die **Android P (API-28)** oder spätere Pakete und Tools über den SDK-Manager.

3. Erstellen eines neuen Xamarin.Android-Projekts, das als Ziel Android P (28-API).

4. Konfigurieren Sie einen Emulator oder Gerät zum Testen von apps für Android P.

Jeder dieser Schritte wird in den folgenden Abschnitten erläutert:


### <a name="update-visual-studio"></a>Aktualisieren von Visual Studio 2017

Aktualisieren Sie zum Hinzufügen von Android-P-Unterstützung zu Visual Studio auf Visual Studio 2017 Version 15,8 Preview-Version 5 oder höher als erläutert in [Aktualisieren von Visual Studio 2017 auf die neueste Version](https://docs.microsoft.com/visualstudio/install/update-visual-studio).
Zum Hinzufügen der Android-P-Unterstützung in Visual Studio für Mac, aktualisieren Sie auf die neueste Betaversion von Visual Studio 2017 für Mac Siehe [Aktualisieren von Visual Studio für Mac](https://docs.microsoft.com/visualstudio/mac/update).


### <a name="install-the-android-sdk"></a>Installieren Sie das Android SDK

Zum Erstellen eines Projekts mit Xamarin.Android 9.0, müssen Sie zuerst den Android SDK Manager verwenden, installieren Sie die SDK-Plattform für **Android P (API-Ebene 28)** oder höher.

1. Starten Sie den SDK-Manager. Klicken Sie in Visual Studio auf **Tools > Android > Android SDK Manager**. Klicken Sie in Visual Studio für Mac auf **Extras > SDK-Manager**.

2. Klicken Sie in der unteren rechten Ecke, klicken Sie auf das Zahnradsymbol, und wählen Sie **Repository > Google (nicht unterstützt)**:

    [![Das Repository festlegen an Google](android-p-images/vs/set-repo-sml.png)](android-p-images/vs/set-repo.png#lightbox)

3. Installieren Sie die **Android P** -Pakete, die als angezeigt werden **Android SDK Platform-28** in die **Plattformen** Registerkarte (Weitere Informationen zur Verwendung des SDK-Managers finden Sie unter (Android SDK-Setup)[~/android/get-started/installation/android-sdk.md]): 

    [![Installieren von Android-P-Paketen](android-p-images/vs/sdk-manager-sml.png)](android-p-images/vs/sdk-manager.png#lightbox)

4. Wenn Sie einen Emulator verwenden, erstellen Sie ein virtuelles Gerät, unterstützt **-API-Ebene 28**. Weitere Informationen zum Erstellen von virtuellen Geräten finden Sie unter [Verwalten von virtuellen Geräten mit Android-Geräte-Manager](~/android/get-started/installation/android-emulator/device-manager.md).



### <a name="start-a-xamarinandroid-project"></a>Ein Xamarin.Android-Projekt starten

Erstellen eines neuen Xamarin.Android-Projekts an. Wenn Sie die Android-Entwicklung mit Xamarin vertraut sind, finden Sie unter [Hallo, Android](~/android/get-started/hello-android/index.md) um weitere Informationen zum Erstellen von Xamarin.Android-Projekte.

Wenn Sie ein Android-Projekt erstellen, müssen Sie die versionseinstellungen Ziel Android P konfigurieren oder höher. Z. B. zur Ausrichtung auf des Projekts für Android-P, müssen Sie konfigurieren die Android-API-Zielebene des Projekts in **Android P (API-28)**. Es wird empfohlen, dass Sie auch Ihre Ziel-Frameworkebene und API-28 oder höher festlegen. Weitere Informationen zum Konfigurieren von Android-API-Ebene Level, finden Sie unter [Understanding Android API-Ebenen](~/android/app-fundamentals/android-api-levels.md).


### <a name="configure-a-device-or-emulator"></a>Konfigurieren von einem Gerät oder Emulator

Wenn Sie z. B. eines Pixels ein physisches Gerät verwenden, können Sie Ihr Gerät auf die Android-P-Vorschau aktualisieren, mithilfe der Anweisungen in [Android P-Beta-Geräte](https://developer.android.com/preview/devices/).

Wenn Sie einen Emulator verwenden, erstellen Sie ein virtuelles Gerät für API-Ebene mithilfe eines Images X86-basierten 28. Weitere Informationen zur Verwendung von Android-Geräte-Manager zum Erstellen und Verwalten von virtuellen Geräten finden Sie unter [Verwalten von virtuellen Geräten mit Android-Geräte-Manager](~/android/get-started/installation/android-emulator/device-manager.md).
Weitere Informationen zur Verwendung von Android-Emulator zum Testen und Debuggen, finden Sie unter [Debuggen mit der Google Android Emulator](~/android/deploy-test/debugging/android-sdk-emulator/index.md).



## <a name="new-features"></a>Neue Funktionen

Android P wird eine Vielzahl neuer Features eingeführt. Einige dieser neuen Features sollen nutzen, neue Hardwarefunktionen, die von der neuesten Android-Geräte bereitgestellt werden, während andere entworfen werden, um die Android-benutzerfreundlichkeit weiter zu verbessern:

-   **Anzeigeunterstützung Ausschnitt** &ndash; bietet APIs, um den Speicherort und die Form des finden die _Ausschnitt_ am oberen Rand des Bildschirms auf neueren Android-Geräten.

-   **Verbesserungen der Benachrichtigung** &ndash; können jetzt Benachrichtigungen anzeigen, Bilder und ein neues `Person` Klasse wird verwendet, um die Teilnehmer der Konversation zu vereinfachen.

-   **Ruhiges Positionierung** &ndash; Neuheit Unterstützung für das WLAN-Round-Trip-Zeit-Protokoll, das apps über WiFi-Geräte für die Navigation in ruhiges Einstellungen ermöglicht.

-   **Unterstützung für Multi-Kamera** &ndash; gleichzeitig bietet die Möglichkeit in Streams für den Zugriff von mehreren physischen Kameras (z. B. Dual-Front "und" Dual-Back-Kameras).


In den folgenden Abschnitten markieren diese Funktionen und angeben, dass die Nutzung in Ihrer app kurze Codebeispiele können Sie beginnen.

### <a name="display-cutout-support"></a>Ausschnitt anzeigeunterstützung

Viele neuere Android-Geräte mit Edge-to-Edge-Bildschirme sind eine *Ausschnitt anzeigen* (oder "Kerbe") am oberen Rand der Anzeige der Kamera und hält Vorträge.
Der folgende Screenshot enthält ein Beispiel für Emulator einen Ausschnitt:

[![Android-Emulator simulieren-Ausschnitt](android-p-images/02-example-cutout-sml.png)](android-p-images/02-example-cutout.png#lightbox)

Um zu verwalten wie Ihre app-Fenster seinen Inhalt auf Geräten mit einem Display-Ausschnitt zeigt, Android P wurde hinzugefügt, ein neues [LayoutInDisplayCutoutMode](https://developer.android.com/reference/android/view/WindowManager.LayoutParams.html#layoutInDisplayCutoutMode) Fenster Layout-Attribut. Dieses Attribut kann auf einen der folgenden Werte festgelegt werden:

-   [LayoutInDisplayCutoutModeNever](https://developer.android.com/reference/android/view/WindowManager.LayoutParams.html#LAYOUT_IN_DISPLAY_CUTOUT_MODE_NEVER) &ndash; Fenster ist nie zulässig Ausschnitt Bereich überschneiden.

-   [LayoutInDisplayCutoutModeShortEdges](https://developer.android.com/reference/android/view/WindowManager.LayoutParams.html#LAYOUT_IN_DISPLAY_CUTOUT_MODE_SHORT_EDGES) &ndash; Fenster in den Bereich der Ausschnitt jedoch nur an der kurzen Kante des Bildschirms erweitern können. 

-   [LayoutInDisplayCutoutModeDefault](https://developer.android.com/reference/android/view/WindowManager.LayoutParams.html#LAYOUT_IN_DISPLAY_CUTOUT_MODE_DEFAULT) &ndash; Fenster kann in den Bereich der Ausschnitt erweitert werden soll, wenn der Ausschnitt in einer Systemleiste enthalten ist.

Um zu verhindern, dass das app-Fenster überschneidet sich mit den Ausschnitt-Bereich, legen Sie beispielsweise den Ausschnitt Layoutmodus auf *nie*: 

```csharp
Window.Attributes.LayoutInDisplayCutoutMode =
    Android.Views.LayoutInDisplayCutoutMode.Never;
```

Die folgenden Beispiele enthalten Beispiele für diesen Ausschnitt-Modi. Der erste Screenshot auf der linken Seite ist für die app im nicht-Vollbildmodus. Im Screenshot Center ist die app wechselt Vollbild-mit `LayoutInDisplayCutoutMode` festgelegt `LayoutInDisplayCutoutModeShortEdges`. Beachten Sie, dass es sich bei der app weißer Hintergrund in den Anzeigebereich der Ausschnitt erweitert:

[![Beispiel Anzeigemodi Ausschnitt im emulator](android-p-images/03-cutout-modes-sml.png)](android-p-images/03-cutout-modes.png#lightbox)

Im letzten Screenshot (oben auf der rechten Seite), `LayoutInDisplayCutoutMode` nastaven NA hodnotu `LayoutInDisplayCutoutModeShortNever` vor zum Vollbildmodus gewechselt wird.
Beachten Sie, dass der app weißer Hintergrund darf nicht auf den Anzeigebereich der Ausschnitt erweitert.

Wenn Sie ausführlichere Informationen zu den Ausschnitt-Bereich auf dem Gerät benötigen, können Sie die neue [DisplayCutout](https://developer.android.com/reference/android/view/DisplayCutout.html) Klasse. `DisplayCutout` Stellt den Bereich der Anzeige, die verwendet werden kann, um Inhalt anzuzeigen. Sie können diese Informationen verwenden, um die Position und Form der Ausschnitt abzurufen, damit Ihre app nicht versucht, Inhalt in diesem Bereich nicht funktionsbezogenen angezeigt.

Weitere Informationen zu den neuen Ausschnitt-Features in Android P, finden Sie unter [Ausschnitt Anzeigeunterstützung](https://developer.android.com/preview/features#cutout).



### <a name="notifications-enhancements"></a>Verbesserungen für Benachrichtigungen

Android P führt die folgenden Verbesserungen messaging verbessern:

-   Benachrichtigungskanäle (eingeführt in [Android Oreo](~/android/platform/oreo.md)) unterstützt jetzt die Blockierung des Channel-Gruppen.

-   Das Benachrichtigungssystem verfügt über drei neue-Not-stören Kategorien (Priorisieren von Alarmen, Systemsounds und Medien). Darüber hinaus stehen sieben neue-Not-stören Modi, die mit dem visual Unterbrechungen (z. B. Badges, Benachrichtigung Beleuchtung, Status Leiste Darstellungen und Vollbild-Aktivitäten starten) unterdrückt werden können.

-   Ein neues [Person](https://developer.android.com/reference/android/app/Person.html) -Klasse wurde hinzugefügt, die den Absender einer Nachricht darstellt. Diese Klasse hilft, die um das Rendern von jede Benachrichtigung zu optimieren, indem Sie in einer Konversation (einschließlich ihrer Avatare und URIs) beteiligten Personen zu identifizieren.

-   Benachrichtigungen können Images jetzt anzeigen. 

Das folgende Beispiel veranschaulicht, wie Sie die neuen APIs verwenden, um eine Benachrichtigung generieren, die ein Bild enthält. In den folgenden Screenshots eine SMS-Benachrichtigung gesendet wird und eine Benachrichtigung mit der ein eingebettetes Bild folgt. Die zweite Benachrichtigung wird vergrößert, wenn die Benachrichtigungen erweitert werden, (wie auf der rechten Seite dargestellt), wird der Text von der ersten Benachrichtigung angezeigt, und das Bild in eingebetteten:

[![Beispiel-Benachrichtigung mit Bild](android-p-images/04-example-notifications-sml.png)](android-p-images/04-example-notifications.png#lightbox)

Das folgende Beispiel veranschaulicht, wie Sie ein Bild in einer Android-P-Benachrichtigung enthalten, und es veranschaulicht die Verwendung der neuen `Person` Klasse:

1. Erstellen Sie eine `Person` -Objekt, den Absender darstellt. Z. B. Name und das Symbol des Senders befinden sich im `fromPerson`:

    ```csharp
    Icon senderIcon = Icon.CreateWithResource(this, Resource.Drawable.sender_icon);
    Person fromPerson = new Person.Builder()
        .SetIcon(senderIcon)
        .SetName("Mark Sender")
        .Build();
    ```

2. Erstellen Sie eine `Notification.MessagingStyle.Message` , enthält das Bild, das senden möchten, übergeben das Bild, das die neue [Notification.MessagingStyle.Message.SetData](https://developer.android.com/reference/android/app/Notification.MessagingStyle.Message.html#setData%28java.lang.String,%20android.net.Uri) Methode.
   Zum Beispiel:

    ```csharp
    Uri imageUri = Uri.Parse("android.resource://com.xamarin.pminidemo/drawable/example_image");
    Notification.MessagingStyle.Message message = new Notification.MessagingStyle
            .Message("Here's a picture of where I'm currently standing", 0, fromPerson)
            .SetData("image/", imageUri);
    ```

3. Fügen Sie die Nachricht an eine `Notification.MessagingStyle` Objekt. Zum Beispiel:

    ```csharp
    Notification.MessagingStyle style = new Notification.MessagingStyle(fromPerson)
            .AddMessage(message);
    ```

4. Schließen Sie dieses Format, in der Benachrichtigung-Generator. Zum Beispiel:

    ```csharp
    builder = new Notification.Builder(this, MY_CHANNEL)
        .SetContentTitle("Tour of the Colosseum")
        .SetContentText("I'm standing right here!")
        .SetSmallIcon(Resource.Mipmap.ic_notification)
        .SetStyle(style)
        .SetChannelId(MY_CHANNEL);
    ```

5. Veröffentlichen Sie die Benachrichtigung ein. Zum Beispiel:

    ```csharp
    const int notificationId = 1000;
    notificationManager.Notify(notificationId, builder.Build());
    ```

Weitere Informationen zum Erstellen von Benachrichtigungen finden Sie unter [lokale Benachrichtigungen](~/android/app-fundamentals/notifications/local-notifications.md).


### <a name="indoor-positioning"></a>Ruhiges Positionierung

Android P bietet Unterstützung für IEEE 802.11mc (auch bekannt als _WiFi Round-Trip-Zeit_ oder _WiFi RTT_), wodurch es möglich, für apps, um die Entfernung zu einem zu erkennen oder weitere Wi-Fi-Zugriffspunkte. Mithilfe dieser Informationen kann für Ihre app nutzen *ruhiges Positionierung* mit einer Genauigkeit von ein bis zwei Verbrauchseinheiten. Auf Android-Geräten, die für IEEE 801.11mc Hardware unterstützen, kann Ihre app Navigationsfunktionen, z. B. standortbasierte-Steuerelement von smarten Geräten über autonomes oder Turn-von-Turn-Anweisungen über eine Store anbieten:

[![Beispiel für ruhiges Navigation, die über WiFi RTT](android-p-images/05-wifi-rtt-sml.png)](android-p-images/05-wifi-rtt.png#lightbox)

Die neue [WifiRttManager](https://developer.android.com/reference/android/net/wifi/rtt/WifiRttManager) Klasse und mehrere Hilfsklassen, bietet die Möglichkeit zum Messen der Entfernung für Wi-Fi-Geräte. Weitere Informationen zu den ruhiges positionierungs-APIs, die in Android P eingeführt wurden, finden Sie unter [Android.Net.Wifi.Rtt](https://developer.android.com/reference/android/net/wifi/rtt/package-summary).


### <a name="multi-camera-support"></a>Multi-Kamera-Unterstützung

Viele neuere Android-Geräte haben Dual-Front "und/oder" Dual-Back-Kameras, die nützlich für Features wie Stereo Bildanalyse, verbesserte visuelle Effekte und verbesserte Zoom-Funktion sind. Android P wird ein neuer [Multi-Kamera](https://developer.android.com/preview/features#camera) -API, die Ihre app ermöglicht ein *logische Kamera* (oder *logische Multi-Kamera*), basiert auf zwei oder mehr physische Kameras.
Um zu bestimmen, ob das Gerät eine logische Multi-Kamera unterstützt, sehen Sie sich die Funktionen von jede Kamera auf dem Gerät, um festzustellen, ob es unterstützt [RequestAvailableCapabilitiesLogicalMultiCamera](https://developer.android.com/reference/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA).

Android P enthält auch eine neue [SessionConfiguration](https://developer.android.com/reference/android/hardware/camera2/params/SessionConfiguration.html) -Klasse, die zum Reduzieren Verzögerungen bei der ersten Erfassung und ist somit überflüssig zu starten, und starten die Kamera-Datenstrom verwendet werden kann.

Weitere Informationen zu Multi-Kamera-Unterstützung in Android P, finden Sie unter [Multi-Kamera-Unterstützung und Kamera Updates](https://developer.android.com/preview/features#camera).


### <a name="other-features"></a>Andere Funktionen

Darüber hinaus unterstützt Android P mehrere neue Features:

-   Die neue [AnimatedImageDrawable](https://developer.android.com/reference/android/graphics/drawable/AnimatedImageDrawable.html) -Klasse, die zum Zeichnen und Anzeigen von animierten Bildern verwendet werden kann.

-   Ein neues [ImageDecoder](https://developer.android.com/reference/android/graphics/ImageDecoder.html) -Klasse, die ersetzt `BitmapFactory`. `ImageDecoder` kann verwendet werden, um die Decodierung einer `AnimatedImageDrawable`.

-   Images für HDR (hoch dynamischen Bereich)-Video und HEIF (hohe Effizienz Image File Format) unterstützt.

-   Die [JobScheduler](https://developer.android.com/reference/android/app/job/JobScheduler.html) wurde verbessert, um intelligentere netzwerkbezogener Aufträge zu verarbeiten. Die neue [GetNetwork](https://developer.android.com/reference/android/app/job/JobParameters#getNetwork%28%29) Methode der [JobParameters](https://developer.android.com/reference/android/app/job/JobParameters) -Klasse gibt das beste Netzwerk für die Durchführung jeder netzwerkanforderungen für einen bestimmten Auftrag zurück.

Weitere Informationen über die neuesten Android-P-Funktionen finden Sie unter [Android P-Funktionen und APIs](https://developer.android.com/preview/features).


## <a name="behavior-changes"></a>Verhaltensänderungen

Wenn die Android-Zielversion auf API-Ebene 28 festgelegt ist, sind mehrere plattformänderungen, die das Verhalten Ihrer app auswirken können, selbst wenn Sie nicht die neuen Features, die oben beschriebenen implementieren. Im folgenden finden eine kurze Zusammenfassung dieser Änderungen:

-  Apps müssen die Vordergrund-Berechtigung vor der Verwendung von vordergrunddienste jetzt anfordern.

-  Wenn Ihre Anwendung mehr als einem Prozess verfügt, kann nicht es Freigeben eines einzelnen [WebView](https://developer.xamarin.com/api/type/Android.Webkit.WebView/) Datenverzeichnis zwischen Prozessen.

-  Direkten Zugriff auf eine andere app-Datenverzeichnis anhand des Pfads ist nicht mehr zulässig.

Weitere Informationen zu verhaltensänderungen für apps für Android-P, finden Sie unter [Verhaltensänderungen](https://developer.android.com/preview/behavior-changes.html#p-apps).


## <a name="sample-code"></a>Beispielcode

[AndroidPMiniDemo](https://github.com/xamarin/monodroid-samples/tree/master/android-p/AndroidPMiniDemo) wird von eine Xamarin.Android-Beispiel-app für Android-P, das die festzulegende veranschaulicht, Ausschnitt, der Anzeigemodi Verwendung der neuen `Person` -Klasse, und wie Sie eine Benachrichtigung zu senden, die ein Bild enthält.


## <a name="summary"></a>Zusammenfassung

In diesem Artikel eingeführt, die Android-P-Preview und erläutert, wie zum Installieren und konfigurieren die neuesten Tools und Pakete für Xamarin.Android-Entwicklung mit der Android-P-Vorschau. Sie haben einen Überblick über die wichtigsten Features in Android-P, mit Beispiel-Quellcode für mehrere dieser Features bereitgestellt. Sie enthalten Links zur Dokumentation der API und erste Schritte mit Android-Entwickler-Themen, die Sie unterstützen Erstellen von apps für Android P. Sie markiert auch die wichtigsten Android P verhaltensänderungen, die vorhandene apps auswirken können.


## <a name="related-links"></a>Verwandte Links

- [Android-P-Entwicklervorschau](https://developer.android.com/preview/)