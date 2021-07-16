---
title: Raccolta User-Mode dump
description: A partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1), è possibile configurare Segnalazione errori Windows (WER) in modo che i dump completi in modalità utente siano raccolti e archiviati in locale dopo l'arresto anomalo di un'applicazione in modalità utente.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6291d3ad8dfeb641582a93f6789ca7844594ad
ms.sourcegitcommit: 892997f4126d44df413286074e08a9c6065313ec
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/16/2021
ms.locfileid: "114300186"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="7e91c-103">Raccolta User-Mode dump</span><span class="sxs-lookup"><span data-stu-id="7e91c-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="7e91c-104">A partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1), è possibile configurare Segnalazione errori Windows (WER) in modo che i dump completi in modalità utente siano raccolti e archiviati in locale dopo l'arresto anomalo di un'applicazione in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="7e91c-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="7e91c-105">Le applicazioni che esere la propria segnalazione di arresti anomalo del sistema, incluse le applicazioni .NET, non sono supportate da questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7e91c-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="7e91c-106">Per impostazione predefinita questa funzionalità non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="7e91c-106">This feature is not enabled by default.</span></span> <span data-ttu-id="7e91c-107">L'abilitazione della funzionalità richiede privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="7e91c-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="7e91c-108">Per abilitare e configurare la funzionalità, usare i valori del Registro di sistema seguenti nella **chiave HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Segnalazione errori Windows \_ \\ \\ \\ \\ \\ LocalDumps.**</span><span class="sxs-lookup"><span data-stu-id="7e91c-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e91c-109">Valore</span><span class="sxs-lookup"><span data-stu-id="7e91c-109">Value</span></span></th>
<th><span data-ttu-id="7e91c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e91c-110">Description</span></span></th>
<th><span data-ttu-id="7e91c-111">Type</span><span class="sxs-lookup"><span data-stu-id="7e91c-111">Type</span></span></th>
<th><span data-ttu-id="7e91c-112">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="7e91c-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e91c-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="7e91c-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="7e91c-114">Percorso in cui archiviare i file di dump.</span><span class="sxs-lookup"><span data-stu-id="7e91c-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="7e91c-115">Se non si usa il percorso predefinito, assicurarsi che la cartella contenga ACL che consentono al processo di arresto anomalo di scrivere dati nella cartella.</span><span class="sxs-lookup"><span data-stu-id="7e91c-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="7e91c-116">Per gli arresti anomali del servizio, il dump viene scritto in cartelle del profilo specifiche del servizio a seconda dell'account del servizio usato.</span><span class="sxs-lookup"><span data-stu-id="7e91c-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="7e91c-117">Ad esempio, la cartella del profilo per i servizi di sistema è %WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="7e91c-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="7e91c-118">Per Servizi di rete e locali, la cartella è %WINDIR%\ServiceProfiles.</span><span class="sxs-lookup"><span data-stu-id="7e91c-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="7e91c-119">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="7e91c-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="7e91c-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="7e91c-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e91c-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="7e91c-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="7e91c-122">Numero massimo di file di dump nella cartella.</span><span class="sxs-lookup"><span data-stu-id="7e91c-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="7e91c-123">Quando viene superato il valore massimo, il file di dump meno recente nella cartella verrà sostituito con il nuovo file dump.</span><span class="sxs-lookup"><span data-stu-id="7e91c-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="7e91c-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7e91c-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="7e91c-125">10</span><span class="sxs-lookup"><span data-stu-id="7e91c-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e91c-126"><strong>DumpType</strong></span><span class="sxs-lookup"><span data-stu-id="7e91c-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="7e91c-127">Specificare uno dei tipi di dump seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e91c-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="7e91c-128">0: dump personalizzato</span><span class="sxs-lookup"><span data-stu-id="7e91c-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="7e91c-129">1: Mini dump</span><span class="sxs-lookup"><span data-stu-id="7e91c-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="7e91c-130">2: Dump completo</span><span class="sxs-lookup"><span data-stu-id="7e91c-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="7e91c-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7e91c-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="7e91c-132">1</span><span class="sxs-lookup"><span data-stu-id="7e91c-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e91c-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="7e91c-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="7e91c-134">Opzioni di dump personalizzate da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7e91c-134">The custom dump options to be used.</span></span> <span data-ttu-id="7e91c-135">Questo valore viene usato solo quando <strong>DumpType</strong> è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="7e91c-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="7e91c-136">Le opzioni sono una combinazione bit per bit dei <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="7e91c-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="7e91c-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7e91c-137">REG_DWORD</span></span></td>
 <td><span data-ttu-id="7e91c-138"><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></span><span class="sxs-lookup"><span data-stu-id="7e91c-138"><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></span></span></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="7e91c-139">Un dump di arresto anomalo del sistema non viene raccolto quando si imposta il debug automatico per gli arresti [ **anomali dell'applicazione.**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)</span><span class="sxs-lookup"><span data-stu-id="7e91c-139">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="7e91c-140">Questi valori del Registro di sistema rappresentano le impostazioni globali.</span><span class="sxs-lookup"><span data-stu-id="7e91c-140">These registry values represent the global settings.</span></span> <span data-ttu-id="7e91c-141">È anche possibile specificare impostazioni per applicazione che sostituiscono le impostazioni globali.</span><span class="sxs-lookup"><span data-stu-id="7e91c-141">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="7e91c-142">Per creare un'impostazione per applicazione, creare una nuova chiave per l'applicazione in **HKEY \_ LOCAL MACHINE Software Microsoft Windows Segnalazione errori Windows \_ \\ \\ \\ \\ \\ LocalDumps** (ad **esempio, HKEY \_ LOCAL MACHINE Software Microsoft Windows Segnalazione errori Windows \_ \\ \\ \\ \\ \\ LocalDumps \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="7e91c-142">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="7e91c-143">Aggiungere le impostazioni di dump nella **chiaveMyApplication.exe** dump.</span><span class="sxs-lookup"><span data-stu-id="7e91c-143">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="7e91c-144">Se l'applicazione si arresta in modo anomalo, WER leggerà prima le impostazioni globali e quindi eseguirà l'override di qualsiasi impostazione con le impostazioni specifiche dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e91c-144">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="7e91c-145">Dopo l'arresto anomalo di un'applicazione e prima della chiusura, il sistema controlla le impostazioni del Registro di sistema per determinare se deve essere raccolto un dump locale.</span><span class="sxs-lookup"><span data-stu-id="7e91c-145">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="7e91c-146">Al termine della raccolta di dump, l'applicazione sarà autorizzata a terminare normalmente.</span><span class="sxs-lookup"><span data-stu-id="7e91c-146">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="7e91c-147">Se l'applicazione supporta il ripristino, il dump locale viene raccolto prima che venga chiamato il callback di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7e91c-147">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="7e91c-148">Questi dump vengono configurati e controllati indipendentemente dal resto dell'infrastruttura WER.</span><span class="sxs-lookup"><span data-stu-id="7e91c-148">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="7e91c-149">È possibile usare la raccolta di dump locali anche se WER è disabilitato o se l'utente annulla la creazione di report WER.</span><span class="sxs-lookup"><span data-stu-id="7e91c-149">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="7e91c-150">Il dump locale può essere diverso dal dump inviato a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7e91c-150">The local dump can be different than the dump sent to Microsoft.</span></span>

 

