---
title: Raccolta di dump di User-Mode
description: A partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1), è possibile configurare Segnalazione errori Windows (WER) in modo che i dump completi della modalità utente vengano raccolti e archiviati localmente dopo l'arresto anomalo di un'applicazione in modalità utente.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872338"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="c739d-103">Raccolta di dump di User-Mode</span><span class="sxs-lookup"><span data-stu-id="c739d-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="c739d-104">A partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1), è possibile configurare Segnalazione errori Windows (WER) in modo che i dump completi della modalità utente vengano raccolti e archiviati localmente dopo l'arresto anomalo di un'applicazione in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="c739d-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="c739d-105">Questa funzionalità non supporta le applicazioni che eseguono una segnalazione di arresti anomali personalizzata, incluse le applicazioni .NET.</span><span class="sxs-lookup"><span data-stu-id="c739d-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="c739d-106">Per impostazione predefinita questa funzionalità non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="c739d-106">This feature is not enabled by default.</span></span> <span data-ttu-id="c739d-107">Per abilitare la funzionalità sono necessari i privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="c739d-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="c739d-108">Per abilitare e configurare la funzionalità, usare i seguenti valori del registro di sistema nella chiave **HKEY \_ locale \_ \\ software \\ Microsoft \\ Windows \\ segnalazione errori Windows \\ LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="c739d-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c739d-109">Valore</span><span class="sxs-lookup"><span data-stu-id="c739d-109">Value</span></span></th>
<th><span data-ttu-id="c739d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c739d-110">Description</span></span></th>
<th><span data-ttu-id="c739d-111">Type</span><span class="sxs-lookup"><span data-stu-id="c739d-111">Type</span></span></th>
<th><span data-ttu-id="c739d-112">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="c739d-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c739d-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="c739d-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="c739d-114">Percorso in cui archiviare i file di dump.</span><span class="sxs-lookup"><span data-stu-id="c739d-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="c739d-115">Se non si usa il percorso predefinito, assicurarsi che la cartella contenga ACL che consentono al processo di arresto anomalo di scrivere i dati nella cartella.</span><span class="sxs-lookup"><span data-stu-id="c739d-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="c739d-116">Per gli arresti anomali del servizio, il dump viene scritto in cartelle di profili specifiche del servizio a seconda dell'account di servizio utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c739d-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="c739d-117">Ad esempio, la cartella del profilo per i servizi di sistema è%WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="c739d-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="c739d-118">Per i servizi di rete e locali, la cartella è%WINDIR%\ServiceProfiles.</span><span class="sxs-lookup"><span data-stu-id="c739d-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="c739d-119">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="c739d-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="c739d-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="c739d-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c739d-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="c739d-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="c739d-122">Numero massimo di file di dump nella cartella.</span><span class="sxs-lookup"><span data-stu-id="c739d-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="c739d-123">Quando viene superato il valore massimo, il file di dump meno recente nella cartella verrà sostituito con il nuovo file di dump.</span><span class="sxs-lookup"><span data-stu-id="c739d-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="c739d-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c739d-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="c739d-125">10</span><span class="sxs-lookup"><span data-stu-id="c739d-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c739d-126"><strong>DumpType</strong></span><span class="sxs-lookup"><span data-stu-id="c739d-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="c739d-127">Specificare uno dei seguenti tipi di dump:</span><span class="sxs-lookup"><span data-stu-id="c739d-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="c739d-128">0: dump personalizzato</span><span class="sxs-lookup"><span data-stu-id="c739d-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="c739d-129">1: dump minimo</span><span class="sxs-lookup"><span data-stu-id="c739d-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="c739d-130">2: dump completo</span><span class="sxs-lookup"><span data-stu-id="c739d-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="c739d-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c739d-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="c739d-132">1</span><span class="sxs-lookup"><span data-stu-id="c739d-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c739d-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="c739d-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="c739d-134">Opzioni di dump personalizzate da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c739d-134">The custom dump options to be used.</span></span> <span data-ttu-id="c739d-135">Questo valore viene utilizzato solo quando <strong>DumpType</strong> è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="c739d-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="c739d-136">Le opzioni sono una combinazione bit per bit dei valori di enumerazione <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c739d-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="c739d-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c739d-137">REG_DWORD</span></span></td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="c739d-138">Un dump di arresto anomalo del sistema non viene raccolto quando si imposta il [debug automatico per arresti anomali **dell'applicazione**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)</span><span class="sxs-lookup"><span data-stu-id="c739d-138">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="c739d-139">Questi valori del registro di sistema rappresentano le impostazioni globali.</span><span class="sxs-lookup"><span data-stu-id="c739d-139">These registry values represent the global settings.</span></span> <span data-ttu-id="c739d-140">È anche possibile specificare impostazioni per applicazione che eseguono l'override delle impostazioni globali.</span><span class="sxs-lookup"><span data-stu-id="c739d-140">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="c739d-141">Per creare un'impostazione per ogni applicazione, creare una nuova chiave per l'applicazione in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ segnalazione errori Windows \\ LocalDumps** (ad esempio, **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ segnalazione errori Windows \\ LocalDumps \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="c739d-141">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="c739d-142">Aggiungere le impostazioni di dump sotto la chiave **MyApplication.exe** .</span><span class="sxs-lookup"><span data-stu-id="c739d-142">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="c739d-143">Se l'applicazione si arresta in modo anomalo, WER legge prima le impostazioni globali e quindi esegue l'override di qualsiasi impostazione con le impostazioni specifiche dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c739d-143">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="c739d-144">Dopo l'arresto anomalo di un'applicazione e prima della terminazione, il sistema verificherà le impostazioni del registro di sistema per determinare se è necessario raccogliere un dump locale.</span><span class="sxs-lookup"><span data-stu-id="c739d-144">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="c739d-145">Al termine della raccolta di dump, l'applicazione verrà terminata normalmente.</span><span class="sxs-lookup"><span data-stu-id="c739d-145">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="c739d-146">Se l'applicazione supporta il ripristino, il dump locale viene raccolto prima che venga chiamato il callback di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c739d-146">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="c739d-147">Questi dump sono configurati e controllati indipendentemente dal resto dell'infrastruttura di WER.</span><span class="sxs-lookup"><span data-stu-id="c739d-147">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="c739d-148">È possibile usare la raccolta di dump locale anche se WER è disabilitato o se l'utente annulla la segnalazione di WER.</span><span class="sxs-lookup"><span data-stu-id="c739d-148">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="c739d-149">Il dump locale può essere diverso dal dump inviato a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c739d-149">The local dump can be different than the dump sent to Microsoft.</span></span>

 

