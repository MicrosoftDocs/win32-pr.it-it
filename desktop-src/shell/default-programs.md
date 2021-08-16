---
description: Usare Programmi predefiniti per impostare l'esperienza utente predefinita.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programmi predefiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1cd54afe23291c191fdd045ca3cb42b68361aa8f7f3d8ef431042cfe9f5c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861358"
---
# <a name="default-programs"></a>Programmi predefiniti

Usare **Programmi predefiniti per** impostare l'esperienza utente predefinita. Gli utenti possono **accedere a Programmi** predefiniti Pannello di controllo o direttamente dal menu **Start.** [Lo strumento SPAD (Program Access and Computer Defaults),](cpl-setprogramaccess.md) l'esperienza predefinita principale per gli utenti in Windows XP, fa ora parte di **Programmi predefiniti.**

> [!IMPORTANT]
> Questo argomento non si applica a Windows 10. Il funzionamento delle associazioni di file predefinite è stato modificato in Windows 10. Per altre informazioni, vedere la sezione Modifiche **alla gestione** Windows 10 app predefinite in questo [post.](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

Quando un utente imposta le impostazioni predefinite del programma utilizzando Programmi predefiniti **,** l'impostazione predefinita si applica solo a tale utente e non ad altri utenti che potrebbero usare lo stesso computer. **Programmi** predefiniti fornisce un set di API (deprecate in Windows 8) che consentono ai fornitori di software indipendenti (ISV) di includere programmi o applicazioni nel sistema predefinito. Il set di API consente anche agli ISV di gestire meglio lo stato come valori predefiniti.

Questo argomento è organizzato come segue:

-   [Introduzione ai programmi predefiniti e al relativo set di API correlato](#introduction-to-default-programs-and-its-related-api-set)
-   [Registrazione di un'applicazione per l'utilizzo con programmi predefiniti](#registering-an-application-for-use-with-default-programs)
    -   [Progid](#progids)
    -   [Sottochiave di registrazione e descrizioni dei valori](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Esempio di registrazione completa](#full-registration-example)
-   [Diventare il browser predefinito](#becoming-the-default-browser)
-   [Interfaccia utente dei programmi predefiniti](#default-programs-ui)
-   [Procedure consigliate per l'utilizzo di programmi predefiniti](#best-practices-for-using-default-programs)
    -   [Durante l'installazione](#during-installation)
    -   [Dopo l'installazione](#after-installation)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Introduzione ai programmi predefiniti e al relativo set di API correlato

**Programmi predefiniti** è progettato principalmente per applicazioni che usano tipi di file standard, ad esempio file .mp3 o .jpg o protocolli standard, ad esempio HTTP o mailto. Le applicazioni che usano protocolli proprietari e associazioni di file non usano in genere la **funzionalità Programmi** predefiniti.

Dopo aver registrato un'applicazione per **la funzionalità Programmi** predefiniti, le opzioni e le funzionalità seguenti sono disponibili tramite il set di API:

-   Ripristinare tutte le impostazioni predefinite registrate per un'applicazione. Deprecato per Windows 8.
-   Ripristinare un singolo valore predefinito registrato per un'applicazione. Deprecato per Windows 8.
-   Eseguire una query per trovare il proprietario di un valore predefinito specifico in una singola chiamata anziché eseguire una ricerca nel Registro di sistema. È possibile eseguire una query per l'impostazione predefinita di un verbo canonico di associazione di file, protocollo o menu **Start.**
-   Avviare un'interfaccia utente per un'applicazione specifica in cui un utente può impostare i singoli valori predefiniti.
-   Rimuovere tutte le associazioni per utente.

**Programmi predefiniti** fornisce anche un'interfaccia utente che consente di registrare un'applicazione per fornire informazioni aggiuntive all'utente. Ad esempio, un'applicazione con firma digitale può includere un URL per il nome del home page.

L'uso del set di API associato consente a un'applicazione di funzionare correttamente con la funzionalità di controllo dell'account utente introdotta in Windows Vista. In Controllo dell'account utente un amministratore viene visualizzato nel sistema come utente standard, in modo che l'amministratore non possa in genere scrivere nel sottoalbero **HKEY \_ LOCAL \_ MACHINE.** Questa restrizione è una funzionalità di sicurezza che impedisce a un processo di agire come amministratore senza che l'amministratore ne sia a conoscenza.

L'installazione di un programma da parte di un utente viene in genere eseguita come processo con privilegi elevati. Tuttavia, i tentativi da parte di un'applicazione di modificare i comportamenti di associazione predefiniti a livello di computer dopo l'installazione avranno esito negativo. Le impostazioni predefinite devono invece essere registrate a livello di singolo utente, impedendo a più utenti di sovrascrivere le impostazioni predefinite.

La struttura gerarchica del Registro di sistema per le associazioni di file e protocolli ha la precedenza sulle impostazioni predefinite per utente rispetto alle impostazioni predefinite a livello di computer. Alcune applicazioni includono punti nel codice che elevano temporaneamente i propri diritti quando attestano i valori predefiniti registrati in **HKEY \_ LOCAL \_ MACHINE.** Queste applicazioni potrebbero verificarsi risultati imprevisti se un'altra applicazione è già registrata come impostazione predefinita per utente. **L'uso di programmi** predefiniti impedisce questa ambiguità e garantisce i risultati previsti a livello di singolo utente.

## <a name="registering-an-application-for-use-with-default-programs"></a>Registrazione di un'applicazione per l'utilizzo con programmi predefiniti

Questa sezione illustra le sottochiavi del Registro di sistema e i valori necessari per registrare un'applicazione con **Programmi predefiniti**. Include un esempio completo.

Questa sezione contiene i seguenti argomenti:

-   [Progid](#progids)
-   [Sottochiave di registrazione e descrizioni dei valori](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Esempio di registrazione completa](#full-registration-example)

**Programmi predefiniti richiede** a ogni applicazione di registrare in modo esplicito le associazioni di file, le associazioni MIME e i protocolli per i quali l'applicazione deve essere elencata come possibile impostazione predefinita. Per registrare le associazioni, usare gli elementi del Registro di sistema seguenti, illustrati in dettaglio più avanti in questo argomento in Descrizione dei valori e delle [sottochiavi di registrazione:](#registration-subkey-and-value-descriptions)

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

L'esempio seguente mostra le voci del Registro di sistema per un browser Fittizio Contoso denominato WebBrowser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a>Progid

Un'applicazione deve fornire un [ProgID specifico.](fa-progids.md) Assicurarsi di includere tutte le informazioni generalmente scritte nella sottochiave predefinita generica per l'estensione. Ad esempio, il lettore multimediale Litware fittizio fornisce la sottochiave **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Classes** \\ **LitwarePlayer11.AssocFile.MP3** specifica dell'applicazione. Tale sottochiave include tutte le informazioni nella sottochiave predefinita generica **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Classes.mp3più eventuali informazioni aggiuntive che si desidera registrare \\  \\  \\ **** l'applicazione. In questo modo, se l'utente ripristina l'associazione .mp3 al lettore Litware, le informazioni del lettore Litware sono intatte e non sono state sovrascritte da un'altra applicazione. La sovrascrittura può verificarsi se la sottochiave predefinita è l'unica origine di queste informazioni.

Quando si esegue il mapping di un ProgID a un'estensione di file o a un protocollo, un'applicazione può eseguire il mapping uno-a-uno o uno-a-molti. Nell'esempio Contoso ContosoHTML punta a un singolo ProgID che fornisce informazioni sull'esecuzione della shell per le estensioni .htm, .html, shtml, xht e xhtml. Poiché per ogni protocollo esiste un ProgID diverso, quando si usano protocolli si abilita ogni protocollo in modo che abbia una propria stringa di esecuzione.

Quando il tipo MIME può essere visualizzato inline in un browser, il ProgID per il tipo MIME deve contenere la sottochiave **CLSID** che usa l'identificatore di classe (CLSID) dell'applicazione corrispondente. Questo CLSID viene utilizzato in una ricerca in base al CLSID nel database MIME archiviato in **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Classes** \\ **MIME** \\ **Database** \\ **Content Type**. Se il tipo MIME non deve essere visualizzato inline in un browser, questo passaggio può essere omesso.

### <a name="registration-subkey-and-value-descriptions"></a>Sottochiave di registrazione e descrizioni dei valori

In questa sezione vengono descritte le singole sottochiavi del Registro di sistema e i valori utilizzati nella registrazione di un'applicazione con Programmi predefiniti **,** come illustrato in precedenza.

### <a name="capabilities"></a>Funzionalità

La **sottochiave Capabilities** contiene tutte le **informazioni sui programmi** predefiniti per un'applicazione specifica. Il segnaposto %ApplicationCapabilityPath% fa riferimento al percorso del Registro di sistema da **HKEY \_ CURRENT \_ USER** o **HKEY \_ LOCAL \_ MACHINE** alla sottochiave **Capabilities dell'applicazione.** Questa sottochiave contiene i valori significativi illustrati nella tabella seguente.



| Valore                  | Type                       | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ SZ o REG \_ EXPAND \_ SZ | **Obbligatorio**. Per consentire a un utente di effettuare una scelta di assegnazione predefinita informata, un'applicazione deve fornire una stringa che descrive le funzionalità dell'applicazione. Anche se l'esempio precedente di Contoso assegna la descrizione direttamente al valore ApplicationDescription, le applicazioni in genere forniscono la descrizione come risorsa incorporata in un file .dll per facilitare la localizzazione. Se ApplicationDescription non viene specificato, l'applicazione non viene visualizzata negli elenchi dell'interfaccia utente di potenziali programmi predefiniti.                                                            |
| ApplicationName        | REG \_ SZ o REG \_ EXPAND \_ SZ | **Facoltativo.** Nome con cui il programma viene visualizzato nell'interfaccia utente dei programmi predefiniti. Se questi dati non vengono forniti dall'applicazione, nell'interfaccia utente viene usato il nome del programma eseguibile associato al primo ProgID registrato per l'applicazione. ApplicationName deve sempre corrispondere al nome registrato in [RegisteredApplications.](#registeredapplications) È possibile usare ApplicationName se si vuole che tipi di applicazione diversi, ad esempio un browser e un client di posta elettronica, puntino allo stesso file eseguibile mentre vengono visualizzati come nomi diversi.<br/> |
| Nascosto                 | REG \_ DWORD                 | **Facoltativo.** Impostare questo valore su 1 per eliminare l'applicazione dall'elenco dei programmi nella **finestra di dialogo Imposta programmi** predefiniti. Se questo valore è 0 o non è presente, l'applicazione viene visualizzata normalmente nell'elenco.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>FileAssociations

La **sottochiave FileAssociations** contiene associazioni di file specifiche rivendicate dall'applicazione. Queste attestazioni vengono archiviate come valori, con un valore per ogni estensione. Le associazioni puntano a un ProgID specifico dell'applicazione anziché a un ProgID generico. Tuttavia, non è necessario che tutte le associazioni puntino allo stesso ProgID.

### <a name="mimeassociations"></a>MimeAssociations

La **sottochiave MIMEAssociations** contiene tipi MIME specifici che vengono rivendicati dall'applicazione. Queste attestazioni vengono archiviate come valori, con un valore per ogni tipo MIME. Il nome del valore per ogni tipo MIME deve corrispondere esattamente al nome MIME archiviato nel database MIME. Al valore deve essere assegnato anche un ProgID specifico dell'applicazione che contiene il CLSID corrispondente dell'applicazione.

### <a name="startmenu"></a>Startmenu

La **sottochiave Startmenu** è associata alle voci **internet** e **di posta** elettronica assegnabili dall'utente nel menu **Start.** Un'applicazione deve registrarsi separatamente come concorrente per tali voci. Per altre informazioni, vedere [Registrazione di programmi con tipi client](reg-middleware-apps.md).

> [!Note]  
> A partire Windows 7, non sono più  presenti voci **Internet** e Posta elettronica nel menu **Start.** I dati del  Registro di sistema associati alla voce di posta elettronica vengono ancora usati per il client MAPI predefinito, ma i dati del Registro di sistema associati alla voce **Internet** non vengono usati dal Windows.

 

Associando la registrazione del menu **Start** di un'applicazione alla registrazione dei programmi predefiniti, l'applicazione viene visualizzata come potenziale impostazione predefinita nell'interfaccia utente **Imposta associazioni.**  Se l'utente ha scelto l'applicazione come predefinita e quindi sceglie di ripristinare tutte le impostazioni predefinite dell'applicazione in un secondo momento, l'applicazione viene ripristinata nella posizione del menu **Start** per tale utente. Per altre informazioni e un'illustrazione, vedere la [sezione Default Programs UI](#default-programs-ui) più avanti in questo argomento.

La **sottochiave Startmenu** include due voci: StartMenuInternet e Mail, che corrispondono alle posizioni **canoniche di Internet** e **Posta** elettronica nel menu **Start.** Un'applicazione assegna a StartMenuInternet o Mail un valore uguale al nome della sottochiave registrata dell'applicazione in **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **StartMenuInternet** o **HKEY LOCAL \_ \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **Mail** (come [](reg-middleware-apps.md)descritto in Registrazione di programmi con tipi client).

Nel caso della posizione canonica **E-mail** nel menu **Start,** rappresenta il client MAPI predefinito e pertanto si presuppone che sia in grado di effettuare chiamate MAPI. In Windows 7, mentre non è più presente una posizione **canonica** di posta elettronica nel menu **Start,** questa sottochiave continua a essere usata per il client MAPI predefinito. Un'applicazione che attesta l'impostazione predefinita della posta elettronica deve registrarsi come gestore MAPI nella sottochiave seguente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Se un client di posta elettronica non può supportare MAPI ma vuole comunque sostenere la posizione **canonica** di posta elettronica del menu **Start,** può registrare una riga di comando nella sottochiave seguente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

Inoltre, in **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **Mail** \\ *CanonicalName* aggiungere un valore predefinito con il nome dell'applicazione.

Queste voci consentono l'avvio dell'applicazione **dalla** posizione di posta elettronica **del** menu Start. Si noti che le chiamate MAPI vengono ancora effettuate all'applicazione e passano al gestore MAPI precedente o hanno esito negativo se non è stato impostato alcun gestore MAPI. Per altre informazioni, vedere [Registrazione di programmi con tipi client](reg-middleware-apps.md).

### <a name="urlassociations"></a>UrlAssociations

La **sottochiave UrlAssociations** contiene i protocolli URL specifici rivendicati dall'applicazione. Queste attestazioni vengono archiviate come valori, con un valore per ogni protocollo. Ogni protocollo deve puntare a un ProgID specifico dell'applicazione anziché a un ProgID generico. Come accennato nell'esempio di Contoso, è possibile usare un ProgID diverso per ogni protocollo in modo che ognuno abbia una propria stringa di esecuzione.

### <a name="registeredapplications"></a>RegisteredApplications

La sottochiave completa per **RegisteredApplications** è:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **RegisteredApplications**

Questa sottochiave fornisce al sistema operativo il percorso del Registro di sistema delle **informazioni sui programmi** predefiniti per l'applicazione. Il percorso viene archiviato come valore il cui nome deve corrispondere al nome dell'applicazione.

### <a name="full-registration-example"></a>Esempio di registrazione completa

Questo esempio illustra le sottochiavi e i valori usati nella registrazione del lettore multimediale Litware fittizio. L'esempio include le voci ProgID per mostrare come si inserisce tutto insieme.

La sottochiave seguente mostra il ProgID specifico dell'applicazione per il .mp3 MIME:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

Successivamente è il ProgID specifico dell'applicazione che associa il programma Litware all'.mp3 di file.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

Le voci seguenti mostrano il ProgID combinato sia per il tipo MIME .mpeg l'estensione del nome file.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

Le voci seguenti registrano il programma Litware in **Programmi predefiniti** e usano i ProgID registrati in precedenza

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

Infine, in questo esempio viene registrato il percorso della registrazione di Litware **Default Programs.**

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Diventare il browser predefinito

La registrazione del browser deve seguire le procedure consigliate descritte in questo argomento. Quando il browser è installato, Windows presentare all'utente una notifica di sistema tramite la quale l'utente può selezionare il browser come predefinito del sistema. Questa notifica viene visualizzata quando vengono soddisfatte queste condizioni:

-   Il programma di installazione del browser chiama [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con il flag **SHCNE \_ ASSOCCHANGED** per indicare Windows che sono stati registrati nuovi gestori di protocollo.
-   Windows rileva che una o più nuove applicazioni sono state registrate per gestire i protocolli http:// e https:// e che l'utente non ha ancora avuto una notifica. In altre parole, all'utente non è stato mostrato nessuno dei seguenti elementi: una notifica di sistema che pubblicizza l'applicazione, un riquadro a comparsa OpenWith che contiene l'applicazione o la pagina Pannello di controllo Set User Defaults (SUD) per l'applicazione.

Nell'esempio seguente viene illustrato il codice di registrazione consigliato che deve essere eseguito dal programma di installazione del browser dopo la scrittura delle chiavi del Registro di sistema.

[**SHChangeNotify notifica**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) innanzitutto al sistema che sono disponibili nuove opzioni di associazione. La **chiamata SHChangeNotify** è necessaria per garantire il corretto funzionamento delle impostazioni predefinite del sistema.

[**Un'istruzione Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) consente quindi ai processi di sistema di gestire la notifica.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Se l'utente chiude o ignora la notifica o il riquadro a comparsa risultante senza effettuare una nuova selezione predefinita del browser, il browser predefinito rimane invariato. Si noti che l'utente può anche modificare il browser predefinito in qualsiasi momento tramite altri meccanismi, tra cui Impostare le impostazioni predefinite utente nel Pannello di controllo.

## <a name="default-programs-ui"></a>Interfaccia utente di Programmi predefiniti

Le illustrazioni in questa sezione mostrano l'interfaccia utente **per i programmi predefiniti,** come illustrato dall'utente.

La figura seguente mostra la finestra **principale Programmi** predefiniti in Pannello di controllo.

![Screenshot della pagina di immissione dei programmi predefiniti](images/defaultprogramsmain.png)

Quando un utente sceglie **l'opzione Imposta i programmi** predefiniti, viene visualizzata la finestra seguente. Gli utenti possono usare questa pagina per assegnare un programma predefinito per tutti i tipi di file e i protocolli per cui il programma è un'impostazione predefinita possibile. Come illustrato nella figura seguente, tutti i [programmi](#registering-an-application-for-use-with-default-programs) registrati e l'icona del programma vengono visualizzati nella **casella Programmi** a sinistra.

![Screenshot della pagina imposta i programmi predefiniti](images/setyourdefaultprograms.png)

Quando l'utente seleziona un programma dall'elenco, vengono visualizzati l'icona del programma e il provider. Se l'URL è incorporato nel certificato con firma digitale del programma, il programma può anche visualizzare un URL. I programmi non firmati digitalmente non possono visualizzare un URL.

Viene visualizzato anche il testo descrittivo fornito dal programma durante la registrazione. Questo testo è obbligatorio. Sotto la casella di descrizione è visualizzato un'indicazione del numero di impostazioni predefinite attualmente assegnate al programma in base al numero completo registrato per la gestione.

Per assegnare o ripristinare un programma come predefinito per tutti i file e i protocolli per cui è registrato, l'utente fa clic sull'opzione Imposta il programma **come** predefinito.

Per assegnare singoli tipi di file e protocolli  a un programma, l'utente  fa clic sull'opzione Scegli impostazioni predefinite per questo programma, che visualizza una finestra Imposta associazioni per un programma come quella riportata nella figura seguente.

> [!Note]  
> È consigliabile chiamare le associazioni **Set** per un programma usando [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).

 

![Screenshot dell'associazione impostata per una pagina del programma](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Procedure consigliate per l'uso di programmi predefiniti

In questa sezione vengono fornite linee guida sulle procedure consigliate per l'uso **dei programmi predefiniti** quando si registrano le applicazioni. Offre anche suggerimenti di progettazione per la creazione di un'applicazione che offre agli utenti funzionalità **ottimali dei programmi** predefiniti.

### <a name="during-installation"></a>Durante l'installazione

Oltre alle procedure di installazione normalmente praticate in Windows XP, un'applicazione basata su  Windows Vista o versione successiva deve registrarsi con la funzionalità Programmi predefiniti per sfruttarne le funzionalità.

Eseguire la sequenza di passaggi seguente durante l'installazione. I passaggi da 1 a 3 corrispondono ai passaggi usati in Windows XP; Il passaggio 4 era nuovo in Windows Vista.

1.  Installare i file binari necessari.
2.  Scrivere progID in HKEY \_ LOCAL \_ MACHINE. Si noti che le applicazioni devono creare progID specifici dell'applicazione per le relative associazioni.
3.  Registrare l'applicazione **con Programmi predefiniti come** illustrato in precedenza in Registrazione di un'applicazione per [l'uso con i programmi predefiniti](#registering-an-application-for-use-with-default-programs).

### <a name="after-installation"></a>Dopo l'installazione

Questa sezione illustra in che modo il prompt dell'applicazione deve prima presentare le opzioni predefinite a ogni utente. Viene inoltre illustrato in che modo un'applicazione può monitorare lo stato come predefinito per le associazioni e i protocolli possibili.

### <a name="first-run-experiences"></a>Esperienze di prima esecuzione

Quando l'applicazione viene eseguita da un utente per la prima volta, è consigliabile che l'applicazione visualizza l'interfaccia utente per l'utente che in genere include queste due opzioni:

-   Accettare le impostazioni predefinite dell'applicazione. Questa opzione è selezionata per impostazione predefinita.
-   Personalizzare le impostazioni predefinite dell'applicazione.

Prima di Windows 8, se l'utente accetta le impostazioni predefinite, l'applicazione chiama [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), che converte tutte le associazioni a livello di computer dichiarate durante l'installazione in impostazioni per utente per tale utente.

Se l'utente decide di personalizzare le impostazioni, l'applicazione chiama [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) per visualizzare l'interfaccia utente di associazione file. La figura seguente mostra questa finestra per il lettore multimediale Litware fittizio.

![Screenshot delle associazioni dei set per una pagina del programma per litware](images/setassociationsforaprogramforlitware.png)

La finestra di associazione file mostra le impostazioni predefinite registrate dall'applicazione e mostra anche l'impostazione predefinita corrente per altre estensioni e protocolli. Al termine della personalizzazione delle impostazioni predefinite, l'utente fa clic sul **pulsante Salva** per eseguire il commit delle modifiche. Se l'utente fa clic **su Annulla**, la finestra viene chiusa senza salvare le modifiche.

È consigliabile usare questa interfaccia utente per le applicazioni anziché crearne di personalizzate. In questo modo, si salvano le risorse precedentemente necessarie per sviluppare l'interfaccia utente di associazione file. Si garantisce anche che le associazioni vengano salvate correttamente.

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>Impostare un'applicazione per verificare se è l'impostazione predefinita

> [!Note]  
> Questo non è più supportato a Windows 8.

 

Le applicazioni controllano in genere se sono impostate come predefinite quando vengono eseguite. Impostare le applicazioni per eseguire questo controllo chiamando [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) o [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).

Se l'applicazione determina che non è l'impostazione predefinita, può presentare l'interfaccia utente che chiede all'utente se accettare la situazione corrente o impostare l'applicazione come predefinita. Includere sempre una casella di controllo nell'interfaccia utente selezionata per impostazione predefinita e che presenti l'opzione per non chiedere di nuovo.

> [!Note]  
> La scelta dell'impostazione predefinita deve essere basata sull'utente. Un'applicazione non deve mai recuperare un valore predefinito senza chiedere all'utente.

 

La figura seguente mostra una finestra di dialogo di esempio.

![Screenshot di una finestra di dialogo di esempio](images/notthedefaultui.png)

## <a name="additional-resources"></a>Risorse aggiuntive

-   [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per le associazioni di file](fa-best-practices.md)
</dt> <dt>

[Scenario di esempio di associazione file](fa-sample-scenarios.md)
</dt> <dt>

[Linee guida per la gestione delle applicazioni predefinite in Windows Vista e versioni successive](vista-managing-defaults.md)
</dt> <dt>

[Impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
