# Sestavení APK

* * *

***Mějte prosím na paměti** při vytváření AndroidAPS 2.0 apk: **Konfigurace na vyžádání** není podporována v aktuální verzi Android Gradle pluginu! Jestliže vytváření apk selže s chybou "on demand configuration", proveďte následující změnu:*

     * * Otevřete okno Preferences klepnutím na File > Settings (v systému Mac, Android Studio > Preferences). *
     * * V levém podokně klepněte na Build, Execution, Deployment > Compiler.*
     * * Zrušte zaškrtnutí políčka Configure on demand.*
    

## * *Klepněte na tlačítko použít nebo OK.*

### Tento článek je rozdělený do dvou částí.

* V části Přehled najdete vysvětlení, které kroky jsou obecně nutné, abyste sestavili soubor APK.
* V části Průvodce krok za krokem najdete snímky obrazovky z konkrétní instalace. Jelikož se Android Studio (vývojové prostředí, které použijeme k sestavení APK) v čase mění velmi rychle, nebudou snímky úplně shodné s vaší instalací, ale určitě vám poskytnou dobrý záchytný bod. Android studio běží na Windows, Linuxu a Mac OS X, a proto mohou být na různých platformách malé rozdíly. Jestliže najdete něco zásadního, co je špatně, nebo vám něco chybí, prosím informujte o tom facebookovou skupinu „AndroidAPS users“ nebo použijte Gitter chat [Android APS](https://gitter.im/MilosKozak/AndroidAPS) nebo [AndroidAPSwiki](https://gitter.im/AndroidAPSwiki/Lobby), abychom se na to mohli podívat.

## Přehled

Následují obecné kroky k sestavení souboru APK:

* Instalujte git
* Instalujte a nastavte Android Studio.
* Použijte git, abyste si naklonovali zdrojové kódy z centrálního úložiště na Githubu, kam vývojáři umístili poslední zdrojové kódy aplikace.
* Otevřete naklonovaný projekt v Android Studiu jako aktivní projekt.
* Sestavete podepsané APK.
* Doručte podepsané APK na váš telefon.

## Průvodce krok za krokem

Následuje detailní popis kroků nutných k sestavení souboru APK.

## Nainstalujte Android Studio

* Instalujte git 
  * [Windows](https://gitforwindows.org/)
  * [Mac OS X](http://sourceforge.net/projects/git-osx-installer/)
  * Linux - prostě instalujte balíček git správcem balíčků z vaší distribuce
* Instalujte [Android Studio](https://developer.android.com/studio/install.html).
* Nastavte Android Studio při prvním spuštění

Zvolte "Do not import settings", protože jste tento software zatím nevyužívali.

![Snímek 1](../images/Installation_Screenshot_01.png)

Klikněte na "Next".

![Snímek 2](../images/Installation_Screenshot_02.png)

Vyberte "Standard" instalaci a klikněte na "Next".

![Snímek 3](../images/Installation_Screenshot_03.png)

Vyberte "Intellij" jako schéma uživatelského prostředí a klikněte na "Next".

![Snímek 4](../images/Installation_Screenshot_04.png)

Klikněte na "Next" v dialogovém okně "Verify Settings".

![Snímek 5](../images/Installation_Screenshot_05.png)

Emulátor Androidu (pro simulaci telefonu na vašem PC nebo Macu) se pro sestavení APK nepoužívá. Můžete kliknout na "Finish", abyste dokončili instalaci a odložili četbu dokumentace později na vyžádání.

![Snímek 6](../images/Installation_Screenshot_06.png)

Android Studio stahuje velké množství softwarových komponent, které používá. Můžete kliknout na tlačítko "Show Details" pro zobrazení detailů, které ale vůbec nejsou důležité.

![Snímek 7](../images/Installation_Screenshot_07.png)

![Snímek 8](../images/Installation_Screenshot_08.png)

Jakmile jsou stahování dokončena, klikněte na tlačítko "Finish".

![Snímek 9](../images/Installation_Screenshot_09.png)

* Hurá, hurá, nyní jste dokončili instalaci Android Studia a můžete začít s klonováním zdrojových souborů. Možná je teď vhodná doba na krátkou přestávku?

## Stáhněte si kód a další komponenty

* Použijte klonování gitu v Android Studiu, jak je vidět na snímku níže. Zvolte "Check out project from Version Control" s "Git" jako konkrétní verzí správce zdrojových kódů.

![Snímek 10](../images/Installation_Screenshot_10.png) ![Version_Control_Git](../images/Version_Control_Git.png)

Zadejte URL adresu do hlavního úložiště AndroidAPS ("https://github.com/MilosKozak/AndroidAPS") a klepněte na "Clone".

![Snímek 13](../images/Installation_Screenshot_13.png)

Android Studio začne s klonováním. Neklikejte na "Background", což by věci nyní pouze zkomplikovalo.

![Snímek 14](../images/Installation_Screenshot_14.png)

Dokončete načtení projektu od správce zdrojových kódů kliknutím na "Yes", což projekt otevře.

![Snímek 15](../images/Installation_Screenshot_15.png)

Použijte standardní "default gradle wrapper" a klikněte na "OK".

![Snímek 16](../images/Installation_Screenshot_16.png)

Přečtěte si okno "Tip of Day" a kliknutím na "Close" je zavřete.

![Snímek 17](../images/Installation_Screenshot_17.png)

* Super, máte vlastní kopii zdrojového kódu a jste připraveni na vytvoření Apk.
* Nyní se blížíme k první chybové zprávě. Naštěstí nám Android Studio nabídne její řešení.

Klikněte na "Install missing platform(s) and sync project", protože Android Studio potřebuje doinstalovat chybějící platformu.

![Snímek 18](../images/Installation_Screenshot_18.png)

Přijměte licenční ujednání zvolením "Accept" a kliknutím na "Next".

![Snímek 19](../images/Installation_Screenshot_19.png)

Jak již bylo řečeno v dialogovém okně, počkejte, než se stahování dokončí.

![Snímek 20](../images/Installation_Screenshot_20.png)

Nyní je dokončené. Prosím, klikněte na "Finish".

![Snímek 21](../images/Installation_Screenshot_21.png)

Aaaach, další chyba. Ale Android Studio navrhuje podobné řešení. Klikněte na "Install Build Tools and sync project", protože Android Studio potřebuje stáhnout chybějící pomůcky.

![Snímek 22](../images/Installation_Screenshot_22.png)

Jak již bylo řečeno v dialogovém okně, počkejte, než se stahování dokončí.

![Snímek 23](../images/Installation_Screenshot_23.png)

Nyní je dokončené. Prosím, klikněte na "Finish".

![Snímek 24](../images/Installation_Screenshot_24.png)

A další chyba k řešení, protože Android Studio potřebuje zase stáhnout chybějící platformu. Klikněte na "Install missing platform(s) and sync project".

![Snímek 25](../images/Installation_Screenshot_25.png)

Jak již bylo řečeno v dialogovém okně, počkejte, než se stahování dokončí.

![Snímek 26](../images/Installation_Screenshot_26.png)

Nyní je dokončené. Prosím, klikněte na "Finish".

![Snímek 27](../images/Installation_Screenshot_27.png)

Klikněte na "Install Build Tools and sync project", protože Android Studio potřebuje stáhnout chybějící pomůcky.

![Snímek 28](../images/Installation_Screenshot_28.png)

Jak již bylo řečeno v dialogovém okně, počkejte, než se stahování dokončí.

![Snímek 29](../images/Installation_Screenshot_29.png)

Nyní je dokončené. Prosím, klikněte na "Finish".

![Snímek 30](../images/Installation_Screenshot_30.png)

Ano, chybové zprávy jsou pryč a první gradle sestavení běží. Možná je čas dát si trochu vody?

![Snímek 31](../images/Installation_Screenshot_31.png)

<!--- Android Studio recommends we now update the gradle system to version 4.4. If you made this build for an AndroidAPS version before the release of at least a release candidate(RC) of version 2.0 do not follow this recommendation. Otherwise, the build will fail. The gradle system is a tool which Android Studio uses to control the build process. For AndroidAPS there is no disadvantage to using the old gradle version. The APK file in the end is not different. If you build a APK for version 2 of AndroidAPS feel free to upgrade the gradle system to version 4.4. ---> Android Studio recommends to update the gradle system. 

**Never update gradle!** This might lead to difficulties!

Please click "Don't remind me again for this project".

![Screenshot 32](../images/AS_NoGradleUpdate.png)

The build is running again.

![Screenshot 33](../images/Installation_Screenshot_33.png)

Yeah, the first build is successful but we are not finished.

![Screenshot 34](../images/Installation_Screenshot_34.png)

## Vytvořte podepsaný soubor APK

<!--- Do not forget to copy to update-to-new-version.md --->

In the menu select "Build" and then "Generate Signed Bundle / APK...". (The menu in Android Studio changed as of September 2018. In older versions select in the menu “Build” and then “Generate Signed APK...”.)  
Signing means that you sign your generated app but in a digital way as a kind of digital fingerprint in the app itself. That is necessary because Android has a rule that it only accepts signed code to run for security reasons. For more information on this topic, follow the link [here](https://developer.android.com/studio/publish/app-signing.html#generate-key) Security is a deep and complex topic and you don't need this now.

![Screenshot 39a](../images/Installation_Screenshot_39a.PNG)

In the following dialogue box select "APK" instead of "Android App Bundle" and click button "Next".

![Screenshot 39b](../images/Installation_Screenshot_39b.PNG)

Select "app" and click "Next".

![Screenshot 40](../images/Installation_Screenshot_40.png)

Click "Create new..." to start creating your keystore. A keystore in this case is nothing more than a file in which the information for signing is stored. It is encrypted and the information is secured with passwords. We suggest storing it in your home folder and remember the passwords but if you lose this information it's not a big issue because then you just have to create a new one. Best practice is to store this information carefully.

![Screenshot 41](../images/Installation_Screenshot_41.png)

* Vyplňte údaje pro další dialogové okno. 
  * Key store path: je cesta k vašemu úložišti klíčů
  * Políčka s hesly níže jsou pro úložiště klíčů a jsou zdvojená, aby se zabránilo překlepům.
  * Alias je název pro klíč, který potřebujete. Můžete ponechat výchozí, anebo si vybrat jakýkoli jiný název.
  * Políčka s hesly pod tím jsou pro samotný klíč. Jako vždy jsou zdvojená, aby se zabránilo překlepům.
  * Můžete ponechat "Validity (years)" na výchozí hodnotě 25.
  * Povinná pole jsou pouze jméno a příjmení, ale klidně můžete vyplnit i zbývající údaje. Pak klikněte na tlačítko „OK“.

![Screenshot 42](../images/Installation_Screenshot_42.png)

Fill in the information of the last dialog in this dialog and click "Next".

![Screenshot 43](../images/Installation_Screenshot_43.png)

Select "full" as flavour for the generated app. Select V1 "Jar Signature" (V2 is optional) and click "Finish". The following information might be important for later use.

* Možnost „Release“ by měla být výchozí volbou pro „Build Type“, možnost „Debug“ je pouze pro vývojáře.
* Vyberte typ sestavení, jaký budete chtít. 
  * full (tj. automatické doporučení pro uzavřenou smyčku)
  * openloop (tj. doporučení pro uživatele s otevřenou smyčkou)
  * pumpcontrol (tj. vzdálené ovládání pumpy bez smyčky)
  * nsclient (tj. zobrazují se data jiného uživatele se smyčkou a lze vkládat záznamy ošetření)

![Screenshot 44](../images/Installation_Screenshot_44.png)

In the event log you see that the Signed APK was generated successfully.

![Screenshot 45](../images/Installation_Screenshot_45.png)

Click the "locate" link in the event log.

![Screenshot 46](../images/Installation_Screenshot_46.png)

## Přeneste soubor APK do telefonu

<!--- Do not forget to copy to update-to-new-version.md --->

A file manager window opens. It might look a bit different on your system as I am using Linux. On Windows there will be the File Explorer and on Mac OS X the Finder. There you should see the directory with the generated APK file. Unfortunately this is the wrong place as "wear-release.apk" is not the signed "app" APK we are searching for.

![Screenshot 47](../images/Installation_Screenshot_47.png)

Please change to the directory AndroidAPS/app/full/release to find the "app-full-release.apk" file. Transfer this file to your Android smartphone. You can do it on your preferred way, i.e. Bluetooth, cloud upload, connect computer and phone by cable or use email. I use Gmail here in this example as it is fairly simple for me. I mention this because to install the self-signed app we need to allow Android on our smartphone to do this installation even if this file is received via Gmail which is normally forbidden. If you use something other please proceed accordingly.

![Screenshot 48](../images/Installation_Screenshot_48.png)

In the settings of your smartphone there is an area "unknown apps install" where I have to give Gmail the right to install APK files which I get via Gmail.

Vyberte možnost „Povolit z tohoto zdroje“. Po instalaci můžete tuto volbu zase zakázat.

![Installation from unknown sources](../images/Installation_Screenshot_49-50.png)

Posledním krokem je klepnout na soubor APK, který jsem přijal přes Gmail, a nainstalovat aplikaci. Pokud se APK nechce nainstalovat a máte v telefonu již starší verzi AndroidAPS, pravděpodobně byla podepsaná jiným klíčem – v tom případě musíte starou verzi nejdřív odinstalovat, avšak nezapomeňte předtím exportovat svá nastavení!

Ano, máte to a můžete začít s úvodní konfigurací AndroidAPS (CGM, inzulínová pumpa) atd.