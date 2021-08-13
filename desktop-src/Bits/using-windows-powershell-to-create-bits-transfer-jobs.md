---
title: Utilizzo di Windows PowerShell per creare processi di trasferimento di BITS
description: È possibile usare i cmdlet di PowerShell per creare processi di Servizio trasferimento intelligente in background asincroni e asincroni (BITS).
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e939342414d62e4e1af0551318dfec0fb9a5ca59a7e310f13de7b6b67b0440cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679893"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a>Utilizzo di Windows PowerShell per creare processi di trasferimento di BITS

È possibile usare i cmdlet di PowerShell per creare processi di Servizio trasferimento intelligente in background asincroni e asincroni (BITS).

Tutti gli esempi in questo argomento usano il cmdlet [Start-BitsTransfer.](/previous-versions//dd347701(v=technet.10)) Per usare il cmdlet , assicurarsi di importare prima il modulo. Per installare il modulo, eseguire il comando seguente: Import-Module BitsTransfer. Per altre informazioni, digitare **Get-Help Start-BitsTransfer** al prompt di PowerShell.

> [!IMPORTANT]
>
> Quando si usano i cmdlet [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) dall'interno di un processo eseguito in un contesto non interattivo, ad esempio un servizio Windows, potrebbe non essere possibile aggiungere file ai processi BITS, il che può comportare uno stato sospeso. Per continuare il processo, è necessario accedere all'identità utilizzata per creare un processo di trasferimento. Ad esempio, quando si crea un processo BITS in uno script di PowerShell eseguito come processo Utilità di pianificazione, il trasferimento BITS non verrà mai completato a meno che non sia abilitata l'impostazione dell'attività "Esegui solo quando l'utente è connesso" del Utilità di pianificazione.

 

-   [Per creare un processo di trasferimento BITS sincrono](#to-create-a-synchronous-bits-transfer-job)
-   [Per creare un processo di trasferimento BITS sincrono con più file](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [Per creare un processo di trasferimento BITS sincrono e specificare le credenziali per un server remoto](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [Per creare un processo di trasferimento BITS sincrono da un file CSV](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [Per creare un processo di trasferimento BITS asincrono](#to-create-an-asynchronous-bits-transfer-job)
-   [Per gestire le sessioni remote di PowerShell](#to-manage-powershell-remote-sessions)
-   [Argomenti correlati](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a>Per creare un processo di trasferimento BITS sincrono


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> Il carattere grave-accent ( \` ) viene usato per indicare un'interruzione di riga.

 

Nell'esempio precedente i nomi locali e remoti del file vengono specificati rispettivamente nei parametri *Source* *e Destination.* Il prompt dei comandi viene nuovamente visualizzato quando il trasferimento del file viene completato o entra in stato di errore.

Il tipo di trasferimento predefinito è Download. Quando si caricano file in un percorso HTTP, il *parametro TransferType* deve essere impostato su Upload.

Poiché la posizione del parametro viene applicata per il cmdlet [Start-BitsTransfer,](/previous-versions//dd347701(v=technet.10)) i nomi dei parametri non devono essere specificati per i parametri Source e Destination. Di conseguenza, questo comando può essere semplificato come indicato di seguito.


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a>Per creare un processo di trasferimento BITS sincrono con più file


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



Nell'esempio precedente il comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crea un nuovo processo di trasferimento BITS. Tutti i file vengono aggiunti a questo processo e trasferiti in sequenza al client.

> [!Note]  
> Nel percorso di destinazione non è possibile utilizzare caratteri jolly. Il percorso di destinazione supporta le directory relative, i percorsi radice o le directory implicite ,ovvero la directory corrente. I file di destinazione non possono essere rinominati usando un carattere jolly. Inoltre, gli URL HTTP e HTTPS non funzionano con i caratteri jolly. I caratteri jolly sono validi solo per i percorsi UNC e le directory locali.

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a>Per creare un processo di trasferimento BITS sincrono e specificare le credenziali per un server remoto


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



Nell'esempio precedente un utente crea un processo di trasferimento BITS per scaricare un file da un server che richiede l'autenticazione. All'utente vengono richieste le credenziali e il parametro *Credential* passa un oggetto credenziali al cmdlet [Start-BitsTransfer.](/previous-versions//dd347701(v=technet.10)) L'utente imposta un proxy esplicito e il processo di trasferimento BITS usa solo i proxy definiti dal *parametro ProxyList.* Il *parametro DisplayName* fornisce al processo di trasferimento BITS un nome visualizzato univoco.

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a>Per creare un processo di trasferimento BITS sincrono da un file CSV


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> " \| " è il carattere barra verticale.

 

Nell'esempio precedente un utente crea un processo di trasferimento BITS che carica più file da un client. Il cmdlet [Import-CSV](/previous-versions//dd347665(v=technet.10)) importa i percorsi dei file di origine e di destinazione e li pipe al [comando Start-BitsTransfer.](/previous-versions//dd347701(v=technet.10)) Il [comando Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crea un nuovo processo di trasferimento BITS per ogni file, aggiunge i file al processo e li trasferisce in sequenza al server.

Il contenuto del file Filelist.txt deve essere nel formato seguente:

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a>Per creare un processo di trasferimento BITS asincrono


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



Nell'esempio precedente il processo di trasferimento BITS è stato assegnato alla $Job variabile . I file vengono scaricati in sequenza. Al termine del processo di trasferimento, i file sono immediatamente disponibili. Se $Job.JobState restituisce "Transferred", l'oggetto $Job viene inviato al cmdlet [Complete-BitsTransfer.]( /previous-versions//dd347701(v=technet.10))

Se $Job.JobState restituisce "Error", l'oggetto $Job viene inviato al cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) per elencare gli errori.

## <a name="to-manage-powershell-remote-sessions"></a>Per gestire le sessioni remote di PowerShell

A partire da Windows 10 versione 1607, è possibile eseguire i cmdlet di PowerShell, BITSAdmin o altre applicazioni che usano le interfacce [BITS](bits-interfaces.md) da una riga di comando remota di PowerShell connessa a un altro computer (fisico o virtuale). Questa funzionalità non è disponibile quando si usa una riga di comando di [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) per una macchina virtuale nello stesso computer fisico e non è disponibile quando si usano i cmdlet winrm.

Un processo BITS creato da una sessione remota di PowerShell viene eseguito nel contesto dell'account utente di tale sessione e procede solo quando è presente almeno una sessione di accesso locale attiva o una sessione remota di PowerShell associata a tale account utente. È possibile usare le sessioni PSSession persistenti di PowerShell per eseguire comandi remoti senza la necessità di mantenere aperta una finestra di PowerShell per ogni processo per continuare a procedere, come descritto in [PowerShell Basics: Remote Management](https://techgenix.com/remote-management-powershell-part1/)(Nozioni di base di PowerShell: Gestione remota).

-   [New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) crea una sessione di PowerShell remota persistente. Dopo la creazione, gli oggetti PSSession vengono mantenuti nel computer remoto fino a quando non vengono eliminati in modo esplicito. Tutti i processi BITS avviati in una sessione attiva procederanno al trasferimento dei dati, anche dopo che il client si è disconnesso dalla sessione.
-   [Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnette il computer client da una sessione remota di PowerShell e lo stato della sessione continua a essere mantenuto dal computer remoto. Ancora più importante, l'esecuzione dei processi della sessione remota continuerà e i processi BITS continueranno a procedere. Il computer client può anche riavviare e/o spegnere dopo aver chiamato Disconnect-PSSession.
-   [Connessione-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) riconnetta il computer client a una sessione di PowerShell remota attiva.
-   [Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) rimuove una sessione remota di PowerShell.

L'esempio seguente illustra come usare PowerShell Remote per lavorare con processi di trasferimento BITS asincroni in modo che il processo continui a procedere anche quando non si è attivamente connessi alla sessione remota.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))
</dt> <dt>

[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))
</dt> </dl>

 

 
