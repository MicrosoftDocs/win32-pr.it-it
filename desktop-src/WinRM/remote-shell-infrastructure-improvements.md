---
title: Miglioramenti dell'infrastruttura della shell remota
description: Windows Gestione remota versione 2.0 (WinRM 2.0) offre numerosi miglioramenti all'infrastruttura della shell remota.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf88a472319b4b4677992f97509a3603cfe4a32f272388caf9db100b6e7457ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121661"
---
# <a name="remote-shell-infrastructure-improvements"></a>Miglioramenti dell'infrastruttura della shell remota

Windows Gestione remota versione 2.0 (WinRM 2.0) offre numerosi miglioramenti all'infrastruttura della shell remota. Gli argomenti seguenti descrivono in dettaglio questi miglioramenti:

-   [Supporto multi hop](multi-hop-support.md)
-   [Gestione delle quote per le shell remote](quotas.md)

Uno dei miglioramenti apportati all'infrastruttura della shell remota WinRM è l'aggiunta di un gestore di shell più affidabile che gestisce le informazioni specifiche della shell dell'utente. Gli utenti di Gestione remota Windows possono creare shell in computer remoti per eseguire comandi o script. Inoltre, gli utenti possono creare più shell in un computer. Sia gli utenti che gli amministratori devono poter gestire le shell. Gli utenti possono enumerare, ottenere ed eliminare le shell create. Gli amministratori possono enumerare tutte le shell attive e recuperare i dettagli su shell specifiche in un host locale o remoto. Gli amministratori possono anche eliminare qualsiasi shell attiva in un host locale o remoto.

Quando un utente o un amministratore enumera le shell attive, il servizio Gestione remota Windows può restituire le informazioni seguenti.

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId
</dt> <dd>

Specifica l'identificatore univoco per la shell.

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variabili di ambiente
</dt> <dd>

Specifica le variabili di ambiente impostate dall'utente.

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>Workingdirectory
</dt> <dd>

Specifica la directory iniziale per la shell.

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI
</dt> <dd>

Specifica l'URI della risorsa per l'operazione della shell. L'URI della risorsa può essere usato per recuperare la configurazione del plug-in specifica per l'istanza della shell.

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Specifica la durata massima, in millisecondi, che la shell rimarrà aperta senza alcuna richiesta.

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStream
</dt> <dd>

Specifica i flussi di input per la shell.

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStream
</dt> <dd>

Specifica i flussi di output per la shell.

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Ora di creazione della shell
</dt> <dd>

Specifica il timestamp di creazione per la shell.

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime
</dt> <dd>

Specifica la durata, in millisecondi, dell'inattività della shell.

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>Userid
</dt> <dd>

Specifica l'ID utente.

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nome host o indirizzo IP
</dt> <dd>

Specifica il nome host o l'indirizzo IP del computer che ha creato la shell.

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Utilizzo della memoria della shell
</dt> <dd>

Specifica la quantità di memoria usata dalla shell.

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Numero di processi
</dt> <dd>

Specifica il numero di processi creati dalla shell.

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>Enumerazione di una shell in un host locale

Il comando seguente illustra come usare l'utilità winrm per enumerare le shell in un client WinRM: **winrm enumerate shell**.

Nell'esempio basato su testo seguente viene visualizzato l'output per l'enumerazione della shell:

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

Per altre informazioni, vedere la Guida online fornita eseguendo il comando seguente: **winrm enumerate -?**.

## <a name="retrieving-information-about-a-specific-shell"></a>Recupero di informazioni su una shell specifica

Un amministratore o un utente può anche usare l'identificatore ShellId per recuperare informazioni sulla shell. Il comando seguente illustra come usare l'utilità winrm per ottenere informazioni su una shell specifica: **winrm get shell? ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.

Nell'esempio basato su testo seguente viene visualizzato l'output per le informazioni sulla shell:

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

Per altre informazioni, vedere la Guida online fornita dal comando seguente: **winrm get -?**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto multi hop](multi-hop-support.md)
</dt> <dt>

[Gestione delle quote per le shell remote](quotas.md)
</dt> <dt>

[Informazioni di riferimento gestite WS-Management comandi di PowerShell](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




