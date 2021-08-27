---
description: 'Questo argomento illustra come registrare un programma nel registro Windows come uno dei tipi di client seguenti: browser, posta elettronica, riproduzione multimediale, messaggistica immediata o macchina virtuale per Java.'
title: Registrazione di programmi con tipi client
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9c2d9a4589b684580250c487a6f83c3c9e79dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470419"
---
# <a name="registering-programs-with-client-types"></a>Registrazione di programmi con tipi client

Questo argomento illustra come registrare un programma nel registro Windows come uno dei tipi di client seguenti: browser, posta elettronica, riproduzione multimediale, messaggistica immediata o macchina virtuale per Java.

> [!Note]  
> Queste informazioni si applicano ai sistemi operativi seguenti:
> 
> -   Windows 2000 Service Pack 3 (SP3)
> -   Windows 2000 Service Pack 4 (SP4)
> -   Windows XP Service Pack 1 (SP1)
> -   Windows XP Service Pack 2 (SP2)
> -   Windows XP Service Pack 3 (SP3)
> -   Windows Server 2003
> -   Windows Vista
> -   Windows Vista Service Pack 1 (SP1)
> -   Windows 8

 

In questo argomento sono incluse le sezioni seguenti.

-   [Elementi di registrazione comuni per tutti i tipi di client](#common-registration-elements-for-all-client-types)
    -   [Selezione di un nome canonico](#selecting-a-canonical-name)
    -   [Registrazione del nome visualizzato di un programma](#registering-a-programs-display-name)
    -   [Icona di registrazione di un programma](#registering-a-programs-icon)
    -   [Registrazione di un verbo aperto](#registering-an-open-verb)
    -   [Registrazione delle informazioni di installazione](#registering-installation-information)
-   [Elementi di registrazione per tipi di client specifici](#registration-elements-for-specific-client-types)
    -   [Registrazione del menu Start](#start-menu-registration)
    -   [Registrazione client di posta elettronica](#mail-client-registration)
-   [Completare le registrazioni di esempio](#complete-sample-registrations)
    -   [Un browser di esempio](#a-sample-browser)
    -   [Un browser di posta elettronica di esempio](#a-sample-mail-browser)
    -   [Esempio di Media Player](#a-sample-media-player)
    -   [Un programma Instant Messenger di esempio](#a-sample-instant-messenger-program)
    -   [Una macchina virtuale di esempio per Java](#a-sample-virtual-machine-for-java)
-   [Argomenti correlati](#related-topics)

Questo argomento estende la documentazione esistente sulla registrazione di un programma come tipo di client specifico. Per i collegamenti a tale documentazione, vedere la sezione Argomenti correlati.

## <a name="common-registration-elements-for-all-client-types"></a>Elementi di registrazione comuni per tutti i tipi di client

Quando si registra un programma come tipo di client, la maggior parte delle voci del Registro di sistema sono uguali indipendentemente dal tipo di client. Alcune voci del Registro di sistema, tuttavia, sono specifiche del tipo di client e vengono notate nella sezione Elementi di registrazione [per tipi di client](#registration-elements-for-specific-client-types) specifici.

In questa sezione vengono illustrati gli argomenti seguenti:

-   [Selezione di un nome canonico](#selecting-a-canonical-name)
-   [Registrazione del nome visualizzato di un programma](#registering-a-programs-display-name)
-   [Icona di registrazione di un programma](#registering-a-programs-icon)
-   [Registrazione di un verbo aperto](#registering-an-open-verb)
-   [Registrazione delle informazioni di installazione](#registering-installation-information)

> [!Note]  
> I nomi delle sottochiavi specificati in corsivo in questo argomento sono segnaposto per i nomi di sottochiavi definiti dall'utente o un set di valori possibili. Esempi completi con nomi di esempio sono disponibili nella [sezione Registrazioni di esempio](#complete-sample-registrations) complete.

 

Tutte le informazioni di registrazione del tipo di client vengono archiviate nella sottochiave seguente:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*ClientTypeName* è uno dei nomi delle sottochiavi seguenti:

-   StartMenuInternet (per browser)
-   Posta elettronica (per la posta elettronica)
-   Elementi multimediali (per la riproduzione di contenuti multimediali)
-   Messaggistica immediata (per la messaggistica immediata)
-   JavaVM (per la macchina virtuale per Java)

In questo argomento si noteranno riferimenti a un programma di computer fittizio denominato "Lit View" di Litware Inc., con un file eseguibile denominato Litview.exe. Questo ipotetico programma viene usato in modo intercambiabile come instant messenger, un browser o un altro tipo di programma client, in base alle esigenze a scopo illustrativo.

### <a name="selecting-a-canonical-name"></a>Selezione di un nome canonico

Il fornitore deve scegliere un *nome canonico* per il programma. Il nome canonico non viene mai visualizzato all'utente, quindi non deve essere localizzato. L'unico scopo è fornire una stringa univoca che può essere usata per identificare il programma. In genere corrisponde al nome inglese del programma, ma si tratta semplicemente di una convenzione.

Per i tipi client diversi da browser, il nome canonico può essere qualsiasi stringa. Scegliere un nome univoco, che probabilmente non verrà usato da un altro fornitore.

Per i client browser, il nome canonico deve essere il nome, inclusa l'estensione, dell'eseguibile associato. ad esempio, "Litview.exe".

Ecco alcuni esempi di nomi canonici.

-   Iexplore.exe (browser)
-   Windows Posta elettronica (posta elettronica)
-   Windows Media Player (supporti)
-   Windows Messenger (messaggistica immediata)

Registrare il nome canonico creando una sottochiave come illustrato di seguito. Il nome della sottochiave è il nome canonico. Tutte le informazioni relative alla registrazione del programma saranno disponibili in questa sottochiave.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>Registrazione del nome visualizzato di un programma

Il passaggio successivo nella registrazione consiste nello specificare il nome visualizzato del programma. Viene specificato come valore sotto la chiave del nome canonico, come illustrato di seguito. Si noti anche in questo caso che *CanonicalName* e *ClientTypeName* non sono i nomi effettivi delle chiavi, ma solo i segnaposto per i nomi reali, ad esempio *Lit View.*

> [!Note]  
> A Windows 8, il nome usato per la registrazione per Impostare l'accesso [](default-programs.md) ai programmi e le impostazioni predefinite del [computer (SPAD)](cpl-setprogramaccess.md) e per Programmi predefiniti deve corrispondere per consentire alle modifiche SPAD di attivare le registrazioni di Programmi predefiniti.

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

Il **valore LocalizedString** è una stringa REG SZ ed è costituito da un segno "at" (@), il percorso completo di un file .dll o .exe, una virgola, un segno meno e un numero intero \_ decimale. Il numero intero decimale è l'ID di una risorsa stringa, contenuta nel file .dll o .exe, il cui valore deve essere visualizzato all'utente come nome del client. Si noti che il percorso del file non richiede le virgolette, anche se contiene spazi.

La registrazione della stringa del nome visualizzato in questo modo consente di usare la stessa registrazione per più lingue. Ogni installazione della lingua fornisce un file di risorse diverso con il nome visualizzato archiviato nello stesso ID risorsa.

L'esempio seguente illustra la registrazione per un programma di messaggistica istantanea Lit View fittizio. Poiché si tratta di un programma di messaggistica immediata, la sottochiave *CanonicalName* (in questo caso *Lit View)* viene archiviata nella sottochiave **IM.**

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Si noti l'uso della voce (Default) come dichiarazione secondaria del nome visualizzato del client. Se **LocalizedString** non è presente, viene usato il valore (Predefinito). Funziona con tutti i tipi di client (browser Internet, browser di posta elettronica, messaggistica istantanea e lettori multimediali). Per compatibilità con le versioni precedenti con il layout del Registro di sistema client di [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), i programmi di posta elettronica devono impostare il valore (predefinito) della sottochiave *CanonicalName* sul nome visualizzato del client nella lingua attualmente installata.

### <a name="registering-a-programs-icon"></a>Icona di registrazione di un programma

> [!Note]  
> Questa sezione non si applica a Windows 2000.

 

Per impostazione predefinita, la sezione superiore del **menu** Start Windows XP e Windows Vista contiene le icone **Internet** **e Posta** elettronica. Queste icone non sono presenti in Windows 7 e versioni successive. Per i client browser e di posta elettronica, quando un programma viene assegnato come predefinito per il tipo di client, per tali voci del menu **Start** viene visualizzata l'icona registrata del programma.

La registrazione dell'icona di un programma è obbligatoria per i client browser e di posta elettronica. La registrazione di un'icona per la riproduzione multimediale, la messaggistica immediata o la macchina virtuale per i tipi di client Java è facoltativa e le icone registrate per tali tipi di client non vengono attualmente usate da Windows e non vengono visualizzate nella sezione superiore dei **menu** Start di Windows XP o Windows Vista.

Per registrare un'icona per un programma client, aggiungere una **sottochiave DefaultIcon** con un valore predefinito, come illustrato di seguito.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

Il **valore FilePath** è il percorso completo del file che contiene l'icona. Questo percorso non richiede virgolette, anche se contiene spazi.

Il **valore IconIndex** viene interpretato come segue:

-   Se **IconIndex** è un numero positivo, il numero viene usato come indice della matrice in base *zero* delle icone archiviate nel file. Ad esempio, se **IconIndex** è 1, la seconda icona viene caricata dal file.
-   Se **IconIndex è** un numero negativo, il valore assoluto **di IconIndex** viene usato come identificatore di risorsa (anziché l'indice) per l'icona. Ad esempio, se **IconIndex** è -3, l'icona il cui identificatore di risorsa è 3 viene caricata dal file.

L'esempio seguente illustra la registrazione di un ipotetico browser Lit View. La seconda icona archiviata nel file Litview.exe viene usata come impostazione predefinita.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>Registrazione di un verbo aperto

> [!Note]  
> Questa sezione non si applica a Windows 2000. Il passaggio seguente è necessario solo per i client browser e di posta elettronica.

 

Si supponga che un utente abbia selezionato il programma come programma Internet o di posta elettronica predefinito. L'utente fa clic **sull'icona Internet** o **Posta** elettronica nel **menu** Start Windows XP o Windows Di Vista per aprire il programma. A questo punto, viene eseguita la riga di comando registrata come illustrato di seguito.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

La riga di comando deve specificare un percorso assoluto completo del file, seguito da opzioni facoltative della riga di comando. Se il tipo di voce è REG EXPAND SZ, è possibile usare variabili di \_ \_ ambiente nel percorso. Usare le virgolette in modo appropriato per assicurarsi che gli spazi nella riga di comando non siano interpretati erroneamente. La riga di comando deve eseguire il programma con le impostazioni predefinite appropriate. Per impostazione predefinita, i browser vengono home page. I programmi di posta elettronica in genere aprono la cartella Posta in **arrivo dell'utente.**

L'esempio seguente illustra la registrazione di un `open` verbo per un ipotetico browser Lit View. Non specifica opzioni della riga di comando.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

Si noti che in questo valore le virgolette vengono inserite intorno al percorso perché contiene spazi incorporati. L'omissione di queste virgolette potrebbe causare un'errata interpretazione della riga di comando.

### <a name="registering-installation-information"></a>Registrazione delle informazioni di installazione

> [!Note]  
> Questa sezione non si applica a Windows Server 2003.

 

-   [Comando Reinstalla](#the-reinstall-command)
-   [Comando Nascondi icone](#the-hide-icons-command)
-   [Comando Mostra icone](#the-show-icons-command)
-   [Configurazione del programma di gruppo](#group-program-configuration)
-   [Esempio di registrazione del browser](#browser-registration-example)

La funzionalità in base alla quale l'utente seleziona i programmi predefiniti per computer viene denominata e vi si accede come illustrato nella tabella seguente. (Windows Vista ha introdotto una nuova funzionalità, Imposta i programmi **predefiniti,** in base alla quale un utente può impostare le impostazioni predefinite per utente.




| Sistema operativo | Titolo | Percorso di accesso | 
|------------------|-------|-----------------|
| Windows 7 | Impostare l'accesso ai programmi e le impostazioni predefinite del computer | <ul><li><strong>Opzione</strong> <strong>Programmi predefiniti del</strong> menu Start</li><li><strong>Programmi predefiniti</strong> Pannello di controllo elemento</li></ul> | 
| Windows Vista | Impostare l'accesso ai programmi e le impostazioni predefinite del computer | <ul><li><strong>Opzione</strong> <strong>Programmi predefiniti del</strong> menu Start</li><li><strong>Programmi predefiniti</strong> Pannello di controllo elemento</li></ul> | 
| Windows XP SP2 | Impostare l'accesso ai programmi e le impostazioni predefinite | <ul><li><strong>Menu Start</strong></li><li><strong>Installazione applicazioni</strong> Pannello di controllo elemento</li></ul> | 
| Windows XP SP1 | Configurare i programmi | <ul><li><strong>Installazione applicazioni</strong> Pannello di controllo elemento</li></ul> | 




 

Per semplicità, questo argomento usa il Windows 7 della funzionalità. Tutte le versioni della funzionalità sono comunemente definite SPAD.

> [!Note]  
> Se si esegue Windows 2000 o Windows XP, è necessario avere installato almeno Windows 2000 SP3 o Windows XP SP1 per visualizzare la pagina Imposta accesso ai programmi e impostazioni **predefinite.** In Windows Vista e versioni successive, l'accesso alla pagina **Imposta** accesso ai programmi e impostazioni predefinite computer richiede privilegi di amministratore. Per questo motivo, gli sviluppatori sono invitati a registrarsi per l'elemento Imposta i programmi [predefiniti](default-programs.md) Pannello di controllo in modo che qualsiasi utente possa gestire le impostazioni predefinite dell'applicazione.

 

L'albero del Registro di sistema seguente mostra l'ampia gamma di informazioni che devono essere registrate nella chiave **InstallInfo** del programma in modo che il programma venga visualizzato nella pagina Imposta l'accesso ai programmi e le impostazioni predefinite del **computer** come opzione per il tipo di client. Ognuno di questi valori viene descritto in dettaglio nelle sezioni seguenti.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

La riga di comando deve specificare un percorso assoluto completo del file, seguito da opzioni facoltative della riga di comando. Usare le virgolette in modo appropriato per assicurarsi che gli spazi nella riga di comando non siano interpretati erroneamente.

### <a name="the-reinstall-command"></a>Comando Reinstalla

La riga di comando di reinstallazione dichiarata nel valore ReinstallCommand viene eseguita quando l'utente usa la pagina Imposta accesso ai programmi e impostazioni predefinite del **computer** per selezionare il programma come predefinito per il tipo di client. In Windows Vista e versioni successive, l'accesso a questa pagina richiede un livello di privilegi di amministratore. In Windows 8, se l'applicazione è stata registrata  con lo stesso nome sia per Impostazione accesso ai programmi che per Impostazioni predefinite computer e Programmi predefiniti **,** le impostazioni predefinite specificate **in** Programmi predefiniti per tale applicazione verranno applicate per l'utente corrente, nonché per l'esecuzione del comando reinstallazione.

Il programma avviato dalla riga di comando di reinstallazione [](/previous-versions//aa767743(v=vs.85)) deve associare l'applicazione al set completo di tipi di [file](fa-intro.md) e protocollo che l'applicazione può gestire. Tutte le applicazioni devono stabilire la funzionalità del gestore nel comando reinstallazione. Le applicazioni possono usare il comando reinstallazione per registrare la funzionalità e, facoltativamente, stabilire lo stato predefinito. Quando un'applicazione sceglie di implementare sia la funzionalità che lo stato del gestore predefinito nel comando di reinstallazione, deve anche ripristinare tutti i collegamenti o i collegamenti visibili desiderati. I punti di ingresso visibili che la maggior parte delle applicazioni sceglie sono elencati nel [comando Nascondi icone](#the-hide-icons-command).

> [!Note]  
> È consigliabile che le applicazioni implementino la funzionalità di gestione nel comando reinstallazione.

 

Al termine del processo di reinstallazione, il programma avviato dalla riga di comando di reinstallazione dovrebbe uscire. Non deve avviare il programma corrispondente. deve semplicemente registrare le impostazioni predefinite. Ad esempio, il comando reinstalla per un browser non deve aprire il home page dell'utente.

> [!Note]  
> Per i client browser e di posta elettronica in Windows XP e Windows Vista, le applicazioni che scelgono di stabilire la funzionalità di gestione e lo stato predefinito nel comando reinstalla devono registrarsi per l'icona corrispondente nella parte superiore del menu Start. Per [altre informazioni, vedere Registrazione](#start-menu-registration) del menu Start.

 

### <a name="the-hide-icons-command"></a>Comando Nascondi icone

La riga di comando dichiarata nel valore HideIconsCommand  viene eseguita quando l'utente deseleziona la casella Abilita accesso a questo programma nella pagina Imposta accesso ai programmi e impostazioni **predefinite del** computer. Questa riga di comando deve nascondere tutti i punti di accesso del programma visibili nell'interfaccia utente. Le linee guida specifiche sono la rimozione di collegamenti e icone dalle posizioni seguenti:

-   Icone del desktop
-   menu Start, incluso il **gruppo Startup**
-   Avvio veloce sulla barra
-   Area delle notifiche
-   Menu di scelta rapida
-   Banda attività cartella

Questa riga di comando deve anche impedire chiamate automatiche del programma, ad esempio quelle specificate nella **chiave esegui** del Registro di sistema. I fornitori sono invitati a implementare queste linee guida nel callback Nascondi accesso dell'applicazione.

Non è necessario rinunciare alla registrazione (funzionalità dell'applicazione) dei tipi di file quando le icone sono nascoste. Non è inoltre necessario rinunciare allo stato predefinito dell'applicazione per i tipi di file e di protocollo. Questa operazione può causare un'esperienza utente non ottimale quando questi tipi vengono rilevati nell'interfaccia utente.

Dopo aver nascosto correttamente le icone, è necessario aggiornare il valore del Registro di sistema IconsVisible su 0, come illustrato:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

La voce IconsVisible è di tipo **REG \_ DWORD**.

### <a name="an-alternate-hide-icons-method-in-spad"></a>Metodo Nascondi icone alternative in SPAD

Per alcune applicazioni legacy, un'implementazione completa di Nascondi accesso potrebbe non essere pratica. Un metodo alternativo che ottiene lo stesso effetto consiste nel disinstallare l'applicazione. La sezione seguente illustra il comportamento di esempio e il codice di esempio per implementare questa alternativa. In generale, i fornitori di software indipendenti (ISV) devono evitare questa alternativa perché:

-   Disinstallare completamente l'applicazione dal sistema.
-   Rimuovere le impostazioni predefinite selezionate in precedenza.
-   Non lasciare alcuna opzione dell'interfaccia utente per reinstallare l'applicazione.
-   Rendere la funzionalità di abilitazione dell'accesso non più disponibile, poiché una disinstallazione rimuove completamente l'applicazione da SPAD.

L'esperienza utente consigliata è la seguente:

-   Quando l'utente deseleziona la casella **Abilita l'accesso** a questo programma in SPAD, viene visualizzata l'interfaccia utente seguente.

    ![finestra di dialogo che consente di nascondere l'accesso al programma](images/hideaccessvista.png)

-   Quando l'utente seleziona **OK,** viene avviato **l'elemento Programmi** e funzionalità Pannello di controllo per consentire all'utente di disinstallare l'applicazione.
-   Windows Gli utenti XP devono essere presentati con questa finestra di dialogo.

    ![finestra di dialogo equivalente di Windows XP](images/hideaccessxp.png)

-   Quando l'Windows XP seleziona **OK**, viene avviata la voce Installazione applicazioni **Pannello di controllo** per consentire all'utente di disinstallare l'applicazione.

Il codice seguente fornisce un'implementazione riutilizzabile per la funzionalità Nascondi accesso come descritto in precedenza. Può essere usato in Windows XP, Windows Vista e Windows 7.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a>Comando Mostra icone

La riga di comando dichiarata nella voce ShowIconsCommand  viene eseguita quando l'utente controlla la casella Abilita accesso a questo programma nella pagina Imposta impostazioni predefinite per l'accesso al programma **e il** computer. Questa riga di comando può ripristinare i punti di accesso del programma, inclusi quelli nel menu **Start,** sul desktop e nel gruppo **Avvio,** nonché le normali chiamate automatiche, ad esempio quelle specificate nella chiave del Registro di sistema **Esegui.** I punti di accesso visibili di interesse per la maggior parte delle applicazioni sono elencati nel [comando Nascondi icone](#the-hide-icons-command). L'applicazione non deve modificare le impostazioni predefinite per utente. Tale modifica deve essere eseguita dall'utente tramite **Programmi predefiniti**.

Dopo aver visualizzato correttamente le icone, è necessario aggiornare il valore del Registro di sistema IconsVisible su 1, come illustrato di seguito:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

Si noti che se è stata usata la voce HideIconsCommand per richiedere una disinstallazione dell'applicazione, la voce ShowIconsCommand non è utile. Deve essere rimosso dal Registro di sistema con il resto delle informazioni dell'applicazione durante il processo di disinstallazione.

### <a name="group-program-configuration"></a>Configurazione del programma di gruppo

> [!Note]  
> Questa sezione non si applica a Windows 2000.

 

Come parte della preparazione del sistema, un OEM può stabilire una configurazione che nasconde i punti di accesso per il browser Microsoft, la posta elettronica, la riproduzione di contenuti multimediali, la messaggistica istantanea o la macchina virtuale per i programmi client Java e specifica i propri programmi predefiniti. Gli OEM possono consentire agli utenti di reimpostare i computer in qualsiasi momento su questa configurazione predefinita impostando i valori del Registro di sistema seguenti.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

Se queste chiavi sono impostate, gli utenti possono  ripristinare la configurazione OEM selezionando l'opzione Produttore computer nella **pagina Imposta l'accesso** ai programmi e le impostazioni predefinite del computer. Se queste chiavi non sono impostate, **l'opzione Produttore** computer non viene visualizzata.

La **voce OEMShowIcons,** se presente, imposta lo stato di visualizzazione dell'icona per il client specificato che viene applicato se l'utente seleziona **Produttore computer**. Il valore 1 fa sì che le icone siano visualizzate e il valore 0 fa sì che le icone non siano visualizzate. Se **OEMMostraIcons** è assente, la selezione di **Produttore** computer non ha alcun effetto sull'impostazione di visualizzazione dell'icona. **OEMShowIcons** è di tipo **REG \_ DWORD**.

La **voce OEMDefault,** se presente e impostata su 1, stabilisce la preferenza OEM per il client predefinito del tipo indicato. Solo un client di un determinato tipo può essere contrassegnato come predefinito OEM. Se più di un client di registrazione contiene la **voce OEMDefault,** tutti vengono ignorati e il client corrente continua a essere usato come client predefinito. Se la **voce OEMDefault** non è presente o è presente e impostata su 0, quel particolare client non viene usato come client predefinito se l'utente seleziona **Produttore computer**. **OEMDefault** è di tipo **REG \_ DWORD**.

Oltre all'opzione per ripristinare la configurazione predefinita stabilita dall'OEM, gli utenti hanno altre tre opzioni di configurazione:

-   Impostare il computer su una configurazione Windows Microsoft. In questo caso, la **pagina Imposta** l'accesso ai programmi e le impostazioni predefinite del computer consente l'accesso a tutto il software Microsoft e non Microsoft nel computer registrato nelle categorie di prodotti pertinenti. I Windows microsoft sono selezionati come opzione predefinita per ogni categoria.
-   Impostare il computer su una configurazione non Microsoft. Questa configurazione nasconde i punti di accesso ,ad esempio il menu **Start,** Windows Internet Explorer, Windows Media Player, Windows Messenger e Microsoft Outlook Express. Consente l'accesso al software non Microsoft nel computer in queste categorie. Inoltre, se un programma non Microsoft è disponibile in una categoria, viene impostato come predefinito per tale categoria. Se in una categoria sono disponibili più programmi non Microsoft, all'utente viene chiesto di scegliere quale programma non Microsoft usare come predefinito.
-   Stabilire una configurazione personalizzata. Gli utenti effettuano le proprie selezioni per abilitare o rimuovere l'accesso, combinando i programmi Microsoft e non Microsoft in base alle esigenze. Gli utenti stabiliscono opzioni predefinite per categoria.

Gli utenti possono modificare queste opzioni in qualsiasi momento.

### <a name="browser-registration-example"></a>Esempio di registrazione del browser

L'esempio seguente illustra la registrazione **completa di InstallInfo** per un browser lit view fittizio. In questo caso le opzioni della riga di comando consentono al file Litview.exe di eseguire tutte le azioni necessarie per ogni valore.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

Si noti che le virgolette vengono posizionate intorno ai percorsi perché contengono spazi incorporati.

## <a name="registration-elements-for-specific-client-types"></a>Elementi di registrazione per tipi di client specifici

Le informazioni seguenti sono disponibili anche nelle risorse elencate nella sezione Argomenti correlati alla fine di questo argomento.

-   [Registrazione del menu Start](#start-menu-registration)
-   [Registrazione del client di posta elettronica](#mail-client-registration)

### <a name="start-menu-registration"></a>Registrazione del menu Start

In Windows XP le applicazioni in genere registrate come predefinite in un ambito a livello di computer (**HKEY \_ LOCAL \_ MACHINE**) anziché in un ambito utente **(HKEY \_ CURRENT \_ USER).** Con l'introduzione Windows Vista del controllo dell'account utente, le applicazioni che attestano gli slot **Internet** e **posta** elettronica nel menu **Start** devono implementare il comando reinstall nel contesto di esecuzione corretto.

> [!Note]  
> Il menu Start **posta elettronica** è stato rimosso a Windows 7. Tuttavia, la registrazione descritta in questa sezione deve comunque essere eseguita perché assegna il client MAPI predefinito.

 

Un utente limitato in Windows XP, Windows Vista o Windows 7 non può accedere a SPAD. Per questo motivo, gli sviluppatori sono invitati a registrarsi per l'elemento Impostare i programmi predefiniti **Pannello di controllo** in modo che qualsiasi utente possa gestire le impostazioni predefinite delle applicazioni per utente.

Le selezioni effettuate in SPAD dovrebbero influire solo sulle impostazioni per computer.

Impostare il valore del Registro di sistema come indicato di seguito.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> **Le informazioni seguenti si applicano solo Windows XP.**
> 
> Se la registrazione dell'impostazione predefinita a livello di computer in HKEY LOCAL MACHINE come illustrato in precedenza ha esito positivo, l'applicazione deve eliminare il valore assegnato alla voce Default nella \_ \_ sottochiave seguente:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> Se la registrazione dell'impostazione predefinita a livello di computer in HKEY LOCAL MACHINE come illustrato in precedenza ha esito negativo, in genere perché l'utente non dispone dell'autorizzazione di scrittura per la sottochiave, l'applicazione deve impostare il \_ \_ valore seguente:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> In questo modo il nome canonico viene registrato solo per l'utente corrente, non per tutti gli utenti.

 

Dopo aver aggiornato le chiavi del Registro di sistema, il programma deve trasmettere il messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con **wParam** = 0 e **lParam** che punta alla stringa con terminazione Null "Client \\ \\ **ClientTypeName**" per notificare al sistema operativo che il client predefinito è stato modificato.

### <a name="mail-client-registration"></a>Registrazione del client di posta elettronica

Per un client di posta elettronica, il programma deve avere le impostazioni registrate nella chiave **mailto HKEY \_ CLASSES \_ ROOT** per poter soddisfare gli \\  URL che usano il `mailto` protocollo. Impostare i valori e le chiavi che rispecchiano tali impostazioni nella chiave seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

Questa gerarchia del Registro di sistema sostituisce la `mailto` gerarchia del Registro di sistema esistente disponibile in **HKEY \_ CLASSES \_ ROOT** \\ **mailto**. La gerarchia rimane invariata, solo la posizione è stata modificata. Il formato di questa gerarchia è documentato in MSDN in [Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85)). In genere, il protocollo viene registrato in un programma anziché in un protocollo asincrono, nel qual caso si applica la documentazione relativa alla registrazione di un'applicazione `mailto` [in uno schema URI.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

Nell'esempio seguente viene `mailto` illustrata la sezione della registrazione per un `mailto` gestore registrato in un programma.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

Il valore del Registro di sistema EditFlags è documentato in [Tipi di file](fa-file-types.md) nella sezione intitolata "Definizione degli attributi dei tipi di file".

## <a name="complete-sample-registrations"></a>Completare le registrazioni di esempio

Gli esempi seguenti vengono forniti per illustrare i requisiti di registrazione completi per i vari tipi di client.

-   [Browser di esempio](#a-sample-browser)
-   [Browser di posta elettronica di esempio](#a-sample-mail-browser)
-   [Esempio di Media Player](#a-sample-media-player)
-   [Programma Instant Messenger di esempio](#a-sample-instant-messenger-program)
-   [Una macchina virtuale di esempio per Java](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a>Browser di esempio

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a>Browser di posta elettronica di esempio

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a>Esempio di Media Player

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a>Programma Instant Messenger di esempio

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a>Una macchina virtuale di esempio per Java

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

*Le aziende, le organizzazioni, i prodotti, i nomi di dominio, gli indirizzi di posta elettronica, i logo, le persone, i luoghi e gli eventi di esempio qui rappresentati sono fittizi. Nessuna associazione con società, organizzazione, prodotto, nome di dominio, indirizzo di posta elettronica, logo, persona, luogo o evento è prevista o deve essere dedotta.*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmi predefiniti](default-programs.md)
</dt> <dt>

[Come registrare un browser Internet o un client di posta elettronica con Windows Menu Start](start-menu-reg.md)
</dt> <dt>

[Internet Explorer layout del Registro di sistema client (vedere la sezione "Definizioni delle chiavi del Registro di sistema del client")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[Panoramiche ed esercitazioni sul protocollo di collegamento asincrono](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
