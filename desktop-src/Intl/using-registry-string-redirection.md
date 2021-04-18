---
description: L'archiviazione di stringhe hardcoded nel registro di sistema fa parte di un modello di localizzazione precedente a Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Uso del reindirizzamento delle stringhe del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319472"
---
# <a name="using-registry-string-redirection"></a>Uso del reindirizzamento delle stringhe del registro di sistema

L'archiviazione di stringhe hardcoded nel registro di sistema fa parte di un modello di localizzazione precedente a Windows Vista. Non è supportato da MUI. Nel modello corrente, l'interfaccia utente per il sistema operativo viene eseguita in file di risorse specifici della lingua in base a una base indipendente dalla lingua. I componenti del sistema operativo utilizzano il registro di sistema in modo indipendente dalla lingua.

MUI usa solo le stringhe del registro di sistema reindirizzate definite dalle risorse PE Win32 nel file di risorse della lingua di base. Il reindirizzamento viene definito separatamente, ad esempio, in un file con estensione inf. Questo tipo di archiviazione consente al caricatore di risorse di selezionare automaticamente le risorse di lingua corrette durante il caricamento del modulo delle risorse.

> [!Note]  
> Questo argomento riguarda solo le risorse PE di Win32. Se si usano risorse PE non Win32, è necessario fornire il reindirizzamento personalizzato della stringa del registro di sistema, se necessario.

 

## <a name="create-a-language-neutral-resource"></a>Creare una risorsa Language-Neutral

Un'applicazione MUI eseguita in Windows Vista e versioni successive utilizza una risorsa di stringa indipendente dal linguaggio per consentire l'accesso alle stringhe specifiche della lingua archiviate in una tabella delle risorse di stringa. Il codice dell'applicazione che legge questi valori dal registro di sistema è descritto nella sezione caricare una Language-Neutral valore del registro di sistema di [individuazione delle stringhe reindirizzate](locating-redirected-strings.md).

Il formato dei dati per un valore del registro di sistema indipendente dalla lingua è " `@<PE-path>,-<stringID>[;<comment>]` ", dove:

-   *PE-Path* specifica il percorso del file eseguibile. Per supportare la distribuzione, è possibile specificare il percorso usando una variabile di ambiente, ad esempio% ProgramFiles%. Un'alternativa alla creazione di un riferimento di stringa consiste nel lasciare le informazioni sul percorso del file. In questo caso, l'applicazione deve avere un mezzo, ad esempio un altro valore del registro di sistema, per comunicare la propria directory di installazione.
-   *stringID* specifica l'identificatore numerico della risorsa stringa pertinente, che viene implementato esattamente come qualsiasi altra risorsa di tipo stringa localizzabile.
-   il *Commento* specifica informazioni facoltative per il debug o la leggibilità del valore del registro di sistema. Le funzioni API del registro di sistema ignorano il commento durante il caricamento della stringa.

> [!Note]  
> I dati per il valore del registro di sistema non fanno riferimento esplicito al file di risorse specifico del linguaggio. Il file corretto viene determinato in fase di esecuzione, in base alle preferenze correnti della lingua dell'interfaccia utente.

 

Viene immesso un valore del registro di sistema senza uno spazio tra "," e "-". Un valore del registro di sistema corretto è:

`shell32.dll,-22912`

Il valore del registro di sistema non è corretto:

`shell32.dll, -22912`

Un esempio di Windows Vista è il valore del registro di sistema con i dati seguenti:

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Creare risorse per le stringhe di collegamento

Quando l'applicazione MUI Visualizza il nome nell'interfaccia utente della shell, viene visualizzata una stringa InfoTip per l'icona dell'applicazione. È necessario creare le risorse di stringa per il nome visualizzato dell'applicazione e la stringa InfoTip associata per ogni lingua supportata. Quando le risorse sono pronte, l'applicazione può usare le stringhe come descritto in usare l'API shell per caricare le stringhe di collegamento dalla sezione del registro di sistema di [individuazione delle stringhe reindirizzate](locating-redirected-strings.md).

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>Preparare le risorse per un collegamento creato con Windows Installer

Se si usa Windows Installer (MSI) per creare un collegamento, le risorse di stringa includono il nome visualizzato e la descrizione del collegamento. Nella [tabella dei collegamenti MSI](../msi/shortcut-table.md)viene fatto riferimento alla DLL delle risorse nelle colonne appropriate e gli identificatori di risorsa per il nome visualizzato e la descrizione del collegamento vengono usati nelle colonne dell'identificatore di risorsa corrispondenti.

Affinché il collegamento dell'applicazione funzioni correttamente con la tecnologia delle risorse MUI, tenere presenti i seguenti punti quando si preparano le stringhe di collegamento:

-   Usare le variabili di ambiente o un percorso relativo per registrare la DLL. È possibile specificare @% systemroot% \\ system32 \\shell32.dll purché il tipo di stringa del registro di sistema sia reg \_ expand \_ SZ. L'identificatore di risorsa di stringa per "documento di testo" nel Shell32.dll è 12345.
-   Non usare spazi attorno ai simboli "," e "-". Un esempio corretto è "shell32.dll,-22912".
-   Non usare un nome di file breve. Questo tipo di nome non funziona con il caricatore di risorse.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Preparare le risorse per un collegamento usando il formato INF

Se si usa il formato di file INF per creare stringhe di collegamento, il file di risorse deve apportare le impostazioni del registro di sistema seguenti. Queste istruzioni presuppongono l'uso della sintassi ProfileItems dell'API di installazione.

1.  Modificare il valore InfoTip in modo che punti al riferimento di reindirizzamento di stringa, usando il percorso e l'identificatore di risorsa.
2.  Aggiungere il nuovo valore DisplayResource nelle sezioni di installazione di ProfileItems.

Di seguito è riportato un esempio che illustra l'aggiunta dell'applicazione Calculator al menu **Start** :


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Usare la sintassi illustrata di seguito quando si usa INF per aggiungere elementi, ad esempio una cartella del gruppo di accesso, al menu **Start** . Questa sintassi presuppone l'uso del \[ \] supporto StartMenuItems dal programma di installazione, simile alla sintassi utilizzata in Syssetup. inf.


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



Impostare il valore *infotip* sul riferimento di stringa " `@<path>,-resID` ".

Il nome visualizzato è determinato dai valori *resDLL* e *da un Resid* . Il valore *da un Resid* specifica l'identificatore di risorsa per una risorsa di stringa associata al file indipendente dalla lingua. Il valore *resDLL* specifica il percorso del file indipendente dalla lingua.

## <a name="create-resources-for-friendly-document-type-names"></a>Creare risorse per i nomi descrittivi dei tipi di documento

È necessario implementare le stringhe nome descrittivo e InfoTip per l'applicazione come risorse di stringa. Per consentire i nomi dei tipi di documenti descrittivi per rispondere alla lingua dell'interfaccia utente, l'applicazione deve registrare i nomi usando il valore FriendlyTypeName sotto la chiave identificatore del programma per il tipo di file. Per mantenere la compatibilità con le versioni precedenti, è necessario conservare il valore predefinito per la chiave dell'identificatore del programma. Per informazioni sull'accesso ai nomi dall'applicazione, vedere i nomi dei tipi di documento descrittivo per la query nella sezione del registro di sistema per [individuare le stringhe reindirizzate](locating-redirected-strings.md).

Il lavoro specifico prevede i passaggi seguenti:

1.  Implementare il nome descrittivo e le stringhe InfoTip come risorse di stringa specifiche della lingua.
2.  Aggiungere il valore FriendlyTypeName sotto la chiave del registro di sistema del tipo di documento. I dati per il valore seguono il modello " `@<path>,-<resID>` ", dove *path* indica il file eseguibile e *da un Resid* è l'identificatore di risorsa di una risorsa di tipo stringa localizzabile associata a tale eseguibile.
3.  Specificare il valore del registro di sistema InfoTip in base al formato " `@<path>,-<resID>` ".

Nell'esempio seguente vengono illustrate le impostazioni del registro di sistema per un file con estensione txt:


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>Fornire risorse per le stringhe di azione dei verbi della shell

Le stringhe di azione per determinati verbi, ad esempio "Open" e "Edit", vengono visualizzate nel menu a comparsa visualizzato quando l'utente fa clic con il pulsante destro del mouse su un file in Esplora risorse. Non è necessario che l'applicazione specifichi stringhe per i verbi comuni della shell, perché per questi verbi la shell ha le proprie impostazioni predefinite abilitate per MUI. Tuttavia, è necessario fornire risorse di stringa localizzabili per le stringhe che rappresentano i verbi non comuni.

Nei sistemi operativi precedenti a Windows XP, viene eseguito il rendering delle stringhe per i verbi della shell nel registro di sistema utilizzando la sintassi seguente, dove *verbo* specifica il nome effettivo del verbo:


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Ecco un esempio:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



In Windows XP e versioni successive, è possibile utilizzare un livello di riferimento indiretto per fare in modo che una stringa di azione dipenda dalla lingua dell'interfaccia utente. Questi sistemi operativi supportano un valore MUIVerb per la definizione di una stringa compatibile con MUI. Di seguito è riportato un esempio di una voce del registro di sistema per un verbo non comune:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



L'applicazione MUI dovrebbe inoltre essere in grado di registrare il valore predefinito precedente come stringa localizzabile, come illustrato di seguito:


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> La registrazione del valore predefinito precedente non è consigliata perché richiede una configurazione diversa in Windows XP e versioni successive rispetto alla configurazione usata nei sistemi operativi precedenti.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Creazione di risorse per verbi, protocolli e stringhe AuxUserType

È necessario creare risorse di stringa localizzabili per le stringhe verb, Protocol e AuxUserType. Usare le impostazioni del registro di sistema seguenti:


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



Il valore specificato per LocalizedString contiene o sostituisce solo il valore per il *verbo*, non i due valori di flag.

Di seguito è riportato un riepilogo per garantire la correttezza delle impostazioni del registro di sistema:

-   Se CLSID contiene una \\ \\ chiave inseribile CLSID {CLSID} HKCR \\ , definire il valore CLSID predefinito utilizzando HKCR \\ CLSID \\ {CLSID} \\ LocalizedString.
-   Se CLSID contiene una o più sottochiavi sotto il \\ verbo HKCR CLSID \\ {CLSID} \\ , definire ogni singola stringa del verbo usando HKCR \\ CLSID \\ {CLSID} \\ Verb \\ xxx \\ LocalizedString.
-   Se CLSID ha una o più sottochiavi sotto il \\ verbo StdFileEditing del protocollo HKCR {ProgID} \\ \\ \\ , definire ogni singola stringa del verbo usando il \\ verbo StdFileEditing di HKCR {ProgID} \\ protocollo \\ \\ \\ xxx \\ LocalizedString.
-   Se CLSID contiene una o più sottochiavi AuxUserType elencate in HKCR \\ CLSID \\ {CLSID} \\ AuxUserType, definire ogni voce AuxUserType usando HKCR \\ CLSID \\ {CLSID} \\ AuxUserType \\ xxx LocalizedString \\ .

## <a name="create-a-resource-for-the-uninstall-program"></a>Creare una risorsa per il programma di disinstallazione

Per registrare il programma di disinstallazione per l'applicazione, è possibile creare i valori del registro di sistema nella sottochiave identificatore univoco per l'applicazione nella chiave del registro di sistema HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall. I valori da impostare includono: DisplayName, DisplayVersion, Publisher, ProductID, regownr, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, comments, DisplayIcon, Readme, UrlUpdateInfo.

> [!Note]  
> Per abilitare la tecnologia MUI per ogni valore, è possibile aggiungere " \_ localizzato" al nome del valore.

 

I componenti del sistema operativo sono necessari per fornire un valore per DisplayName \_ localizzato in modo specifico per MUI. È necessario inserire il nome visualizzato in una DLL, ad esempio Res.dll, come una risorsa di tipo stringa, supponendo che l'identificatore sia 1245. L'applicazione può quindi registrare il nome visualizzato come DisplayName \_ localizzato con il valore "@ \\res.DLL,-1245". Tutte le altre impostazioni del registro di sistema devono essere mantenute così come sono, incluso il valore originale per DisplayName.

## <a name="create-resources-for-sound-events"></a>Creazione di risorse per eventi audio

Windows associa determinati eventi a file audio, ad esempio un nuovo evento di notifica di posta elettronica o un evento di allarme batteria critico. I nomi degli eventi devono essere visualizzati dall'interfaccia utente e devono supportare la globalizzazione. Pertanto, è necessario implementare una risorsa di stringa localizzabile per la descrizione di ogni descrizione dell'evento. Aggiungere un nuovo valore del registro di sistema per ogni nome di evento, oltre al valore predefinito hardcoded.

Per abilitare un evento audio, effettuare le operazioni seguenti:

1.  Implementare la descrizione come una risorsa di stringa localizzabile.
2.  Aggiungere un nuovo valore del registro di sistema per il nome visualizzato, oltre al valore predefinito hardcoded. Il layout del registro di sistema associato è illustrato di seguito:


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Se la shell non riesce a trovare o recuperare il valore di DispFileName, viene usata la descrizione predefinita.

## <a name="create-resources-for-keyboard-layout-strings"></a>Creare risorse per le stringhe di layout della tastiera

Se l'applicazione implementa un layout di tastiera, richiede una risorsa di stringa localizzabile per il nome del layout per la visualizzazione dello schermo, ad esempio negli elenchi dei layout di tastiera. Ogni layout di tastiera ha una chiave del registro di sistema in HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ keyboard layouts.

Tra i valori per tale chiave si trovano testo di layout, un nome leggibile per la compatibilità con le versioni precedenti e il nome visualizzato del layout. I dati forniti per il nome visualizzato del layout devono essere un riferimento di stringa nel formato " `@<path>,-resID` ", che fa riferimento a una risorsa di tipo stringa localizzabile associata al layout della tastiera.

Di seguito è riportato un esempio di impostazione del registro di sistema per il layout di tastiera spagnolo (Spagna):

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Rappresenta stringhe della finestra di dialogo comuni dell'oggetto Insert OLE

È possibile implementare il nome visualizzato di un oggetto OLE Insertable come risorsa di stringa localizzabile associata al codice che implementa tale oggetto. La finestra di [dialogo OLE Inserisci oggetto](/cpp/mfc/reference/coleinsertdialog-class) ottiene un nome visualizzato dalla chiave del registro \\ di sistema HKCR CLSID \\ { *<GUID>* }, dove *GUID* identifica l'identificatore di classe di un oggetto OLE inseribile. Windows Vista e versioni successive implementano questo tipo di oggetto in modo localizzabile, usando un nome visualizzato compatibile con MUI che consente la personalizzazione della lingua dell'interfaccia utente. Al contrario, i sistemi operativi precedenti a Windows Vista implementano il nome visualizzato per questo tipo di oggetto utilizzando il valore predefinito della chiave del registro di sistema corrispondente. Questo nome è in genere un nome in lingua inglese (Stati Uniti) o un nome nella lingua dell'interfaccia utente predefinita del sistema.

> [!Note]  
> Non tutti gli oggetti che corrispondono alle sottochiavi della chiave del registro di sistema sono inseribili.

 

Il valore predefinito della \\ \\ chiave CLSID { *<GUID>* } HKCR deve conservare un nome leggibile per la compatibilità con le versioni precedenti. Tuttavia, deve definire anche il valore LocalizedString, nel formato " `@<path>,-ResID` ", dove path identifica il file eseguibile che implementa l'oggetto. Il valore da un Resid specifica l'identificatore di risorsa della stringa localizzabile per il nome visualizzato.

Ad esempio, lo script di registrazione per l'oggetto Insertable media clip include le righe seguenti:


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



La prima riga fornisce la compatibilità con le versioni precedenti inserendo una stringa di testo semplice nel registro di sistema come nome visualizzato predefinito. La seconda riga consente di accedere al nome visualizzato compatibile con MUI. Indica l'identificatore di stringa archiviato in Mplay32.exe. La stringa con identificatore 9217 in Mplay32.exe può essere associata a valori di risorse stringa per un numero qualsiasi di lingue. Il nome inglese (Stati Uniti) è "clip multimediale".

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Creare risorse di stringa per Microsoft Management Console Snap-Ins

È necessario creare una risorsa di stringa localizzabile per ogni snap-in di Microsoft Management Console (MMC) usato dall'applicazione MUI. Poiché lo snap-in fa parte di una console di, dispone di un'interfaccia utente e deve essere globalizzato per operare in più linguaggi.

Nella maggior parte dei casi, gli snap-in MMC generano gli stessi problemi di globalizzazione e localizzazione dell'applicazione MUI. Uno snap-in di MMC deve riflettere il nome nel registro di sistema per la visualizzazione. La voce del registro di sistema deve includere sia un riferimento indiretto a una risorsa stringa localizzabile che una stringa letterale per la compatibilità con le versioni precedenti.

Ogni snap-in MMC dispone di una chiave del registro di sistema in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ MMC \\ snap-in. Tra i valori per la chiave sono NameString, specificando un nome leggibile per la compatibilità con le versioni precedenti e NameStringIndirect, specificando un riferimento indiretto a una risorsa di stringa localizzabile. Per NameStringIndirect, è necessario fornire un riferimento di stringa nel formato " `@<path>,-resID` ", che rappresenta una risorsa stringa localizzabile.

Ad esempio, è possibile impostare l'impostazione seguente per Mymmc.dll, dove 12345 è l'identificatore della risorsa stringa corrispondente contenente il nome localizzabile dello snap-in:


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Alcuni snap-in registrano altri valori stringa del registro di sistema che MMC non legge dal registro di sistema. Per ulteriori informazioni sull'utilizzo di questi valori, vedere registrare Microsoft Management Console Snap-In stringhe non lette dal registro di sistema in [individuazione di stringhe reindirizzate](locating-redirected-strings.md).

## <a name="create-string-resources-for-a-windows-service"></a>Creare risorse di stringa per un servizio Windows

Sebbene un servizio di Windows in genere disponga di un'interfaccia utente piccola o nessuna, deve visualizzare un nome conforme a MUI e in genere fornisce una descrizione specifica del linguaggio compatibile con MUI. La chiave del registro di sistema che descrive un servizio Windows supporta solo il valore DisplayName per il nome del servizio e il valore Description per la descrizione del servizio.

Le impostazioni per il servizio Windows vengono effettuate dall'applicazione, come descritto in impostare il nome visualizzato e la descrizione di un servizio Windows dal registro di sistema in [individuazione delle stringhe reindirizzate](locating-redirected-strings.md). Se l'applicazione non imposta i valori del registro di sistema per l'interfaccia utente del servizio, i valori nel registro di sistema rimangono impostati sull'inglese, anche se l'interfaccia utente è in un'altra lingua.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Preparazione delle risorse](preparing-resources.md)
</dt> <dt>

[Individuazione di stringhe reindirizzate](locating-redirected-strings.md)
</dt> </dl>

 

 
