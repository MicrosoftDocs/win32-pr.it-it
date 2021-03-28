---
description: Utilizzare i programmi predefiniti per impostare l'esperienza utente predefinita.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programmi predefiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2021
ms.locfileid: "103885874"
---
# <a name="default-programs"></a>Programmi predefiniti

Utilizzare i **programmi predefiniti** per impostare l'esperienza utente predefinita. Gli utenti possono accedere ai **programmi predefiniti** dal pannello di controllo o direttamente dal menu **Start** . [Impostare l'accesso al programma e lo strumento SPAD (computer defaults)](cpl-setprogramaccess.md) , l'esperienza dei valori predefiniti primari per gli utenti di Windows XP, è ora una parte dei **programmi predefiniti**.

> [!IMPORTANT]
> Questo argomento non è applicabile a Windows 10. Il modo in cui le associazioni di file predefinite cambiano in Windows 10. Per ulteriori informazioni, vedere la sezione relativa alle **modifiche apportate al modo in cui Windows 10 gestisce le app predefinite** in [questo post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Quando un utente imposta le impostazioni predefinite del programma utilizzando **programmi predefiniti**, l'impostazione predefinita si applica solo a tale utente e non ad altri utenti che potrebbero utilizzare lo stesso computer. **Programmi predefiniti** fornisce un set di API (deprecate in Windows 8) che consentono ai fornitori di software indipendenti (ISV) di includere i programmi o le applicazioni nel sistema predefinito. Il set di API consente inoltre agli ISV di gestire meglio il proprio stato come impostazioni predefinite.

Questo argomento è organizzato nel modo seguente:

-   [Introduzione ai programmi predefiniti e al set di API correlati](#introduction-to-default-programs-and-its-related-api-set)
-   [Registrazione di un'applicazione per l'utilizzo con i programmi predefiniti](#registering-an-application-for-use-with-default-programs)
    -   [ProgID](#progids)
    -   [Sottochiave di registrazione e descrizioni dei valori](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Esempio di registrazione completa](#full-registration-example)
-   [Diventare il browser predefinito](#becoming-the-default-browser)
-   [Interfaccia utente programmi predefiniti](#default-programs-ui)
-   [Procedure consigliate per l'utilizzo di programmi predefiniti](#best-practices-for-using-default-programs)
    -   [Durante l'installazione](#during-installation)
    -   [Dopo l'installazione](#after-installation)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Introduzione ai programmi predefiniti e al set di API correlati

I **programmi predefiniti** sono progettati principalmente per le applicazioni che usano tipi di file standard, ad esempio file con estensione MP3 o jpg o protocolli standard, ad esempio http o mailto. Le applicazioni che usano i propri protocolli proprietari e associazioni di file in genere non usano la funzionalità **programmi predefiniti** .

Dopo aver registrato un'applicazione per la funzionalità **programmi predefiniti** , le opzioni e le funzionalità seguenti sono disponibili tramite il set di API:

-   Ripristinare tutte le impostazioni predefinite registrate per un'applicazione. Deprecato per Windows 8.
-   Ripristinare un singolo valore predefinito registrato per un'applicazione. Deprecato per Windows 8.
-   Eseguire una query per il proprietario di un valore predefinito specifico in una singola chiamata anziché eseguire una ricerca nel registro di sistema. È possibile eseguire una query per il valore predefinito di un'associazione di file, un protocollo o un verbo canonico del menu **Start** .
-   Avvia un'interfaccia utente per un'applicazione specifica in cui un utente può impostare impostazioni predefinite singole.
-   Rimuovere tutte le associazioni per ogni utente.

**Programmi predefiniti** fornisce anche un'interfaccia utente che consente di registrare un'applicazione per fornire informazioni aggiuntive all'utente. Ad esempio, un'applicazione con firma digitale può includere un URL per il home page del produttore.

L'utilizzo del set di API associato può consentire una corretta funzione dell'applicazione con la funzionalità controllo dell'account utente introdotta in Windows Vista. In controllo dell'account utente, un amministratore appare al sistema come utente standard, in modo che l'amministratore non possa in genere scrivere nel sottoalbero del **\_ \_ computer locale HKEY** . Questa restrizione è una funzionalità di sicurezza che impedisce a un processo di fungere da amministratore senza la conoscenza dell'amministratore.

L'installazione di un programma da un utente viene in genere eseguita come processo con privilegi elevati. Tuttavia, i tentativi eseguiti da un'applicazione per modificare i comportamenti di associazione predefiniti a livello di computer dopo l'installazione non saranno riusciti. Al contrario, i valori predefiniti devono essere registrati a livello di utente, impedendo a più utenti di sovrascrivere le impostazioni predefinite.

La struttura del registro di sistema gerarchica per le associazioni di file e protocolli offre la precedenza ai valori predefiniti per utente rispetto ai valori predefiniti a livello di computer. Alcune applicazioni includono punti nel codice che elevano temporaneamente i propri diritti quando attestano le impostazioni predefinite registrate **nel \_ \_ computer locale HKEY**. Queste applicazioni possono generare risultati imprevisti se un'altra applicazione è già registrata come impostazione predefinita per singolo utente. L'utilizzo di **programmi predefiniti** impedisce questa ambiguità e garantisce risultati previsti a livello di utente.

## <a name="registering-an-application-for-use-with-default-programs"></a>Registrazione di un'applicazione per l'utilizzo con i programmi predefiniti

Questa sezione illustra le sottochiavi del registro di sistema e i valori necessari per registrare un'applicazione con i **programmi predefiniti**. Include un esempio completo.

Questa sezione contiene i seguenti argomenti:

-   [ProgID](#progids)
-   [Sottochiave di registrazione e descrizioni dei valori](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Esempio di registrazione completa](#full-registration-example)

Per i **programmi predefiniti** è necessario che ogni applicazione registri in modo esplicito le associazioni di file, le associazioni MIME e i protocolli per i quali l'applicazione deve essere elencata come un possibile valore predefinito. È possibile registrare le associazioni usando gli elementi del registro di sistema seguenti, descritti in dettaglio più avanti in questo argomento nella [sottochiave di registrazione e descrizioni dei valori](#registration-subkey-and-value-descriptions):

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

Nell'esempio seguente vengono illustrate le voci del registro di sistema per un browser contoso fittizio denominato WebBrowser:

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

### <a name="progids"></a>ProgID

Un'applicazione deve fornire un [ProgID](fa-progids.md)specifico. Assicurarsi di includere tutte le informazioni scritte in genere nella sottochiave predefinita generica per l'estensione. Ad esempio, fictional Litware Media Player fornisce le classi software del **\_ \_ computer locale HKEY** specifiche dell'applicazione \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** sottochiave. Questa sottochiave include tutte le informazioni contenute nella sottochiave predefinita generica **HKEY \_ Local \_ Machine** \\ **software** \\ **Classis** \\ **. mp3** più eventuali informazioni aggiuntive che si desidera registrare nell'applicazione. In questo modo si garantisce che se l'utente ripristina l'associazione. mp3 al lettore Litware, le informazioni del lettore Litware sono intatte e non sono state sovrascritte da un'altra applicazione. La sovrascrittura potrebbe verificarsi se la sottochiave predefinita è l'unica fonte di tali informazioni.

Quando si esegue il mapping di un ProgID a un'estensione o a un protocollo di un nome di file, un'applicazione può eseguire il mapping uno-a-uno o uno-a-molti. Nell'esempio di Contoso ContosoHTML punta a un singolo ProgID che fornisce informazioni ShellExecute per le estensioni. htm,. html,. shtml,. XHT e. XHTML. Poiché esiste un ProgID diverso per ogni protocollo, quando si usano i protocolli si abilita ogni protocollo per avere una propria stringa di esecuzione.

Quando il tipo MIME può essere visualizzato inline in un browser, il ProgID per il tipo MIME deve contenere la sottochiave **CLSID** che usa l'identificatore di classe (CLSID) dell'applicazione corrispondente. Questo CLSID viene utilizzato in una ricerca rispetto al CLSID nel database MIME archiviato nel tipo di contenuto del database MIME delle classi software **\_ del \_ computer locale HKEY** \\  \\  \\  \\  \\ . Se il tipo MIME non è destinato a essere visualizzato inline in un browser, questo passaggio può essere omesso.

### <a name="registration-subkey-and-value-descriptions"></a>Sottochiave di registrazione e descrizioni dei valori

Questa sezione descrive le singole sottochiavi del registro di sistema e i valori usati per la registrazione di un'applicazione con i **programmi predefiniti**, come illustrato in precedenza.

### <a name="capabilities"></a>Funzionalità

La sottochiave **capabilities** contiene tutte le informazioni sui **programmi predefiniti** per un'applicazione specifica. Il segnaposto% ApplicationCapabilityPath% si riferisce al percorso del registro di sistema dall' **\_ \_ utente corrente di HKEY** o dal **\_ \_ computer locale HKEY** alla sottochiave delle **funzionalità** dell'applicazione. Questa sottochiave contiene i valori significativi indicati nella tabella seguente.



| Valore                  | Type                       | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ sz o reg \_ expand \_ SZ | **Obbligatorio**. Per consentire a un utente di effettuare una scelta di assegnazione predefinita informata, un'applicazione deve fornire una stringa che descrive le funzionalità dell'applicazione. Sebbene l'esempio precedente di Contoso assegni la descrizione direttamente al valore ApplicationDescription, le applicazioni in genere forniscono la descrizione come risorsa incorporata in un file con estensione dll per facilitare la localizzazione. Se ApplicationDescription non viene specificato, l'applicazione non viene visualizzata negli elenchi dell'interfaccia utente dei potenziali programmi predefiniti.                                                            |
| ApplicationName        | REG \_ sz o reg \_ expand \_ SZ | **Facoltativo.** Nome con cui il programma viene visualizzato nell'interfaccia utente dei programmi predefiniti. Se questi dati non vengono forniti dall'applicazione, il nome del programma eseguibile associato al primo ProgID registrato per l'applicazione viene utilizzato nell'interfaccia utente. ApplicationName deve sempre corrispondere al nome registrato in [RegisteredApplications](#registeredapplications). È possibile utilizzare ApplicationName se si desidera che tipi di applicazione diversi, ad esempio un browser e un client di posta elettronica, facciano riferimento allo stesso file eseguibile quando vengono visualizzati come nomi diversi.<br/> |
| Nascosto                 | REG \_ DWORD                 | **Facoltativo.** Impostare questo valore su 1 per non visualizzare l'applicazione dall'elenco dei programmi nella finestra di dialogo **Imposta programmi predefiniti** . Se questo valore è 0 o non è presente, l'applicazione viene visualizzata normalmente nell'elenco.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>FileAssociations

La sottochiave **FileAssociations** contiene associazioni di file specifiche richieste dall'applicazione. Queste attestazioni vengono archiviate come valori, con un valore per ogni estensione. Le associazioni fanno riferimento a un ProgID specifico dell'applicazione anziché a un ProgID generico. Tuttavia, non è necessario che tutte le associazioni puntino allo stesso ProgID.

### <a name="mimeassociations"></a>MIMEAssociations

La sottochiave **MIMEAssociations** contiene tipi MIME specifici richiesti dall'applicazione. Queste attestazioni vengono archiviate come valori, con un valore per ogni tipo MIME. Il nome del valore per ogni tipo MIME deve corrispondere esattamente al nome MIME archiviato nel database MIME. Al valore deve essere assegnato anche un ProgID specifico dell'applicazione che contiene il CLSID corrispondente dell'applicazione.

### <a name="startmenu"></a>StartMenu

La sottochiave **StartMenu** è associata alle voci di **posta elettronica** e **Internet** assegnabili dall'utente nel menu **Start** . Un'applicazione deve essere registrata separatamente come un contendente per tali voci. Per ulteriori informazioni, vedere [la pagina relativa alla registrazione di programmi con i tipi di client](reg-middleware-apps.md).

> [!Note]  
> A partire da Windows 7, nel menu **Start** non sono più presenti **Internet** e voci di **posta elettronica** . I dati del registro di sistema associati alla voce di **posta elettronica** vengono comunque utilizzati per il client MAPI predefinito, ma i dati del registro di sistema associati alla voce **Internet** non vengono utilizzati da Windows.

 

Associando la registrazione del menu **Start** di un'applicazione alla registrazione dei **Programmi predefinita** , l'applicazione viene visualizzata come un potenziale valore predefinito nell'interfaccia utente di **set Associations** . Se l'utente ha scelto l'applicazione come predefinita e quindi sceglie di ripristinare tutte le impostazioni predefinite dell'applicazione in un secondo momento, l'applicazione viene ripristinata nella posizione del menu **Start** per tale utente. Per ulteriori informazioni e per un'illustrazione, vedere la sezione relativa all' [interfaccia utente dei programmi predefiniti](#default-programs-ui) più avanti in questo argomento.

La sottochiave **StartMenu** include due voci: StartMenuInternet e mail, che corrispondono alle posizioni canoniche **Internet** e di **posta elettronica** nel menu **Start** . Un'applicazione assegna a StartMenuInternet o mail un valore uguale al nome della sottochiave registrata dell'applicazione in **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** o **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **mail** (come descritto in [registrazione di programmi con tipi di client](reg-middleware-apps.md)).

Nel caso della posizione canonica del **messaggio di posta elettronica** nel menu **Start** , rappresenta il client MAPI predefinito e pertanto si presuppone che sia in grado di passare le chiamate MAPI. In Windows 7, anche se non è più disponibile una posizione canonica di **posta elettronica** nel menu **Start** , questa sottochiave continua a essere utilizzata per il client MAPI predefinito. Un'applicazione che rivendica l'impostazione predefinita della posta dovrebbe registrarsi come gestore MAPI nella sottochiave seguente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Se un client di posta elettronica non è in grado di supportare MAPI ma vuole comunque contendersi la **posizione canonica** del menu **Start** , può registrare una riga di comando nella sottochiave seguente:

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

Inoltre, in **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **mail** \\ *CanonicalName* aggiungere un valore predefinito con il nome dell'applicazione.

Queste voci consentono l'avvio dell'applicazione dalla posizione di **posta elettronica** del menu **Start** . Si noti che le chiamate MAPI vengono ancora apportate all'applicazione e che passano al gestore MAPI precedente oppure hanno esito negativo se non è stato impostato alcun gestore MAPI. Per ulteriori informazioni, vedere [la pagina relativa alla registrazione di programmi con i tipi di client](reg-middleware-apps.md).

### <a name="urlassociations"></a>UrlAssociations

La sottochiave **UrlAssociations** contiene i protocolli URL specifici richiesti dall'applicazione. Queste attestazioni vengono archiviate come valori, con un valore per ogni protocollo. Ogni protocollo deve puntare a un ProgID specifico dell'applicazione anziché a un ProgID generico. Come indicato nell'esempio di Contoso, è possibile usare un ProgID diverso per ogni protocollo affinché ognuno disponga di una propria stringa di esecuzione.

### <a name="registeredapplications"></a>RegisteredApplications

La sottochiave completa per **RegisteredApplications** è la seguente:

**HKEY \_ RegisteredApplications software del \_ computer locale** \\  \\ 

Questa sottochiave fornisce al sistema operativo il percorso del registro di sistema delle informazioni sui **programmi predefiniti** per l'applicazione. Il percorso viene archiviato come valore il cui nome deve corrispondere al nome dell'applicazione.

### <a name="full-registration-example"></a>Esempio di registrazione completa

Questo esempio mostra le sottochiavi e i valori usati per la registrazione del lettore multimediale Litware fittizio. Nell'esempio sono incluse le voci ProgID per illustrare il modo in cui si integra.

La sottochiave seguente mostra il ProgID specifico dell'applicazione per il tipo MIME. mp3:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

Di seguito è presente il ProgID specifico dell'applicazione che associa il programma Litware all'estensione di file. mp3.

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

Nelle voci successive viene mostrato il ProgID combinato sia per il tipo MIME. MPEG che per l'estensione del nome di file.

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

Le voci successive registrano il programma Litware nei **programmi predefiniti** e usano i ProgID precedentemente registrati

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

Infine, in questo esempio viene registrato il percorso della registrazione dei **programmi predefiniti** di Litware.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Diventare il browser predefinito

La registrazione del browser deve seguire le procedure consigliate descritte in questo argomento. Quando il browser è installato, Windows può presentare all'utente una notifica di sistema tramite la quale l'utente può selezionare il browser come impostazione predefinita del sistema. Questa notifica viene visualizzata quando vengono soddisfatte le condizioni seguenti:

-   Il programma di installazione del browser chiama [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con il flag **SHCNE \_ ASSOCCHANGED** per indicare a Windows che sono stati registrati nuovi gestori del protocollo.
-   Windows rileva che una o più nuove applicazioni sono state registrate per gestire i protocolli http://e https://e che l'utente non ha ancora ricevuto una notifica. In altre parole, nessuno dei seguenti elementi è stato visualizzato all'utente: una notifica di sistema che annuncia l'applicazione, un riquadro a comparsa OpenWith che contiene l'applicazione o la pagina del pannello di controllo imposta impostazioni predefinite utente (SUD) per l'applicazione.

Nell'esempio seguente viene illustrato il codice di registrazione consigliato che deve essere eseguito dal programma di installazione del browser dopo la scrittura delle chiavi del registro di sistema.

[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) notifica innanzitutto al sistema che sono disponibili nuove opzioni di associazione. La chiamata **SHChangeNotify** è necessaria per garantire il corretto funzionamento delle impostazioni predefinite del sistema.

Un'istruzione [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) consente quindi al tempo necessario ai processi di sistema di gestire la notifica.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Se l'utente ignora o ignora la notifica risultante o il riquadro a comparsa senza effettuare una nuova selezione predefinita del browser, il browser predefinito rimane invariato. Si noti che l'utente può anche modificare il browser predefinito in qualsiasi momento tramite altri meccanismi, inclusa l'impostazione delle impostazioni predefinite dell'utente nel pannello di controllo.

## <a name="default-programs-ui"></a>Interfaccia utente programmi predefiniti

Nelle illustrazioni di questa sezione viene illustrata l'interfaccia utente per i **programmi predefiniti** come visualizzato dall'utente.

La figura seguente mostra la finestra principali **programmi predefiniti** nel pannello di controllo.

![screenshot della pagina di immissione dei programmi predefinita](images/defaultprogramsmain.png)

Quando un utente sceglie l'opzione **Imposta programmi predefiniti** , viene visualizzata la finestra seguente. Gli utenti possono utilizzare questa pagina per assegnare un programma predefinito per tutti i tipi di file e protocolli per i quali il programma è un possibile valore predefinito. Come illustrato nella figura seguente, tutti i programmi [registrati](#registering-an-application-for-use-with-default-programs) e l'icona del programma vengono visualizzati nella casella **programmi** a sinistra.

![screenshot della pagina impostare i programmi predefiniti](images/setyourdefaultprograms.png)

Quando l'utente seleziona un programma dall'elenco, vengono visualizzati l'icona e il provider del programma. Se l'URL è incorporato nel certificato con firma digitale del programma, il programma può anche visualizzare un URL. I programmi senza firma digitale non possono visualizzare un URL.

Viene visualizzato anche un testo descrittivo, fornito dal programma durante la registrazione. Questo testo è obbligatorio. Sotto la casella Descrizione è indicato il numero di valori predefiniti attualmente assegnati al programma dal numero intero che è stato registrato per la gestione.

Per assegnare o ripristinare un programma come valore predefinito per tutti i file e i protocolli per i quali è stato registrato, l'utente fa clic sull'opzione **imposta questo programma come predefinito** .

Per assegnare singoli tipi di file e protocolli a un programma, l'utente fa clic sull'opzione **scegliere le impostazioni predefinite per il programma** , che consente di visualizzare le **associazioni set per una** finestra del programma come quella illustrata nella figura seguente.

> [!Note]  
> Si consiglia di chiamare le **associazioni set per un programma** usando [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).

 

![screenshot della pagina set associazioni per un programma](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Procedure consigliate per l'utilizzo di programmi predefiniti

In questa sezione vengono fornite indicazioni sulle procedure consigliate per l'utilizzo di **programmi predefiniti** quando si registrano le applicazioni. Offre anche suggerimenti di progettazione per la creazione di un'applicazione che fornisce agli utenti funzionalità di **programmi predefiniti** ottimali.

### <a name="during-installation"></a>Durante l'installazione

Oltre alle procedure di installazione normalmente in Windows XP, un'applicazione basata su Windows Vista o versioni successive deve eseguire la registrazione con la funzionalità **programmi predefiniti** per sfruttare i vantaggi della funzionalità.

Eseguire la sequenza di passaggi seguente durante l'installazione. I passaggi 1-3 corrispondono ai passaggi utilizzati in Windows XP. il passaggio 4 era una novità di Windows Vista.

1.  Installare i file binari necessari.
2.  Scrivere i ProgID nel \_ computer locale HKEY \_ . Si noti che le applicazioni devono creare ProgID specifici dell'applicazione per le rispettive associazioni.
3.  Registrare l'applicazione con i **programmi predefiniti** come descritto in precedenza in [registrazione di un'applicazione per l'uso con i programmi predefiniti](#registering-an-application-for-use-with-default-programs).

### <a name="after-installation"></a>Dopo l'installazione

In questa sezione viene illustrato il modo in cui il prompt dell'applicazione deve presentare le opzioni predefinite a ogni utente. Viene inoltre illustrato il modo in cui un'applicazione può monitorarne lo stato come predefinito per le associazioni e i protocolli possibili.

### <a name="first-run-experiences"></a>Esperienze di prima esecuzione

Quando l'applicazione viene eseguita da un utente per la prima volta, è consigliabile che l'applicazione visualizzi l'interfaccia utente che in genere include le due opzioni seguenti:

-   Accettare le impostazioni predefinite dell'applicazione. Questa opzione è selezionata per impostazione predefinita.
-   Personalizzare le impostazioni predefinite dell'applicazione.

Prima di Windows 8, se l'utente accetta le impostazioni predefinite, l'applicazione chiama [**IApplicationAssociationRegistration:: SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), che converte tutte le associazioni a livello di computer dichiarate durante l'installazione in impostazioni per utente per tale utente.

Se l'utente decide di personalizzare le impostazioni, l'applicazione chiama [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) per visualizzare l'interfaccia utente dell'associazione di file. Nella figura seguente è illustrata questa finestra per il Media Player di Litware fittizio.

![screenshot della pagina delle associazioni set per un programma per Litware](images/setassociationsforaprogramforlitware.png)

La finestra Associazione file Mostra le impostazioni predefinite registrate dall'applicazione e Mostra anche l'impostazione predefinita corrente per altre estensioni e protocolli. Al termine della personalizzazione dei valori predefiniti, l'utente fa clic sul pulsante **Salva** per eseguire il commit delle modifiche. Se l'utente fa clic su **Annulla**, la finestra viene chiusa senza salvare le modifiche.

È consigliabile usare questa interfaccia utente per le applicazioni anziché per crearne una personalizzata. In questo modo, si salvano le risorse necessarie in precedenza per sviluppare l'interfaccia utente di associazione file. Si garantisce inoltre che le associazioni vengano salvate correttamente.

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>Impostare un'applicazione per verificare se è l'impostazione predefinita

> [!Note]  
> Questa operazione non è più supportata a partire da Windows 8.

 

Le applicazioni in genere controllano se sono impostate come predefinite quando vengono eseguite. Per eseguire questa verifica, impostare le applicazioni chiamando [**IApplicationAssociationRegistration:: QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) o [**IApplicationAssociationRegistration:: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).

Se l'applicazione determina che non è l'impostazione predefinita, può presentare un'interfaccia utente che chiede all'utente se accettare la situazione corrente o se impostarla come predefinita. Includere sempre una casella di controllo in questa interfaccia utente selezionata per impostazione predefinita e che presenta l'opzione che non viene più richiesta.

> [!Note]  
> La scelta del valore predefinito deve essere basata sull'utente. Un'applicazione non deve mai recuperare un valore predefinito senza richiedere l'intervento dell'utente.

 

Nella figura seguente è illustrata una finestra di dialogo di esempio.

![Screenshot di una finestra di dialogo di esempio](images/notthedefaultui.png)

## <a name="additional-resources"></a>Risorse aggiuntive

-   [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per le associazioni di file](fa-best-practices.md)
</dt> <dt>

[Scenario di esempio di associazione di file](fa-sample-scenarios.md)
</dt> <dt>

[Linee guida per la gestione di applicazioni predefinite in Windows Vista e versioni successive](vista-managing-defaults.md)
</dt> <dt>

[Impostazione dell'accesso al programma e delle impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
