---
title: Uso dei cmdlet Windows PowerShell WinRM per gestire i processi di trasferimento BITS
description: Windows I cmdlet di PowerShell per la gestione remota possono Servizio trasferimento intelligente in background processi di trasferimento di Servizio trasferimento intelligente in background (BITS).
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f24f4776d8a8431ac8c910fb8145633961bf353721698f8c3e5b4737ee0a1c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004641"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>Uso dei cmdlet Windows PowerShell WinRM per gestire i processi di trasferimento BITS

Windows I cmdlet di PowerShell per la gestione remota possono Servizio trasferimento intelligente in background processi di trasferimento di Servizio trasferimento intelligente in background (BITS). Per altre informazioni sulla gestione remota BITS, vedere Classi [del provider BITS](/previous-versions/windows/desktop/bitsprov/bits-provider) e [del provider BITS]( /previous-versions//dd904507(v=vs.85)).

Gli esempi seguenti richiedono il [provider BITS](/previous-versions/windows/desktop/bitsprov/bits-provider). Il provider BITS è disponibile dopo l'installazione del server BITS Compact. Per informazioni sull'installazione di Compact Server, vedere la [documentazione di BITS Compact Server.](bits-compact-server.md)

1.  Creare un processo di trasferimento BITS.

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    Il cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) richiede le credenziali dell'utente per connettersi al computer remoto e le assegna all'oggetto $cred.

    Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) crea il processo di trasferimento BITS in Client1 creando un'istanza della [classe BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) e usando le informazioni nella tabella hash definita nel parametro *Valueset.* Il *parametro Valueset* specifica le informazioni necessarie per popolare i parametri del [metodo CreateJob.](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) Nell'esempio precedente l'utente imposta il *parametro Type* su 0 (download). L'utente specifica anche il nome dei file remoti e locali per il processo di download. Per altre informazioni sulla creazione di processi di trasferimento BITS e per informazioni dettagliate sui parametri, vedere [Metodo CreateJob.](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob)

    Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) assegna il risultato alla $result variabile.

    > [!Note]  
    > Il carattere grave-accent ( \` ) viene usato per indicare un'interruzione di riga.

     

2.  Impostare la priorità del processo di trasferimento BITS.

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    Il cmdlet [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) modifica la priorità del nuovo processo di trasferimento BITS in 0 **(BG \_ JOB PRIORITY \_ \_ FOREGROUND).** Per altre informazioni sui livelli di priorità, vedere [**l'enumerazione BG \_ JOB \_ PRIORITY.**](/windows/desktop/api/Bits/ne-bits-bg_job_priority)

3.  Riprendere il processo di trasferimento BITS.

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    Il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il [metodo SetJobState,](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) che imposta lo stato del processo su 2 (Resume the Job).

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

    

    L'esempio precedente è uno script per eseguire il polling dello stato del processo ed eseguire un'azione in base allo stato. Sono possibili le azioni seguenti:

    -   Se $result. Lo stato è 4 **(BG \_ JOB \_ STATE \_ ERROR),** il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il [metodo SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e annulla il processo.
    -   Se $result. Lo stato è 5 **(BG \_ JOB STATE TRANSIENT \_ \_ \_ ERROR),** il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il [metodo SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e annulla il processo.
    -   Se $result. Lo stato è 6 **(BG \_ JOB \_ STATE \_ TRANSFERRED),** il cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chiama il [metodo SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e imposta lo stato da completare.

    Per altre informazioni sugli stati dei processi, vedere [**l'enumerazione BG \_ JOB \_ STATE.**](/windows/desktop/api/Bits/ne-bits-bg_job_state)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
