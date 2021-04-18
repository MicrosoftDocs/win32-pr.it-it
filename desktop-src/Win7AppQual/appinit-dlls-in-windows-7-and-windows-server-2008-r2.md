---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318896"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="1ad35-103">\_Dll di AppInit in Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ad35-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="1ad35-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="1ad35-104">Platform</span></span>

<span data-ttu-id="1ad35-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ad35-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="1ad35-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ad35-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="1ad35-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="1ad35-107">Feature Impact</span></span>

 <span data-ttu-id="1ad35-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="1ad35-108">**Severity** - Low</span></span>  
<span data-ttu-id="1ad35-109">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="1ad35-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="1ad35-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ad35-110">Description</span></span>

<span data-ttu-id="1ad35-111">AppInit \_ dll è un meccanismo che consente di caricare un elenco arbitrario di dll in ogni processo in modalità utente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1ad35-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="1ad35-112">Microsoft sta modificando la funzionalità dll di AppInit in Windows 7 e Windows Server 2008 R2 per aggiungere un nuovo requisito per la firma del codice.</span><span class="sxs-lookup"><span data-stu-id="1ad35-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="1ad35-113">Ciò consentirà di migliorare l'affidabilità e le prestazioni del sistema, nonché di migliorare la visibilità dell'origine del software.</span><span class="sxs-lookup"><span data-stu-id="1ad35-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="1ad35-114">Configurazione</span><span class="sxs-lookup"><span data-stu-id="1ad35-114">Configuration</span></span>

<span data-ttu-id="1ad35-115">I valori archiviati in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows Key nel registro di sistema determinano il comportamento dell' \_ infrastruttura di DLL AppInit.</span><span class="sxs-lookup"><span data-stu-id="1ad35-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="1ad35-116">La tabella seguente descrive i valori del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="1ad35-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1ad35-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1ad35-117">Value</span></span></th>
<th><span data-ttu-id="1ad35-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ad35-118">Description</span></span></th>
<th><span data-ttu-id="1ad35-119">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="1ad35-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="1ad35-120">LoadAppInit_DLLs (REG_DWORD) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1ad35-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="1ad35-121">Abilita o Disabilita globalmente AppInit_DLLs. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1ad35-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1ad35-122">0x0: AppInit_DLLs sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="1ad35-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ad35-123">0x1: AppInit_DLLs sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="1ad35-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="1ad35-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="1ad35-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="1ad35-125">Spazio o elenco delimitato da virgole di dll da caricare.</span><span class="sxs-lookup"><span data-stu-id="1ad35-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="1ad35-126">Il percorso completo della DLL deve essere specificato utilizzando nomi brevi.</span><span class="sxs-lookup"><span data-stu-id="1ad35-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="1ad35-127">C:\ PROGRA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</span><span class="sxs-lookup"><span data-stu-id="1ad35-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="1ad35-128">RequireSignedAppInit_DLLs (REG_DWORD) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1ad35-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="1ad35-129">Carica solo le dll con firma codice. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1ad35-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1ad35-130">0x0: carica qualsiasi dll.</span><span class="sxs-lookup"><span data-stu-id="1ad35-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ad35-131">0x1: carica solo le dll con firma di codice.</span><span class="sxs-lookup"><span data-stu-id="1ad35-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="1ad35-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="1ad35-132">**Windows 7**</span></span>

<span data-ttu-id="1ad35-133">Tutte le DLL caricate dall'infrastruttura di \_ DLL AppInit devono essere firmate dal codice.</span><span class="sxs-lookup"><span data-stu-id="1ad35-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="1ad35-134">Per motivi di compatibilità delle applicazioni, il sistema operativo Windows 7 caricherà tutte le DLL AppInit.</span><span class="sxs-lookup"><span data-stu-id="1ad35-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="1ad35-135">Tuttavia, Microsoft consiglia a tutti gli sviluppatori di applicazioni di firmare il codice delle proprie DLL per migliorare l'affidabilità di Windows e prepararsi per l'imposizione della firma del codice nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="1ad35-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="1ad35-136">La \_ chiave del registro di sistema dll RequireSignedAppInit controlla questo comportamento e il relativo valore in Windows 7 è impostato su 0 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1ad35-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="1ad35-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ad35-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="1ad35-138">Tutte le DLL caricate dall' \_ infrastruttura dll di AppInit devono avere la firma del codice.</span><span class="sxs-lookup"><span data-stu-id="1ad35-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="1ad35-139">La \_ chiave del registro di sistema dll RequireSignedAppInit controlla questo comportamento e il relativo valore in Windows Server 2008 R2 è impostato su 1 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1ad35-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1ad35-140">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="1ad35-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="1ad35-141">Dll di AppInit in Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ad35-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
