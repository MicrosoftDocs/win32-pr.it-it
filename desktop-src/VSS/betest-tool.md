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
# <a name="betest-tool"></a><span data-ttu-id="76b38-103">Strumento di test</span><span class="sxs-lookup"><span data-stu-id="76b38-103">BETest Tool</span></span>

<span data-ttu-id="76b38-104">Il test è un richiedente del servizio Copia Shadow del volume che verifica le operazioni avanzate di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="76b38-104">BETest is a VSS requester that tests advanced backup and restore operations.</span></span> <span data-ttu-id="76b38-105">Questo strumento può essere utilizzato per verificare l'utilizzo di un'applicazione di funzionalità VSS complesse, come le seguenti:</span><span class="sxs-lookup"><span data-stu-id="76b38-105">This tool can be used to test an application's use of complex VSS features such as the following:</span></span>

-   <span data-ttu-id="76b38-106">Backup incrementale e differenziale</span><span class="sxs-lookup"><span data-stu-id="76b38-106">Incremental and differential backup</span></span>
-   <span data-ttu-id="76b38-107">Opzioni di ripristino complesse, ad esempio ripristino autorevole</span><span class="sxs-lookup"><span data-stu-id="76b38-107">Complex restore options, such as authoritative restore</span></span>
-   <span data-ttu-id="76b38-108">Opzioni di rollforward</span><span class="sxs-lookup"><span data-stu-id="76b38-108">Rollforward options</span></span>

> [!Note]  
> <span data-ttu-id="76b38-109">L'attività di testing è inclusa in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="76b38-109">BETest is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="76b38-110">VSS 7,2 SDK include una versione di test che viene eseguita solo in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="76b38-110">The VSS 7.2 SDK includes a version of BETest that runs only on Windows Server 2003.</span></span> <span data-ttu-id="76b38-111">Questo argomento descrive la versione Windows SDK di test, non la versione di Windows Server 2003 inclusa in VSS 7,2 SDK.</span><span class="sxs-lookup"><span data-stu-id="76b38-111">This topic describes the Windows SDK version of BETest, not the Windows Server 2003 version included in the VSS 7.2 SDK.</span></span> <span data-ttu-id="76b38-112">Per informazioni sul download del Windows SDK e di VSS 7,2 SDK, vedere [servizio Copia Shadow del volume](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="76b38-112">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="76b38-113">Nell'installazione di Windows SDK, lo strumento di testing si trova in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (per Windows a 64 bit) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (per windows a 32 bit).</span><span class="sxs-lookup"><span data-stu-id="76b38-113">In the Windows SDK installation, the BETest tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="running-the-betest-tool"></a><span data-ttu-id="76b38-114">Esecuzione dello strumento di testing</span><span class="sxs-lookup"><span data-stu-id="76b38-114">Running the BETest Tool</span></span>

<span data-ttu-id="76b38-115">Per eseguire lo strumento di test dalla riga di comando, usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="76b38-115">To run the BETest tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="76b38-116">Esegui **test** della *riga di comando-Opzioni*</span><span class="sxs-lookup"><span data-stu-id="76b38-116">**BETest** *command-line-options*</span></span>

<span data-ttu-id="76b38-117">Nell'esempio di utilizzo riportato di seguito viene illustrato come utilizzare lo strumento di testing insieme allo [strumento VSS writer di test](vss-test-writer-tool.md), che è un VSS writer.</span><span class="sxs-lookup"><span data-stu-id="76b38-117">The following usage example shows how to use the BETest tool together with the [VSS Test Writer tool](vss-test-writer-tool.md), which is a VSS writer.</span></span>

<span data-ttu-id="76b38-118">**Esempio di utilizzo dello strumento di test**</span><span class="sxs-lookup"><span data-stu-id="76b38-118">**BETest Tool Usage Example**</span></span>

1.  <span data-ttu-id="76b38-119">Creare una directory di test denominata C: \\ Comtest.</span><span class="sxs-lookup"><span data-stu-id="76b38-119">Create a test directory named C:\\BETest.</span></span> <span data-ttu-id="76b38-120">Copiare i file seguenti in questa directory:</span><span class="sxs-lookup"><span data-stu-id="76b38-120">Copy the following files into this directory:</span></span>
    -   <span data-ttu-id="76b38-121">betest.exe</span><span class="sxs-lookup"><span data-stu-id="76b38-121">betest.exe</span></span>
    -   <span data-ttu-id="76b38-122">vswriter.exe</span><span class="sxs-lookup"><span data-stu-id="76b38-122">vswriter.exe</span></span>
    -   [<span data-ttu-id="76b38-123">BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="76b38-123">BetestSample.xml</span></span>](#sample-xml-configuration-file-betestsamplexml)
    -   [<span data-ttu-id="76b38-124">VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="76b38-124">VswriterSample.xml</span></span>](#sample-xml-configuration-file-vswritersamplexml)
2.  <span data-ttu-id="76b38-125">Creare una directory denominata C: \\ TestPath.</span><span class="sxs-lookup"><span data-stu-id="76b38-125">Create a directory named C:\\TestPath.</span></span> <span data-ttu-id="76b38-126">Inserire alcuni file di dati di test in questa directory.</span><span class="sxs-lookup"><span data-stu-id="76b38-126">Put some test data files in this directory.</span></span>
3.  <span data-ttu-id="76b38-127">Creare una directory denominata C: \\ BackupDestination.</span><span class="sxs-lookup"><span data-stu-id="76b38-127">Create a directory named C:\\BackupDestination.</span></span> <span data-ttu-id="76b38-128">Lasciare vuota questa directory.</span><span class="sxs-lookup"><span data-stu-id="76b38-128">Leave this directory empty.</span></span>
4.  <span data-ttu-id="76b38-129">Aprire due finestre dei comandi con privilegi elevati e impostare la directory di lavoro in ogni per C: eseguire un \\ test.</span><span class="sxs-lookup"><span data-stu-id="76b38-129">Open two elevated command windows and set the working directory in each to C:\\BETest.</span></span>
5.  <span data-ttu-id="76b38-130">Nella prima finestra di comando avviare lo [strumento VSS writer di test](vss-test-writer-tool.md) come segue:</span><span class="sxs-lookup"><span data-stu-id="76b38-130">In the first command window, start the [VSS Test Writer tool](vss-test-writer-tool.md) as follows:</span></span>

    <span data-ttu-id="76b38-131">**vswriter.exe VswriterSample.xml**</span><span class="sxs-lookup"><span data-stu-id="76b38-131">**vswriter.exe VswriterSample.xml**</span></span>

    <span data-ttu-id="76b38-132">Il file vswriterSample.xml configura lo strumento vswriter (VSS test writer Tool) per segnalare il contenuto della directory c: \\ TestPath in preparazione per un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="76b38-132">The vswriterSample.xml file configures the VSS Test Writer tool (vswriter) to report the contents of the c:\\TestPath directory in preparation for a backup operation.</span></span> <span data-ttu-id="76b38-133">Si noti che lo strumento VSS writer di test non produrrà l'output fino a quando non rileva l'attività da un richiedente, ad esempio un test.</span><span class="sxs-lookup"><span data-stu-id="76b38-133">Note that the VSS Test Writer tool will not produce output until it detects activity from a requester such as BETest.</span></span> <span data-ttu-id="76b38-134">Per arrestare lo strumento VSS writer di test, premere CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="76b38-134">To stop the VSS Test Writer tool, press CTRL+C.</span></span>

6.  <span data-ttu-id="76b38-135">Nella seconda finestra di comando usare lo strumento di test per eseguire un'operazione di backup, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="76b38-135">In the second command window, use the BETest tool to perform a backup operation as follows:</span></span>

    <span data-ttu-id="76b38-136">**betest.exe/B/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="76b38-136">**betest.exe /B /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

    <span data-ttu-id="76b38-137">Il test eseguirà il backup dei file dalla directory C: \\ TestPath alla directory c: \\ BackupDestination.</span><span class="sxs-lookup"><span data-stu-id="76b38-137">BETest will back up the files from the C:\\TestPath directory to the C:\\BackupDestination directory.</span></span> <span data-ttu-id="76b38-138">Il documento del componente di backup verrà salvato in C: \\backup.xml di test \\ .</span><span class="sxs-lookup"><span data-stu-id="76b38-138">It will save the backup component document to C:\\BETest\\backup.xml.</span></span>

7.  <span data-ttu-id="76b38-139">Se l'operazione di backup ha esito positivo, eliminare il contenuto della \\ directory C: TestPath e utilizzare lo strumento di test per eseguire un'operazione di ripristino come segue:</span><span class="sxs-lookup"><span data-stu-id="76b38-139">If the backup operation is successful, delete the contents of the C:\\TestPath directory, and use the BETest tool to perform a restore operation as follows:</span></span>

    <span data-ttu-id="76b38-140">**betest.exe/R/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="76b38-140">**betest.exe /R /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

## <a name="betest-tool-command-line-options"></a><span data-ttu-id="76b38-141">Opzioni di Command-Line dello strumento di test</span><span class="sxs-lookup"><span data-stu-id="76b38-141">BETest Tool Command-Line Options</span></span>

<span data-ttu-id="76b38-142">Lo strumento di test usa le seguenti opzioni della riga di comando per identificare le attività da eseguire.</span><span class="sxs-lookup"><span data-stu-id="76b38-142">The BETest tool uses the following command-line options to identify the work to perform.</span></span>

<dl> <dt>

<span data-ttu-id="76b38-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span><span class="sxs-lookup"><span data-stu-id="76b38-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-144">Esegue un'operazione di ripristino autorevole per Active Directory o Active Directory Application Mode.</span><span class="sxs-lookup"><span data-stu-id="76b38-144">Performs an authoritative restore operation for Active Directory or Active Directory Application Mode.</span></span>

<span data-ttu-id="76b38-145">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-145">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-146"><span id="_B"></span><span id="_b"></span>**/B**</span><span class="sxs-lookup"><span data-stu-id="76b38-146"><span id="_B"></span><span id="_b"></span>**/B**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-147">Esegue un'operazione di backup ma non esegue un ripristino.</span><span class="sxs-lookup"><span data-stu-id="76b38-147">Performs a backup operation but does not perform a restore.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span><span class="sxs-lookup"><span data-stu-id="76b38-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-149">Esegue solo l'operazione di completamento del backup.</span><span class="sxs-lookup"><span data-stu-id="76b38-149">Performs only the backup complete operation.</span></span>

<span data-ttu-id="76b38-150">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-150">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span> *Nome file* /c</span><span class="sxs-lookup"><span data-stu-id="76b38-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Filename*</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="76b38-152">Questa opzione della riga di comando viene fornita solo per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="76b38-152">This command-line option is provided only for backward compatibility.</span></span> <span data-ttu-id="76b38-153">Usare invece l'opzione della riga di comando **/x** .</span><span class="sxs-lookup"><span data-stu-id="76b38-153">The **/X** command-line option should be used instead.</span></span>

 

<span data-ttu-id="76b38-154">Seleziona i componenti di cui eseguire il backup o il ripristino in base al contenuto del file di configurazione specificato da *filename*.</span><span class="sxs-lookup"><span data-stu-id="76b38-154">Selects the components to be backed up or restored based on the contents of the configuration file specified by *Filename*.</span></span> <span data-ttu-id="76b38-155">Questo file deve contenere solo caratteri ANSI nell'intervallo compreso tra 0 e 127 e non deve essere maggiore di 1 MB.</span><span class="sxs-lookup"><span data-stu-id="76b38-155">This file must contain only ANSI characters in the range from 0 through 127, and it must be no larger than 1 MB.</span></span> <span data-ttu-id="76b38-156">Ogni riga nel file deve usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="76b38-156">Each line in the file must use the following format:</span></span>

<span data-ttu-id="76b38-157">*WriterId* : *ComponentName*;</span><span class="sxs-lookup"><span data-stu-id="76b38-157">*WriterId* : *ComponentName*;</span></span>

<span data-ttu-id="76b38-158">Dove *WriterId* è l'ID del writer e *ComponentName* è il nome di uno dei componenti del writer.</span><span class="sxs-lookup"><span data-stu-id="76b38-158">Where *WriterId* is the writer ID, and *ComponentName* is the name of one of the writer's components.</span></span> <span data-ttu-id="76b38-159">I nomi di ID e componente del writer devono essere racchiusi tra virgolette e devono essere presenti spazi prima e dopo i due punti (:).</span><span class="sxs-lookup"><span data-stu-id="76b38-159">The writer ID and component names must be in quotation marks, and there must be spaces before and after the colon (:).</span></span> <span data-ttu-id="76b38-160">Se vengono specificati due o più componenti, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="76b38-160">If two or more components are specified, they must be separated by commas.</span></span> <span data-ttu-id="76b38-161">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="76b38-161">For example:</span></span>

<span data-ttu-id="76b38-162">"5affb034-969f-4919-8875-88f830d0ef89": "TestFiles1", "TestFiles2", "TestFiles3";</span><span class="sxs-lookup"><span data-stu-id="76b38-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span></span>

</dd> <dt>

<span data-ttu-id="76b38-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *percorso*</span><span class="sxs-lookup"><span data-stu-id="76b38-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *Path*</span></span>
</dt> <dd>

<span data-ttu-id="76b38-164">Salvare i file di cui è stato eseguito il backup in o ripristinarli dalla directory di backup specificata da *path*.</span><span class="sxs-lookup"><span data-stu-id="76b38-164">Save the backed-up files to or restore them from the backup directory specified by *Path*.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span><span class="sxs-lookup"><span data-stu-id="76b38-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-166">Omette l'operazione di completamento del backup.</span><span class="sxs-lookup"><span data-stu-id="76b38-166">Omits the backup complete operation.</span></span>

<span data-ttu-id="76b38-167">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-167">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-168"><span id="_O"></span><span id="_o"></span>**/O**</span><span class="sxs-lookup"><span data-stu-id="76b38-168"><span id="_O"></span><span id="_o"></span>**/O**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-169">Specifica che il backup include uno stato del sistema di avvio.</span><span class="sxs-lookup"><span data-stu-id="76b38-169">Specifies that the backup includes a bootable system state.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-170"><span id="_P"></span><span id="_p"></span>**/P**</span><span class="sxs-lookup"><span data-stu-id="76b38-170"><span id="_P"></span><span id="_p"></span>**/P**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-171">Crea una copia shadow permanente.</span><span class="sxs-lookup"><span data-stu-id="76b38-171">Creates a persistent shadow copy.</span></span>

<span data-ttu-id="76b38-172">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-172">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Nome file* /pre</span><span class="sxs-lookup"><span data-stu-id="76b38-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="76b38-174">Se il tipo di backup specificato nell'opzione della riga di comando **/t** è incrementale o differenziale, impostare il documento di backup sul file specificato da *filename* per il backup completo o incrementale precedente.</span><span class="sxs-lookup"><span data-stu-id="76b38-174">If the backup type specified in the **/T** command-line option is INCREMENTAL or DIFFERENTIAL, set the backup document to the file specified by *Filename* for previous full or incremental backup.</span></span>

<span data-ttu-id="76b38-175">**Windows Server 2003 e Windows XP:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-175">**Windows Server 2003 and Windows XP:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-176"><span id="_R"></span><span id="_r"></span>**/R**</span><span class="sxs-lookup"><span data-stu-id="76b38-176"><span id="_R"></span><span id="_r"></span>**/R**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-177">Esegue il ripristino, ma non esegue il backup.</span><span class="sxs-lookup"><span data-stu-id="76b38-177">Performs restore but does not perform backup.</span></span> <span data-ttu-id="76b38-178">Deve essere usato in combinazione con l'opzione della riga di comando **/s** .</span><span class="sxs-lookup"><span data-stu-id="76b38-178">Must be used together with the **/S** command-line option.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span><span class="sxs-lookup"><span data-stu-id="76b38-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-180">Crea una copia shadow che può essere utilizzata per il rollback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76b38-180">Creates a shadow copy that can be used for application rollback.</span></span>

<span data-ttu-id="76b38-181">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-181">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *nomefile*</span><span class="sxs-lookup"><span data-stu-id="76b38-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="76b38-183">In caso di backup, Salva il documento di backup nel file specificato da *filename*.</span><span class="sxs-lookup"><span data-stu-id="76b38-183">In case of backup, saves the backup document to the file specified by *Filename*.</span></span> <span data-ttu-id="76b38-184">In caso di ripristino, carica il documento di backup da questo file.</span><span class="sxs-lookup"><span data-stu-id="76b38-184">In case of restore only, loads the backup document from this file.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span><span class="sxs-lookup"><span data-stu-id="76b38-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-186">Crea una copia shadow del volume, ma non esegue il backup o il ripristino.</span><span class="sxs-lookup"><span data-stu-id="76b38-186">Creates a volume shadow copy but does not perform backup or restore.</span></span>

<span data-ttu-id="76b38-187">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-187">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span><span class="sxs-lookup"><span data-stu-id="76b38-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-189">Arresta il test quando viene rilevato il primo errore del writer.</span><span class="sxs-lookup"><span data-stu-id="76b38-189">Stops BETest when the first writer error is encountered.</span></span>

<span data-ttu-id="76b38-190">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-190">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span><span class="sxs-lookup"><span data-stu-id="76b38-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span></span>
</dt> <dd>

<span data-ttu-id="76b38-192">Specifica il tipo di backup.</span><span class="sxs-lookup"><span data-stu-id="76b38-192">Specifies the backup type.</span></span> <span data-ttu-id="76b38-193">*BackupType* può essere pieno, log, copia, incrementale o differenziale.</span><span class="sxs-lookup"><span data-stu-id="76b38-193">*BackupType* can be FULL, LOG, COPY, INCREMENTAL, or DIFFERENTIAL.</span></span> <span data-ttu-id="76b38-194">Per ulteriori informazioni sui tipi di backup, [**vedere \_ \_ tipo di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span><span class="sxs-lookup"><span data-stu-id="76b38-194">For more information about backup types, see [**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span></span>

</dd> <dt>

<span data-ttu-id="76b38-195"><span id="_V"></span><span id="_v"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="76b38-195"><span id="_V"></span><span id="_v"></span>**/V**</span></span>
</dt> <dd>

<span data-ttu-id="76b38-196">Genera un output dettagliato che può essere utilizzato per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="76b38-196">Generates verbose output that can be used for troubleshooting.</span></span>

<span data-ttu-id="76b38-197">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-197">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="76b38-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *nomefile*</span><span class="sxs-lookup"><span data-stu-id="76b38-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="76b38-199">Seleziona i componenti di cui eseguire il backup o il ripristino in base al contenuto del file di configurazione XML specificato da *filename*.</span><span class="sxs-lookup"><span data-stu-id="76b38-199">Selects the components to be backed up or restored based on the contents of the XML configuration file specified by *Filename*.</span></span> <span data-ttu-id="76b38-200">Questo file deve contenere solo caratteri ANSI nell'intervallo compreso tra 0 e 127.</span><span class="sxs-lookup"><span data-stu-id="76b38-200">This file must contain only ANSI characters in the range from 0 through 127.</span></span> <span data-ttu-id="76b38-201">Il formato del file XML viene definito dallo schema nel file di BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="76b38-201">The format of the XML file is defined by the schema in the BETest.xml file.</span></span> <span data-ttu-id="76b38-202">Per un file di configurazione di esempio, vedere BetestSample.xml.</span><span class="sxs-lookup"><span data-stu-id="76b38-202">For a sample configuration file, see BetestSample.xml.</span></span> <span data-ttu-id="76b38-203">Entrambi questi file si trovano nella directory vsstools</span><span class="sxs-lookup"><span data-stu-id="76b38-203">Both of these files are in the vsstools directory.</span></span>

> [!Note]  
> <span data-ttu-id="76b38-204">È possibile visualizzare il file di BETest.xml in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="76b38-204">You can view the BETest.xml file in Internet Explorer.</span></span> <span data-ttu-id="76b38-205">Prima di aprire il file, assicurarsi che il file XDR-Schema. xsl si trovi nella stessa directory BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="76b38-205">Before you open this file, make sure that the xdr-schema.xsl file is in the same directory as BETest.xml.</span></span> <span data-ttu-id="76b38-206">Il file XDR-Schema. xsl contiene istruzioni per il rendering che rendono più leggibile il file di BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="76b38-206">The xdr-schema.xsl file contains rendering instructions that make the BETest.xml file more readable.</span></span>

 

<span data-ttu-id="76b38-207">**Windows Server 2003:** Questa opzione della riga di comando non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76b38-207">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a><span data-ttu-id="76b38-208">File di configurazione XML di esempio: BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="76b38-208">Sample XML Configuration File: BetestSample.xml</span></span>

<span data-ttu-id="76b38-209">Il file di configurazione di esempio seguente, BetestSample.xml, si trova nella directory Vsstools</span><span class="sxs-lookup"><span data-stu-id="76b38-209">The following sample configuration file, BetestSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

<span data-ttu-id="76b38-210">Questo esempio di un semplice file di configurazione seleziona un componente di cui eseguire il backup o il ripristino.</span><span class="sxs-lookup"><span data-stu-id="76b38-210">This example of a simple configuration file selects one component to be backed up or restored.</span></span>

## <a name="sample-xml-configuration-file-vswritersamplexml"></a><span data-ttu-id="76b38-211">File di configurazione XML di esempio: VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="76b38-211">Sample XML Configuration File: VswriterSample.xml</span></span>

<span data-ttu-id="76b38-212">Il file di configurazione di esempio seguente, VswriterSample.xml, si trova nella directory Vsstools</span><span class="sxs-lookup"><span data-stu-id="76b38-212">The following sample configuration file, VswriterSample.xml, can be found in the Vsstools directory.</span></span>

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

<span data-ttu-id="76b38-213">L'elemento radice in questo file di configurazione è denominato TestWriter.</span><span class="sxs-lookup"><span data-stu-id="76b38-213">The root element in this configuration file is named TestWriter.</span></span> <span data-ttu-id="76b38-214">Tutti gli altri elementi sono disposti nell'elemento TestWriter.</span><span class="sxs-lookup"><span data-stu-id="76b38-214">All other elements are arranged under the TestWriter element.</span></span>

<span data-ttu-id="76b38-215">Il primo attributo associato a TestWriter è l'attributo Usage.</span><span class="sxs-lookup"><span data-stu-id="76b38-215">The first attribute associated with TestWriter is the usage attribute.</span></span> <span data-ttu-id="76b38-216">Questo attributo specifica il tipo di utilizzo riportato tramite il metodo [**IVssExamineWriterMetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) .</span><span class="sxs-lookup"><span data-stu-id="76b38-216">This attribute specifies the usage type reported through the [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) method.</span></span> <span data-ttu-id="76b38-217">Uno dei possibili valori di questo attributo è costituito dai \_ dati utente.</span><span class="sxs-lookup"><span data-stu-id="76b38-217">One of the possible values for this attribute is USER\_DATA.</span></span>

<span data-ttu-id="76b38-218">Il secondo attributo è l'attributo deleteFiles.</span><span class="sxs-lookup"><span data-stu-id="76b38-218">The second attribute is the deleteFiles attribute.</span></span> <span data-ttu-id="76b38-219">Questo attributo è descritto in [configurazione degli attributi del writer](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="76b38-219">This attribute is described in [Configuring Writer Attributes](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="76b38-220">Il primo elemento figlio dell'elemento radice è un elemento RestoreMethod.</span><span class="sxs-lookup"><span data-stu-id="76b38-220">The first child element of the root element is a RestoreMethod element.</span></span> <span data-ttu-id="76b38-221">Questo elemento specifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="76b38-221">This element specifies the following:</span></span>

-   <span data-ttu-id="76b38-222">Metodo Restore (in questo caso, RESTOre \_ if \_ può \_ essere \_ sostituito)</span><span class="sxs-lookup"><span data-stu-id="76b38-222">The restore method (in this case, RESTORE\_IF\_CAN\_BE\_REPLACED)</span></span>
-   <span data-ttu-id="76b38-223">Indica se il writer richiede eventi di ripristino (in questo caso, always)</span><span class="sxs-lookup"><span data-stu-id="76b38-223">Whether the writer requires restore events (in this case, always)</span></span>
-   <span data-ttu-id="76b38-224">Indica se è necessario riavviare il computer dopo il ripristino del writer, in questo caso no.</span><span class="sxs-lookup"><span data-stu-id="76b38-224">Whether a reboot is required after the writer is restored (in this case, no)</span></span>

<span data-ttu-id="76b38-225">Questo elemento può facoltativamente specificare un mapping in un percorso alternativo.</span><span class="sxs-lookup"><span data-stu-id="76b38-225">This element can optionally specify an alternate-location mapping.</span></span> <span data-ttu-id="76b38-226">In questo caso non viene specificato alcun percorso alternativo. Per ulteriori informazioni, vedere [specifica di mapping dei percorsi alternativi](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="76b38-226">(In this case, no alternate location is specified.) For more information, see [Specifying Alternate Location Mappings](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="76b38-227">Il secondo elemento figlio è un elemento Component.</span><span class="sxs-lookup"><span data-stu-id="76b38-227">The second child element is a Component element.</span></span> <span data-ttu-id="76b38-228">Questo elemento fa sì che il writer aggiunga un componente ai relativi metadati.</span><span class="sxs-lookup"><span data-stu-id="76b38-228">This element causes the writer to add a component to its metadata.</span></span> <span data-ttu-id="76b38-229">Un elemento Component contiene gli attributi per descrivere il componente e gli elementi figlio per descrivere il contenuto del componente, ad esempio quanto segue:</span><span class="sxs-lookup"><span data-stu-id="76b38-229">A Component element contains attributes to describe the component and child elements to describe the content of the component, such as the following:</span></span>

-   <span data-ttu-id="76b38-230">componentType per indicare se si tratta di un filegroup o di un database, in questo caso un filegroup</span><span class="sxs-lookup"><span data-stu-id="76b38-230">componentType to indicate whether this is a filegroup or a database (in this case, a filegroup)</span></span>
-   <span data-ttu-id="76b38-231">logicalPath per il percorso logico del componente (in questo caso, non è specificato alcun valore)</span><span class="sxs-lookup"><span data-stu-id="76b38-231">logicalPath for the component logical path (in this case, none is specified)</span></span>
-   <span data-ttu-id="76b38-232">ComponentName per il nome del componente (in questo caso, "TestFiles")</span><span class="sxs-lookup"><span data-stu-id="76b38-232">componentName for the name of the component (in this case, "TestFiles")</span></span>
-   <span data-ttu-id="76b38-233">selezionabile per indicare lo stato selezionabile per il backup</span><span class="sxs-lookup"><span data-stu-id="76b38-233">selectable to indicate selectable-for-backup status</span></span>

<span data-ttu-id="76b38-234">L'elemento Component dispone anche di un elemento figlio denominato ComponentFile per aggiungere una specifica del file a questo componente.</span><span class="sxs-lookup"><span data-stu-id="76b38-234">The Component element also has a child element named ComponentFile to add a file specification to this component.</span></span> <span data-ttu-id="76b38-235">Un elemento Component può avere un numero arbitrario di elementi ComponentFile che può essere specificato per ogni componente. Questo elemento ComponentFile ha gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="76b38-235">(A Component element can have an arbitrary number of ComponentFile elements that can be specified for each component.) This ComponentFile element has the following attributes:</span></span>

-   <span data-ttu-id="76b38-236">path = "c: \\ TestPath"</span><span class="sxs-lookup"><span data-stu-id="76b38-236">path="c:\\TestPath"</span></span>
-   <span data-ttu-id="76b38-237">filespec = " \* "</span><span class="sxs-lookup"><span data-stu-id="76b38-237">filespec="\*"</span></span>
-   <span data-ttu-id="76b38-238">ricorsivo = "No"</span><span class="sxs-lookup"><span data-stu-id="76b38-238">recursive="no"</span></span>

 

 



