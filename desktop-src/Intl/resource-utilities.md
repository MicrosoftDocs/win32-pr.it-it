---
description: In questo argomento vengono descritte due utilità usate per compilare applicazioni MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilità per le risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9bb8a8608c97b700beebb53ce95fdf4b85c4d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481507"
---
# <a name="resource-utilities"></a>Utilità per le risorse

In questo argomento vengono descritte due utilità usate per compilare applicazioni MUI. Anche se MUIRCT è uno strumento specifico di MUI, MUI usa anche l'utilità del compilatore RC Windows standard. Le istruzioni per l'uso di queste utilità sono disponibili in [Localizzazione delle risorse e Compilazione dell'applicazione](localizing-resources-and-building-the-application.md).

## <a name="muirct-utility"></a>Utilità MUIRCT

MUIRCT (Muirct.exe) è un'utilità della riga di comando per la suddivisione di un file eseguibile standard in un file LN e in file di risorse specifici del linguaggio (ovvero localizzabili). Ognuno dei file risultanti contiene i dati di configurazione delle risorse per l'associazione di file. MUIRCT è incluso in Microsoft Windows SDK per Windows Vista.

> [!Note]  
> A partire da Windows Vista, il caricatore di risorse Win32 viene aggiornato per caricare risorse da file specifici della lingua e da file LN.

 

### <a name="muirct-usages"></a>Utilizzi di MUIRCT

1.  Suddividere binary in file binario principale e file mui in base al file di \_ configurazione rc.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Estrarre il checksum dal file di checksum \_ e inserirlo nel file di \_ output.

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Calcolare il checksum in base al file di checksum \_ e inserirlo nel file di \_ output.

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Eseguire il dump del contenuto dei dati di configurazione delle risorse dal \_ file di input.

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>Sintassi MUIRCT

MUIRCT può assumere la direzione dalle opzioni della riga di comando e/o da un file di configurazione delle risorse, specificato tramite l'opzione -q.


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**Opzioni e argomenti**




| | | -h|-? | Visualizza la schermata della Guida. | | -c | Specifica l'input checksum_file da cui estrarre o calcolare il checksum della risorsa. Checksum_file deve essere un file binario Win32 contenente risorse localizzabili. Se checksum_file contiene risorse per più lingue, è necessario usare l'opzione -b per specificare quale di queste deve essere usata in caso contrario MUIRCT ha esito negativo. <br /> | | -b | Specifica la lingua da utilizzare quando l'checksum_file specificata con -c contiene risorse in più lingue. Questa opzione può essere usata solo in combinazione con l'opzione -c. L'identificatore di lingua può essere in formato decimale o esadecimale. MUIRCT ha esito negativo se il checksum_file contiene risorse in più lingue e -b non è specificato o se non è possibile trovare la lingua specificata dall'opzione -b nel checksum_file. <br /> | | -g | Specifica l'ID lingua da includere come lingua di fallback finale nella sezione dei dati di configurazione delle risorse del file LN. Se il caricatore di risorse non riesce a caricare un file con estensione mui richiesto dalle lingue dell'interfaccia utente preferite del thread, usa la lingua di fallback finale come ultimo tentativo. Il valore LangID può essere specificato in formato decimale o esadecimale. Ad esempio, l'inglese (Stati Uniti) può essere specificato da -g 0x409 o -g 1033. <br /> | | -q | Specifica che il source_file deve essere suddiviso in output_LN_file e output_MUI_file in base al layout rc_config file. Il rc_config file è un file in formato XML che specifica le risorse che verranno estratte nel file mui e che verranno lasciati nel file LN. Il rc_config può specificare la distribuzione dei tipi di risorsa e dei singoli elementi denominati tra il output_LN_file e output_MUI_file. Il source_file deve essere un file binario Win32 che contiene risorse in un'unica lingua; in caso contrario, MUIRCT non riesce. MUIRCT non suddivide il file se è indipendente dalla lingua, che viene indicato con solo il valore di ID lingua 0 nel file. I output_LN_file e output_mui_file sono i nomi del file con estensione mui e indipendente dalla lingua in cui viene suddivisa la source_file lingua. Questi nomi di file sono facoltativi. Se non vengono specificati, MUIRCT aggiunge le estensioni .ln e .mui source_file. In genere è necessario rimuovere l'estensione ".ln" prima di distribuire il file. MUIRCT associa i output_LN_file e output_MUI_file calcolando un checksum in base al nome e alla versione del file source_file e inserendo il risultato nella sezione di configurazione delle risorse di ogni file di output. Se usata insieme all'opzione -c, l'opzione -q ha la precedenza. Se il file rc_config fornito con l'opzione -q contiene un file MUIRCT di checksum, ignora l'opzione -c e inserisce il valore di checksum dal valore, il file rc_config nei file LN e mui. Se non viene trovato alcun valore di checksum nel rc_config, MUIRCT calcola il checksum delle risorse in base al comportamento dell'opzione -c. <br /> | | -v | Specifica il livello di dettaglio per la registrazione. Specificare 1 per stampare tutti i messaggi di errore di base e i risultati dell'operazione. Specificare 2 per includere anche le informazioni sulla risorsa (tipo, nome, identificatore di lingua) incluse nel file mui e nel file LN. Il valore predefinito è -v 1 <br /> | | -x | Specifica l'ID lingua con cui MUIRCT contrassegna tutti i tipi di risorse aggiunti alla sezione resource del file con estensione mui. Il valore LangID può essere specificato in formato decimale o esadecimale. Ad esempio, l'inglese (Stati Uniti) può essere specificato da -x 0x409 o -x 1033. <br /> | | -e | Estrae il checksum della risorsa contenuto nel checksum_file fornito con l'opzione -c e lo inserisce nel valore output_file. Se si specifica -e, MUIRCT ignora tutte le opzioni diverse dall'opzione -c. In questo caso il checksum_file deve essere un file binario Win32 che contiene una sezione dei dati di configurazione delle risorse con un valore di checksum. Il output_file deve essere un file LN o un file con estensione mui esistente. <br /> | | -z | Calcola e inserisce i dati di checksum delle risorse nel file di output specificato. MUIRCT basa il calcolo del checksum sull'input fornito con l'opzione -c e sull'opzione facoltativa -b. Se si specifica un file di output per l'opzione -z che non esiste, MUIRCT viene chiuso con un errore.<br /> Esempio: calcola il checksum in base alle risorse localizzabili in Notepad.exe e inserisce il checksum nel file di output Notepad2.exe.<br /><code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br /> | | -f | Abilita la creazione di un file mui con la risorsa versione che è l'unica risorsa localizzabile. Per impostazione predefinita, MUIRCT non consente questa operazione.<br /> | | -d | Individua e visualizza i dati di configurazione delle risorse incorporate nel file di origine. Quando si specifica questa opzione, MUIRCT ignora tutte le altre opzioni della riga di comando.<br /> | | -m | Specifica il numero di versione da utilizzare per il calcolo del checksum per l'associazione output_LN_file e output_MUI_file. <br /> | | source_filename | Nome del file di origine binario localizzato. Non è possibile usare caratteri jolly. Questo file può contenere solo risorse in un'unica lingua. Se il file contiene risorse in più lingue, MUIRCT ha esito negativo, a meno che non venga usata l'opzione -b. Se il file contiene risorse con identificatori di lingua con valore solo 0, MUIRCT non suddivide il file perché un identificatore di lingua pari a 0 indica una lingua neutra.<br /> Per l'opzione -d, source_filename è un file LN o un file di risorse specifico della lingua per cui MUIRCT deve visualizzare i dati di configurazione delle risorse. <br /> | | language_neutral_filename | Opzionale. Nome del file LN. Se non si specifica il nome di questo file, MUIRCT aggiunge una seconda estensione ".ln" al nome del file di origine da usare come nome di file indipendente dalla lingua. In genere è necessario rimuovere l'estensione ".ln" prima di distribuire il file.<blockquote>[!Note]<br />Il file LN non deve contenere stringhe o menu. È necessario rimuoverli manualmente.</blockquote><br /> | | mui_filename | Opzionale. Nome del file di risorse specifico della lingua. Se non si specifica un nome, MUIRCT aggiunge una seconda estensione ".mui" al nome del file di origine da usare come nome file. In genere, MUIRCT crea un file di risorse specifico della lingua. Tuttavia, non crea un file di risorse se esiste una delle condizioni seguenti:<br /><ul><li>Nel file binario originale non sono presenti risorse localizzabili.</li><li>L'unica lingua della risorsa trovata nel file binario originale è la lingua neutra.</li><li>Il file binario originale include risorse per più lingue, senza contare la lingua neutra. Se il file binario contiene risorse per due lingue e una di esse è la lingua neutra, l'utilità considera il file monolingue e crea un file di risorse specifico della lingua se sono presenti risorse localizzabili.</li></ul> | 




 

### <a name="muirct-language-output"></a>Output del linguaggio MUIRCT

MUIRCT sceglie il valore dell'attributo "UltimateFallbackLanguage" da inserire nei dati di configurazione delle risorse file LN in base all'ordine seguente, dalla priorità più alta alla più bassa:

1.  Attributo "UltimateFallbackLanguage" nel file di configurazione della risorsa di origine, se ne viene passato uno come input.
2.  Lingua specificata con l'opzione -g.
3.  Lingua del file di input.

MUIRCT seleziona il valore dell'attributo "language" da inserire nei dati di configurazione delle risorse del file mui in base all'ordine seguente:

1.  Attributo "language" nel file di configurazione della risorsa di origine, se ne viene passato uno come input.
2.  Lingua specificata dall'opzione -x (force language).
3.  Lingua del file di input.

### <a name="muirct-checksum-handling"></a>Gestione del checksum MUIRCT

Il sistema operativo calcola in genere il checksum sulle risorse specifiche della lingua in un file, a meno che non si specifici il checksum tramite un file di configurazione delle risorse. Se il checksum è lo stesso per il file LN e tutti i file di risorse specifici della lingua associati e l'attributo language nella configurazione delle risorse nella corrispondenza dipendente da LN e lingua, il caricatore di risorse può caricare correttamente le risorse.

MUIRCT supporta diversi metodi per inserire checksum appropriati nei dati di configurazione delle risorse:

1.  Compilare un eseguibile per ogni linguaggio, contenente sia il codice che le risorse. Successivamente, usare MUIRCT per suddividere ognuno di questi file in un file LN e in un file di risorse specifico della lingua. MUIRCT viene eseguito più volte, una volta per generare un file di risorse per ogni lingua. È possibile eseguire la compilazione nei modi seguenti:
    1.  Usare l'opzione -q per specificare un valore di checksum nel file di configurazione delle risorse. MUIRCT inserisce questo valore in tutti i file LN e nei file di risorse specifici della lingua prodotti. È necessario adottare una strategia per la scelta di questo valore, come descritto più avanti in questo argomento.
    2.  Usare l'opzione -c (e, facoltativamente, l'opzione -b) per scegliere un'unica lingua con risorse da cui MUIRCT estrae il checksum.
    3.  Usare l'opzione -z per scegliere una singola lingua con risorse da cui MUIRCT estrae sempre il checksum. Applicare questo checksum dopo che i file sono stati compilati usando altri metodi.
2.  Compilare un eseguibile contenente sia il codice che le risorse per un singolo linguaggio. Successivamente, usare MUIRCT per suddividere le risorse tra il file LN e il file di risorse specifico della lingua. Usare infine uno strumento di localizzazione binaria per modificare il file di risorse risultante per ogni lingua.

La convenzione più comune per la gestione dei checksum è basare il checksum sulle risorse in lingua inglese (Stati Uniti). È possibile adottare una convenzione diversa, purché sia coerente per ogni file LN. Ad esempio, è perfettamente accettabile per un'azienda di sviluppo software basare i checksum nel software che si basa su risorse in francese (Francia) anziché in inglese (Stati Uniti), purché tutte le applicazioni dispongono di risorse in francese (Francia) su cui basare i checksum. È anche accettabile usare il file di configurazione delle risorse per assegnare un valore esadecimale arbitrario di un massimo di 16 cifre esadecimali come checksum. Quest'ultima strategia preclude l'uso effettivo delle opzioni -z, -c e -b di MUIRCT. Richiede l'adozione di un metodo usando [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) o un altro strumento per generare valori di checksum. Questa strategia richiede anche di configurare criteri per determinare quando modificare il valore quando si aggiungono nuove risorse localizzabili.

Per applicare il checksum inglese (Stati Uniti) a tutti i file, è possibile usare uno dei metodi di gestione del checksum descritti in precedenza. Ad esempio, è possibile generare il file LN e il file di risorse specifico della lingua per l'inglese (Stati Uniti), quindi usare l'opzione MUIRCT -d per ottenere il checksum risultante. È possibile copiare questo checksum nel file di configurazione delle risorse e usare l'opzione -q con MUIRCT per applicare il checksum a tutti gli altri file.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Uso di un file di configurazione delle risorse con MUIRCT

È possibile specificare i dati di configurazione delle risorse quando si usa MUIRCT. Indipendentemente dal fatto che venga specificato in modo esplicito un file di configurazione delle risorse, ogni file di risorse specifico della lingua include dati di configurazione delle risorse, così come qualsiasi file LN con un file di risorse associato. Ad esempio:

-   Se si usa l'opzione -q per specificare un file di configurazione delle risorse, ma non sono presenti risorse localizzabili nel file di origine di input, non viene generato alcun file di risorse specifico della lingua e il file LN risultante non contiene dati di configurazione delle risorse. Inoltre, se il file di origine di input ha risorse multilingue, MUIRCT non suddividerà il file.

> [!Note]  
> Attualmente il comportamento di MUIRCT è incoerente quando l'elemento neutralResources del file di configurazione delle risorse non contiene elementi resourceType e l'elemento localizedResources contiene stringhe e menu, ad esempio. In tal caso, MUIRCT suddivide le risorse come segue:
>
> -   Tutte le risorse nel file binario originale (incluse stringhe e menu), oltre alle risorse MUI, vengono inserite nel file LN.
> -   Stringhe, menu e risorse MUI vengono inseriti nel file di risorse specifico della lingua appropriato.

 

### <a name="examples-for-using-muirct"></a>Esempi per l'uso di MUIRCT

**Esempi di utilizzo standard**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Esempio di output del file LN con l'opzione -d**

Di seguito è riportato un esempio dell'output dei dati di configurazione delle risorse da un file LN, Shell32.dll, usando l'opzione -d con MUIRCT:


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



**Esempio di output Language-Specific file di risorse usando l'opzione -d**

Di seguito è riportato un esempio dell'output dei dati di configurazione delle risorse da un file con estensione mui, Shell32.dll.mui, usando l'opzione -d per MUIRCT:


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a>Utilità del compilatore RC

Il compilatore RC (Rc.exe) è un'utilità della riga di comando per la compilazione di un file script di definizione delle risorse (estensione RC) in file di risorse (estensione res). Il compilatore RC è incluso in Windows SDK. Questo documento illustra solo l'uso del compilatore RC con funzionalità correlate a MUI del caricatore di risorse. Per informazioni complete sul compilatore, vedere [Informazioni sui file di risorse.](../menurc/about-resource-files.md)

Il compilatore RC consente di compilare, da un singolo set di origini, un file LN e un file di risorse specifico del linguaggio separato. Come per MUIRCT, i file sono associati ai dati di configurazione delle risorse.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>Sintassi del compilatore RC usata per le risorse MUI

Le opzioni del compilatore RC sono definite in dettaglio in [Uso di RC.](../menurc/using-rc-the-rc-command-line-.md) Questa sezione definisce solo le opzioni usate per compilare le risorse MUI. Tenere presente che ogni opzione non fa distinzione tra maiuscole e minuscole. Si presuppone che i tipi di risorse siano indipendenti dalla lingua, se non diversamente indicato.


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**Opzioni e argomenti**




| | | -h|-? | Mostra la schermata della Guida. | | -fm | Usa il file di risorse specificato per le risorse specifiche della lingua. In genere il compilatore di risorse crea un file di risorse specifico del linguaggio. Tuttavia, non crea il file se si verifica una delle condizioni seguenti:<br /><ul><li>Non sono presenti risorse localizzabili nel file RC.</li><li>L'unica lingua delle risorse trovata nel file RC è la lingua neutra.</li><li>Il file RC contiene risorse per più di una lingua, senza contare la lingua neutra. Se il file RC contiene risorse per due linguaggi e uno di essi è il linguaggio neutro, il compilatore considera il file come monolingue. Se sono presenti risorse localizzabili, il compilatore crea un file di risorse specifico del linguaggio.</li></ul> | | -q | Usa il file di configurazione delle risorse specificato per ottenere i tipi di risorse da inserire nel file di risorse specifico del linguaggio e nel file LN. Per altre informazioni, vedere <a href="preparing-a-resource-configuration-file.md">Preparazione di un file di configurazione delle risorse.</a> In alternativa a questa opzione, è possibile usare le opzioni -j e -k, ma è preferibile usare un file di configurazione delle risorse. <br /> Usando l'opzione -q con un file di configurazione delle risorse, è possibile implementare una suddivisione basata su elementi e fornire attributi che finiranno con la configurazione delle risorse binarie nel nome locale e nel file di risorse specifico della lingua. Questa suddivisione non è possibile usando le opzioni -j e -k.<blockquote>[!Note]<br />Il processo di suddivisione del compilatore RC non funziona correttamente se si archiviano le risorse e le informazioni sulla versione in file di configurazione delle risorse diversi. In questo caso, il compilatore RC non suddivide le informazioni sulla versione. Pertanto, si verifica un errore del linker durante il collegamento del file di risorse specifico del linguaggio perché il file non dispone di risorse di versione.</blockquote><br /><br /> | | -g | Specifica l'identificatore <a href="language-identifiers.md">di lingua di fallback</a> finale in formato esadecimale.<br /> | | -g1 | Crea un file MUI con estensione res anche se la risorsa VERSION è l'unico contenuto localizzabile. Per impostazione predefinita, il compilatore RC non produce un file con estensione res se VERSION è l'unica risorsa localizzabile.<br /> | | -g2 | Specifica il numero di versione personalizzato da utilizzare per il calcolo del checksum.<br /> | | mui_res_name | File di risorse per risorse specifiche della lingua.<br /> | | rc_config_file_name | File di configurazione delle risorse.<br /> | | langid | Identificatore di lingua.<br /> | | Versione | Numero di versione personalizzato, in un formato come "6.2.0.0".<br /> | 




 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Esempio per l'uso del compilatore RC per compilare risorse MUI

Per illustrare l'operazione del compilatore RC con le risorse MUI, esaminare la riga di comando seguente per il file di risorse Myfile.rc:


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Questa riga di comando consente al compilatore RC di eseguire le operazioni seguenti:

-   Creare il file di risorse myfile res.res specifico della lingua e un file di risorse indipendente dalla lingua che per impostazione predefinita è Myfile.res, in base al nome del \_ file RC.
-   Aggiungere i tipi di risorsa 2 (elemento 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY TYPE al file CON ESTENSIONE RES specifico del linguaggio, se sono \_ nel file RC.
-   Aggiungere il tipo di risorsa 16, insieme a qualsiasi altro tipo di risorsa descritto nel file di risorse, al file con estensione res indipendente dalla lingua e al file con estensione res specifico della lingua. Si noti che, in questo esempio, il tipo di risorsa 16 viene aggiunto in due posizioni.
-   Scegliere il valore dell'attributo "UltimateFallbackLanguage" da inserire nei dati di configurazione delle risorse file LN in base ai criteri seguenti, ordinati dalla priorità più alta alla più bassa:
    -   Attributo "UltimateFallbackLanguage" nel file di configurazione delle risorse, se ne viene passato uno come input.
    -   Valore dell'attributo Language da inserire nei dati di configurazione delle risorse in base all'ordine del linguaggio del compilatore RC (linguaggio indipendente dal linguaggio e linguaggio specifico del file di risorse). Le considerazioni includono la lingua nel file RC, il valore della lingua dell'opzione -gl e l'identificatore 0x0409 per l'inglese (Stati Uniti).

## <a name="remarks"></a>Commenti

Se si include un tipo di risorsa ICON(3), DIALOG(5), STRING(6) o VERSION(16) nell'elemento neutralResources, è necessario duplicare tale voce nell'elemento localizedResources nel file di configurazione delle risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[interfaccia utente multilingue Riferimento](multilingual-user-interface-reference.md)
</dt> <dt>

[Gestione delle risorse MUI](mui-resource-management.md)
</dt> <dt>

[Localizzazione delle risorse e compilazione dell'applicazione](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
