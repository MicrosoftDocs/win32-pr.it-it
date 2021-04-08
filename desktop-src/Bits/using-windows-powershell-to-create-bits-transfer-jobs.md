---
title: Utilizzo di Windows PowerShell per creare processi di trasferimento di BITS
description: È possibile usare i cmdlet di PowerShell per creare processi di trasferimento di Servizio trasferimento intelligente in background (BITS) sincroni e asincroni.
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af4879d1fc8f1b25fa0b1b51816432aad3bed8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748506"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a><span data-ttu-id="97bdf-103">Utilizzo di Windows PowerShell per creare processi di trasferimento di BITS</span><span class="sxs-lookup"><span data-stu-id="97bdf-103">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>

<span data-ttu-id="97bdf-104">È possibile usare i cmdlet di PowerShell per creare processi di trasferimento di Servizio trasferimento intelligente in background (BITS) sincroni e asincroni.</span><span class="sxs-lookup"><span data-stu-id="97bdf-104">You can use PowerShell cmdlets to create synchronous and asynchronous Background Intelligent Transfer Service (BITS) transfer jobs.</span></span>

<span data-ttu-id="97bdf-105">Tutti gli esempi in questo argomento usano il cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="97bdf-105">All of the examples in this topic use the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="97bdf-106">Per usare il cmdlet, assicurarsi di importare prima il modulo.</span><span class="sxs-lookup"><span data-stu-id="97bdf-106">To use the cmdlet, be sure to import the module first.</span></span> <span data-ttu-id="97bdf-107">Per installare il modulo, eseguire il comando seguente: Import-Module BitsTransfer.</span><span class="sxs-lookup"><span data-stu-id="97bdf-107">To install the module, run the following command: Import-Module BitsTransfer.</span></span> <span data-ttu-id="97bdf-108">Per ulteriori informazioni, digitare **Get-Help Start-BitsTransfer** al prompt di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="97bdf-108">For more information, type **Get-Help Start-BitsTransfer** at the PowerShell prompt.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="97bdf-109">Quando si usano i cmdlet [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) dall'interno di un processo che viene eseguito in un contesto non interattivo, ad esempio un servizio Windows, potrebbe non essere possibile aggiungere file ai processi BITS, che possono causare lo stato Suspended.</span><span class="sxs-lookup"><span data-stu-id="97bdf-109">When you use [\*-BitsTransfer](/previous-versions//dd819413(v=technet.10)) cmdlets from within a process that runs in a noninteractive context, such as a Windows service, you may not be able to add files to BITS jobs, which can result in a suspended state.</span></span> <span data-ttu-id="97bdf-110">Affinché il processo continui, è necessario eseguire l'accesso all'identità utilizzata per creare un processo di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="97bdf-110">For the job to proceed, the identity that was used to create a transfer job must be logged on.</span></span> <span data-ttu-id="97bdf-111">Ad esempio, quando si crea un processo BITS in uno script di PowerShell che è stato eseguito come processo di Utilità di pianificazione, il trasferimento BITS non verrà completato a meno che non sia abilitata l'impostazione dell'attività di Utilità di pianificazione "Esegui solo quando l'utente è connesso".</span><span class="sxs-lookup"><span data-stu-id="97bdf-111">For example, when creating a BITS job in a PowerShell script that was executed as a Task Scheduler job, the BITS transfer will never complete unless the Task Scheduler's task setting "Run only when user is logged on" is enabled.</span></span>

 

-   [<span data-ttu-id="97bdf-112">Per creare un processo di trasferimento BITS sincrono</span><span class="sxs-lookup"><span data-stu-id="97bdf-112">To create a synchronous BITS transfer job</span></span>](#to-create-a-synchronous-bits-transfer-job)
-   [<span data-ttu-id="97bdf-113">Per creare un processo di trasferimento BITS sincrono con più file</span><span class="sxs-lookup"><span data-stu-id="97bdf-113">To create a synchronous BITS transfer job with multiple files</span></span>](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [<span data-ttu-id="97bdf-114">Per creare un processo di trasferimento BITS sincrono e specificare le credenziali per un server remoto</span><span class="sxs-lookup"><span data-stu-id="97bdf-114">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [<span data-ttu-id="97bdf-115">Per creare un processo di trasferimento BITS sincrono da un file CSV</span><span class="sxs-lookup"><span data-stu-id="97bdf-115">To create a synchronous BITS transfer job from a CSV file</span></span>](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [<span data-ttu-id="97bdf-116">Per creare un processo di trasferimento BITS asincrono</span><span class="sxs-lookup"><span data-stu-id="97bdf-116">To create an asynchronous BITS transfer job</span></span>](#to-create-an-asynchronous-bits-transfer-job)
-   [<span data-ttu-id="97bdf-117">Per gestire le sessioni remote di PowerShell</span><span class="sxs-lookup"><span data-stu-id="97bdf-117">To manage PowerShell Remote sessions</span></span>](#to-manage-powershell-remote-sessions)
-   [<span data-ttu-id="97bdf-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97bdf-118">Related topics</span></span>](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a><span data-ttu-id="97bdf-119">Per creare un processo di trasferimento BITS sincrono</span><span class="sxs-lookup"><span data-stu-id="97bdf-119">To create a synchronous BITS transfer job</span></span>


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> <span data-ttu-id="97bdf-120">Il carattere di accento grave ( \` ) viene usato per indicare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="97bdf-120">The grave-accent character (\`) is used to indicate a line break.</span></span>

 

<span data-ttu-id="97bdf-121">Nell'esempio precedente, i nomi locali e remoti del file vengono specificati rispettivamente nei parametri di *origine* e di *destinazione* .</span><span class="sxs-lookup"><span data-stu-id="97bdf-121">In the preceding example, the local and remote names of the file are specified in the *Source* and *Destination* parameters, respectively.</span></span> <span data-ttu-id="97bdf-122">Il prompt dei comandi viene nuovamente visualizzato quando il trasferimento del file viene completato o entra in stato di errore.</span><span class="sxs-lookup"><span data-stu-id="97bdf-122">The command prompt returns when the file transfer is complete or when it enters an error state.</span></span>

<span data-ttu-id="97bdf-123">Il tipo di trasferimento predefinito è download.</span><span class="sxs-lookup"><span data-stu-id="97bdf-123">The default transfer type is Download.</span></span> <span data-ttu-id="97bdf-124">Quando si caricano file in un percorso HTTP, è necessario impostare il parametro *TransferType* su upload.</span><span class="sxs-lookup"><span data-stu-id="97bdf-124">When you upload files to an HTTP location, the *TransferType* parameter must be set to Upload.</span></span>

<span data-ttu-id="97bdf-125">Poiché la posizione del parametro viene applicata per il cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) , non è necessario specificare i nomi di parametro per i parametri di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="97bdf-125">Because parameter position is enforced for the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet, the parameter names do not need to be specified for the Source and Destination parameters.</span></span> <span data-ttu-id="97bdf-126">Questo comando può quindi essere semplificato come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="97bdf-126">Therefore, this command can be simplified as follows.</span></span>


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a><span data-ttu-id="97bdf-127">Per creare un processo di trasferimento BITS sincrono con più file</span><span class="sxs-lookup"><span data-stu-id="97bdf-127">To create a synchronous BITS transfer job with multiple files</span></span>


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



<span data-ttu-id="97bdf-128">Nell'esempio precedente, il comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crea un nuovo processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="97bdf-128">In the preceding example, the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job.</span></span> <span data-ttu-id="97bdf-129">Tutti i file vengono aggiunti a questo processo e trasferiti in sequenza al client.</span><span class="sxs-lookup"><span data-stu-id="97bdf-129">All of the files are added to this job and transferred sequentially to the client.</span></span>

> [!Note]  
> <span data-ttu-id="97bdf-130">Nel percorso di destinazione non è possibile utilizzare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="97bdf-130">The destination path cannot use wildcard characters.</span></span> <span data-ttu-id="97bdf-131">Il percorso di destinazione supporta directory relative, percorsi radice o directory implicite, ovvero la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="97bdf-131">The destination path supports relative directories, root paths, or implicit directories (that is, the current directory).</span></span> <span data-ttu-id="97bdf-132">Non è possibile rinominare i file di destinazione usando un carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="97bdf-132">Destination files cannot be renamed by using a wildcard character.</span></span> <span data-ttu-id="97bdf-133">Inoltre, gli URL HTTP e HTTPS non funzionano con i caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="97bdf-133">Additionally, HTTP and HTTPS URLs do not work with wildcards.</span></span> <span data-ttu-id="97bdf-134">I caratteri jolly sono validi solo per i percorsi UNC e le directory locali.</span><span class="sxs-lookup"><span data-stu-id="97bdf-134">Wildcards are only valid for UNC paths and local directories.</span></span>

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a><span data-ttu-id="97bdf-135">Per creare un processo di trasferimento BITS sincrono e specificare le credenziali per un server remoto</span><span class="sxs-lookup"><span data-stu-id="97bdf-135">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



<span data-ttu-id="97bdf-136">Nell'esempio precedente, un utente crea un processo di trasferimento BITS per scaricare un file da un server che richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="97bdf-136">In the preceding example, a user creates a BITS transfer job to download a file from a server that requires authentication.</span></span> <span data-ttu-id="97bdf-137">All'utente vengono richieste le credenziali e il parametro *Credential* passa un oggetto credenziale al cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="97bdf-137">The user is prompted for credentials, and the *Credential* parameter passes a credential object to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="97bdf-138">L'utente imposta un proxy esplicito e il processo di trasferimento BITS utilizza solo i proxy definiti dal parametro *proxy* .</span><span class="sxs-lookup"><span data-stu-id="97bdf-138">The user sets an explicit proxy, and the BITS transfer job uses only the proxies that are defined by the *ProxyList* parameter.</span></span> <span data-ttu-id="97bdf-139">Il parametro *DisplayName* assegna al processo di trasferimento BITS un nome visualizzato univoco.</span><span class="sxs-lookup"><span data-stu-id="97bdf-139">The *DisplayName* parameter gives the BITS transfer job a unique display name.</span></span>

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a><span data-ttu-id="97bdf-140">Per creare un processo di trasferimento BITS sincrono da un file CSV</span><span class="sxs-lookup"><span data-stu-id="97bdf-140">To create a synchronous BITS transfer job from a CSV file</span></span>


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> <span data-ttu-id="97bdf-141">" \| " È il carattere barra verticale.</span><span class="sxs-lookup"><span data-stu-id="97bdf-141">The "\|" is the pipe character.</span></span>

 

<span data-ttu-id="97bdf-142">Nell'esempio precedente, un utente crea un processo di trasferimento BITS che carica più file da un client.</span><span class="sxs-lookup"><span data-stu-id="97bdf-142">In the preceding example, a user creates a BITS transfer job that uploads multiple files from a client.</span></span> <span data-ttu-id="97bdf-143">Il cmdlet [Import-CSV](/previous-versions//dd347665(v=technet.10)) importa i percorsi dei file di origine e di destinazione e li invia tramite pipe al comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="97bdf-143">The [Import-CSV](/previous-versions//dd347665(v=technet.10)) cmdlet imports the source and destination file locations and pipes them to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command.</span></span> <span data-ttu-id="97bdf-144">Il comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crea un nuovo processo di trasferimento BITS per ogni file, aggiunge i file al processo e li trasferisce in sequenza al server.</span><span class="sxs-lookup"><span data-stu-id="97bdf-144">The [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job for each file, adds the files to the job, and then transfers them sequentially to the server.</span></span>

<span data-ttu-id="97bdf-145">Il contenuto del file di Filelist.txt deve essere nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="97bdf-145">The contents of the Filelist.txt file should be in the following format:</span></span>

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a><span data-ttu-id="97bdf-146">Per creare un processo di trasferimento BITS asincrono</span><span class="sxs-lookup"><span data-stu-id="97bdf-146">To create an asynchronous BITS transfer job</span></span>


```PowerShell
$Job = Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip `
       -Destination d:\temp\downloads\ -Asynchronous

while (($Job.JobState -eq "Transferring") -or ($Job.JobState -eq "Connecting")) `
       { sleep 5;} # Poll for status, sleep for 5 seconds, or perform an action.

Switch($Job.JobState)
{
    "Transferred" {Complete-BitsTransfer -BitsJob $Job}
    "Error" {$Job | Format-List } # List the errors.
    default {"Other action"} #  Perform corrective action.
}

```



<span data-ttu-id="97bdf-147">Nell'esempio precedente, il processo di trasferimento BITS è stato assegnato alla variabile $Job.</span><span class="sxs-lookup"><span data-stu-id="97bdf-147">In the preceding example, the BITS transfer job was assigned to the $Job variable.</span></span> <span data-ttu-id="97bdf-148">I file vengono scaricati in sequenza.</span><span class="sxs-lookup"><span data-stu-id="97bdf-148">The files are downloaded sequentially.</span></span> <span data-ttu-id="97bdf-149">Al termine del processo di trasferimento, i file sono immediatamente disponibili.</span><span class="sxs-lookup"><span data-stu-id="97bdf-149">After the transfer job is complete, the files are immediately available.</span></span> <span data-ttu-id="97bdf-150">Se $Job. JobState restituisce "trasferito", l'oggetto $Job viene inviato al cmdlet [complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="97bdf-150">If $Job.JobState returns "Transferred", the $Job object is sent to the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="97bdf-151">Se $Job. JobState restituisce "Error", l'oggetto $Job viene inviato al cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) per elencare gli errori.</span><span class="sxs-lookup"><span data-stu-id="97bdf-151">If $Job.JobState returns "Error", the $Job object is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet to list the errors.</span></span>

## <a name="to-manage-powershell-remote-sessions"></a><span data-ttu-id="97bdf-152">Per gestire le sessioni remote di PowerShell</span><span class="sxs-lookup"><span data-stu-id="97bdf-152">To manage PowerShell Remote sessions</span></span>

<span data-ttu-id="97bdf-153">A partire da Windows 10, versione 1607, è possibile eseguire i cmdlet di PowerShell, BITSAdmin o altre applicazioni che usano le [interfacce](bits-interfaces.md) BITS da una riga di comando remota di PowerShell connessa a un altro computer (fisico o virtuale).</span><span class="sxs-lookup"><span data-stu-id="97bdf-153">Starting with Windows 10, version 1607, you can run PowerShell Cmdlets, BITSAdmin, or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="97bdf-154">Questa funzionalità non è disponibile quando si usa una riga di comando di [PowerShell diretta](/virtualization/hyper-v-on-windows/user_guide/vmsession) in una macchina virtuale nello stesso computer fisico e non è disponibile quando si usano i cmdlet WinRM.</span><span class="sxs-lookup"><span data-stu-id="97bdf-154">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>

<span data-ttu-id="97bdf-155">Un processo BITS creato da una sessione remota di PowerShell viene eseguito nel contesto dell'account utente della sessione e viene eseguito solo quando è presente almeno una sessione di accesso locale attiva o una sessione remota di PowerShell associata a tale account utente.</span><span class="sxs-lookup"><span data-stu-id="97bdf-155">A BITS Job created from a Remote PowerShell session runs under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="97bdf-156">È possibile usare le sessioni PSSession permanenti di PowerShell per eseguire comandi remoti senza la necessità di mantenere aperta una finestra di PowerShell per ogni processo per continuare a procedere, come descritto in [nozioni di base su PowerShell: gestione remota](https://techgenix.com/remote-management-powershell-part1/).</span><span class="sxs-lookup"><span data-stu-id="97bdf-156">You can use PowerShell's persistent PSSessions to run remote commands without the need to keep a PowerShell window open for each job to continue making progress, as described in [PowerShell Basics: Remote Management](https://techgenix.com/remote-management-powershell-part1/).</span></span>

-   <span data-ttu-id="97bdf-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) crea una sessione di PowerShell remota permanente.</span><span class="sxs-lookup"><span data-stu-id="97bdf-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) creates a persistent Remote PowerShell session.</span></span> <span data-ttu-id="97bdf-158">Una volta creati, gli oggetti PSSession vengono salvati nel computer remoto fino a quando non vengono eliminati in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="97bdf-158">Once created, the PSSession objects persist in the remote machine until explicitly deleted.</span></span> <span data-ttu-id="97bdf-159">Qualsiasi processo BITS avviato in una sessione attiva effettuerà il trasferimento dei dati, anche dopo la disconnessione del client dalla sessione.</span><span class="sxs-lookup"><span data-stu-id="97bdf-159">Any BITS jobs initiated in an active session will make progress transferring data, even after the client has disconnected from the session.</span></span>
-   <span data-ttu-id="97bdf-160">Disconnect [-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnette il computer client da una sessione remota di PowerShell e lo stato della sessione continua a essere gestito dal computer remoto.</span><span class="sxs-lookup"><span data-stu-id="97bdf-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnects the client machine from a Remote PowerShell session and the session’s state continues to be maintained by the remote machine.</span></span> <span data-ttu-id="97bdf-161">In particolare, i processi della sessione remota continueranno a essere eseguiti e i processi BITS continueranno a progredire.</span><span class="sxs-lookup"><span data-stu-id="97bdf-161">Most importantly, the remote session’s processes will continue executing, and BITS jobs will continue to make progress.</span></span> <span data-ttu-id="97bdf-162">Il computer client può anche essere riavviato e/o spento dopo la chiamata a Disconnect-PSSession.</span><span class="sxs-lookup"><span data-stu-id="97bdf-162">The client machine can even reboot and/or turn off after calling Disconnect-PSSession.</span></span>
-   <span data-ttu-id="97bdf-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) connette nuovamente il computer client a una sessione remota di PowerShell attiva.</span><span class="sxs-lookup"><span data-stu-id="97bdf-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) re-connects the client machine to an active Remote PowerShell session.</span></span>
-   <span data-ttu-id="97bdf-164">[Remove-PSSession rimuove](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) una sessione remota di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="97bdf-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) tears down a Remote PowerShell session.</span></span>

<span data-ttu-id="97bdf-165">Nell'esempio seguente viene illustrato come usare PowerShell remote per lavorare con processi di trasferimento BITS asincroni in modo da consentire al processo di continuare a avanzare anche quando non si è connessi attivamente alla sessione remota.</span><span class="sxs-lookup"><span data-stu-id="97bdf-165">The example below shows how to use PowerShell Remote to work with asynchronous BITS transfer jobs in a way that allows the job to continue to make progress even when you are not actively connected to the remote session.</span></span>


```PowerShell
# Establish a PowerShell Remote session in Server01 with name 'MyRemoteSession'
New-PSSession -ComputerName Server01 -Name MyRemoteSession -Credential Domain01\User01

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# While running in the context of the PowerShell Remote session, start a new BITS transfer
Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip -Destination c:\temp\downloads\ -Asynchronous

# Exit the PowerShell Remote session's context
Exit-PSSession

# Disconnect the 'MyRemoteSession' PowerShell Remote session from the current PowerShell window
# After this command, it is safe to close the current PowerShell window and turn off the local machine
Disconnect-PSSession -Name MyRemoteSession


# The commands below can be executed from a different PowerShell window, even after rebooting the local machine
# Connect the 'MyRemoteSession' PowerShell Remote session to the current PowerShell window
Connect-PSSession -ComputerName Server01 -Name MyRemoteSession

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# Manage BITS transfers on the remote machine via Complete-BitsTransfer, Remove-BitsTransfer, etc.

# Exit the PowerShell Remote session's context
Exit-PSSession

# Destroy the 'MyRemoteSession' PowerShell Remote session when no longer needed
Remove-PSSession -Name MyRemoteSession
```



## <a name="related-topics"></a><span data-ttu-id="97bdf-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97bdf-166">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="97bdf-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="97bdf-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="97bdf-168">[Operazione completata-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="97bdf-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span></span>
</dt> </dl>

 

 
