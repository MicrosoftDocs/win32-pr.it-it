---
description: Il test è un richiedente del servizio Copia Shadow del volume che verifica le operazioni avanzate di backup e ripristino.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Strumento di test
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885413"
---
# <a name="betest-tool"></a>Strumento di test

Il test è un richiedente del servizio Copia Shadow del volume che verifica le operazioni avanzate di backup e ripristino. Questo strumento può essere utilizzato per verificare l'utilizzo di un'applicazione di funzionalità VSS complesse, come le seguenti:

-   Backup incrementale e differenziale
-   Opzioni di ripristino complesse, ad esempio ripristino autorevole
-   Opzioni di rollforward

> [!Note]  
> L'attività di testing è inclusa in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive. VSS 7,2 SDK include una versione di test che viene eseguita solo in Windows Server 2003. Questo argomento descrive la versione Windows SDK di test, non la versione di Windows Server 2003 inclusa in VSS 7,2 SDK. Per informazioni sul download del Windows SDK e di VSS 7,2 SDK, vedere [servizio Copia Shadow del volume](volume-shadow-copy-service-portal.md).

 

Nell'installazione di Windows SDK, lo strumento di testing si trova in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (per Windows a 64 bit) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (per windows a 32 bit).

## <a name="running-the-betest-tool"></a>Esecuzione dello strumento di testing

Per eseguire lo strumento di test dalla riga di comando, usare la sintassi seguente:

Esegui **test** della *riga di comando-Opzioni*

Nell'esempio di utilizzo riportato di seguito viene illustrato come utilizzare lo strumento di testing insieme allo [strumento VSS writer di test](vss-test-writer-tool.md), che è un VSS writer.

**Esempio di utilizzo dello strumento di test**

1.  Creare una directory di test denominata C: \\ Comtest. Copiare i file seguenti in questa directory:
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  Creare una directory denominata C: \\ TestPath. Inserire alcuni file di dati di test in questa directory.
3.  Creare una directory denominata C: \\ BackupDestination. Lasciare vuota questa directory.
4.  Aprire due finestre dei comandi con privilegi elevati e impostare la directory di lavoro in ogni per C: eseguire un \\ test.
5.  Nella prima finestra di comando avviare lo [strumento VSS writer di test](vss-test-writer-tool.md) come segue:

    **vswriter.exe VswriterSample.xml**

    Il file vswriterSample.xml configura lo strumento vswriter (VSS test writer Tool) per segnalare il contenuto della directory c: \\ TestPath in preparazione per un'operazione di backup. Si noti che lo strumento VSS writer di test non produrrà l'output fino a quando non rileva l'attività da un richiedente, ad esempio un test. Per arrestare lo strumento VSS writer di test, premere CTRL + C.

6.  Nella seconda finestra di comando usare lo strumento di test per eseguire un'operazione di backup, come indicato di seguito:

    **betest.exe/B/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**

    Il test eseguirà il backup dei file dalla directory C: \\ TestPath alla directory c: \\ BackupDestination. Il documento del componente di backup verrà salvato in C: \\backup.xml di test \\ .

7.  Se l'operazione di backup ha esito positivo, eliminare il contenuto della \\ directory C: TestPath e utilizzare lo strumento di test per eseguire un'operazione di ripristino come segue:

    **betest.exe/R/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>Opzioni di Command-Line dello strumento di test

Lo strumento di test usa le seguenti opzioni della riga di comando per identificare le attività da eseguire.

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

Esegue un'operazione di ripristino autorevole per Active Directory o Active Directory Application Mode.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_B"></span><span id="_b"></span>**/B**
</dt> <dd>

Esegue un'operazione di backup ma non esegue un ripristino.

</dd> <dt>

<span id="_BC"></span><span id="_bc"></span>**/BC**
</dt> <dd>

Esegue solo l'operazione di completamento del backup.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span> *Nome file* /c
</dt> <dd>

> [!Note]  
> Questa opzione della riga di comando viene fornita solo per compatibilità con le versioni precedenti. Usare invece l'opzione della riga di comando **/x** .

 

Seleziona i componenti di cui eseguire il backup o il ripristino in base al contenuto del file di configurazione specificato da *filename*. Questo file deve contenere solo caratteri ANSI nell'intervallo compreso tra 0 e 127 e non deve essere maggiore di 1 MB. Ogni riga nel file deve usare il formato seguente:

*WriterId* : *ComponentName*;

Dove *WriterId* è l'ID del writer e *ComponentName* è il nome di uno dei componenti del writer. I nomi di ID e componente del writer devono essere racchiusi tra virgolette e devono essere presenti spazi prima e dopo i due punti (:). Se vengono specificati due o più componenti, devono essere separati da virgole. Ad esempio:

"5affb034-969f-4919-8875-88f830d0ef89": "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *percorso*
</dt> <dd>

Salvare i file di cui è stato eseguito il backup in o ripristinarli dalla directory di backup specificata da *path*.

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NBC**
</dt> <dd>

Omette l'operazione di completamento del backup.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/O**
</dt> <dd>

Specifica che il backup include uno stato del sistema di avvio.

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/P**
</dt> <dd>

Crea una copia shadow permanente.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Nome file* /pre
</dt> <dd>

Se il tipo di backup specificato nell'opzione della riga di comando **/t** è incrementale o differenziale, impostare il documento di backup sul file specificato da *filename* per il backup completo o incrementale precedente.

**Windows Server 2003 e Windows XP:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/R**
</dt> <dd>

Esegue il ripristino, ma non esegue il backup. Deve essere usato in combinazione con l'opzione della riga di comando **/s** .

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

Crea una copia shadow che può essere utilizzata per il rollback dell'applicazione.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *nomefile*
</dt> <dd>

In caso di backup, Salva il documento di backup nel file specificato da *filename*. In caso di ripristino, carica il documento di backup da questo file.

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

Crea una copia shadow del volume, ma non esegue il backup o il ripristino.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

Arresta il test quando viene rilevato il primo errore del writer.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*
</dt> <dd>

Specifica il tipo di backup. *BackupType* può essere pieno, log, copia, incrementale o differenziale. Per ulteriori informazioni sui tipi di backup, [**vedere \_ \_ tipo di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/V**
</dt> <dd>

Genera un output dettagliato che può essere utilizzato per la risoluzione dei problemi.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *nomefile*
</dt> <dd>

Seleziona i componenti di cui eseguire il backup o il ripristino in base al contenuto del file di configurazione XML specificato da *filename*. Questo file deve contenere solo caratteri ANSI nell'intervallo compreso tra 0 e 127. Il formato del file XML viene definito dallo schema nel file di BETest.xml. Per un file di configurazione di esempio, vedere BetestSample.xml. Entrambi questi file si trovano nella directory vsstools

> [!Note]  
> È possibile visualizzare il file di BETest.xml in Internet Explorer. Prima di aprire il file, assicurarsi che il file XDR-Schema. xsl si trovi nella stessa directory BETest.xml. Il file XDR-Schema. xsl contiene istruzioni per il rendering che rendono più leggibile il file di BETest.xml.

 

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>File di configurazione XML di esempio: BetestSample.xml

Il file di configurazione di esempio seguente, BetestSample.xml, si trova nella directory Vsstools

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

Questo esempio di un semplice file di configurazione seleziona un componente di cui eseguire il backup o il ripristino.

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>File di configurazione XML di esempio: VswriterSample.xml

Il file di configurazione di esempio seguente, VswriterSample.xml, si trova nella directory Vsstools

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

L'elemento radice in questo file di configurazione è denominato TestWriter. Tutti gli altri elementi sono disposti nell'elemento TestWriter.

Il primo attributo associato a TestWriter è l'attributo Usage. Questo attributo specifica il tipo di utilizzo riportato tramite il metodo [**IVssExamineWriterMetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) . Uno dei possibili valori di questo attributo è costituito dai \_ dati utente.

Il secondo attributo è l'attributo deleteFiles. Questo attributo è descritto in [configurazione degli attributi del writer](vss-test-writer-tool.md).

Il primo elemento figlio dell'elemento radice è un elemento RestoreMethod. Questo elemento specifica quanto segue:

-   Metodo Restore (in questo caso, RESTOre \_ if \_ può \_ essere \_ sostituito)
-   Indica se il writer richiede eventi di ripristino (in questo caso, always)
-   Indica se è necessario riavviare il computer dopo il ripristino del writer, in questo caso no.

Questo elemento può facoltativamente specificare un mapping in un percorso alternativo. In questo caso non viene specificato alcun percorso alternativo. Per ulteriori informazioni, vedere [specifica di mapping dei percorsi alternativi](vss-test-writer-tool.md).

Il secondo elemento figlio è un elemento Component. Questo elemento fa sì che il writer aggiunga un componente ai relativi metadati. Un elemento Component contiene gli attributi per descrivere il componente e gli elementi figlio per descrivere il contenuto del componente, ad esempio quanto segue:

-   componentType per indicare se si tratta di un filegroup o di un database, in questo caso un filegroup
-   logicalPath per il percorso logico del componente (in questo caso, non è specificato alcun valore)
-   ComponentName per il nome del componente (in questo caso, "TestFiles")
-   selezionabile per indicare lo stato selezionabile per il backup

L'elemento Component dispone anche di un elemento figlio denominato ComponentFile per aggiungere una specifica del file a questo componente. Un elemento Component può avere un numero arbitrario di elementi ComponentFile che può essere specificato per ogni componente. Questo elemento ComponentFile ha gli attributi seguenti:

-   path = "c: \\ TestPath"
-   filespec = " \* "
-   ricorsivo = "No"

 

 



