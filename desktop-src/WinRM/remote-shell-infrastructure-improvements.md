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
# <a name="remote-shell-infrastructure-improvements"></a><span data-ttu-id="e52df-103">Miglioramenti dell'infrastruttura della shell remota</span><span class="sxs-lookup"><span data-stu-id="e52df-103">Remote Shell Infrastructure Improvements</span></span>

<span data-ttu-id="e52df-104">Gestione remota Windows versione 2,0 (WinRM 2,0) offre molti miglioramenti dell'infrastruttura della shell remota.</span><span class="sxs-lookup"><span data-stu-id="e52df-104">Windows Remote Management version 2.0 (WinRM 2.0) offers many remote shell infrastructure improvements.</span></span> <span data-ttu-id="e52df-105">Negli argomenti seguenti vengono descritti in dettaglio questi miglioramenti:</span><span class="sxs-lookup"><span data-stu-id="e52df-105">The following topics describe these improvements in detail:</span></span>

-   [<span data-ttu-id="e52df-106">Supporto di più hop</span><span class="sxs-lookup"><span data-stu-id="e52df-106">Multi-Hop Support</span></span>](multi-hop-support.md)
-   [<span data-ttu-id="e52df-107">Gestione delle quote per le shell remote</span><span class="sxs-lookup"><span data-stu-id="e52df-107">Quota Management for Remote Shells</span></span>](quotas.md)

<span data-ttu-id="e52df-108">Uno dei miglioramenti apportati all'infrastruttura della shell remota WinRM è costituito dall'aggiunta di una gestione Shell più affidabile che mantiene le informazioni sulla shell specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e52df-108">One of the improvements to the WinRM remote shell infrastructure is the addition of a more robust shell manager that maintains user-specific shell information.</span></span> <span data-ttu-id="e52df-109">Gli utenti WinRM possono creare Shell sui computer remoti per eseguire comandi o script.</span><span class="sxs-lookup"><span data-stu-id="e52df-109">WinRM users can create shells on remote computers to run commands or scripts.</span></span> <span data-ttu-id="e52df-110">Inoltre, gli utenti possono creare più shell in un computer.</span><span class="sxs-lookup"><span data-stu-id="e52df-110">In addition, users can create multiple shells on a computer.</span></span> <span data-ttu-id="e52df-111">Gli utenti e gli amministratori devono avere la possibilità di gestire le shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-111">Users and administrators both need the ability to manage shells.</span></span> <span data-ttu-id="e52df-112">Gli utenti possono enumerare, ottenere ed eliminare le shell create.</span><span class="sxs-lookup"><span data-stu-id="e52df-112">Users can enumerate, get, and delete the shells that they have created.</span></span> <span data-ttu-id="e52df-113">Gli amministratori possono enumerare tutte le Shell attive e recuperare i dettagli relativi a Shell specifiche in un host locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="e52df-113">Administrators can enumerate over all active shells and retrieve details about specific shells on a local or remote host.</span></span> <span data-ttu-id="e52df-114">Gli amministratori possono inoltre eliminare eventuali Shell attive in un host locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="e52df-114">Administrators can also delete any active shells on a local or remote host.</span></span>

<span data-ttu-id="e52df-115">Quando un utente o un amministratore enumera le Shell attive, il servizio WinRM può restituire le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e52df-115">When a user or administrator enumerates the active shells, the following information can be returned by the WinRM service.</span></span>

<dl> <dt>

<span data-ttu-id="e52df-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span><span class="sxs-lookup"><span data-stu-id="e52df-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span></span>
</dt> <dd>

<span data-ttu-id="e52df-117">Specifica l'identificatore univoco della shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-117">Specifies the unique identifier for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="e52df-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Environment variables</span></span>
</dt> <dd>

<span data-ttu-id="e52df-119">Specifica le variabili di ambiente impostate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e52df-119">Specifies any environment variables set by the user.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="e52df-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span></span>
</dt> <dd>

<span data-ttu-id="e52df-121">Specifica la directory iniziale per la Shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-121">Specifies the starting directory for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span><span class="sxs-lookup"><span data-stu-id="e52df-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span></span>
</dt> <dd>

<span data-ttu-id="e52df-123">Specifica l'URI della risorsa per l'operazione della shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-123">Specifies the resource URI for the shell operation.</span></span> <span data-ttu-id="e52df-124">L'URI della risorsa può essere usato per recuperare la configurazione del plug-in specifica per l'istanza della shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-124">The resource URI can be used to retrieve plug-in configuration that is specific to the shell instance.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="e52df-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="e52df-126">Specifica la durata massima, in millisecondi, per cui la shell resterà aperta senza alcuna richiesta.</span><span class="sxs-lookup"><span data-stu-id="e52df-126">Specifies the maximum duration, in milliseconds, that the shell will stay open without any request.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span><span class="sxs-lookup"><span data-stu-id="e52df-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span></span>
</dt> <dd>

<span data-ttu-id="e52df-128">Specifica i flussi di input per la Shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-128">Specifies the input streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span><span class="sxs-lookup"><span data-stu-id="e52df-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span></span>
</dt> <dd>

<span data-ttu-id="e52df-130">Specifica i flussi di output per la Shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-130">Specifies the output streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Ora di creazione della shell</span><span class="sxs-lookup"><span data-stu-id="e52df-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell creation time</span></span>
</dt> <dd>

<span data-ttu-id="e52df-132">Specifica il timestamp di creazione della shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-132">Specifies the creation timestamp for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>Tempoinattività</span><span class="sxs-lookup"><span data-stu-id="e52df-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span></span>
</dt> <dd>

<span data-ttu-id="e52df-134">Specifica la durata, in millisecondi, in cui la shell è rimasta inattiva.</span><span class="sxs-lookup"><span data-stu-id="e52df-134">Specifies the duration, in milliseconds, that the shell has been idle.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span><span class="sxs-lookup"><span data-stu-id="e52df-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span></span>
</dt> <dd>

<span data-ttu-id="e52df-136">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="e52df-136">Specifies the user ID.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nome host o indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="e52df-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname or IP address</span></span>
</dt> <dd>

<span data-ttu-id="e52df-138">Specifica il nome host o l'indirizzo IP del computer che ha creato la Shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-138">Specifies either the host name or IP address of the computer that created the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Utilizzo memoria Shell</span><span class="sxs-lookup"><span data-stu-id="e52df-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell memory usage</span></span>
</dt> <dd>

<span data-ttu-id="e52df-140">Specifica la quantità di memoria utilizzata dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-140">Specifies the amount of memory that has been used by the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e52df-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Numero di processi</span><span class="sxs-lookup"><span data-stu-id="e52df-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Number of processes</span></span>
</dt> <dd>

<span data-ttu-id="e52df-142">Specifica il numero di processi creati dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-142">Specifies the number of processes that have been created by the shell.</span></span>

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a><span data-ttu-id="e52df-143">Enumerazione di una shell in un host locale</span><span class="sxs-lookup"><span data-stu-id="e52df-143">Enumerating a Shell on a Local Host</span></span>

<span data-ttu-id="e52df-144">Il comando seguente illustra come usare l'utilità WinRM per enumerare le shell in un client WinRM: **WinRM enumera Shell**.</span><span class="sxs-lookup"><span data-stu-id="e52df-144">The following command demonstrates how to use the winrm utility to enumerate shells on a WinRM client: **winrm enumerate shell**.</span></span>

<span data-ttu-id="e52df-145">Nell'esempio basato su testo seguente viene visualizzato l'output per l'enumerazione Shell:</span><span class="sxs-lookup"><span data-stu-id="e52df-145">The following text-based example displays the output for shell enumeration:</span></span>

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

<span data-ttu-id="e52df-146">Per ulteriori informazioni, vedere la guida online fornita eseguendo il comando seguente: **WinRM enumerate-?**.</span><span class="sxs-lookup"><span data-stu-id="e52df-146">For more information, see the online help provided by running the following command: **winrm enumerate -?**.</span></span>

## <a name="retrieving-information-about-a-specific-shell"></a><span data-ttu-id="e52df-147">Recupero di informazioni su una shell specifica</span><span class="sxs-lookup"><span data-stu-id="e52df-147">Retrieving Information About a Specific Shell</span></span>

<span data-ttu-id="e52df-148">Un amministratore o un utente può anche usare l'identificatore ShellId per recuperare le informazioni sulla Shell.</span><span class="sxs-lookup"><span data-stu-id="e52df-148">An administrator or user can also use the ShellId identifier to retrieve information about the shell.</span></span> <span data-ttu-id="e52df-149">Il comando seguente illustra come usare l'utilità WinRM per ottenere informazioni su una shell specifica: **WinRM Get Shell? ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span><span class="sxs-lookup"><span data-stu-id="e52df-149">The following command demonstrates how to use the winrm utility to get information about a specific shell: **winrm get shell?ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span></span>

<span data-ttu-id="e52df-150">Nell'esempio basato su testo seguente viene visualizzato l'output per le informazioni della shell:</span><span class="sxs-lookup"><span data-stu-id="e52df-150">The following text-based example displays the output for shell information:</span></span>

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

<span data-ttu-id="e52df-151">Per ulteriori informazioni, vedere la guida online fornita dal comando seguente: **WinRM Get-?**.</span><span class="sxs-lookup"><span data-stu-id="e52df-151">For more information, see the online help provided by the following command: **winrm get -?**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e52df-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e52df-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e52df-153">Supporto di più hop</span><span class="sxs-lookup"><span data-stu-id="e52df-153">Multi-Hop Support</span></span>](multi-hop-support.md)
</dt> <dt>

[<span data-ttu-id="e52df-154">Gestione delle quote per le shell remote</span><span class="sxs-lookup"><span data-stu-id="e52df-154">Quota Management for Remote Shells</span></span>](quotas.md)
</dt> <dt>

[<span data-ttu-id="e52df-155">Riferimenti gestiti per i comandi di WS-Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="e52df-155">Managed Reference for WS-Management PowerShell Commands</span></span>](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




