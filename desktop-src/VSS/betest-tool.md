---
description: BETest è un richiedente VSS che testa le operazioni avanzate di backup e ripristino.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Strumento BETest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f37e8bfc224061a8205bf0759cbba4798b0d53227e4f12d89b1e9ddf629d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471151"
---
# <a name="betest-tool"></a>Strumento BETest

BETest è un richiedente VSS che testa le operazioni avanzate di backup e ripristino. Questo strumento può essere usato per testare l'uso di funzionalità vss complesse di un'applicazione, ad esempio le seguenti:

-   Backup incrementale e differenziale
-   Opzioni di ripristino complesse, ad esempio il ripristino autorevole
-   Opzioni rollforward

> [!Note]  
> BETest è incluso in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive. VSS 7.2 SDK include una versione di BETest che viene eseguita solo in Windows Server 2003. Questo argomento descrive la Windows SDK di BETest, non la versione di Windows Server 2003 inclusa in VSS 7.2 SDK. Per informazioni sul download di Windows SDK e VSS 7.2 SDK, vedere [Servizio Copia Shadow del volume](volume-shadow-copy-service-portal.md).

 

Nell'installazione di Windows SDK, lo strumento BETest è disponibile in (per Windows a 64 bit) e (per le Windows `%Program Files(x86)%\Windows Kits\8.1\bin\x64` `%Program Files(x86)%\Windows Kits\8.1\bin\x86` a 32 bit).

## <a name="running-the-betest-tool"></a>Esecuzione dello strumento BETest

Per eseguire lo strumento BETest dalla riga di comando, usare la sintassi seguente:

Opzioni della *riga di comando di* **BETest**

L'esempio di utilizzo seguente illustra come usare lo strumento BETest con lo strumento [VSS Test Writer,](vss-test-writer-tool.md)che è un VSS writer.

**Esempio di utilizzo dello strumento BETest**

1.  Creare una directory di test denominata C: \\ BETest. Copiare i file seguenti in questa directory:
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  Creare una directory denominata C: \\ TestPath. Inserire alcuni file di dati di test in questa directory.
3.  Creare una directory denominata C: \\ BackupDestination. Lasciare vuota questa directory.
4.  Aprire due finestre dei comandi con privilegi elevati e impostare la directory di lavoro in ognuna su C: \\ BETest.
5.  Nella prima finestra di comando avviare lo strumento [VSS Test Writer](vss-test-writer-tool.md) come indicato di seguito:

    **vswriter.exe VswriterSample.xml**

    Il file vswriterSample.xml configura lo strumento VSS Test Writer (vswriter) per segnalare il contenuto della directory c: TestPath in preparazione di \\ un'operazione di backup. Si noti che lo strumento VSS Test Writer non produrrà output finché non rileva l'attività da un richiedente, ad esempio BETest. Per arrestare lo strumento VSS Test Writer, premere CTRL+C.

6.  Nella seconda finestra di comando usare lo strumento BETest per eseguire un'operazione di backup come indicato di seguito:

    **betest.exe /B /S backup.xml /D C: \\ BackupDestination /X BetestSample.xml**

    BETest esererà il backup dei file dalla directory C: \\ TestPath alla directory C: \\ BackupDestination. Il documento del componente di backup verrà salvato in C: \\ BETest \\backup.xml.

7.  Se l'operazione di backup ha esito positivo, eliminare il contenuto della directory C: TestPath e usare lo strumento BETest per eseguire \\ un'operazione di ripristino come indicato di seguito:

    **betest.exe /R /S backup.xml /D C: \\ BackupDestination /X BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>Opzioni Command-Line strumenti BETest

Lo strumento BETest usa le opzioni della riga di comando seguenti per identificare le operazioni da eseguire.

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

Esegue un'operazione di ripristino autorevole per Active Directory o la modalità applicazione Active Directory.

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

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Nome file*
</dt> <dd>

> [!Note]  
> Questa opzione della riga di comando viene fornita solo per la compatibilità con le versioni precedenti. In **alternativa,** è necessario usare l'opzione della riga di comando /X.

 

Seleziona i componenti di cui eseguire il backup o il ripristino in base al contenuto del file di configurazione specificato da *Nome file*. Questo file deve contenere solo caratteri ANSI nell'intervallo compreso tra 0 e 127 e non deve essere maggiore di 1 MB. Ogni riga del file deve usare il formato seguente:

*WriterId:* *ComponentName*;

Dove *WriterId* è l'ID writer e *ComponentName* è il nome di uno dei componenti del writer. L'ID writer e i nomi dei componenti devono essere racchiusi tra virgolette e devono essere presenti spazi prima e dopo i due punti (:). Se vengono specificati due o più componenti, devono essere separati da virgole. Esempio:

"5affb034-969f-4919-8875-88f830d0ef89": "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *Percorso*
</dt> <dd>

Salvare i file di cui è stato eseguito il backup o ripristinarli dalla directory di backup specificata da *Percorso*.

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NBC**
</dt> <dd>

Omette l'operazione di backup completata.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/o**
</dt> <dd>

Specifica che il backup include uno stato di sistema avviabile.

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/p**
</dt> <dd>

Crea una copia shadow permanente.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre Nome** *file*
</dt> <dd>

Se il tipo di backup specificato nell'opzione della riga di comando **/T** è INCREMENTAL o DIFFERENZIALE, impostare il documento di backup sul file specificato da *Filename* per il backup completo o incrementale precedente.

**Windows Server 2003 e Windows XP:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/r**
</dt> <dd>

Esegue il ripristino ma non esegue il backup. Deve essere usato insieme all'opzione della riga di comando **/S.**

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

Crea una copia shadow che può essere usata per il rollback dell'applicazione.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Nome file*
</dt> <dd>

In caso di backup, salva il documento di backup nel file specificato da *Nome file*. In caso di ripristino, carica il documento di backup da questo file.

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

Crea una copia shadow del volume, ma non esegue il backup o il ripristino.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

Arresta BETest quando viene rilevato il primo errore del writer.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*
</dt> <dd>

Specifica il tipo di backup. *BackupType* può essere FULL, LOG, COPY, INCREMENTAL o DIFFERENTIAL. Per altre informazioni sui tipi di backup, vedere [**VSS \_ BACKUP \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/v**
</dt> <dd>

Genera un output dettagliato che può essere usato per la risoluzione dei problemi.

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X Nome** *file*
</dt> <dd>

Seleziona i componenti di cui eseguire il backup o il ripristino in base al contenuto del file di configurazione XML specificato da *Nome file*. Questo file deve contenere solo caratteri ANSI nell'intervallo compreso tra 0 e 127. Il formato del file XML è definito dallo schema nel file BETest.xml file. Per un file di configurazione di esempio, vedere BetestSample.xml. Entrambi questi file sono nella directory vsstools.

> [!Note]  
> È possibile visualizzare il file BETest.xml in Internet Explorer. Prima di aprire questo file, assicurarsi che il file xdr-schema.xsl si trova nella stessa directory BETest.xml. Il file xdr-schema.xsl contiene istruzioni per il rendering che rendono BETest.xml file più leggibile.

 

**Windows Server 2003:** Questa opzione della riga di comando non è supportata.

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>File di configurazione XML di esempio: BetestSample.xml

Il file di configurazione di esempio BetestSample.xml è disponibile nella directory Vsstools.

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

Questo esempio di file di configurazione semplice seleziona un componente di cui eseguire il backup o il ripristino.

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>File di configurazione XML di esempio: VswriterSample.xml

Il file di configurazione di esempio VswriterSample.xml è disponibile nella directory Vsstools.

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

L'elemento radice in questo file di configurazione è denominato TestWriter. Tutti gli altri elementi sono disposti sotto l'elemento TestWriter.

Il primo attributo associato a TestWriter è l'attributo di utilizzo. Questo attributo specifica il tipo di utilizzo segnalato tramite il [**metodo IVssExamineWriterMetadata::GetIdentity.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) Uno dei valori possibili per questo attributo è USER \_ DATA.

Il secondo attributo è l'attributo deleteFiles. Questo attributo è descritto in [Configurazione degli attributi del writer.](vss-test-writer-tool.md)

Il primo elemento figlio dell'elemento radice è un elemento RestoreMethod. Questo elemento specifica quanto segue:

-   Il metodo di ripristino (in questo caso, RESTORE \_ IF \_ CAN BE \_ \_ REPLACED)
-   Se il writer richiede eventi di ripristino (in questo caso, sempre)
-   Se è necessario un riavvio dopo il ripristino del writer (in questo caso, no)

Questo elemento può specificare facoltativamente un mapping di percorso alternativo. In questo caso, non viene specificata alcuna posizione alternativa. Per altre informazioni, vedere [Specifica di mapping di percorsi alternativi.](vss-test-writer-tool.md)

Il secondo elemento figlio è un elemento Component. Questo elemento fa sì che il writer abiliti un componente ai relativi metadati. Un elemento Component contiene attributi che descrivono il componente e gli elementi figlio per descrivere il contenuto del componente, ad esempio:

-   componentType per indicare se si tratta di un filegroup o di un database (in questo caso, un filegroup)
-   logicalPath per il percorso logico del componente (in questo caso, non è specificato nessuno)
-   componentName per il nome del componente (in questo caso,"TestFiles")
-   selezionabile per indicare lo stato selectable-for-backup

L'elemento Component include anche un elemento figlio denominato ComponentFile per aggiungere una specifica di file a questo componente. Un elemento Component può avere un numero arbitrario di elementi ComponentFile che possono essere specificati per ogni componente. Questo elemento ComponentFile ha gli attributi seguenti:

-   path="c: \\ TestPath"
-   filespec=" \* "
-   recursive="no"

 

 



