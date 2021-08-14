---
description: Il writer di test è un'utilità che è possibile usare per testare le applicazioni richiedente vss.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: Strumento VSS Test Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93f0b81bd5e27db9fdfb70ca52e6f43bbb1e853af87bc12e1d76f01d7966ef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344234"
---
# <a name="vss-test-writer-tool"></a>Strumento VSS Test Writer

Il writer di test è un'utilità che è possibile usare per testare le applicazioni richiedente vss. Questo writer può essere configurato per eseguire quasi tutte le azioni che un VSS writer può eseguire. Inoltre, il writer di test esegue controlli approfonditi per garantire che il richiedente abbia gestito correttamente queste azioni del writer.

Ogni istanza del writer viene inizializzata con un file di configurazione XML che descrive esattamente i componenti su cui il writer reporterà e il comportamento del writer. Il writer può essere configurato per creare report su vari tipi di scenari, inclusi scenari più complessi che usano le interfacce incrementali e differenziali. Il writer eseguirà controlli in vari punti durante il processo per garantire che il richiedente si comporti in modo corretto. Al termine del ripristino, il writer verifica che tutti i file necessari siano stati ripristinati senza danneggiamento. Il writer può anche essere configurato per eseguire altre operazioni, ad esempio l'esito negativo di eventi specifici.

> [!Note]  
> Questo strumento è incluso in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive. È possibile scaricare l'SDK Windows da [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

Nell'installazione Windows SDK di , lo strumento VssSampleProvider è disponibile in (per i Windows `%Program Files(x86)%\Windows Kits\8.1\bin\x64` a 64 bit) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Esecuzione dello strumento Di scrittura test

Per avviare Test Writer, digitare quanto segue al prompt dei comandi:

**vswriter.exe** *config-file*

dove *config-file* è il percorso di un file di configurazione che specifica il comportamento di questo writer.

Per arrestare Test Writer, premere CTRL+C.

È possibile eseguire più istanze del writer di test contemporaneamente. Tuttavia, ogni istanza del writer segnala lo stesso ID di classe del writer (anche se un ID istanza del writer diverso), pertanto i percorsi logici e i nomi dei componenti devono essere univoci in tutte le istanze del writer in esecuzione simultanea.

Per assicurarsi che il writer possa verificare correttamente che il richiedente abbia rispettato le specifiche di file di esclusione, tutti i file di cui è stato eseguito il backup devono essere eliminati dal volume originale prima di tentare di ripristinarli. È consigliabile archiviare un modello di ogni scenario di scrittura, in modo che lo scenario possa essere facilmente ricreato.

## <a name="using-a-configuration-file"></a>Uso di un file di configurazione

Il file di configurazione di esempio seguente, vswriterconfig.xml, è disponibile in nelle piattaforme \_ `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` x86 e `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` x64.

``` syntax
<TestWriter usage="USER_DATA">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED"
                   writerRestore="always"
                   rebootRequired="no" />

    <ExcludeFile path="c:\writerData\notTheseFiles" 
                 filespec="excludeThisFile.txt" 
                 recursive="no"/>

    <Component componentType="filegroup"
               componentName="TestFiles">
        <ComponentFile path="c:\writerData\myFilesHere" 
                       filespec="*"
                       recursive="no" />
    </Component>

</TestWriter>
```

L'elemento radice in questo file di configurazione è denominato TestWriter. Tutti gli altri elementi sono disposti sotto l'elemento TestWriter.

Uno degli attributi associati a TestWriter è l'attributo di utilizzo. Questo attributo specifica il tipo di utilizzo segnalato tramite [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity). Uno dei valori possibili per questo attributo è USER \_ DATA.

Il primo elemento figlio dell'elemento radice deve essere sempre un elemento RestoreMethod. Questo elemento specifica quanto segue:

-   Il metodo di ripristino (in questo caso, RESTORE \_ IF \_ CAN BE \_ \_ REPLACED)
-   Se il writer richiede eventi di ripristino (in questo caso, sempre)
-   Se è necessario un riavvio dopo il ripristino del writer (in questo caso, no)

Questo elemento può specificare facoltativamente un mapping di percorso alternativo. In questo caso, non viene specificata alcuna posizione alternativa.

Il secondo elemento figlio è un elemento ExcludeFile. Questo elemento fa in modo che il writer escludi un file o un set di file dal backup.

Il terzo elemento figlio è un elemento Component. Questo elemento fa sì che il writer abiliti un componente ai relativi metadati. Un elemento Component contiene attributi che descrivono il componente e gli elementi figlio per descrivere il contenuto del componente, ad esempio:

-   componentType per indicare se si tratta di un filegroup o di un database
-   logicalPath per il percorso logico del componente
-   componentName per il nome del componente
-   selezionabile per indicare lo stato selectable-for-backup

L'elemento Component include anche un elemento figlio denominato ComponentFile per aggiungere una specifica di file a questo componente. Un elemento Component può avere un numero arbitrario di elementi ComponentFile che possono essere specificati per ogni componente. Questo elemento ComponentFile ha gli attributi seguenti:

-   path="c: \\ writerData \\ myFilesHere"
-   filespec=" \* "
-   recursive="no"

Sebbene il writer di test verifichi il comportamento del richiedente, non verifica che il file di configurazione mantenga sempre la semantica documentata per un writer. Esistono molte operazioni che un writer ben comportato non deve eseguire (ad esempio, segnalare lo stesso file in più componenti) ed è l'autore del file di configurazione XML a mantenere questa semantica.

## <a name="configuring-writer-attributes"></a>Configurazione degli attributi del writer

L'elemento radice TestWriter contiene attributi che determinano vari comportamenti del writer. Di seguito sono riportati alcuni dei comportamenti che è possibile modificare:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="verbosity"></span><span id="VERBOSITY"></span>Dettaglio<br/></td>
<td>Il writer stampa lo stato nella console quando riceve gli eventi e li elabora. Il livello di dettaglio visualizzato viene specificato dall'attributo verbosity. È possibile scegliere tra tre livelli di dettaglio:<br/> <dl> <dt><span id="low"></span><span id="LOW"></span>Basso</dt> <dd> Verranno stampati solo gli errori nel writer o un comportamento non corretto del richiedente.<br/> </dd> <dt><span id="medium"></span><span id="MEDIUM"></span>Medio</dt> <dd> Tutti gli elementi con livello di dettaglio basso vengono stampati oltre a informazioni aggiuntive sullo stato, ad esempio quando vengono ricevuti gli eventi. Si tratta del livello predefinito.<br/> </dd> <dt><span id="high"></span><span id="HIGH"></span>alto</dt> <dd> Vengono segnalate informazioni dettagliate sullo stato dell'operazione del writer.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br/></td>
<td>Per eseguire una verifica aggiuntiva, impostare questo attributo su sì per fare in modo che il writer elimini tutti i relativi file immediatamente dopo la creazione della &quot; &quot; copia shadow del volume. Il richiedente deve quindi copiare i file dalla copia shadow, perché non esistono più nel volume originale. <br/>
<blockquote>
[!Note]<br />
Nel caso di writer di writer, i file vengono eliminati dal percorso originale dopo l'operazione di copia shadow, ma prima della creazione della copia shadow. Dopo aver creato la copia shadow, i file vengono eliminati dalla directory dei file.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br/></td>
<td>Per eliminare file parziali, impostare questo attributo su &quot; yes &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br/></td>
<td>Per eliminare i file con differenze, impostare questo attributo su &quot; yes &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br/></td>
<td>Impostare questo attributo su sì per fare in modo che il writer controlli che ogni file di cui è stato eseguito il backup sia stato ripristinato in un percorso appropriato e che il &quot; file non sia stato &quot; danneggiato. Anche i file parziali e i file con differenze vengono gestiti correttamente.<br/></td>
</tr>
<tr class="even">
<td><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br/></td>
<td>Impostare questo attributo su sì per fare in modo che il writer controlli che i file corrispondenti a una &quot; &quot; specifica di file nell'elenco di esclusione non vengono ripristinati. Per il corretto funzionamento, le directory di ripristino devono essere svuotate prima del ripristino.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a>Specifica di mapping di percorsi alternativi

Un mapping di percorso alternativo specifica un percorso in cui eseguire il ripristino se il metodo di ripristino è VSS WRE RESTORE TO ALTERNATE LOCATION o se il ripristino normale \_ di un componente non \_ \_ \_ \_ riesce. Un writer può segnalare i mapping del percorso alternativo al richiedente usando il metodo [**IVssExamineWriterMetadata::GetAlternateLocationMapping.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) È possibile aggiungere mapping di percorsi alternativi al file di configurazione del writer di test aggiungendo sottoelementi AlternateLocationMapping all'elemento RestoreMethod.

L'elemento RestoreMethod seguente contiene un sottoelemento AlternateLocationMapping.

``` syntax
<RestoreMethod method="RESTORE_IF_CAN_REPLACE"
              writerRestore="always"
              rebootRequired="no">
    <AlternateLocationMapping path="c:\files"
                              filespec="*.txt"
                              recursive="no"
                              alternatePath="c:\altfiles"/>
</RestoreMethod>
```

Questo esempio specifica che il richiedente deve prima tentare di ripristinare tutti i file corrispondenti ai file c:.txt \\ \\ \* nella directory \\ c: files. Se uno di questi file non può essere sostituito, il richiedente deve ripristinare tutti i file nella directory c: \\ altfiles. Il richiedente deve salvare il mapping del percorso alternativo usando il metodo [**IVssBackupComponents::AddAlternativeLocationMapping.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) Se test writer è configurato per controllare se i file sono stati ripristinati, controlla anche se il richiedente ha chiamato **AddAlternativeLocationMapping.**

## <a name="specifying-files-to-be-excluded"></a>Specifica dei file da escludere

Ogni writer può specificare un elenco di specifiche di file che specificano i file che il richiedente deve escludere dal backup. È possibile aggiungere queste specifiche di file al file di configurazione del writer di test aggiungendo sottoelementi ExcludeFile all'elemento radice TestWriter.

Di seguito è riportato un esempio di sottoelemento ExcludeFile che esclude tutti i file nella directory C: files che corrispondono a \\ C: temp \\ \* \* .

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Backup di writer di writer

Molti writer fungono da "writer writer". Un writer crea file intermedi, o "file di archivio", in base a un set originale di file e inserisce i file in un percorso alternativo in fase di backup. Il writer usa il [**metodo IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) per notificare al richiedente che deve eseguire il backup di questi file dal percorso alternativo. Tuttavia, questi file devono comunque essere ripristinati nel percorso attivo dei file originali. Test Writer può essere configurato in modo da fungere da writer per una specifica di file specifica specifica.

L'elemento ComponentFile seguente contiene un attributo alternatePath:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

In questo esempio viene configurato Test Writer per copiare tutti i file corrispondenti a c:.txt nella \\ \\ \* directory c:files\backup immediatamente prima della creazione della \\ copia shadow del \\ volume. Il richiedente deve eseguire il backup dei file dalla \\ directory c:\files\ \\ Se Test Writer è configurato per eliminare i file, elimina i file originali prima della creazione della copia shadow, in modo che non vengano visualizzati nella directory c: files nel \\ volume della copia shadow. In questo caso, i file in c:\file\backup vengono eliminati dopo la creazione della copia shadow, quindi è necessario eseguire il backup dalla \\ \\ directory \\ c:\files\backup nel volume \\ della copia shadow.

## <a name="reporting-component-dependencies"></a>Creazione di report sulle dipendenze dei componenti

I writer possono specificare una dipendenza tra un componente locale e un componente presente in un altro writer. Queste dipendenze vengono segnalate al richiedente [**usando IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). È possibile configurare Test Writer per segnalare queste dipendenze aggiungendo uno o più sottoelementi Dependency all'elemento Component.

L'elemento Component seguente contiene un sottoelemento Dependency:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
         <Dependency writerId="<GUID of target writer>"
                     logicalPath="ComponentPath"
                     componentName="Writer2Component" />
    </Component>
```

La dipendenza viene specificata come attributi dell'elemento Dependency. writerId è l'ID classe del writer contenente la destinazione della dipendenza, logicalPath è il percorso logico del componente in tale writer e componentName è il nome del componente. In questo caso, se il richiedente sta eseguire il backup di "WriterComponent" nel writer corrente, deve eseguire anche il backup del componente "ComponentPath \\ Writer2Component" nel writer di destinazione.

> [!Note]  
> Test Writer non esegue alcun controllo per assicurarsi che le dipendenze siano rispettate.

 

## <a name="failing-events"></a>Eventi con esito negativo

Il writer di test può essere configurato in modo da non riuscire a uno qualsiasi degli eventi normali ricevuti da un writer. Questi eventi sono i seguenti:



| Event                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identificare<br/>                                     | Ricevuto come risposta a una [**chiamata IVssBackupComponents::GatherWriterMetadata.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) L'errore in questo caso causerà la mancata notifica del writer.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Ricevuto come risposta al richiedente che chiama [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | Ricevuto quando il richiedente chiama [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), ma prima della creazione della copia shadow.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Congelare<br/>                                             | Ricevuto immediatamente dopo [*PrepareForSnapshot,*](vssgloss-p.md)ma ancora prima della creazione della copia shadow.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Disgelo<br/>                                                     | Ricevuto al termine della creazione della copia shadow.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot<br/>                     | Ricevuto dopo il completamento di Thaw, ma prima del completamento [**di IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Interrompere<br/>                                                 | Ricevuto se è trascorso troppo tempo tra [*Freeze*](vssgloss-f.md) e [*Thaw*](vssgloss-t.md) o se il richiedente chiama [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Ricevuto alla chiusura del richiedente. Gli errori non verranno mai segnalati.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>PreRestore<br/>                             | Ricevuto quando il richiedente chiama [**IVssBackupComponents::P restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore<br/>                         | Ricevuto quando il richiedente chiama [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).<br/>                                                                                                                                         |



 

Questi errori vengono configurati aggiungendo uno o più sottoelementi FailEvent all'elemento radice TestWriter. È possibile impostare due classi di errori: riprovabile e non ripetibile. Gli errori che possono essere ripetuti sono errori che possono scomparire se viene ripetuto l'intero processo di backup, mentre è improbabile che gli errori non ripetibili scompaiano. Il tipo di errore per l'evento viene scelto in base all'attributo retryable.

Di seguito è riportato un esempio di errore di base non ripetibile:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

In questo esempio il writer avrà esito negativo durante [*l'evento Freeze.*](vssgloss-f.md) [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) segnala che l'errore del writer è VSS \_ E \_ WRITERERROR \_ NONRETRYABLE.

Di seguito è riportato un esempio di errore di base che è possibile ripetere:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

In questo esempio il writer avrà esito negativo le prime due volte che riceve un [*evento Freeze.*](vssgloss-f.md) Dopo le prime due volte, il writer avrà sempre esito positivo. L'errore del writer segnalato tramite [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) sarà un codice di errore casuale che è possibile ripetere.

## <a name="declaring-supported-backup-types"></a>Dichiarazione dei tipi di backup supportati

I writer comunicano quali tipi di backup sono supportati tramite la chiamata [**IVssExamineWriterMetadata::GetBackupSchema del richiedente.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) L'elemento radice TestWriter contiene attributi per ogni tipo di backup per indicare il supporto. Questi attributi sono supportsCopy, supportsDifferential, supportsIncremental e supportsLog. Per indicare il supporto per un particolare tipo di backup, impostare l'attributo corrispondente su "sì".

Se il richiedente imposta il tipo di backup su un tipo di backup non supportato dal writer, il writer noterà questo fatto durante [**PrepareForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)ma in caso contrario funzionerà correttamente.

## <a name="indicating-the-file-backup-type"></a>Indicazione del tipo di backup file

Il [**metodo IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) restituisce una maschera di bit al richiedente che indica come eseguire il backup di un file. Ciò indicherà se un file è obbligatorio o meno durante tipi specifici di backup e anche se è necessaria una copia shadow durante tipi specifici di backup. I tipi di backup in questa maschera di bit sono illustrati più a lungo nel documento Ruolo richiedente [in Backup di archivi complessi](requestor-role-in-backing-up-complex-stores.md).

In Test Writer gli elementi di questa maschera di bit vengono specificati impostando gli attributi in ogni elemento ComponentFile. Gli attributi fullBackupRequired, diffBackupRequired, incBackupRequired e logBackupRequired specificano quando è necessario eseguire il backup di un file. Gli attributi fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired e logSnapshotRequired specificano quando è necessario eseguire il backup di un file da una copia shadow di un volume (e mai dal volume originale). L'impostazione predefinita per tutti questi valori è "sì", a indicare che è sempre necessario eseguire il backup di un file e di eseguire il backup da una copia shadow di un volume.

## <a name="adding-partial-files"></a>Aggiunta di file parziali

Durante l'elaborazione [**di DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)un writer ha la possibilità di aggiungere file parziali a ogni componente. Questi file parziali vengono segnalati tramite [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). Il writer di test può essere configurato per aggiungere file parziali specificando sottoelementi PartialFile in un elemento Component.

Di seguito è riportato un esempio di un elemento Component con due sottoelementi PartialFile:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <PartialFile path="c:\files"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
        <PartialFile path="c:\files2"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
    </Component>
```

In questo modo devono essere specificati solo i file parziali che corrispondono parzialmente a un ComponentFile esistente (come nel primo file parziale nell'esempio) o i nuovi file parziali che si trovano nello stesso volume di un ComponentFile esistente (come nel secondo file parziale). Per questo componente, il richiedente deve eseguire il backup completo di tutti i file corrispondenti a c:.txt ad eccezione di \\ \\ \* partial.txt. Il richiedente deve quindi eseguire il backup degli intervalli specificati (dove un intervallo è un offset seguito da una lunghezza) per i file c: \\ files \\partial.txt e c: \\ files2 \\partial.txt.

Se il writer è configurato per controllare i ripristini dei file, verranno controllati solo gli intervalli di backup del file parziale in fase di ripristino. Le modifiche ad altre parti del file non verranno visualizzate. Se l'attributo deletePartialFiles dell'elemento radice TestWriter è impostato, i file parziali vengono eliminati dal volume originale immediatamente dopo la creazione della copia shadow.

## <a name="adding-differenced-files"></a>Aggiunta di file con differenze

Durante l'elaborazione [**di DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)un writer può aggiungere file con differenze a ogni componente. Questi file con differenze vengono segnalati tramite [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). È possibile configurare Test Writer per aggiungere file con differenze specificando sottoelementi DifferencedFile in un elemento Component.

Di seguito è riportato un esempio di elemento Component con due sottoelementi DifferencedFile:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <DifferencedFile path="c:\files"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
        <DifferencedFile path="c:\files2"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
    </Component>
```

A differenza dei file parziali, i file con differenze non devono mai corrispondere parzialmente a una specifica ComponentFile. La specifica del file in un elemento DifferencedFile deve corrispondere esattamente a un elemento ComponentFile (come nel primo file con differenze nell'esempio) o non deve corrispondere affatto a tale elemento, ma deve essere in un volume a cui viene fatto riferimento in ComponentFile (come nel secondo file con differenze). I valori di data e ora devono essere relativi al fuso orario locale, ma verranno convertiti in GMT prima di essere segnalati al richiedente. Nell'esempio verrà eseguito il backup solo dei file corrispondenti a c: files.txt o c: files2.txt che sono stati modificati dal \\ \\ \* \\ \\ \* 22/1/01/2003:12:44:17.

Se Test Writer è configurato per controllare i ripristini dei file, verrà verificata la presenza di ripristini solo per i file modificati. Se l'attributo deleteDifferencedFiles dell'elemento radice TestWriter è impostato, i file con differenze vengono eliminati dal volume originale immediatamente dopo la creazione della copia shadow.

## <a name="new-targets"></a>Nuove destinazioni

Alcuni writer consentono al richiedente di informarli che è stato scelto un nuovo percorso in cui ripristinare determinati file. Il writer indica che supporta questa modalità come parte della maschera di bit restituita da [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Per impostazione predefinita, test writer supporta sempre nuove destinazioni. Questo supporto può essere disabilitato impostando l'attributo supportsNewTarget nell'elemento radice TestWriter su "no".

Se un writer supporta nuove destinazioni, il richiedente può informare il writer delle nuove destinazioni chiamando [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget). Il writer verificherà quindi il nuovo percorso di destinazione per verificare il ripristino anziché il percorso originale.

## <a name="more-information"></a>Altre informazioni

Test Writer supporta altre opzioni di configurazione non descritte qui. Lo schema completo per tutte le funzionalità di configurazione del test writer è specificato in swriter.xml in (per il Windows a 64 bit) e (per le Windows `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` a 32 bit). Questo file contiene uno schema XML che descrive completamente tutti gli elementi e gli attributi che costituiscono un file di configurazione. Ogni elemento e ogni attributo in questo file è commentato con una descrizione che documenta l'uso dell'elemento o dell'attributo.

 

 




