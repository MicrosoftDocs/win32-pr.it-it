---
description: AppInit_DLLs in Windows 7 e Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088709"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="4fd3e-103">DLL AppInit \_ in Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fd3e-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="4fd3e-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="4fd3e-104">Platform</span></span>

<span data-ttu-id="4fd3e-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="4fd3e-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="4fd3e-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fd3e-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="4fd3e-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="4fd3e-107">Feature Impact</span></span>

 <span data-ttu-id="4fd3e-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="4fd3e-108">**Severity** - Low</span></span>  
<span data-ttu-id="4fd3e-109">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="4fd3e-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="4fd3e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fd3e-110">Description</span></span>

<span data-ttu-id="4fd3e-111">Le DLL AppInit sono un meccanismo che consente il caricamento di un elenco arbitrario di DLL in ogni processo in modalità \_ utente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="4fd3e-112">Microsoft sta modificando la funzionalità delle DLL AppInit in Windows 7 e Windows Server 2008 R2 per aggiungere un nuovo requisito di firma del codice.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="4fd3e-113">Ciò consente di migliorare l'affidabilità e le prestazioni del sistema, nonché di migliorare la visibilità sull'origine del software.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="4fd3e-114">Configurazione</span><span class="sxs-lookup"><span data-stu-id="4fd3e-114">Configuration</span></span>

<span data-ttu-id="4fd3e-115">I valori archiviati nella chiave HKEY LOCAL MACHINE SOFTWARE Microsoft Windows NT currentVersion di Windows nel Registro di sistema determinano il comportamento dell'infrastruttura \_ \_ delle DLL \\ \\ \\ \\ \\ \_ AppInit.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="4fd3e-116">La tabella seguente descrive questi valori del Registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="4fd3e-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4fd3e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4fd3e-117">Value</span></span></th>
<th><span data-ttu-id="4fd3e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fd3e-118">Description</span></span></th>
<th><span data-ttu-id="4fd3e-119">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="4fd3e-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4fd3e-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="4fd3e-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="4fd3e-121">Abilita o disabilita a livello globale AppInit_DLLs.${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="4fd3e-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4fd3e-122">0x0: AppInit_DLLs disabilitate.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fd3e-123">0x1: AppInit_DLLs abilitate.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="4fd3e-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="4fd3e-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="4fd3e-125">Elenco delimitato da spazi o virgole di DLL da caricare.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="4fd3e-126">Il percorso completo della DLL deve essere specificato usando nomi brevi.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="4fd3e-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span><span class="sxs-lookup"><span data-stu-id="4fd3e-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="4fd3e-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="4fd3e-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="4fd3e-129">Caricare solo LE DLL firmate dal codice.${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="4fd3e-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4fd3e-130">0x0: caricare le DLL.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fd3e-131">0x1: caricare solo LE DLL firmate dal codice.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="4fd3e-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="4fd3e-132">**Windows 7**</span></span>

<span data-ttu-id="4fd3e-133">Tutte le DLL caricate dall'infrastruttura delle DLL AppInit devono \_ essere firmate dal codice.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="4fd3e-134">Nell'interesse della compatibilità delle applicazioni, il sistema operativo Windows 7 carica tutte le DLL AppInit.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="4fd3e-135">Tuttavia, Microsoft consiglia a tutti gli sviluppatori di applicazioni di firmare il codice delle DLL per migliorare l'affidabilità di Windows e prepararsi per l'applicazione della firma del codice nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="4fd3e-136">La chiave del Registro di sistema RequireSignedAppInit controlla questo comportamento e il relativo valore in Windows 7 è impostato \_ su 0 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="4fd3e-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4fd3e-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="4fd3e-138">Tutte le DLL caricate dall'infrastruttura delle DLL AppInit \_ devono essere firmate con codice.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="4fd3e-139">La chiave del Registro di sistema RequireSignedAppInit controlla questo comportamento e il relativo valore \_ in Windows Server 2008 R2 è impostato su 1 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4fd3e-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="4fd3e-140">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="4fd3e-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="4fd3e-141">DLL AppInit in Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fd3e-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
