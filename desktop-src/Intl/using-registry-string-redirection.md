---
description: Archiviazione di stringhe hard-coded nel Registro di sistema fa parte di un modello di localizzazione Windows Vista preliminare.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Uso del reindirizzamento delle stringhe del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f0804d0586f8340e5a84e9da9c82ca39ffc30b55f72f4695d5216cbb26aab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389417"
---
# <a name="using-registry-string-redirection"></a>Uso del reindirizzamento delle stringhe del Registro di sistema

Archiviazione di stringhe hard-coded nel Registro di sistema fa parte di un modello di localizzazione Windows Vista preliminare. Non è supportato da MUI. Nel modello corrente l'interfaccia utente per il sistema operativo viene eseguita in file di risorse specifici della lingua in una base indipendente dalla lingua. I componenti del sistema operativo usano il Registro di sistema in modo indipendente dalla lingua.

MUI usa solo stringhe del Registro di sistema reindirizzate definite dalle risorse PE Win32 nel file di risorse della lingua di base. Il reindirizzamento viene definito separatamente, ad esempio in un file inf. Questo tipo di archiviazione consente al caricatore di risorse di selezionare automaticamente le risorse di lingua corrette durante il caricamento del modulo delle risorse.

> [!Note]  
> Questo argomento riguarda solo le risorse PE Win32. Se si usano risorse pe non Win32, è necessario fornire il reindirizzamento personalizzato delle stringhe del Registro di sistema, se necessario.

 

## <a name="create-a-language-neutral-resource"></a>Creare una risorsa Language-Neutral locale

Un'applicazione MUI in esecuzione in Windows Vista e versioni successive usa una risorsa stringa indipendente dalla lingua per consentire l'accesso alle stringhe specifiche della lingua archiviate in una tabella di risorse stringa. Il codice dell'applicazione che legge questi valori dal Registro di sistema è descritto nella sezione Caricare un Language-Neutral del Registro di sistema di [Individuazione di stringhe reindirizzate](locating-redirected-strings.md).

I dati per un valore del Registro di sistema indipendente dalla lingua hanno il formato " `@<PE-path>,-<stringID>[;<comment>]` ", dove:

-   *PE-path* specifica il percorso del file eseguibile. È possibile specificare il percorso usando una variabile di ambiente, ad esempio %ProgramFiles%, per supportare la distribuzione. Un'alternativa per fare riferimento alla stringa consiste nell'osare le informazioni sul percorso del file. In questo caso, l'applicazione deve avere alcuni mezzi, ad esempio un altro valore del Registro di sistema, per comunicare la propria directory di installazione.
-   *stringID* specifica l'identificatore di risorsa numerica della risorsa stringa pertinente, implementato come qualsiasi altra risorsa stringa localizzabile.
-   *comment* specifica informazioni facoltative per il debug o la leggibilità del valore del Registro di sistema. Le funzioni API del Registro di sistema ignorano il commento durante il caricamento della stringa.

> [!Note]  
> I dati per il valore del Registro di sistema non fanno riferimento esplicito al file di risorse specifico del linguaggio. Il file corretto viene determinato in fase di esecuzione, in base alle preferenze di lingua correnti dell'interfaccia utente.

 

Un valore del Registro di sistema viene immesso senza uno spazio tra "," e "-". Un valore del Registro di sistema corretto è:

`shell32.dll,-22912`

Un valore del Registro di sistema non corretto è:

`shell32.dll, -22912`

Un esempio di Windows Vista è il valore del Registro di sistema con i dati seguenti:

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Creare risorse per le stringhe di collegamento

Quando l'applicazione MUI visualizza il nome nell'interfaccia utente della shell, viene visualizzata una stringa infotip per l'icona dell'applicazione. È necessario creare risorse stringa per il nome visualizzato dell'applicazione e la stringa del suggerimento informazioni associata per ogni lingua supportata. Quando le risorse sono pronte, l'applicazione può usare le stringhe come descritto nella sezione Usare l'API Shell per caricare stringhe di collegamento dal Registro di sistema di [Individuazione di stringhe reindirizzate](locating-redirected-strings.md).

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>Preparare le risorse per un collegamento creato con il Windows di installazione

Se si usa il Windows installer (MSI) per creare un collegamento, le risorse stringa includono il nome visualizzato e la descrizione del collegamento. Nella tabella [dei collegamenti MSI](../msi/shortcut-table.md)viene fatto riferimento alla DLL della risorsa nelle colonne appropriate e gli identificatori di risorsa per il nome visualizzato del collegamento e la descrizione vengono usati nelle colonne corrispondenti dell'identificatore di risorsa.

In modo che il collegamento all'applicazione funzioni correttamente con la tecnologia delle risorse MUI, tenere presenti i punti seguenti quando si preparano le stringhe di collegamento:

-   Usare variabili di ambiente o un percorso relativo per registrare la DLL. È possibile specificare @%systemroot% system32shell32.dll se il tipo di stringa del Registro di sistema \\ \\ è REG EXPAND \_ \_ SZ. L'identificatore di risorsa stringa per "Documento di testo" Shell32.dll è 12345.
-   Non usare spazi intorno ai simboli "," e "-". Un esempio corretto è "shell32.dll,-22912".
-   Non usare un nome file breve. Questo tipo di nome non funziona con il caricatore di risorse.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Preparare le risorse per un collegamento usando il formato INF

Se si usa il formato di file INF per creare stringhe di collegamento, il file di risorse deve apportare le impostazioni del Registro di sistema seguenti. Queste istruzioni presuppongono l'uso della sintassi ProfileItems dell'API di installazione.

1.  Modificare il valore della descrizione comando in modo che punti al riferimento di reindirizzamento della stringa usando il percorso e l'identificatore di risorsa.
2.  Aggiungere il nuovo valore DisplayResource nelle sezioni di installazione ProfileItems.

Di seguito è riportato un esempio che mostra l'aggiunta dell'applicazione Calculator al menu **Start:**


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Usare la sintassi illustrata di seguito quando si usa INF per aggiungere elementi, ad esempio una cartella Gruppo di accesso, al menu **Start.** Questa sintassi presuppone l'uso del supporto StartMenuItems dal programma di installazione, simile alla sintassi usata \[ \] in Syssetup.inf.


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



Impostare il *suggerimento sul* valore sul riferimento alla stringa " `@<path>,-resID` ".

Il nome visualizzato è determinato dai *valori resDLL* *e resID.* Il *valore resID* specifica l'identificatore di risorsa per una risorsa stringa associata al file indipendente dalla lingua. Il *valore resDLL* specifica il percorso del file indipendente dalla lingua.

## <a name="create-resources-for-friendly-document-type-names"></a>Creare risorse per nomi descrittivi dei tipi di documento

È necessario implementare stringhe di nome descrittivo e infotip per l'applicazione come risorse stringa. Per consentire ai nomi descrittivi dei tipi di documento di reagire alla lingua dell'interfaccia utente, l'applicazione deve registrare i nomi usando il valore FriendlyTypeName nella chiave dell'identificatore di programma per il tipo di file. Il valore predefinito per la chiave dell'identificatore di programma deve essere mantenuto per mantenere la compatibilità con le versioni precedenti. Per informazioni sull'accesso ai nomi dall'applicazione, vedere la sezione Nomi dei tipi di documento descrittivi per le query nel Registro di sistema di [Individuazione di stringhe reindirizzate](locating-redirected-strings.md).

Il lavoro specifico prevede i passaggi seguenti:

1.  Implementare il nome descrittivo e le stringhe del suggerimento informazioni come risorse stringa specifiche della lingua.
2.  Aggiungere il valore FriendlyTypeName nella chiave del Registro di sistema del tipo di documento. I dati per il valore seguono il modello " ", dove percorso indica l'eseguibile e resID è l'identificatore di risorsa di una risorsa stringa localizzabile associata a `@<path>,-<resID>` tale eseguibile.  
3.  Specificare il valore del Registro di sistema InfoTip in base al formato " `@<path>,-<resID>` ".

L'esempio seguente illustra le impostazioni del Registro di sistema per un file .txt:


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

Le stringhe di azione per determinati verbi, ad esempio "open" e "edit", vengono visualizzate nel menu popup visualizzato quando l'utente fa clic con il pulsante destro del mouse su un file in Windows Explorer. L'applicazione non deve specificare stringhe per i verbi della shell comuni, perché la shell ha le proprie impostazioni predefinite abilitate per MUI per questi verbi. Tuttavia, è necessario fornire risorse stringa localizzabili per stringhe che rappresentano verbi non comuni.

Nei sistemi operativi Windows XP, il rendering delle stringhe per i verbi della shell nel Registro di sistema viene eseguito usando la sintassi seguente, dove *verbo* specifica il nome effettivo del verbo:


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Ecco un esempio:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



In Windows XP e versioni successive, è possibile usare un livello di riferimento indiretto per fare in modo che una stringa di azione dipersi dalla lingua dell'interfaccia utente. Questi sistemi operativi supportano un valore MUIVerb per la definizione di una stringa compatibile con MUI. Di seguito è riportato un esempio di voce del Registro di sistema per un verbo non comune:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



L'applicazione MUI dovrebbe anche essere in grado di registrare il valore predefinito precedente come stringa localizzabile, come illustrato di seguito:


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> La registrazione del valore predefinito precedente non è consigliata perché richiede una configurazione diversa in Windows XP e versioni successive rispetto all'installazione usata nei sistemi operativi precedenti.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Creare risorse per stringhe verbo, protocollo e AuxUserType

È necessario creare risorse stringa localizzabili per le stringhe Verb, Protocol e AuxUserType. Usare le impostazioni del Registro di sistema seguenti:


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



Il valore specificato per LocalizedString contiene o sostituisce solo il valore per *Il verbo,* non i due valori di flag.

Di seguito è disponibile un riepilogo che consente di verificare le impostazioni corrette del Registro di sistema:

-   Se CLSID ha un CLSID HKCR {clsid} Chiave inseribile, definire il valore CLSID predefinito usando \\ \\ \\ HKCR \\ CLSID \\ {clsid} \\ LocalizedString.
-   Se CLSID ha una o più sottochiavi nel verbo HKCR CLSID {clsid}, definire ogni singola stringa verbo usando \\ \\ \\ HKCR \\ CLSID \\ {clsid} \\ \\ Verbo xxx \\ LocalizedString.
-   Se CLSID ha una o più sottochiavi in HKCR {progid} Protocol Stdfileediting Verb, definire ogni singola stringa verbo usando \\ \\ \\ \\ HKCR \\ {progid} \\ Protocol \\ Stdfileediting \\ Verb xxx \\ \\ LocalizedString.
-   Se CLSID include una o più sottochiavi AuxUserType elencate in HKCR \\ CLSID \\ {clsid} \\ AuxUserType, definire ogni voce AuxUserType usando HKCR \\ CLSID \\ {clsid} \\ AuxUserType \\ xxx \\ LocalizedString.

## <a name="create-a-resource-for-the-uninstall-program"></a>Creare una risorsa per il programma di disinstallazione

Per registrare il programma di disinstallazione per l'applicazione, è possibile creare i valori del Registro di sistema nella sottochiave identificatore univoco per l'applicazione nella chiave del Registro di sistema HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Uninstall. I valori da impostare includono: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.

> [!Note]  
> Per abilitare la tecnologia MUI per ogni valore, è possibile aggiungere \_ "Localized" al nome del valore.

 

I componenti del sistema operativo sono necessari per fornire un valore per DisplayName \_ Localizzato in modo specifico di MUI. È necessario inserire il nome visualizzato in una DLL, ad esempio Res.dll, come risorsa stringa, presupponendo che l'identificatore sia 1245. L'applicazione può quindi registrare il nome visualizzato come DisplayName Localized con il valore \_ "@ \\res.DLL,-1245". Tutte le altre impostazioni del Registro di sistema devono essere mantenute così come sono, incluso il valore originale per DisplayName.

## <a name="create-resources-for-sound-events"></a>Creare risorse per eventi sonori

Windows associa determinati eventi a file audio, ad esempio un evento di notifica di nuova posta o un evento di avviso critico della batteria. I nomi degli eventi devono essere visualizzati dall'interfaccia utente e devono supportare la globalizzazione. È pertanto consigliabile implementare una risorsa stringa localizzabile per la descrizione di ogni descrizione dell'evento. Aggiungere un nuovo valore del Registro di sistema per ogni nome di evento, oltre al valore predefinito hard-coded.

Eseguire le operazioni seguenti per abilitare un evento audio:

1.  Implementare la descrizione come risorsa stringa localizzabile.
2.  Aggiungere un nuovo valore del Registro di sistema per il nome visualizzato, oltre al valore predefinito hard-coded. Il layout del Registro di sistema associato è illustrato di seguito:


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Se la shell non riesce a trovare o recuperare il valore di DispFileName, usa la descrizione predefinita.

## <a name="create-resources-for-keyboard-layout-strings"></a>Creare risorse per le stringhe di layout di tastiera

Se l'applicazione implementa un layout di tastiera, è necessaria una risorsa stringa localizzabile per il nome del layout per la visualizzazione dello schermo, ad esempio negli elenchi di layout di tastiera. Ogni layout di tastiera ha una chiave del Registro di sistema in HKEY \_ LOCAL \_ MACHINE Sistema \\ \\ CurrentControlSet Layout di tastiera del \\ \\ controllo.

Tra i valori per tale chiave sono Testo layout, un nome leggibile per la compatibilità con le versioni precedenti e Nome visualizzato del layout. I dati forniti per Layout Display Name devono essere un riferimento stringa nel formato " ", che fa riferimento a una risorsa `@<path>,-resID` stringa localizzabile associata al layout di tastiera.

Di seguito è riportato un esempio di impostazione del Registro di sistema per il layout di tastiera spagnolo (Spagna):

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Rappresentare le stringhe di finestra di dialogo comuni dell'oggetto Insert OLE

È possibile implementare il nome visualizzato di un oggetto ole inseribile come risorsa stringa localizzabile associata al codice che implementa tale oggetto. La [finestra di dialogo](/cpp/mfc/reference/coleinsertdialog-class) Inserisci oggetto OLE ottiene un nome visualizzato dalla chiave del Registro di sistema HKCR CLSID { }, dove GUID identifica l'identificatore di classe di un oggetto OLE \\ \\ *<GUID>* inseribile.  Windows Vista e versioni successive implementano questo tipo di oggetto in modo localizzabile, usando un nome visualizzato conforme a MUI che consente la personalizzazione della lingua dell'interfaccia utente. Al contrario, i sistemi operativi Windows Vista implementano il nome visualizzato per questo tipo di oggetto usando il valore predefinito della chiave del Registro di sistema corrispondente. In genere questo nome è un nome inglese (Stati Uniti) o un nome nella lingua predefinita dell'interfaccia utente del sistema.

> [!Note]  
> Non tutti gli oggetti che corrispondono alle sottochiavi della chiave del Registro di sistema sono inseribili.

 

Il valore predefinito della chiave CLSID HKCR { } deve mantenere un nome leggibile per \\ \\ la *<GUID>* compatibilità con le versioni precedenti. Tuttavia, deve anche definire il valore LocalizedString, nel formato " ", dove path identifica il `@<path>,-ResID` file eseguibile che implementa l'oggetto. Il valore ResID specifica l'identificatore di risorsa della stringa localizzabile per il nome visualizzato.

Ad esempio, lo script di registrazione per l'oggetto Media Clip inseribile include le righe seguenti:


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



La prima riga garantisce la compatibilità con le versioni precedenti inserendo una semplice stringa di testo nel Registro di sistema come nome visualizzato predefinito. La seconda riga fornisce l'accesso al nome visualizzato conforme a MUI. Indica l'identificatore di stringa archiviato in Mplay32.exe. La stringa con identificatore 9217 in Mplay32.exe può essere associata ai valori delle risorse stringa per un numero qualsiasi di lingue. Il nome inglese (Stati Uniti) è "Media Clip".

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Creare risorse stringa per Microsoft Management Console Snap-Ins

È necessario creare una risorsa stringa localizzabile per ogni snap-in Microsoft Management Console (MMC) usato dall'applicazione MUI. Poiché uno snap-in fa parte di una console, ha un'interfaccia utente e deve essere globalizzato per operare in più lingue.

Per la maggior parte, gli snap-in MMC generano gli stessi problemi di globalizzazione e localizzazione dell'applicazione MUI stessa. Uno snap-in MMC deve riflettere il nome nel Registro di sistema per la visualizzazione. La voce del Registro di sistema deve includere sia un riferimento indiretto a una risorsa stringa localizzabile che una stringa letterale per la compatibilità con le versioni precedenti.

Ogni snap-in MMC ha una chiave del Registro di sistema in HKEY \_ LOCAL MACHINE Software Microsoft MMC \_ \\ \\ \\ \\ SnapIns. Tra i valori per tale chiave sono NameString, specificando un nome leggibile per la compatibilità con le versioni precedenti e NameStringIndirect, specificando un riferimento indiretto a una risorsa stringa localizzabile. Per NameStringIndirect è necessario specificare un riferimento stringa nel formato " ", che `@<path>,-resID` rappresenta una risorsa stringa localizzabile.

Ad esempio, è possibile eseguire l'impostazione seguente per Mymmc.dll, dove 12345 è l'identificatore della risorsa stringa corrispondente contenente il nome localizzabile dello snap-in:


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Alcuni snap-in registrano altri valori stringa del Registro di sistema che MMC non legge dal Registro di sistema. Per altre informazioni sull'uso di questi valori, vedere Registrare Microsoft Management Console Snap-In stringhe non lette dal Registro di sistema in [Individuazione di stringhe reindirizzate](locating-redirected-strings.md).

## <a name="create-string-resources-for-a-windows-service"></a>Creare risorse stringa per un Windows servizio

Anche se un servizio Windows ha in genere un'interfaccia utente piccola o nessuna, deve visualizzare un nome conforme a MUI e in genere fornisce una descrizione specifica del linguaggio conforme a MUI. La chiave del Registro di sistema che descrive un Windows supporta solo il valore DisplayName per il nome del servizio e il valore Description per la descrizione del servizio.

Impostazioni per il servizio Windows vengono effettuate dall'applicazione, come descritto in Impostare il nome visualizzato e la descrizione per un servizio Windows dal Registro di sistema in Individuazione di stringhe [reindirizzate](locating-redirected-strings.md). Se l'applicazione non imposta i valori del Registro di sistema per l'interfaccia utente del servizio, i valori nel Registro di sistema rimangono impostati sull'inglese, anche se l'interfaccia utente è in un'altra lingua.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Preparazione delle risorse](preparing-resources.md)
</dt> <dt>

[Individuazione di stringhe reindirizzate](locating-redirected-strings.md)
</dt> </dl>

 

 
