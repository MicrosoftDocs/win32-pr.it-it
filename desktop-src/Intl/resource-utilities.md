---
description: In questo argomento vengono descritte due utilità utilizzate per compilare applicazioni MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilità per le risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968106"
---
# <a name="resource-utilities"></a>Utilità per le risorse

In questo argomento vengono descritte due utilità utilizzate per compilare applicazioni MUI. Mentre MUIRCT è uno strumento specifico di MUI, MUI usa anche l'utilità del compilatore Windows RC standard. Le istruzioni per l'uso di queste utilità sono fornite in [localizzazione delle risorse e compilazione dell'applicazione](localizing-resources-and-building-the-application.md).

## <a name="muirct-utility"></a>Utilità MUIRCT

MUIRCT (Muirct.exe) è un'utilità della riga di comando per suddividere un file eseguibile standard in un file di risorse e file di risorse specifici della lingua, ovvero localizzabili. Ognuno dei file risultanti contiene i dati di configurazione delle risorse per l'associazione di file. MUIRCT è incluso nel Microsoft Windows SDK per Windows Vista.

> [!Note]  
> A partire da Windows Vista, il caricatore di risorse Win32 viene aggiornato per caricare le risorse da file specifici della lingua, oltre che da un file.

 

### <a name="muirct-usages"></a>Utilizzi MUIRCT

1.  Suddividere il binario in un file binario e MUI principale basato sul \_ file di configurazione RC.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Estrarre checksum dal file di checksum \_ e inserirlo nel file di output \_ .

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Calcolare il checksum in base al \_ file di checksum e inserirlo nel file di output \_ .

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Dump del contenuto dei dati di configurazione delle risorse dal file di input \_ .

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>Sintassi di MUIRCT

MUIRCT può assumere la direzione dalle opzioni della riga di comando e/o da un file di configurazione delle risorse, specificato con l'opzione-q.


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**Opzioni e argomenti**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>-h |-?</td>
<td>Mostra la schermata della guida.</td>
</tr>
<tr class="even">
<td>-c</td>
<td>Specifica il checksum_file di input da cui estrarre o calcolare il checksum della risorsa. Checksum_file deve essere un file binario Win32 contenente le risorse localizzabili. Se checksum_file contiene risorse per più di un linguaggio, è necessario usare l'opzione-b per specificare quali di queste devono essere usate in caso contrario MUIRCT ha esito negativo. <br/></td>
</tr>
<tr class="odd">
<td>-b</td>
<td>Specifica la lingua da utilizzare quando il checksum_file specificato con-c contiene risorse in più lingue. Questa opzione può essere usata solo in combinazione con l'opzione-c. L'identificatore della lingua può essere in formato decimale o esadecimale. MUIRCT ha esito negativo se il checksum_file contiene risorse in più lingue e il parametro-b non è specificato o se la lingua specificata dall'opzione-b non è stata trovata nel checksum_file. <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Specifica l'ID lingua da includere come lingua di fallback finale nella sezione dati di configurazione delle risorse del file LN. Se il caricatore di risorse non riesce a caricare un file con estensione MUI richiesto dalle lingue dell'interfaccia utente preferita dal thread, usa la lingua di fallback finale come ultimo tentativo. Il valore LangID può essere specificato in formato decimale o esadecimale. Ad esempio, la lingua inglese (Stati Uniti) può essere specificata da-g 0x409 o-g 1033. <br/></td>
</tr>
<tr class="odd">
<td>-Q</td>
<td>Specifica che il source_file deve essere suddiviso nel output_LN_file e output_MUI_file in base al layout del file rc_config. Il file di rc_config è un file in formato XML che specifica le risorse che verranno estratte nel file con estensione MUI e che verranno lasciate nel file in. Il rc_config può specificare la distribuzione dei tipi di risorse e dei singoli elementi denominati tra i output_LN_file e output_MUI_file. Il source_file deve essere un file binario Win32 che contiene risorse in una sola lingua. in caso contrario MUIRCT avrà esito negativo. MUIRCT non suddivide il file se è indipendente dalla lingua, a indicare che nel file è presente solo l'ID lingua valore 0. I output_LN_file e output_mui_file sono i nomi del file con estensione MUI e indipendente dalla lingua in cui è suddiviso il source_file. Questi nomi di file sono facoltativi. Se non vengono specificati, MUIRCT aggiunge le estensioni. LN e. mui a source_file. In genere è consigliabile rimuovere l' &quot; estensione. LN &quot; prima di distribuire il file. MUIRCT associa il output_LN_file e output_MUI_file calcolando un checksum basato sul nome source_file e la versione del file e inserendo il risultato nella sezione di configurazione della risorsa di ogni file di output. Se usato in combinazione con l'opzione-c, l'opzione-q avrà la precedenza. Se il file rc_config fornito con l'opzione-q contiene un checksum MUIRCT ignora l'opzione-c e inserisce il valore di checksum dal valore, rc_config file nei file LN e. mui. Se non viene trovato alcun valore di checksum nella rc_config, MUIRCT calcola il checksum della risorsa in base al comportamento dell'opzione-c. <br/></td>
</tr>
<tr class="even">
<td>-v</td>
<td>Specifica il livello di maggiori per la registrazione. Specificare 1 per stampare tutti i messaggi di errore di base e i risultati dell'operazione. Specificare 2 per includere anche le informazioni sulle risorse (tipo, nome, identificatore della lingua) incluse nel file con estensione MUI e nel file. Il valore predefinito è-v 1 <br/></td>
</tr>
<tr class="odd">
<td>-X</td>
<td>Specifica l'ID lingua con cui MUIRCT contrassegna tutti i tipi di risorsa aggiunti alla sezione delle risorse del file con estensione MUI. Il valore LangID può essere specificato in formato decimale o esadecimale. Ad esempio, la lingua inglese (Stati Uniti) può essere specificata da-x 0x409 o-x 1033. <br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Estrae il checksum della risorsa contenuto nell'checksum_file fornito con l'opzione-c e lo inserisce nella output_file specificata. Quando si specifica-e, MUIRCT ignora tutte le opzioni diverse dall'opzione-c. In questo caso il checksum_file deve essere un file binario Win32 che contiene una sezione di dati di configurazione delle risorse con un valore di checksum. Il output_file deve essere un file esistente o MUI. <br/></td>
</tr>
<tr class="odd">
<td>-Z</td>
<td>Calcola e inserisce i dati di checksum delle risorse nel file di output specificato. MUIRCT basa il calcolo del checksum sull'input fornito con l'opzione-c e l'opzione facoltativa-b. Se si specifica un file di output per l'opzione-z che non esiste, MUIRCT si chiude con un errore.<br/> Esempio: calcola il checksum basato sulle risorse localizzabili in Notepad.exe e inserisce il checksum nel file di output Notepad2.exe.<br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td>-f</td>
<td>Consente la creazione di un file con estensione MUI con la risorsa di versione come unica risorsa localizzabile. Per impostazione predefinita, MUIRCT non consente questa operazione.<br/></td>
</tr>
<tr class="odd">
<td>-d</td>
<td>Individua e Visualizza i dati di configurazione delle risorse incorporati nel file di origine. Quando si specifica questa opzione, MUIRCT ignora tutte le altre opzioni della riga di comando.<br/></td>
</tr>
<tr class="even">
<td>-M</td>
<td>Specifica il numero di versione da usare per il calcolo del checksum per l'associazione dei output_LN_file e output_MUI_file. <br/></td>
</tr>
<tr class="odd">
<td>source_filename</td>
<td>Nome del file di origine binario localizzato; non è possibile usare i caratteri jolly. Questo file può contenere solo risorse in una lingua. Se nel file sono presenti risorse in più lingue, MUIRCT ha esito negativo, a meno che non venga utilizzata l'opzione-b. Se il file contiene risorse con identificatori di lingua con solo valore 0, MUIRCT non suddivide il file perché un identificatore di lingua 0 indica una lingua neutra.<br/> Per l'opzione-d, source_filename è un file in o un file di risorse specifico della lingua per il quale MUIRCT deve visualizzare i dati di configurazione delle risorse. <br/></td>
</tr>
<tr class="even">
<td>language_neutral_filename</td>
<td>facoltativo. Nome del file LN. Se non si specifica il nome del file, MUIRCT aggiunge una seconda estensione &quot; . LN &quot; al nome del file di origine da utilizzare come nome file indipendente dalla lingua. In genere è consigliabile rimuovere l' &quot; estensione. LN &quot; prima di distribuire il file.
<blockquote>
[!Note]<br />
Il file LN non deve contenere stringhe o menu. È necessario rimuoverli manualmente.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>mui_filename</td>
<td>facoltativo. Nome del file di risorse specifico della lingua. Se non si specifica un nome, MUIRCT aggiunge una seconda estensione &quot; MUI &quot; al nome del file di origine da utilizzare come nome file. In genere, MUIRCT crea un file di risorse specifico per la lingua. Tuttavia, non crea un file di risorse se sussistono le condizioni seguenti:<br/>
<ul>
<li>Nessuna risorsa localizzabile si trova nel file binario originale.</li>
<li>L'unica lingua della risorsa trovata nel file binario originale è la lingua neutra.</li>
<li>Il file binario originale contiene risorse per più di una lingua, senza contare la lingua neutra. Se il file binario contiene risorse per due lingue e una di esse è la lingua neutra, l'utilità considera il file come monolingua e crea un file di risorse specifico della lingua se sono presenti risorse localizzabili.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a>Output della lingua MUIRCT

MUIRCT sceglie il valore dell'attributo "UltimateFallbackLanguage" da inserire nei dati di configurazione della risorsa nel file in base all'ordine seguente, dalla priorità più alta a quella più bassa:

1.  Attributo "UltimateFallbackLanguage" nel file di configurazione della risorsa di origine, se ne viene passato uno come input.
2.  Lingua specificata con l'opzione-g.
3.  Lingua del file di input.

MUIRCT sceglie il valore dell'attributo "Language" da inserire nei dati di configurazione delle risorse del file con estensione MUI in base all'ordine seguente:

1.  attributo "Language" nel file di configurazione della risorsa di origine, se ne viene passato uno come input.
2.  Lingua specificata dall'opzione-x (Force Language).
3.  Lingua del file di input.

### <a name="muirct-checksum-handling"></a>Gestione checksum MUIRCT

Il sistema operativo normalmente calcola il checksum sulle risorse specifiche della lingua in un file, a meno che non si specifichi il checksum tramite un file di configurazione delle risorse. Se il checksum è lo stesso per il file in e per tutti i file di risorse specifici della lingua associati e l'attributo Language nella configurazione della risorsa in e la corrispondenza dipendente dalla lingua, il caricatore di risorse è in grado di caricare correttamente le risorse.

MUIRCT supporta diversi metodi per inserire i checksum appropriati nei dati di configurazione delle risorse:

1.  Compilare un eseguibile per ogni lingua, che contiene sia il codice che le risorse. Successivamente, usare MUIRCT per suddividere ognuno di questi file in un file in e in un file di risorse specifico della lingua. MUIRCT viene eseguito più volte, una volta per generare un file di risorse per ciascuna lingua. È possibile eseguire la compilazione nei modi seguenti:
    1.  Usare l'opzione-q per specificare un valore di checksum nel file di configurazione delle risorse. MUIRCT inserisce questo valore in tutti i file di risorse e specifici della lingua prodotti. È necessario adottare una strategia per scegliere questo valore, come descritto più avanti in questo argomento.
    2.  Usare l'opzione-c (e, facoltativamente, l'opzione-b) per scegliere una singola lingua con risorse da cui MUIRCT estrae il checksum.
    3.  Usare l'opzione-z per scegliere una singola lingua con risorse da cui MUIRCT estrae sempre il checksum. Applicare questo checksum dopo che i file sono stati compilati con altri metodi.
2.  Compilare un eseguibile contenente codice e risorse per un singolo linguaggio. Successivamente, usare MUIRCT per suddividere le risorse tra il file LN e il file di risorse specifico della lingua. Infine, usare uno strumento di localizzazione binaria per modificare il file di risorse risultante per ogni lingua.

La convenzione più comune per la gestione dei checksum consiste nel basare il checksum sulle risorse in lingua inglese (Stati Uniti). È possibile adottare una convenzione diversa, purché sia coerente per ogni file in. Ad esempio, è perfettamente accettabile per un'azienda di sviluppo software basare i relativi checksum nel software che si basa su risorse francesi (Francia) invece che in inglese (Stati Uniti), purché tutte le applicazioni dispongano di risorse francesi (Francia) su cui basare i checksum. È inoltre accettabile usare il file di configurazione delle risorse per assegnare un valore esadecimale arbitrario di un massimo di 16 cifre esadecimali come checksum. Questa ultima strategia impedisce l'uso effettivo delle opzioni-z,-c e-b di MUIRCT. Richiede l'adozione di un metodo utilizzando [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) o un altro strumento per generare valori di checksum. Questa strategia richiede anche la configurazione di un criterio per determinare quando modificare il valore quando si aggiungono nuove risorse localizzabili.

Per applicare il checksum in lingua inglese (Stati Uniti) a tutti i file, è possibile usare uno dei metodi di gestione del checksum descritti in precedenza. Ad esempio, è possibile generare il file di risorse nel file e nella lingua per l'inglese (Stati Uniti), quindi usare l'opzione MUIRCT-d per ottenere il checksum risultante. È possibile copiare questo checksum nel file di configurazione delle risorse e usare l'opzione-q con MUIRCT per applicare il checksum a tutti gli altri file.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Uso di un file di configurazione delle risorse con MUIRCT

Quando si usa MUIRCT, è possibile specificare i dati di configurazione delle risorse. Indipendentemente dal fatto che venga specificato in modo esplicito un file di configurazione delle risorse, ogni file di risorse specifico della lingua presenta dati di configurazione delle risorse, così come tutti i file con un file di risorse associato. Ad esempio:

-   Se si usa l'opzione-q per specificare un file di configurazione delle risorse, ma non sono presenti risorse localizzabili nel file di origine di input, non viene generato alcun file di risorse specifico della lingua e il file in risultante non contiene dati di configurazione delle risorse. Inoltre, se il file di origine di input dispone di risorse multilingue, MUIRCT non suddividerà il file.

> [!Note]  
> Attualmente il comportamento di MUIRCT è incoerente quando l'elemento neutralResources del file di configurazione della risorsa non contiene elementi resourceType e l'elemento localizedResources contiene stringhe e menu, ad esempio. In tal caso, MUIRCT suddivide le risorse nel modo seguente:
>
> -   Tutte le risorse nel file binario originale (incluse le stringhe e i menu), oltre alle risorse MUI, vengono inserite nel file LN.
> -   Le stringhe, i menu e le risorse MUI vengono inseriti nel file di risorse specifico della lingua appropriato.

 

### <a name="examples-for-using-muirct"></a>Esempi per l'uso di MUIRCT

**Esempi di utilizzo standard**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Esempio di file di output con l'opzione-d**

Di seguito è riportato un esempio di output dei dati di configurazione delle risorse da un file LN, Shell32.dll, usando l'opzione-d con MUIRCT:


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



**Esempio di Language-Specific output del file di risorse con l'opzione-d**

Di seguito è riportato un esempio di output dei dati di configurazione delle risorse da un file con estensione MUI, Shell32.dll. mui, usando l'opzione-d per MUIRCT:


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



## <a name="rc-compiler-utility"></a>RC (utilità del compilatore)

Il compilatore RC (Rc.exe) è un'utilità della riga di comando per la compilazione di un file di script di definizione di risorsa (estensione RC) in file di risorse (estensione res). Il compilatore RC è incluso nella Windows SDK. Questo documento illustra solo l'uso del compilatore RC con le funzionalità relative a MUI del caricatore di risorse. Per informazioni complete sul compilatore, vedere [informazioni sui file di risorse](../menurc/about-resource-files.md).

Il compilatore RC consente di compilare, da un singolo set di origini, un file LN e un file di risorse distinto specifico per la lingua. Per quanto riguarda MUIRCT, i file sono associati ai dati di configurazione delle risorse.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>Sintassi del compilatore RC usata per le risorse MUI

Le opzioni del compilatore RC sono definite in dettaglio nell' [uso di RC](../menurc/using-rc-the-rc-command-line-.md). Questa sezione definisce solo le opzioni usate per compilare le risorse MUI. Tenere presente che ogni opzione non fa distinzione tra maiuscole e minuscole. I tipi di risorse sono considerati indipendenti dalla lingua, salvo diversa indicazione.


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**Opzioni e argomenti**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>-h |-?</td>
<td>Mostra la schermata della guida.</td>
</tr>
<tr class="even">
<td>-FM</td>
<td>Usa il file di risorse specificato per le risorse specifiche della lingua. Normalmente il compilatore di risorse crea un file di risorse specifico per la lingua. Tuttavia, non crea il file se sussistono le condizioni seguenti:<br/>
<ul>
<li>Nel file RC non sono disponibili risorse localizzabili.</li>
<li>L'unica lingua della risorsa trovata nel file RC è la lingua neutra.</li>
<li>Il file RC contiene risorse per più di un linguaggio, senza contare la lingua neutra. Se il file RC contiene risorse per due lingue e una di esse è la lingua neutra, il compilatore considera il file come monolinguale. Se sono presenti risorse localizzabili, il compilatore crea un file di risorse specifico per la lingua.</li>
</ul></td>
</tr>
<tr class="odd">
<td>-Q</td>
<td>Usa il file di configurazione della risorsa specificato per ottenere i tipi di risorse da inserire nel file di risorse specifico del linguaggio e nel file LN. Per ulteriori informazioni, vedere <a href="preparing-a-resource-configuration-file.md">preparazione di un file di configurazione delle risorse</a>. In alternativa a questa opzione, è possibile usare le opzioni-j e-k, ma è preferibile usare un file di configurazione delle risorse. <br/> Usando l'opzione-q con un file di configurazione delle risorse, è possibile implementare una divisione basata su elementi e fornire gli attributi che finiranno con la configurazione della risorsa binaria nel file di risorse LN e in quello specifico del linguaggio. Questa divisione non è possibile utilizzando le opzioni-j e-k.
<blockquote>
[!Note]<br />
Il processo di suddivisione del compilatore RC non funziona correttamente se si archiviano le risorse e le informazioni sulla versione in file di configurazione delle risorse differenti. In questo caso, il compilatore RC non suddivide le informazioni sulla versione. Pertanto, si verifica un errore del linker durante il collegamento del file di risorse specifico della lingua perché il file non dispone di risorse di versione.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Specifica l'identificatore della <a href="language-identifiers.md">lingua di fallback</a> finale in formato esadecimale.<br/></td>
</tr>
<tr class="odd">
<td>-G1</td>
<td>Crea un file MUI. res anche se la risorsa di versione è l'unico contenuto localizzabile. Per impostazione predefinita, il compilatore RC non produce un file RES se VERSION è l'unica risorsa localizzabile.<br/></td>
</tr>
<tr class="even">
<td>-g2</td>
<td>Specifica il numero di versione personalizzato da usare per il calcolo del checksum.<br/></td>
</tr>
<tr class="odd">
<td>mui_res_name</td>
<td>File di risorse per le risorse specifiche della lingua.<br/></td>
</tr>
<tr class="even">
<td>rc_config_file_name</td>
<td>File di configurazione delle risorse.<br/></td>
</tr>
<tr class="odd">
<td>langid</td>
<td>Identificatore della lingua.<br/></td>
</tr>
<tr class="even">
<td>version</td>
<td>Numero di versione personalizzato, in un formato, ad esempio &quot; 6.2.0.0 &quot; .<br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Esempio per l'uso del compilatore RC per compilare risorse MUI

Per illustrare l'operazione del compilatore RC con le risorse MUI, esaminiamo la seguente riga di comando per il file di risorse MyFile. RC:


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Questa riga di comando fa sì che il compilatore RC esegua le operazioni seguenti:

-   Creare il file di risorse specifico per il linguaggio file \_ res. res e un file di risorse indipendente dalla lingua che per impostazione predefinita è MyFile. res, in base al nome del file RC.
-   Aggiungere 2 (elemento 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 \_ tipi di risorse di tipo nel file con estensione res specifico del linguaggio se sono nel file RC.
-   Aggiungere il tipo di risorsa 16, insieme ad altri tipi di risorse descritti nel file di risorse al file con estensione res indipendente dalla lingua e al file con estensione res specifico della lingua. Si noti che, in questo esempio, il tipo di risorsa 16 viene aggiunto in due posizioni.
-   Scegliere il valore dell'attributo "UltimateFallbackLanguage" da inserire nei dati di configurazione della risorsa nei file in base ai criteri seguenti, ordinati dalla priorità più alta a quella più bassa:
    -   Attributo "UltimateFallbackLanguage" nel file di configurazione della risorsa se ne viene passato uno come input.
    -   Valore dell'attributo Language da inserire nei dati di configurazione delle risorse in base all'ordine del linguaggio del compilatore RC (indipendente dalla lingua e linguaggio del file di risorse specifico della lingua). Le considerazioni includono il linguaggio nel file RC, il valore della lingua dell'opzione-GL e l'identificatore 0x0409 per l'inglese (Stati Uniti).

## <a name="remarks"></a>Commenti

Se si include un tipo di risorsa ICON (3), DIALOG (5), STRING (6) o VERSION (16) nell'elemento neutralResources, è necessario duplicare tale voce nell'elemento localizedResources nel file di configurazione della risorsa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'interfaccia utente multilingue](multilingual-user-interface-reference.md)
</dt> <dt>

[Gestione delle risorse MUI](mui-resource-management.md)
</dt> <dt>

[Localizzazione delle risorse e compilazione dell'applicazione](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
