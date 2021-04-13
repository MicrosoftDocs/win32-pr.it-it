---
title: Versioni di controllo comuni
description: Questo argomento elenca le versioni disponibili della libreria di controlli comuni (ComCtl32.dll), descrive come identificare la versione usata dall'applicazione e spiega come indirizzare l'applicazione per una versione specifica.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc51fe027e6169ab1c28904c3145be2f5042d9a0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474702"
---
# <a name="common-control-versions"></a><span data-ttu-id="97dff-103">Versioni di controllo comuni</span><span class="sxs-lookup"><span data-stu-id="97dff-103">Common Control Versions</span></span>

<span data-ttu-id="97dff-104">Questo argomento elenca le versioni disponibili della libreria di controlli comuni (ComCtl32.dll), descrive come identificare la versione usata dall'applicazione e spiega come indirizzare l'applicazione per una versione specifica.</span><span class="sxs-lookup"><span data-stu-id="97dff-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="97dff-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="97dff-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="97dff-106">Numeri delle versioni DLL di controllo comuni</span><span class="sxs-lookup"><span data-stu-id="97dff-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="97dff-107">Dimensioni della struttura per diverse versioni di controllo comuni</span><span class="sxs-lookup"><span data-stu-id="97dff-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="97dff-108">Utilizzo di DllGetVersion per determinare il numero di versione</span><span class="sxs-lookup"><span data-stu-id="97dff-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="97dff-109">Versioni del progetto</span><span class="sxs-lookup"><span data-stu-id="97dff-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="97dff-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97dff-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="97dff-111">Numeri delle versioni DLL di controllo comuni</span><span class="sxs-lookup"><span data-stu-id="97dff-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="97dff-112">Il supporto per i controlli comuni è fornito da ComCtl32.dll, che tutte le versioni a 32 bit e a 64 bit di Windows includono.</span><span class="sxs-lookup"><span data-stu-id="97dff-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="97dff-113">Ogni versione successiva della DLL supporta le funzionalità e le API delle versioni precedenti e aggiunge nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="97dff-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="97dff-114">Poiché le diverse versioni di ComCtl32.dll sono state distribuite con Internet Explorer, la versione attiva è a volte diversa dalla versione fornita con il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="97dff-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="97dff-115">Pertanto, l'applicazione deve determinare direttamente quale versione di ComCtl32.dll è presente.</span><span class="sxs-lookup"><span data-stu-id="97dff-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="97dff-116">Nella documentazione di riferimento dei controlli comuni, molti elementi di programmazione specificano un numero di versione di DLL minimo supportato.</span><span class="sxs-lookup"><span data-stu-id="97dff-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="97dff-117">Questo numero di versione indica che l'elemento di programmazione viene implementato in tale versione e nelle versioni successive della DLL se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="97dff-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="97dff-118">Se non viene specificato alcun numero di versione, l'elemento di programmazione viene implementato in tutte le versioni esistenti della DLL.</span><span class="sxs-lookup"><span data-stu-id="97dff-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="97dff-119">Nella tabella seguente vengono descritte le diverse versioni di DLL e il modo in cui sono state distribuite nei sistemi operativi supportati.</span><span class="sxs-lookup"><span data-stu-id="97dff-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="97dff-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="97dff-120">ComCtl32.dll</span></span>

<span data-ttu-id="97dff-121">Versione</span><span class="sxs-lookup"><span data-stu-id="97dff-121">Version</span></span>

<span data-ttu-id="97dff-122">Piattaforma di distribuzione</span><span class="sxs-lookup"><span data-stu-id="97dff-122">Distribution Platform</span></span>

<span data-ttu-id="97dff-123">5,81</span><span class="sxs-lookup"><span data-stu-id="97dff-123">5.81</span></span>

<span data-ttu-id="97dff-124">Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 e Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="97dff-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="97dff-125">5,82</span><span class="sxs-lookup"><span data-stu-id="97dff-125">5.82</span></span>

<span data-ttu-id="97dff-126">Windows Server 2003, Windows Vista, Windows Server 2008 e Windows 7</span><span class="sxs-lookup"><span data-stu-id="97dff-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="97dff-127">6.0</span><span class="sxs-lookup"><span data-stu-id="97dff-127">6.0</span></span>

<span data-ttu-id="97dff-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97dff-128">Windows Server 2003</span></span>

<span data-ttu-id="97dff-129">6.10</span><span class="sxs-lookup"><span data-stu-id="97dff-129">6.10</span></span>

<span data-ttu-id="97dff-130">Windows Vista, Windows Server 2008 e Windows 7</span><span class="sxs-lookup"><span data-stu-id="97dff-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="97dff-131">Dimensioni della struttura per diverse versioni di controllo comuni</span><span class="sxs-lookup"><span data-stu-id="97dff-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="97dff-132">I miglioramenti continui apportati ai controlli comuni hanno comportato la necessità di estendere molte delle strutture.</span><span class="sxs-lookup"><span data-stu-id="97dff-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="97dff-133">Per questo motivo, le dimensioni delle strutture sono cambiate tra le diverse versioni di COMmctrl. h.</span><span class="sxs-lookup"><span data-stu-id="97dff-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="97dff-134">Poiché la maggior parte delle strutture di controllo comuni accetta una dimensione della struttura come uno dei parametri, un messaggio o una funzione può avere esito negativo se la dimensione non viene riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="97dff-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="97dff-135">Per ovviare a questo problema, sono state definite costanti di dimensione della struttura per facilitare la destinazione di una versione diversa di ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="97dff-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="97dff-136">Nell'elenco seguente sono definite le costanti della dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="97dff-136">The following list defines the structure size constants.</span></span>



|                               |                                                                                              |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="97dff-137">\_Dimensioni HDITEM V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-137">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="97dff-138">Dimensioni della struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-138">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="97dff-139">\_Dimensioni IMAGELISTDRAWPARAMS V3 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-139">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="97dff-140">Dimensioni della struttura [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) nella versione 5,9.</span><span class="sxs-lookup"><span data-stu-id="97dff-140">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="97dff-141">\_Dimensioni LVCOLUMN V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-141">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="97dff-142">Dimensioni della struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-142">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="97dff-143">\_Dimensioni LVGROUP V5 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-143">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="97dff-144">Dimensioni della struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) nella versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-144">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="97dff-145">\_Dimensioni LVHITTESTINFO V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-145">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="97dff-146">Dimensioni della struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-146">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="97dff-147">\_Dimensioni LVITEM V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-147">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="97dff-148">Dimensioni della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-148">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="97dff-149">\_Dimensioni LVITEM V5 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-149">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="97dff-150">Dimensioni della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) nella versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="97dff-151">\_Dimensioni LVTILEINFO V5 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-151">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="97dff-152">Dimensioni della struttura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) nella versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-152">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="97dff-153">\_Dimensioni MCHITTESTINFO V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-153">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="97dff-154">Dimensioni della struttura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-154">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="97dff-155">\_Dimensioni NMLVCUSTOMDRAW V3 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-155">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="97dff-156">Dimensioni della struttura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) nella versione 4,7.</span><span class="sxs-lookup"><span data-stu-id="97dff-156">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="97dff-157">\_Dimensioni NMTTDISPINFO V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-157">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="97dff-158">Dimensioni della struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-158">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="97dff-159">\_Dimensioni NMTVCUSTOMDRAW V3 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-159">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="97dff-160">Dimensioni della struttura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) nella versione 4,7.</span><span class="sxs-lookup"><span data-stu-id="97dff-160">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="97dff-161">\_Dimensioni PROPSHEETHEADER V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-161">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="97dff-162">Dimensioni della struttura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-162">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="97dff-163">\_Dimensioni PROPSHEETPAGE V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-163">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="97dff-164">Dimensioni della struttura [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-164">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="97dff-165">\_Dimensioni REBARBANDINFO V3 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-165">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="97dff-166">Dimensioni della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) nella versione 4,7.</span><span class="sxs-lookup"><span data-stu-id="97dff-166">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="97dff-167">\_Dimensioni REBARBANDINFO V6 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-167">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="97dff-168">Dimensioni della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) nella versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="97dff-169">\_Dimensioni TTTOOLINFO V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-169">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="97dff-170">Dimensioni della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-170">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="97dff-171">\_Dimensioni TTTOOLINFO v2 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-171">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="97dff-172">Dimensioni della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) nella versione 4,7.</span><span class="sxs-lookup"><span data-stu-id="97dff-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="97dff-173">\_Dimensioni TTTOOLINFO V3 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-173">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="97dff-174">Dimensioni della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) nella versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="97dff-175">\_Dimensioni TVINSERTSTRUCT V1 \_</span><span class="sxs-lookup"><span data-stu-id="97dff-175">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="97dff-176">Dimensioni della struttura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) nella versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-176">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="97dff-177">Utilizzo di DllGetVersion per determinare il numero di versione</span><span class="sxs-lookup"><span data-stu-id="97dff-177">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="97dff-178">La funzione [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) può essere chiamata da un'applicazione per determinare quale versione della dll è presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="97dff-178">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="97dff-179">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) restituisce una struttura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="97dff-179">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="97dff-180">Oltre alle informazioni fornite tramite [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** fornisce anche il numero di hotfix che identifica il Service Pack installato più recente, che fornisce un modo più efficace per confrontare i numeri di versione.</span><span class="sxs-lookup"><span data-stu-id="97dff-180">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="97dff-181">Poiché il primo membro di **DLLVERSIONINFO2** è una struttura **DLLVERSIONINFO** , la struttura successiva è compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="97dff-181">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="97dff-182">La funzione di esempio seguente `GetVersion` carica una DLL specificata e tenta di chiamare la relativa funzione [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="97dff-182">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="97dff-183">Se ha esito positivo, usa una macro per comprimere i numeri di versione principale e secondaria dalla struttura [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) in un **valore DWORD** restituito all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="97dff-183">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="97dff-184">Se la DLL non esporta **DllGetVersion**, la funzione restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="97dff-184">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="97dff-185">È possibile modificare la funzione per gestire la possibilità che **DllGetVersion** restituisca una struttura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="97dff-185">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="97dff-186">In tal caso, usare le informazioni contenute nel membro **ullVersion** della struttura **DLLVERSIONINFO2** per confrontare le versioni, i numeri di build e le versioni Service Pack.</span><span class="sxs-lookup"><span data-stu-id="97dff-186">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="97dff-187">La macro [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) semplifica l'attività di confronto di questi valori con quelli in **ullVersion**.</span><span class="sxs-lookup"><span data-stu-id="97dff-187">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="97dff-188">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può causare rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="97dff-188">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="97dff-189">Per informazioni su come caricare correttamente le dll con versioni diverse di Windows, vedere la documentazione di **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="97dff-189">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```



<span data-ttu-id="97dff-190">Nell'esempio di codice seguente viene illustrato come utilizzare `GetVersion` per verificare se ComCtl32.dll è la versione 6,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="97dff-190">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a><span data-ttu-id="97dff-191">Versioni del progetto</span><span class="sxs-lookup"><span data-stu-id="97dff-191">Project Versions</span></span>

<span data-ttu-id="97dff-192">Per assicurarsi che l'applicazione sia compatibile con diverse versioni di destinazione di un file con estensione dll, le macro della versione sono presenti nei file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="97dff-192">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="97dff-193">Queste macro vengono utilizzate per definire, escludere o ridefinire determinate definizioni per versioni diverse della DLL.</span><span class="sxs-lookup"><span data-stu-id="97dff-193">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="97dff-194">Per una descrizione approfondita di queste macro, vedere [uso delle intestazioni di Windows](/windows/desktop/WinProg/using-the-windows-headers) .</span><span class="sxs-lookup"><span data-stu-id="97dff-194">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="97dff-195">Ad esempio, il nome di macro **\_ Win32 \_ IE** si trova in genere nelle intestazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="97dff-195">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="97dff-196">L'utente è responsabile della definizione della macro come numero esadecimale.</span><span class="sxs-lookup"><span data-stu-id="97dff-196">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="97dff-197">Questo numero di versione definisce la versione di destinazione dell'applicazione che usa la DLL.</span><span class="sxs-lookup"><span data-stu-id="97dff-197">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="97dff-198">La tabella seguente illustra i numeri di versione disponibili e l'effetto di ogni utente sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97dff-198">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="97dff-199">Versione</span><span class="sxs-lookup"><span data-stu-id="97dff-199">Version</span></span> | <span data-ttu-id="97dff-200">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97dff-200">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97dff-201">0x0300</span><span class="sxs-lookup"><span data-stu-id="97dff-201">0x0300</span></span>  | <span data-ttu-id="97dff-202">L'applicazione è compatibile con ComCtl32.dll versione 4,70 e successive.</span><span class="sxs-lookup"><span data-stu-id="97dff-202">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="97dff-203">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,70.</span><span class="sxs-lookup"><span data-stu-id="97dff-203">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="97dff-204">0x0400</span><span class="sxs-lookup"><span data-stu-id="97dff-204">0x0400</span></span>  | <span data-ttu-id="97dff-205">L'applicazione è compatibile con ComCtl32.dll versione 4,71 e successive.</span><span class="sxs-lookup"><span data-stu-id="97dff-205">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="97dff-206">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,71.</span><span class="sxs-lookup"><span data-stu-id="97dff-206">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="97dff-207">0x0401</span><span class="sxs-lookup"><span data-stu-id="97dff-207">0x0401</span></span>  | <span data-ttu-id="97dff-208">L'applicazione è compatibile con ComCtl32.dll versione 4,72 e successive.</span><span class="sxs-lookup"><span data-stu-id="97dff-208">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="97dff-209">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,72.</span><span class="sxs-lookup"><span data-stu-id="97dff-209">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="97dff-210">0x0500</span><span class="sxs-lookup"><span data-stu-id="97dff-210">0x0500</span></span>  | <span data-ttu-id="97dff-211">L'applicazione è compatibile con ComCtl32.dll versione 5,80 e successive.</span><span class="sxs-lookup"><span data-stu-id="97dff-211">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="97dff-212">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 5,80.</span><span class="sxs-lookup"><span data-stu-id="97dff-212">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="97dff-213">0x0501</span><span class="sxs-lookup"><span data-stu-id="97dff-213">0x0501</span></span>  | <span data-ttu-id="97dff-214">L'applicazione è compatibile con ComCtl32.dll versione 5,81 e successive.</span><span class="sxs-lookup"><span data-stu-id="97dff-214">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="97dff-215">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 5,81.</span><span class="sxs-lookup"><span data-stu-id="97dff-215">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="97dff-216">0x0600</span><span class="sxs-lookup"><span data-stu-id="97dff-216">0x0600</span></span>  | <span data-ttu-id="97dff-217">L'applicazione è compatibile con ComCtl32.dll versione 6,0 e successive.</span><span class="sxs-lookup"><span data-stu-id="97dff-217">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="97dff-218">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="97dff-218">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="97dff-219">Se non si definisce la macro di **\_ \_ IE Win32** nel progetto, questa viene definita automaticamente come 0x0500.</span><span class="sxs-lookup"><span data-stu-id="97dff-219">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="97dff-220">Per definire un valore diverso, è possibile aggiungere quanto segue alle direttive del compilatore nel file make; sostituire il numero di versione desiderato per 0x0400.</span><span class="sxs-lookup"><span data-stu-id="97dff-220">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="97dff-221">Un altro metodo consiste nell'aggiungere una riga simile alla seguente nel codice sorgente prima di includere i file di intestazione della shell.</span><span class="sxs-lookup"><span data-stu-id="97dff-221">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="97dff-222">Sostituire il numero di versione desiderato per 0x0400.</span><span class="sxs-lookup"><span data-stu-id="97dff-222">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="97dff-223">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97dff-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97dff-224">Informazioni sui controlli comuni</span><span class="sxs-lookup"><span data-stu-id="97dff-224">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 