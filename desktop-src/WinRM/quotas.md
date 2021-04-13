---
title: Gestione delle quote per le shell remote
description: Gestione delle quote consente agli utenti di gestire le risorse di sistema in modo più efficiente.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331759"
---
# <a name="quota-management-for-remote-shells"></a><span data-ttu-id="a9fb5-103">Gestione delle quote per le shell remote</span><span class="sxs-lookup"><span data-stu-id="a9fb5-103">Quota Management for Remote Shells</span></span>

<span data-ttu-id="a9fb5-104">Gestione delle quote consente agli utenti di gestire le risorse di sistema in modo più efficiente.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-104">Quota management allows users to manage system resources more efficiently.</span></span> <span data-ttu-id="a9fb5-105">Gestione remota Windows (WinRM) ha aggiunto un set specifico di quote che forniscono una migliore qualità del servizio, consentono di evitare problemi di tipo Denial of Service e di allocare le risorse del server agli utenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-105">Windows Remote Management (WinRM) has added a specific set of quotas that provide a better quality of service, help prevent denial of service issues, and allocate server resources to concurrent users.</span></span> <span data-ttu-id="a9fb5-106">Il set di quote WinRM è basato sull'infrastruttura delle quote implementata per il servizio Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="a9fb5-106">The WinRM quota set is based on the quota infrastructure that is implemented for the Internet Information Services (IIS) service.</span></span>

<span data-ttu-id="a9fb5-107">L'implementazione delle quote consentirà di evitare il calo delle prestazioni e problemi di tipo Denial of Service effettuando le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9fb5-107">Implementing quotas will help to prevent performance degradation and denial of service issues by doing the following:</span></span>

-   <span data-ttu-id="a9fb5-108">Limitazione del numero di Shell e processi shell che un utente può creare</span><span class="sxs-lookup"><span data-stu-id="a9fb5-108">Limiting the number of shells and shell processes that a user can create</span></span>
-   <span data-ttu-id="a9fb5-109">Limitazione del numero massimo di utenti simultanei</span><span class="sxs-lookup"><span data-stu-id="a9fb5-109">Limiting the maximum number of concurrent users</span></span>
-   <span data-ttu-id="a9fb5-110">Gestione della quantità di memoria allocata a una shell</span><span class="sxs-lookup"><span data-stu-id="a9fb5-110">Managing the amount of memory that is allocated to a shell</span></span>
-   <span data-ttu-id="a9fb5-111">Impostazione di un timeout per le shell inattive</span><span class="sxs-lookup"><span data-stu-id="a9fb5-111">Setting a time-out for shells that are inactive</span></span>

## <a name="quota-settings"></a><span data-ttu-id="a9fb5-112">Impostazioni quota</span><span class="sxs-lookup"><span data-stu-id="a9fb5-112">Quota Settings</span></span>

<span data-ttu-id="a9fb5-113">Per la gestione della shell remota è necessario applicare le quote seguenti.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-113">The following quotas need to be enforced for remote shell management.</span></span> <span data-ttu-id="a9fb5-114">Queste quote possono essere configurate tramite l'utilità WinRM o tramite Criteri di gruppo impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-114">These quotas can be configured through the winrm utility or through Group Policy settings.</span></span> <span data-ttu-id="a9fb5-115">Le impostazioni configurate da un Criteri di gruppo sostituiscono le quote impostate dall'utilità WinRM.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-115">Settings configured by a Group Policy supersede the quotas set by the winrm utility.</span></span> <span data-ttu-id="a9fb5-116">Per ulteriori informazioni sull'impostazione dei criteri di gruppo per WinRM, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="a9fb5-116">For more information about setting Group Policies for WinRM, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<dl> <dt>

<span data-ttu-id="a9fb5-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="a9fb5-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="a9fb5-118">Tempo massimo, in millisecondi, prima dell'eliminazione di una shell remota inattiva.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-118">The maximum time in milliseconds before an inactive remote shell is deleted.</span></span> <span data-ttu-id="a9fb5-119">Il valore predefinito è 180000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-119">The default is 180000 milliseconds.</span></span> <span data-ttu-id="a9fb5-120">Il tempo minimo è pari a 1000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-120">The minimum time is 1000 milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="a9fb5-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span><span class="sxs-lookup"><span data-stu-id="a9fb5-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span></span>
</dt> <dd>

<span data-ttu-id="a9fb5-122">Numero massimo di processi consentiti per Shell, inclusi i processi figlio della shell.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-122">The maximum number of processes allowed per shell, including the shell's child processes.</span></span> <span data-ttu-id="a9fb5-123">Il valore predefinito è 25.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-123">The default is 25.</span></span>

</dd> <dt>

<span data-ttu-id="a9fb5-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span><span class="sxs-lookup"><span data-stu-id="a9fb5-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span></span>
</dt> <dd>

<span data-ttu-id="a9fb5-125">Quantità massima di memoria allocata per Shell, inclusi i processi figlio della shell.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-125">The maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="a9fb5-126">Il valore predefinito è 1024 MB.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-126">The default is 1024 MB.</span></span>

> [!Note]  
> <span data-ttu-id="a9fb5-127">Il comportamento non è supportato se MaxMemoryPerShellMB è impostato su un valore minore di quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-127">The behavior is unsupported if the MaxMemoryPerShellMB is set to a value that is less than the default.</span></span>

 

</dd> <dt>

<span data-ttu-id="a9fb5-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span><span class="sxs-lookup"><span data-stu-id="a9fb5-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span></span>
</dt> <dd>

<span data-ttu-id="a9fb5-129">Numero massimo di Shell per utente.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-129">The maximum number of shells per user.</span></span> <span data-ttu-id="a9fb5-130">Il valore predefinito è 30.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-130">The default is 30.</span></span>

</dd> <dt>

<span data-ttu-id="a9fb5-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="a9fb5-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span></span>
</dt> <dd>

<span data-ttu-id="a9fb5-132">Numero massimo di utenti simultanei che possono aprire le shell.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-132">The maximum number of concurrent users who can open shells.</span></span> <span data-ttu-id="a9fb5-133">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-133">The default is 10.</span></span>

</dd> </dl>

## <a name="deprecated-quotas"></a><span data-ttu-id="a9fb5-134">Quote deprecate</span><span class="sxs-lookup"><span data-stu-id="a9fb5-134">Deprecated Quotas</span></span>

<span data-ttu-id="a9fb5-135">WinRM 2,0 imposta la quota MaxShellRunTime su sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-135">WinRM 2.0 sets the MaxShellRunTime quota to read-only.</span></span> <span data-ttu-id="a9fb5-136">La modifica del valore per questa quota non avrà alcun effetto sulle shell remote.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-136">Changing the value for this quota will have no effect on the remote shells.</span></span>

## <a name="retrieving-quota-configuration-information"></a><span data-ttu-id="a9fb5-137">Recupero delle informazioni di configurazione della quota</span><span class="sxs-lookup"><span data-stu-id="a9fb5-137">Retrieving Quota Configuration Information</span></span>

<span data-ttu-id="a9fb5-138">Per verificare le impostazioni di configurazione della quota, digitare **WinRM get winrm/config**.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-138">To check the quota configuration settings, type **winrm get winrm/config**.</span></span>

<span data-ttu-id="a9fb5-139">Il frammento di codice seguente è un esempio basato su testo di una configurazione WinRM con le impostazioni di quota predefinite.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-139">The following snippet is a text-based example of a WinRM configuration with the default quota settings.</span></span>

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a><span data-ttu-id="a9fb5-140">Configurazione delle quote della shell</span><span class="sxs-lookup"><span data-stu-id="a9fb5-140">Configuring Shell Quotas</span></span>

<span data-ttu-id="a9fb5-141">Le quote possono essere impostate tramite un'impostazione di Criteri di gruppo o manualmente.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-141">Quotas can be set through a Group Policy setting or manually.</span></span> <span data-ttu-id="a9fb5-142">Per ulteriori informazioni sulle impostazioni di configurazione specifiche, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="a9fb5-142">For more information about specific configuration settings, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="a9fb5-143">**Per impostare una quota con Criteri di gruppo**</span><span class="sxs-lookup"><span data-stu-id="a9fb5-143">**To set a quota with Group Policy**</span></span>

1.  <span data-ttu-id="a9fb5-144">Aprire una finestra del Prompt dei comandi come amministratore.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-144">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="a9fb5-145">Al prompt dei comandi digitare **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-145">At the Command Prompt, type **gpedit.msc**.</span></span> <span data-ttu-id="a9fb5-146">Viene visualizzata la finestra **Editor oggetti Criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="a9fb5-146">The **Group Policy Object Editor** window opens.</span></span>
3.  <span data-ttu-id="a9fb5-147">Trovare gli oggetti **gestione remota Windows** e **windows Remote Shell** criteri di gruppo (GPO) in **Configurazione computer \\ modelli amministrativi \\ componenti di Windows**.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-147">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4.  <span data-ttu-id="a9fb5-148">Nella scheda **esteso** selezionare un'impostazione per visualizzare una descrizione.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-148">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="a9fb5-149">Fare doppio clic su un'impostazione per modificarla.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-149">Double click a setting to edit it.</span></span>

<span data-ttu-id="a9fb5-150">**Per impostare una quota manualmente**</span><span class="sxs-lookup"><span data-stu-id="a9fb5-150">**To set a quota manually**</span></span>

1.  <span data-ttu-id="a9fb5-151">Aprire una finestra del Prompt dei comandi come amministratore.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-151">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="a9fb5-152">Al prompt dei comandi digitare **winrm set winrm/config/winrs ' @ { ***<Quota>*** = " ***<Value>*** "}'**</span><span class="sxs-lookup"><span data-stu-id="a9fb5-152">At the Command Prompt, type **winrm set winrm/config/winrs '@{***<Quota>***="***<Value>***"}'**</span></span>

<span data-ttu-id="a9fb5-153">Ad esempio, per aumentare il numero massimo di Shell per utente da 5 a 7, digitare **winrm set winrm/config/winrs ' @ {MaxShellsPerUser = "7"}'**.</span><span class="sxs-lookup"><span data-stu-id="a9fb5-153">For example, to increase the maximum number of shells per user from 5 to 7, type **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'**.</span></span>

 

 




