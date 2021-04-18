---
description: Il writer di test è un'utilità che è possibile usare per testare le applicazioni del richiedente VSS.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: Strumento writer di test VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ffdbb513697a701866be5ceeb40168e8c28368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307153"
---
# <a name="vss-test-writer-tool"></a>Strumento writer di test VSS

Il writer di test è un'utilità che è possibile usare per testare le applicazioni del richiedente VSS. Questo writer può essere configurato in modo da eseguire quasi tutte le azioni che possono essere eseguite da un VSS writer. Inoltre, il writer di test esegue verifiche estese per garantire che il richiedente abbia gestito correttamente le azioni del writer.

Ogni istanza del writer viene inizializzata con un file di configurazione XML che descrive esattamente quali componenti verranno segnalati dal writer e il comportamento del writer. Il writer può essere configurato in modo da creare report su vari tipi di scenari, tra cui scenari più complicati usando le interfacce incrementali e differenziali. Il writer eseguirà i controlli in vari punti durante il processo per garantire che il richiedente si comporterà in modo corretto. Al termine del ripristino, il writer verificherà che tutti i file necessari siano stati ripristinati senza danneggiamento. Il writer può anche essere configurato per eseguire altre operazioni, ad esempio eventi specifici non riusciti.

> [!Note]  
> Questo strumento è incluso in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive. È possibile scaricare il Windows SDK da [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

Nell'installazione di Windows SDK lo strumento VssSampleProvider si trova in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (per Windows a 64 bit) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Esecuzione dello strumento writer di test

Per avviare il writer di test, digitare quanto segue al prompt dei comandi:

 *File di configurazione* vswriter.exe

dove *config-file* è il percorso di un file di configurazione che specifica il comportamento di questo writer.

Per arrestare il writer di test, premere CTRL + C.

È possibile eseguire contemporaneamente più istanze del writer di test. Tuttavia, ogni istanza del writer restituirà lo stesso ID di classe Writer (anche se un ID istanza di writer diverso), pertanto i percorsi logici e i nomi dei componenti devono essere univoci in tutte le istanze in esecuzione simultanea del writer.

Per assicurarsi che il writer possa verificare correttamente che il richiedente abbia rispettato le specifiche del file di esclusione, tutti i file di cui è stato eseguito il backup devono essere eliminati dal volume originale prima di provare a ripristinarli. È consigliabile archiviare un modello di ogni scenario di writer, in modo che lo scenario possa essere facilmente ricreato.

## <a name="using-a-configuration-file"></a>Uso di un file di configurazione

Il file di configurazione di esempio seguente, vswriter \_config.xml, si trova in `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` su piattaforme x86 e `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` su piattaforme x64.

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

L'elemento radice in questo file di configurazione è denominato TestWriter. Tutti gli altri elementi sono disposti nell'elemento TestWriter.

Uno degli attributi associati a TestWriter è l'attributo Usage. Questo attributo specifica il tipo di utilizzo riportato tramite [**IVssExamineWriterMetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity). Uno dei possibili valori di questo attributo è costituito dai \_ dati utente.

Il primo elemento figlio dell'elemento radice deve essere sempre un elemento RestoreMethod. Questo elemento specifica quanto segue:

-   Metodo Restore (in questo caso, RESTOre \_ if \_ può \_ essere \_ sostituito)
-   Indica se il writer richiede eventi di ripristino (in questo caso, always)
-   Indica se è necessario riavviare il computer dopo il ripristino del writer, in questo caso no.

Questo elemento può facoltativamente specificare un mapping in un percorso alternativo. In questo caso non viene specificato alcun percorso alternativo.

Il secondo elemento figlio è un elemento ExcludeFile. Questo elemento fa sì che il writer escluda un file o un set di file dal backup.

Il terzo elemento figlio è un elemento Component. Questo elemento fa sì che il writer aggiunga un componente ai relativi metadati. Un elemento Component contiene gli attributi per descrivere il componente e gli elementi figlio per descrivere il contenuto del componente, ad esempio quanto segue:

-   componentType per indicare se si tratta di un filegroup o di un database
-   logicalPath per il percorso logico del componente
-   ComponentName per il nome del componente
-   selezionabile per indicare lo stato selezionabile per il backup

L'elemento Component dispone anche di un elemento figlio denominato ComponentFile per aggiungere una specifica del file a questo componente. Un elemento Component può avere un numero arbitrario di elementi ComponentFile che può essere specificato per ogni componente. Questo elemento ComponentFile ha gli attributi seguenti:

-   path = "c: \\ writerData \\ myFilesHere"
-   filespec = " \* "
-   ricorsivo = "No"

Sebbene il writer di test verifichi il comportamento del richiedente, non verifica che il file di configurazione mantenga sempre la semantica documentata per un writer. Sono disponibili molte operazioni che un writer ben funzionante non deve eseguire, ad esempio segnala lo stesso file in più componenti, ed è l'autore del file di configurazione XML per mantenere la semantica.

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
<td><span id="verbosity"></span><span id="VERBOSITY"></span>dettaglio<br/></td>
<td>Il writer stampa lo stato nella console mentre riceve gli eventi e li elabora. Il livello di dettaglio visualizzato viene specificato dall'attributo di dettaglio. È possibile scegliere tra tre livelli di dettaglio:<br/> <dl> <dt><span id="low"></span><span id="LOW"></span>basso</dt> <dd> Verranno stampati solo gli errori del writer o il comportamento errato del richiedente.<br/> </dd> <dt><span id="medium"></span><span id="MEDIUM"></span>media</dt> <dd> Tutti gli elementi a livello di dettaglio basso vengono stampati in aggiunta alle informazioni aggiuntive sullo stato, ad esempio quando vengono ricevuti gli eventi. Si tratta del livello predefinito.<br/> </dd> <dt><span id="high"></span><span id="HIGH"></span>alta</dt> <dd> Vengono restituite informazioni dettagliate sullo stato relative all'operazione del writer.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br/></td>
<td>Per eseguire una verifica aggiuntiva, impostare questo attributo su Sì per fare in modo che &quot; &quot; il writer elimini tutti i file immediatamente dopo la creazione della copia shadow del volume. Il richiedente deve quindi copiare i file dalla copia shadow, perché non esistono più nel volume originale. <br/>
<blockquote>
[!Note]<br />
Nel caso di writer Spit, i file vengono eliminati dal percorso originale dopo lo spiedo ma prima della creazione della copia shadow. Una volta creata la copia shadow, i file vengono eliminati dalla directory spit.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br/></td>
<td>Per eliminare i file parziali, impostare questo attributo su &quot; Sì &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br/></td>
<td>Per eliminare i file differenziati, impostare questo attributo su &quot; Sì &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br/></td>
<td>Impostare questo attributo su &quot; Sì per fare in modo &quot; che il writer verifichi che tutti i file di cui è stato eseguito il backup siano stati ripristinati in un percorso appropriato e che il file non sia danneggiato. Anche i file parziali e i file differenziati vengono gestiti correttamente.<br/></td>
</tr>
<tr class="even">
<td><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br/></td>
<td>Impostare questo attributo su &quot; Sì per fare in modo &quot; che il writer verifichi che i file corrispondenti a una specifica del file nell'elenco di esclusioni non vengano ripristinati. Per il corretto funzionamento, è necessario svuotare le directory di ripristino prima di eseguire il ripristino.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a>Specifica di mapping dei percorsi alternativi

Un mapping del percorso alternativo specifica un percorso in cui eseguire il ripristino se il metodo di ripristino è VSS \_ WRE \_ Restore \_ in un \_ \_ percorso alternativo o se il ripristino normale di un componente ha esito negativo. Un writer può segnalare i mapping dei percorsi alternativi al richiedente usando il metodo [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) . È possibile aggiungere mapping di percorsi alternativi al file di configurazione del writer di test aggiungendo sottoelementi AlternateLocationMapping all'elemento RestoreMethod.

Il seguente elemento RestoreMethod contiene un sottoelemento AlternateLocationMapping.

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

Questo esempio specifica che il richiedente deve prima tentare di ripristinare tutti i file corrispondenti a c: \\ files \\ \* . txt nella directory c: \\ files. Se uno di questi file non può essere sostituito, il richiedente deve ripristinare tutti i file nella directory c: \\ altfiles. Il richiedente deve salvare questo mapping del percorso alternativo usando il metodo [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) . Se il writer di test è configurato per verificare se i file sono stati ripristinati, verificherà anche se il richiedente ha chiamato **AddAlternativeLocationMapping**.

## <a name="specifying-files-to-be-excluded"></a>Specifica dei file da escludere

Ogni writer può specificare un elenco di specifiche di file che specificano i file per il richiedente da escludere dal backup. È possibile aggiungere queste specifiche del file al file di configurazione del writer di test aggiungendo sottoelementi ExcludeFile all'elemento radice TestWriter.

Di seguito è riportato un esempio di un sottoelemento ExcludeFile che esclude tutti i file nella directory C: \\ files che corrispondono a c: \\ temp \* . \* .

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Esecuzione del backup di writer Spit

Molti scrittori agiscono da "Spit Writers". Un writer Spit crea file intermedi, o "Spit file", in base a un set di file originale e inserisce i file Spit in un percorso alternativo in fase di backup. Il writer usa il metodo [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) per notificare al richiedente che deve eseguire il backup di questi file dal percorso alternativo. Tuttavia, questi file devono comunque essere ripristinati nel percorso attivo dei file originali. Il writer di test può essere configurato in modo da fungere da Writer Spit per una specifica specifica del file.

L'elemento ComponentFile seguente contiene un attributo alternatePath:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

In questo esempio il writer di test viene configurato per copiare tutti i file corrispondenti a c: \\ files \\ \* . txt nella directory c: \\ file \\ Spit immediatamente prima della creazione della copia shadow del volume. Il richiedente deve eseguire il backup dei file dalla directory c: \\ files \\ spit. Se il writer di test è configurato per eliminare i file, eliminerà i file originali prima della creazione della copia shadow, in modo che non vengano visualizzati nella \\ directory c: files del volume di copia shadow. In questo caso, i file in c: \\ file \\ Spit vengono eliminati dopo la creazione della copia shadow, quindi è necessario eseguirne il backup dalla directory c: \\ files \\ Spit nel volume della copia shadow.

## <a name="reporting-component-dependencies"></a>Dipendenze componente di report

I writer possono specificare una dipendenza tra un componente locale e un componente presente in un altro writer. Queste dipendenze vengono segnalate al richiedente usando [**IVssWMComponent:: getdependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). Il writer di test può essere configurato per segnalare queste dipendenze aggiungendo uno o più sottoelementi di dipendenza all'elemento Component.

L'elemento componente seguente contiene un sottoelemento Dependency:

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

La dipendenza viene specificata come attributi dell'elemento dependency. writerId è l'ID di classe del writer che contiene la destinazione della dipendenza, logicalPath è il percorso logico del componente in tale writer e ComponentName è il nome del componente. In questo caso, se il richiedente esegue il backup di "WriterComponent" nel writer corrente, deve eseguire anche il backup del componente "ComponentPath \\ Writer2Component" nel writer di destinazione.

> [!Note]  
> Il writer di test non esegue alcun controllo per garantire che le dipendenze siano rispettate.

 

## <a name="failing-events"></a>Eventi in errore

Il writer di test può essere configurato in modo da non riuscire agli eventi normali ricevuti da un writer. Questi eventi sono i seguenti:



| Event                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identificare<br/>                                     | Ricevuta come risposta a una chiamata [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) . In questo caso, il writer non verrà segnalato.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Ricevuta come risposta al richiedente che chiama [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | Ricevuto quando il richiedente chiama [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), ma prima della creazione della copia shadow.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Congelare<br/>                                             | Ricevuto immediatamente dopo [*PrepareForSnapshot*](vssgloss-p.md), ma ancora prima della creazione della copia shadow.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Sblocca<br/>                                                     | Ricevuto al termine della creazione della copia shadow.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot<br/>                     | Ricevuto dopo il completamento del disgelo, ma prima del completamento di [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Interruzione<br/>                                                 | Ricevuta se trascorre troppo tempo tra [*Freeze*](vssgloss-f.md) e [*scongela*](vssgloss-t.md) o se il richiedente chiama [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Ricevuto quando il richiedente viene chiuso. Gli errori non verranno mai segnalati.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>PreRestore<br/>                             | Ricevuto quando il richiedente chiama [**IVssBackupComponents::P Rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore<br/>                         | Ricevuto quando il richiedente chiama [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).<br/>                                                                                                                                         |



 

Questi errori vengono configurati aggiungendo uno o più sottoelementi FailEvent all'elemento radice TestWriter. Esistono due classi di errori che è possibile impostare: riprovabile e non reversibile. Gli errori rilevabili sono errori che possono scomparire se viene eseguito un nuovo tentativo di eseguire l'intero processo di backup, mentre gli errori non ripetibili sono improbabile. Il tipo di errore per l'evento viene scelto in base all'attributo retryable.

Di seguito è riportato un esempio di un errore non irreversibile di base:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

Questo esempio provocherà l'esito negativo del writer durante l'evento [*Freeze*](vssgloss-f.md) . [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) segnala l'errore del writer come VSS E WRITERERROR non può essere \_ \_ \_ ritentato.

Di seguito è riportato un esempio di errore irreversibile di base:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

In questo esempio il writer avrà esito negativo la prima due volte che riceve un evento [*Freeze*](vssgloss-f.md) . Dopo le prime due volte, il writer avrà sempre esito positivo. L'errore del writer segnalato tramite [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) sarà un codice di errore irreversibile casuale.

## <a name="declaring-supported-backup-types"></a>Dichiarazione dei tipi di backup supportati

I writer comunicano quali tipi di backup sono supportati tramite la chiamata di [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)del richiedente. L'elemento radice TestWriter contiene gli attributi per ogni tipo di backup per indicare il supporto. Questi attributi sono supportsCopy, supportsDifferential, supportsIncremental e supportsLog. Per indicare il supporto per un tipo di backup specifico, impostare l'attributo corrispondente su "Yes".

Se il richiedente imposta il tipo di backup su un tipo di backup non supportato dal writer, il writer noterà questo fatto durante [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), ma in caso contrario funzionerà correttamente.

## <a name="indicating-the-file-backup-type"></a>Che indica il tipo di backup del file

Il metodo [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) restituisce una maschera di maschera al richiedente che indica il modo in cui deve essere eseguito il backup di un file. Questa operazione indicherà se un file è obbligatorio o meno durante i tipi specifici di backup e anche se è necessaria una copia shadow durante i tipi specifici di backup. I tipi di backup in questa maschera di maschera sono descritti a una lunghezza maggiore nel [ruolo del richiedente del documento nel backup di archivi complessi](requestor-role-in-backing-up-complex-stores.md).

Nel writer di test, gli elementi della maschera di maschera vengono specificati impostando gli attributi in ogni elemento ComponentFile. Gli attributi fullBackupRequired, diffBackupRequired, incBackupRequired e logBackupRequired specificano quando deve essere eseguito il backup di un file. Gli attributi fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired e logSnapshotRequired specificano quando è necessario eseguire il backup di un file da una copia shadow di un volume e mai dal volume originale. Il valore predefinito per tutti questi valori è "Yes", che indica che un file deve essere sempre sottoposto a backup ed è necessario eseguirne il backup da una copia shadow di un volume.

## <a name="adding-partial-files"></a>Aggiunta di file parziali

Durante l'elaborazione di [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), un writer ha la possibilità di aggiungere file parziali a ogni componente. Questi file parziali vengono segnalati con [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). Il writer di test può essere configurato per aggiungere file parziali specificando sottoelementi PartialFile in un elemento Component.

Di seguito è riportato un esempio di elemento Component con due sottoelementi PartialFile:

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

Solo i file parziali che corrispondono parzialmente a un ComponentFile esistente (come nel primo file parziale nell'esempio) o i nuovi file parziali che si trovano nello stesso volume di un ComponentFile esistente (come nel secondo file parziale) devono essere specificati in questo modo. Per questo componente, il richiedente deve eseguire il backup completo di tutti i file corrispondenti a c: \\ files \\ \* . txt, ad eccezione di partial.txt. Il richiedente deve quindi eseguire il backup degli intervalli specificati (dove un intervallo è un offset seguito da una lunghezza) per i file c: \\ file \\partial.txt e c: \\ files2 \\partial.txt.

Se il writer è configurato per controllare i ripristini dei file, al momento del ripristino verranno controllati solo gli intervalli di backup del file parziale. Le modifiche apportate ad altre parti del file non vengono rilevate. Se l'attributo deletePartialFiles dell'elemento radice TestWriter è impostato, i file parziali vengono eliminati dal volume originale immediatamente dopo la creazione della copia shadow.

## <a name="adding-differenced-files"></a>Aggiunta di file differenziati

Durante l'elaborazione di [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), un writer può aggiungere file differenziati a ogni componente. Questi file differenziati vengono segnalati con [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Il writer di test può essere configurato per aggiungere file differenziati specificando sottoelementi DifferencedFile in un elemento Component.

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

Diversamente dai file parziali, i file differenziati non devono mai corrispondere parzialmente a una specifica ComponentFile. La specifica del file in un elemento DifferencedFile deve corrispondere esattamente a un ComponentFile (come nel primo file differenziato nell'esempio) o non deve corrispondere a tutti, ma deve trovarsi in un volume a cui si fa riferimento in un ComponentFile (come nel secondo file differenziato). I valori di data e ora devono essere relativi al fuso orario locale, ma verranno convertiti in GMT prima di essere segnalati al richiedente. Nell'esempio, verrà eseguito il backup solo dei file corrispondenti a c: \\ file \\ \* . txt o c: \\ files2 \\ \* . txt che sono stati modificati dopo il 1/22/2003:12:44:17.

Se il writer di test è configurato per controllare i ripristini dei file, verranno controllati solo i file modificati per il ripristino. Se l'attributo deleteDifferencedFiles dell'elemento radice TestWriter è impostato, i file differenziati vengono eliminati dal volume originale immediatamente dopo la creazione della copia shadow.

## <a name="new-targets"></a>Nuove destinazioni

Alcuni writer consentono al richiedente di informarli che è stata scelta una nuova località per il ripristino di determinati file. Il writer indica che supporta questa modalità come parte della maschera di maschera restituita da [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Per impostazione predefinita, il writer di test supporta sempre le nuove destinazioni. Questo supporto può essere disabilitato impostando l'attributo supportsNewTarget nell'elemento radice TestWriter su "No".

Se un writer supporta nuove destinazioni, il richiedente può informare il writer di nuove destinazioni chiamando [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget). Il writer verificherà quindi il nuovo percorso di destinazione per verificare il ripristino anziché il percorso originale.

## <a name="more-information"></a>Altre informazioni

Il writer di test supporta più opzioni di configurazione che non sono descritte qui. Lo schema completo per tutte le funzionalità di configurazione del writer di test viene specificato in swriter.xml in `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (per Windows a 64 bit) e `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (per windows a 32 bit). Questo file contiene un XML Schema che descrive completamente tutti gli elementi e gli attributi che costituiscono un file di configurazione. Ogni elemento e ogni attributo in questo file viene commentato con una descrizione che documenta l'uso dell'elemento o dell'attributo.

 

 




