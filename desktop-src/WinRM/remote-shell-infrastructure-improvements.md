---
title: Miglioramenti dell'infrastruttura della shell remota
description: Gestione remota Windows versione 2,0 (WinRM 2,0) offre molti miglioramenti dell'infrastruttura della shell remota.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c67752222f1ca969ea254164a25144168d1eb3
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "104046225"
---
# <a name="remote-shell-infrastructure-improvements"></a>Miglioramenti dell'infrastruttura della shell remota

Gestione remota Windows versione 2,0 (WinRM 2,0) offre molti miglioramenti dell'infrastruttura della shell remota. Negli argomenti seguenti vengono descritti in dettaglio questi miglioramenti:

-   [Supporto di più hop](multi-hop-support.md)
-   [Gestione delle quote per le shell remote](quotas.md)

Uno dei miglioramenti apportati all'infrastruttura della shell remota WinRM è costituito dall'aggiunta di una gestione Shell più affidabile che mantiene le informazioni sulla shell specifiche dell'utente. Gli utenti WinRM possono creare Shell sui computer remoti per eseguire comandi o script. Inoltre, gli utenti possono creare più shell in un computer. Gli utenti e gli amministratori devono avere la possibilità di gestire le shell. Gli utenti possono enumerare, ottenere ed eliminare le shell create. Gli amministratori possono enumerare tutte le Shell attive e recuperare i dettagli relativi a Shell specifiche in un host locale o remoto. Gli amministratori possono inoltre eliminare eventuali Shell attive in un host locale o remoto.

Quando un utente o un amministratore enumera le Shell attive, il servizio WinRM può restituire le informazioni seguenti.

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId
</dt> <dd>

Specifica l'identificatore univoco della shell.

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variabili di ambiente
</dt> <dd>

Specifica le variabili di ambiente impostate dall'utente.

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory
</dt> <dd>

Specifica la directory iniziale per la Shell.

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI
</dt> <dd>

Specifica l'URI della risorsa per l'operazione della shell. L'URI della risorsa può essere usato per recuperare la configurazione del plug-in specifica per l'istanza della shell.

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Specifica la durata massima, in millisecondi, per cui la shell resterà aperta senza alcuna richiesta.

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams
</dt> <dd>

Specifica i flussi di input per la Shell.

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams
</dt> <dd>

Specifica i flussi di output per la Shell.

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Ora di creazione della shell
</dt> <dd>

Specifica il timestamp di creazione della shell.

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>Tempoinattività
</dt> <dd>

Specifica la durata, in millisecondi, in cui la shell è rimasta inattiva.

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId
</dt> <dd>

Specifica l'ID utente.

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nome host o indirizzo IP
</dt> <dd>

Specifica il nome host o l'indirizzo IP del computer che ha creato la Shell.

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Utilizzo memoria Shell
</dt> <dd>

Specifica la quantità di memoria utilizzata dalla Shell.

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Numero di processi
</dt> <dd>

Specifica il numero di processi creati dalla Shell.

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>Enumerazione di una shell in un host locale

Il comando seguente illustra come usare l'utilità WinRM per enumerare le shell in un client WinRM: **WinRM enumera Shell**.

Nell'esempio basato su testo seguente viene visualizzato l'output per l'enumerazione Shell:

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

Per ulteriori informazioni, vedere la guida online fornita eseguendo il comando seguente: **WinRM enumerate-?**.

## <a name="retrieving-information-about-a-specific-shell"></a>Recupero di informazioni su una shell specifica

Un amministratore o un utente può anche usare l'identificatore ShellId per recuperare le informazioni sulla Shell. Il comando seguente illustra come usare l'utilità WinRM per ottenere informazioni su una shell specifica: **WinRM Get Shell? ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.

Nell'esempio basato su testo seguente viene visualizzato l'output per le informazioni della shell:

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

Per ulteriori informazioni, vedere la guida online fornita dal comando seguente: **WinRM Get-?**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto di più hop](multi-hop-support.md)
</dt> <dt>

[Gestione delle quote per le shell remote](quotas.md)
</dt> <dt>

[Riferimenti gestiti per i comandi di WS-Management PowerShell](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




