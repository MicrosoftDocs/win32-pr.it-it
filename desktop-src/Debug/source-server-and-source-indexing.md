---
description: Il server di origine consente a un client di recuperare la versione esatta dei file di origine utilizzati per compilare un'applicazione.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Server di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320052"
---
# <a name="source-server"></a>Server di origine

Il server di origine consente a un client di recuperare la versione esatta dei file di origine utilizzati per compilare un'applicazione. Poiché il codice sorgente di un modulo può variare tra le versioni e per un certo periodo di tempo, è importante esaminare il codice sorgente esistente quando la versione del modulo in questione è stata compilata.

Il server di origine recupera i file appropriati dal controllo del codice sorgente. Per usare il server di origine, l'applicazione deve essere stata indicizzata come origine.

## <a name="source-indexing"></a>Indicizzazione origine

Il sistema di indicizzazione dell'origine è una raccolta di file eseguibili e script Perl. Per gli script Perl è necessario Perl 5,6 o versione successiva.

In genere, i file binari sono indicizzati all'origine durante il processo di compilazione dopo che l'applicazione è stata compilata. Le informazioni necessarie per il server di origine vengono archiviate nei file PDB.

Il server di origine viene attualmente fornito con script che dovrebbero funzionare con i sistemi di controllo del codice sorgente seguenti.

-   Team Foundation Server
-   Perforce
-   Visual SourceSafe
-   CVS
-   Subversion

È anche possibile creare uno script personalizzato per indicizzare il codice per un altro sistema di controllo del codice sorgente.

Nella tabella seguente sono elencati gli strumenti del server di origine.



| Strumento        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | Questo file è l'elenco principale di tutti i server del controllo del codice sorgente. Ogni voce ha il formato seguente:*MyServer* = *la*<br/> Quando si utilizza Perforce, le informazioni sul server sono costituite dal percorso di rete completo del server, seguito da due punti, seguito dal numero di porta utilizzato. Ad esempio:<br/> MyServer = Machine. Corp. Company. com: 1666<br/> Questo file può essere installato nel computer in cui è in esecuzione il debugger. Quando viene avviato, il server di origine esamina Srcsrv.ini per i valori; questi valori eseguiranno l'override delle informazioni contenute nel file PDB. Ciò consente agli utenti di configurare un debugger per l'utilizzo di un server del controllo del codice sorgente alternativo in fase di debug.<br/> Per ulteriori informazioni, vedere l'esempio Srcsrv.ini installato con gli strumenti del server di origine.<br/> |
| Ssindex. cmd | Questo script compila l'elenco dei file archiviati nel controllo del codice sorgente insieme alle informazioni sulla versione di ogni file. Archivia un subset di queste informazioni nei file con estensione pdb generati quando è stata compilata l'applicazione. Lo script usa uno dei moduli Perl seguenti per interfacciarsi con il controllo del codice sorgente: P4.pm (Perforce) o Vss.pm (Visual Source Safe). Per ulteriori informazioni, eseguire lo script con il-? o-?? (Guida dettagliata) o esaminare lo script.<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | Questa utilità elenca tutti i file indicizzati in un file con estensione pdb. Per ogni file vengono elencati il percorso completo, il server di controllo del codice sorgente e il numero di versione del file. È possibile usare queste informazioni per recuperare i file senza usare il server di origine. Per ulteriori informazioni, eseguire l'utilità con/? opzione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | Questa utilità viene utilizzata dagli script di indicizzazione per inserire le informazioni sul controllo della versione nel flusso alternativo "SrcSrv" del file con estensione PDB di destinazione. Può inoltre leggere qualsiasi flusso da un file con estensione pdb. È possibile utilizzare queste informazioni per verificare che gli script di indicizzazione funzionino correttamente. Per ulteriori informazioni, eseguire l'utilità con/? opzione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>Recupero del file di origine

L'API DbgHelp fornisce l'accesso alle funzionalità del server di origine tramite la funzione [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) . Per recuperare il nome del file di origine da recuperare, chiamare la funzione [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) o [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .

## <a name="using-source-server-with-a-debugger"></a>Uso del server di origine con un debugger

Per usare il server di origine con WinDbg, KD, NTSD o CDB, verificare di avere installato una versione recente del pacchetto strumenti di debug per Windows (versione 6,3 o successiva). Includere quindi SRV \* nel comando. Srcpath come indicato di seguito:

**\. Srcpath SRV \* ;** _c: \\ origine_

Si noti che questo esempio include anche un percorso di origine tradizionale. Se il debugger non è in grado di recuperare il file dal server di origine, eseguirà la ricerca nel percorso specificato.

Se un file di origine viene recuperato dal server di origine, rimarrà sul disco rigido al termine della sessione di debug. I file di origine vengono archiviati localmente nella sottodirectory src della directory di installazione degli strumenti di debug per Windows.

## <a name="source-server-data-blocks"></a>Blocchi di dati del server di origine

Il server di origine si basa su due blocchi di dati all'interno del file PDB.

-   Elenco dei file di origine. La compilazione di un modulo crea automaticamente un elenco di percorsi completi per i file di origine usati per compilare il modulo.
-   Blocco di dati. L'indicizzazione dell'origine, come descritto in precedenza, aggiunge un flusso alternativo al file PDB denominato "SrcSrv". Lo script che inserisce questi dati dipende dal processo di compilazione specifico e dal sistema di controllo del codice sorgente in uso.

Nella specifica del linguaggio versione 1 il blocco di dati è suddiviso in tre sezioni: ini, variabili e file di origine. Ha la sintassi seguente.

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

Tutto il testo viene interpretato letteralmente, ad eccezione del testo racchiuso tra segni di percentuale (%). Il testo racchiuso tra simboli di percentuale viene considerato come un nome di variabile da risolvere in modo ricorsivo, a meno che non si tratti di una delle funzioni seguenti:

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()
</dt> <dd>

Il testo del parametro deve essere racchiuso tra simboli di percentuale e considerato come una variabile da espandere.

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()
</dt> <dd>

Tutte le barre (/) nel testo del parametro devono essere sostituite con barre rovesciate ( \\ ).

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()
</dt> <dd>

Tutte le informazioni sul percorso nel testo del parametro devono essere rimosse, lasciando solo il nome del file.

</dd> </dl>

La sezione INI contiene le variabili che descrivono i requisiti. Lo script di indicizzazione può aggiungere un numero qualsiasi di variabili a questa sezione. Alcuni esempi:

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>Versione
</dt> <dd>

Versione della specifica del linguaggio. Questa variabile è obbligatoria.

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>VERCTL
</dt> <dd>

Stringa che descrive il prodotto del controllo del codice sorgente. Questa variabile è facoltativa.

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>DATETIME
</dt> <dd>

Stringa che indica la data e l'ora di elaborazione del file PDB. Questa variabile è facoltativa.

</dd> </dl>

La sezione variables contiene variabili che descrivono come estrarre un file dal controllo del codice sorgente. Può inoltre essere utilizzato per definire il testo comunemente utilizzato come variabile per ridurre le dimensioni del blocco di dati.

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG
</dt> <dd>

Viene descritto come compilare il percorso di destinazione per il file estratto. Si tratta di una variabile obbligatoria.

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD
</dt> <dd>

Viene descritto come compilare il comando per estrarre il file dal controllo del codice sorgente. Sono inclusi il nome del file eseguibile e i relativi parametri della riga di comando. Si tratta di una variabile obbligatoria.

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV
</dt> <dd>

Stringa che elenca le variabili di ambiente da creare durante l'estrazione del file. Separare più voci con un carattere backspace ( \\ b). Si tratta di una variabile facoltativa.

</dd> </dl>

La sezione file di origine contiene una voce per ogni file di origine indicizzato. Il contenuto di ogni riga viene interpretato come variabile con i nomi VAR1, VAR2, VAR3 e così via fino a VAR10. Le variabili sono separate da asterischi. VAR1 deve specificare il percorso completo del file di origine, come elencato altrove nel file PDB. Ad esempio, la riga seguente:

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

viene interpretato nel modo seguente:

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

In questo esempio, VAR4 è un numero di versione. Tuttavia, la maggior parte dei sistemi di controllo del codice sorgente supporta l'assegnazione di etichette ai file in modo da poter ripristinare lo stato di origine di una determinata compilazione. Pertanto, è possibile usare in alternativa l'etichetta per la compilazione. Il blocco di dati di esempio può essere modificato in modo da contenere una variabile come la seguente:

``` syntax
LABEL=BUILD47
```

Quindi, presumendo che il sistema di controllo del codice sorgente usi il simbolo di chiocciola (@) per indicare un'etichetta, è possibile modificare la variabile SRCSRVCMD nel modo seguente:

**sd.exe-p% fnvar%(% var2%) Print-o% srcsrvtrg%-q% Depot%/%var3% @% label%**

## <a name="how-source-server-works"></a>Funzionamento del server di origine

Il client del server di origine viene implementato in Symsrv.dll. Il client non estrae informazioni direttamente dal file PDB. Usa un gestore di simboli, ad esempio quello implementato in Dbghelp.dll. Si tratta essenzialmente di un motore di sostituzione di variabili ricorsive che consente di creare una riga di comando che può essere utilizzata per estrarre il file di origine appropriato dal sistema di controllo del codice sorgente. Il codice non deve chiamare direttamente Symsrv.dll. Per integrare le funzionalità nell'applicazione, usare la funzione [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .

La prima versione del server di origine funziona nel modo seguente. Questo comportamento potrebbe cambiare nelle versioni future.

-   Il client chiama la funzione **SrcSrvInit** con il percorso di destinazione da utilizzare come base per tutte le estrazioni di file di origine. Questo percorso viene archiviato nella variabile es.
-   Il client estrae il flusso SrcSrv dal PDB quando viene caricato il PDB del modulo e chiama la funzione **SrcSrvLoadModule** per passare il blocco di dati al server di origine.
-   Quando dbghelp recupera un file di origine, il client chiama la funzione **SrcSrvGetFile** per recuperare i file di origine dal controllo del codice sorgente.
-   Il server di origine Cerca nel blocco di dati le voci del file di origine per una voce corrispondente al file richiesto. Inserisce VAR1 in VAR *n* con il contenuto della voce del file di origine. Espande quindi la variabile SRCSRVTRG usando VAR1 a VAR *n*. Se il file si trova già in questa posizione, restituisce il percorso al chiamante. In caso contrario, espande la variabile SRCSRVCMD per compilare il comando necessario per recuperare il file dal controllo del codice sorgente e copiarlo nel percorso di destinazione. Infine, viene eseguito questo comando.

## <a name="creating-a-source-control-provider-module"></a>Creazione di un modulo del provider del controllo del codice sorgente

Il server di origine include i moduli provider per Perforce (p4.pm) e Visual Source Safe (vss.pm). Per creare un modulo provider personalizzato, è necessario implementare il seguente set di interfacce.

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module:: SimpleUsage ()**
</dt> <dd>

Scopo: Visualizza informazioni semplici sull'utilizzo del modulo in STDOUT.

Parametri: nessuno

Valore restituito: None

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module:: VerboseUsage ()**
</dt> <dd>

Scopo: Visualizza informazioni dettagliate sull'utilizzo del modulo in STDOUT.

Parametri: nessuno

Valore restituito: None

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module:: New ( \@ CommandArguments)**
</dt> <dd>

Scopo: Inizializza un'istanza del modulo provider.

Parameters: tutti gli @ARGV argomenti che non sono stati riconosciuti da SSIndex. cmd come argomenti generali.

Valore restituito: riferimento che può essere usato nelle operazioni successive.

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation ($SourcePath, $ServerHashReference)**
</dt> <dd>

Scopo: consente al modulo di raccogliere le informazioni di indicizzazione dell'origine necessarie per la directory specificata dal parametro $SourcePath. Il modulo non presuppone che questa voce venga chiamata solo una volta per ogni istanza dell'oggetto, perché SSIndex. cmd può chiamarla più volte per percorsi diversi.

Parameters: (1) directory locale contenente l'origine da indicizzare. (2) riferimento a un hash contenente tutte le voci del file di Srcsrv.ini specificato.

Valore restituito: None

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo ($LocalFile)**
</dt> <dd>

Scopo: fornisce le informazioni necessarie per estrarre un singolo file specifico dal sistema di controllo del codice sorgente.

Parameters: un nome file completo

Valore restituito: (1) un riferimento hash delle variabili necessarie per interpretare il $FileEntry restituito. SSIndex. cmd memorizza nella cache queste variabili per ogni file di origine utilizzato da un singolo file di debug per ridurre la quantità di informazioni scritte nel flusso dell'indice di origine. (2) la voce del file da scrivere nel flusso dell'indice di origine per consentire SrcSrv.dll estrarre il file dal controllo del codice sorgente. Il formato esatto di questa riga è specifico del sistema di controllo del codice sorgente.

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**
</dt> <dd>

Scopo: fornisce una stringa descrittiva per identificare il provider del controllo del codice sorgente per l'utente finale.

Parametri: nessuno

Valore restituito: nome descrittivo del sistema di controllo del codice sorgente.

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**
</dt> <dd>

Scopo: consente al provider del controllo del codice sorgente di aggiungere variabili specifiche del controllo del codice sorgente al flusso di origine per ogni file di debug. I moduli di esempio usano questo metodo per scrivere le \_ variabili di destinazione Extract cmd ed Extract \_ .

Parametri: nessuno

Valore restituito: elenco di voci per le variabili del flusso di origine.

</dd> </dl>

 

 




