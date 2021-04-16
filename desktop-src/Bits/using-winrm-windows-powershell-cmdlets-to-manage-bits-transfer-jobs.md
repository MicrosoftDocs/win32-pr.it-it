---
title: Utilizzo dei cmdlet di Windows PowerShell per WinRM per gestire i processi di trasferimento BITS
description: Gestione remota Windows cmdlet di PowerShell possono gestire i processi di trasferimento Servizio trasferimento intelligente in background (BITS).
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eefd874a1056e959d1516d515891ae216e4aca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523778"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a><span data-ttu-id="a44ba-103">Utilizzo dei cmdlet di Windows PowerShell per WinRM per gestire i processi di trasferimento BITS</span><span class="sxs-lookup"><span data-stu-id="a44ba-103">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>

<span data-ttu-id="a44ba-104">Gestione remota Windows cmdlet di PowerShell possono gestire i processi di trasferimento Servizio trasferimento intelligente in background (BITS).</span><span class="sxs-lookup"><span data-stu-id="a44ba-104">Windows Remote Management PowerShell cmdlets can manage Background Intelligent Transfer Service (BITS) transfer jobs.</span></span> <span data-ttu-id="a44ba-105">Per ulteriori informazioni sulla gestione remota BITS, vedere classi del [provider bits e](/previous-versions/windows/desktop/bitsprov/bits-provider) del [provider bits]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a44ba-105">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

<span data-ttu-id="a44ba-106">Gli esempi seguenti richiedono il [provider bits](/previous-versions/windows/desktop/bitsprov/bits-provider).</span><span class="sxs-lookup"><span data-stu-id="a44ba-106">The following examples require the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider).</span></span> <span data-ttu-id="a44ba-107">Il provider BITS è disponibile dopo l'installazione di BITS Compact Server.</span><span class="sxs-lookup"><span data-stu-id="a44ba-107">The BITS provider is available after the BITS Compact server is installed.</span></span> <span data-ttu-id="a44ba-108">Per informazioni sull'installazione di Compact Server, vedere la documentazione di [BITS Compact Server](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="a44ba-108">For information about installing the Compact server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="a44ba-109">Creazione di un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="a44ba-109">Create a BITS transfer job.</span></span>

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="a44ba-110">Il cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) richiede le credenziali dell'utente per connettersi al computer remoto e assegna le credenziali all'oggetto $cred.</span><span class="sxs-lookup"><span data-stu-id="a44ba-110">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="a44ba-111">Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) crea il processo di trasferimento BITS in CLIENT1 creando un'istanza della classe [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) e usando le informazioni nella tabella hash definita nel parametro *Valuet* .</span><span class="sxs-lookup"><span data-stu-id="a44ba-111">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cmdlet creates the BITS transfer job on Client1 by creating an instance of the [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) class and using the information in the hash table defined in the *Valueset* parameter.</span></span> <span data-ttu-id="a44ba-112">Il parametro *Valuet* specifica le informazioni necessarie per popolare i parametri del metodo [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="a44ba-112">The *Valueset* parameter specifies the information needed to populate the parameters of the [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span> <span data-ttu-id="a44ba-113">Nell'esempio precedente, l'utente imposta il parametro di *tipo* su 0 (download).</span><span class="sxs-lookup"><span data-stu-id="a44ba-113">In the preceding example, the user is sets the *Type* parameter to 0 (download).</span></span> <span data-ttu-id="a44ba-114">L'utente specifica anche il nome dei file remoti e locali per il processo di download.</span><span class="sxs-lookup"><span data-stu-id="a44ba-114">The user also specifies the name of both the remote and local files for the download job.</span></span> <span data-ttu-id="a44ba-115">Per ulteriori informazioni sulla creazione di processi di trasferimento BITS e per informazioni dettagliate sui parametri, vedere metodo [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="a44ba-115">For more information about creating BITS transfer jobs and for detailed information about parameters, see [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span>

    <span data-ttu-id="a44ba-116">Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) assegna il risultato alla variabile $result.</span><span class="sxs-lookup"><span data-stu-id="a44ba-116">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet assigns the result to the $result variable.</span></span>

    > [!Note]  
    > <span data-ttu-id="a44ba-117">Il carattere di accento grave ( \` ) viene usato per indicare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="a44ba-117">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="a44ba-118">Imposta la priorità del processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="a44ba-118">Set the Priority of the BITS transfer job.</span></span>

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="a44ba-119">Il cmdlet [set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) modifica la nuova priorità del processo di trasferimento BITS in 0 (**priorità di \_ \_ \_ primo piano del processo BG**).</span><span class="sxs-lookup"><span data-stu-id="a44ba-119">The [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cmdlet changes the new BITS transfer job priority to 0 (**BG\_JOB\_PRIORITY\_FOREGROUND**).</span></span> <span data-ttu-id="a44ba-120">Per ulteriori informazioni sui livelli di priorità, vedere l' [**enumerazione \_ \_ priorità processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .</span><span class="sxs-lookup"><span data-stu-id="a44ba-120">For more information about the priority levels, see the [**BG\_JOB\_PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) enumeration.</span></span>

3.  <span data-ttu-id="a44ba-121">Riprendere il processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="a44ba-121">Resume the BITS transfer job.</span></span>

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="a44ba-122">Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il metodo [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , che imposta lo stato del processo su 2 (riprende il processo).</span><span class="sxs-lookup"><span data-stu-id="a44ba-122">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method, which sets the job state to 2 (Resume the Job).</span></span>

4.  <span data-ttu-id="a44ba-123">Gestire il processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="a44ba-123">Manage the BITS transfer job.</span></span>

    ```PowerShell
    $IsPprocessing = $TRUE
    while ($IsPprocessing)
    {
        $result = Get-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -selectorset @{JobId = $result.JobId} `
               –ComputerName Client1  -Credential $cred
        if ($result.State -eq 6)
        {

    #Complete the job           
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                          -valueset @{JobState= 1} –ComputerName Client1  -Credential $cred
            "Job Successfully Transferred"
            $IsPprocessing = $FALSE;
        }
        elseif (($result.State -eq 4) -or ($result.State -eq 5))
        {

    #Cancel the job
            "Job is in Error " 
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                         -valueset @{JobState= 0} –ComputerName Client1  -Credential $cred
            # You can troubleshoot or delete the job
            $IsPprocessing = $FALSE;
        }
        else
        {
        "Job is processing\n" 
        }

    # Perform other action or poll in a tight loop. This example sleeps for 5 seconds
    sleep 5
    }
    ```

    

    <span data-ttu-id="a44ba-124">L'esempio precedente è uno script per eseguire il polling dello stato del processo e intraprendere un'azione in base allo stato.</span><span class="sxs-lookup"><span data-stu-id="a44ba-124">The preceding example is a script to poll the status of the job and take an action based on the status.</span></span> <span data-ttu-id="a44ba-125">Sono possibili le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a44ba-125">The following actions are possible:</span></span>

    -   <span data-ttu-id="a44ba-126">Se $result. State è 4 (**\_ errore di \_ stato \_ del processo BG**), il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il metodo [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e Annulla il processo.</span><span class="sxs-lookup"><span data-stu-id="a44ba-126">If $result.State is 4 (**BG\_JOB\_STATE\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="a44ba-127">Se $result. State è 5 (**\_ \_ \_ \_ errore temporaneo stato processo BG**), il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il metodo [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e Annulla il processo.</span><span class="sxs-lookup"><span data-stu-id="a44ba-127">If $result.State is 5 (**BG\_JOB\_STATE\_TRANSIENT\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="a44ba-128">Se $result. Lo stato è 6 **( \_ stato del processo BG \_ \_ trasferito**), il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il metodo [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e imposta lo stato su completato.</span><span class="sxs-lookup"><span data-stu-id="a44ba-128">If $result.State is 6 (**BG\_JOB\_STATE\_TRANSFERRED**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and sets the state to complete.</span></span>

    <span data-ttu-id="a44ba-129">Per ulteriori informazioni sugli stati dei processi, vedere l'enumerazione [**\_ \_ dello stato del processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .</span><span class="sxs-lookup"><span data-stu-id="a44ba-129">For more information about job states, see the [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a44ba-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a44ba-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a44ba-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="a44ba-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

[<span data-ttu-id="a44ba-132">Invoke-WsmanAction</span><span class="sxs-lookup"><span data-stu-id="a44ba-132">Invoke-WsmanAction</span></span>](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[<span data-ttu-id="a44ba-133">Set-WsmanInstance</span><span class="sxs-lookup"><span data-stu-id="a44ba-133">Set-WsmanInstance</span></span>](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
