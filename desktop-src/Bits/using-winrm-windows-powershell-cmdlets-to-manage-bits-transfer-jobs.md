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
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>Utilizzo dei cmdlet di Windows PowerShell per WinRM per gestire i processi di trasferimento BITS

Gestione remota Windows cmdlet di PowerShell possono gestire i processi di trasferimento Servizio trasferimento intelligente in background (BITS). Per ulteriori informazioni sulla gestione remota BITS, vedere classi del [provider bits e](/previous-versions/windows/desktop/bitsprov/bits-provider) del [provider bits]( /previous-versions//dd904507(v=vs.85)).

Gli esempi seguenti richiedono il [provider bits](/previous-versions/windows/desktop/bitsprov/bits-provider). Il provider BITS è disponibile dopo l'installazione di BITS Compact Server. Per informazioni sull'installazione di Compact Server, vedere la documentazione di [BITS Compact Server](bits-compact-server.md) .

1.  Creazione di un processo di trasferimento BITS.

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    Il cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) richiede le credenziali dell'utente per connettersi al computer remoto e assegna le credenziali all'oggetto $cred.

    Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) crea il processo di trasferimento BITS in CLIENT1 creando un'istanza della classe [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) e usando le informazioni nella tabella hash definita nel parametro *Valuet* . Il parametro *Valuet* specifica le informazioni necessarie per popolare i parametri del metodo [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) . Nell'esempio precedente, l'utente imposta il parametro di *tipo* su 0 (download). L'utente specifica anche il nome dei file remoti e locali per il processo di download. Per ulteriori informazioni sulla creazione di processi di trasferimento BITS e per informazioni dettagliate sui parametri, vedere metodo [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .

    Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) assegna il risultato alla variabile $result.

    > [!Note]  
    > Il carattere di accento grave ( \` ) viene usato per indicare un'interruzioni di riga.

     

2.  Imposta la priorità del processo di trasferimento BITS.

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    Il cmdlet [set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) modifica la nuova priorità del processo di trasferimento BITS in 0 (**priorità di \_ \_ \_ primo piano del processo BG**). Per ulteriori informazioni sui livelli di priorità, vedere l' [**enumerazione \_ \_ priorità processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .

3.  Riprendere il processo di trasferimento BITS.

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il metodo [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , che imposta lo stato del processo su 2 (riprende il processo).

4.  Gestire il processo di trasferimento BITS.

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

    

    L'esempio precedente è uno script per eseguire il polling dello stato del processo e intraprendere un'azione in base allo stato. Sono possibili le azioni seguenti:

    -   Se $result. State è 4 (**\_ errore di \_ stato \_ del processo BG**), il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il metodo [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e Annulla il processo.
    -   Se $result. State è 5 (**\_ \_ \_ \_ errore temporaneo stato processo BG**), il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il metodo [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e Annulla il processo.
    -   Se $result. Lo stato è 6 **( \_ stato del processo BG \_ \_ trasferito**), il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il metodo [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e imposta lo stato su completato.

    Per ulteriori informazioni sugli stati dei processi, vedere l'enumerazione [**\_ \_ dello stato del processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
