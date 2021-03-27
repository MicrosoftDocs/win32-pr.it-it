---
description: Questa sezione descrive come determinare la versione delle dll della shell in cui è in esecuzione l'applicazione e come indirizzare l'applicazione per una versione specifica.
title: 'Versioni delle DLL di shell e Shlwapi '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227424"
---
# <a name="shell-and-shlwapi-dll-versions"></a><span data-ttu-id="11a3b-103">Versioni delle DLL di shell e Shlwapi </span><span class="sxs-lookup"><span data-stu-id="11a3b-103">Shell and Shlwapi DLL Versions</span></span>

<span data-ttu-id="11a3b-104">Questa sezione descrive come determinare la versione delle dll della shell in cui è in esecuzione l'applicazione e come indirizzare l'applicazione per una versione specifica.</span><span class="sxs-lookup"><span data-stu-id="11a3b-104">This section describes how to determine which version of the Shell DLLs your application is running on and how to target your application for a specific version.</span></span>

-   [<span data-ttu-id="11a3b-105">Numeri di versione DLL</span><span class="sxs-lookup"><span data-stu-id="11a3b-105">DLL Version Numbers</span></span>](#dll-version-numbers)
-   [<span data-ttu-id="11a3b-106">Utilizzo di DllGetVersion per determinare il numero di versione</span><span class="sxs-lookup"><span data-stu-id="11a3b-106">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
    -   [<span data-ttu-id="11a3b-107">Uso di DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="11a3b-107">Using DllGetVersion</span></span>](#using-dllgetversion)
-   [<span data-ttu-id="11a3b-108">Versioni del progetto</span><span class="sxs-lookup"><span data-stu-id="11a3b-108">Project Versions</span></span>](#project-versions)

## <a name="dll-version-numbers"></a><span data-ttu-id="11a3b-109">Numeri di versione DLL</span><span class="sxs-lookup"><span data-stu-id="11a3b-109">DLL Version Numbers</span></span>

<span data-ttu-id="11a3b-110">Tutti tranne alcuni degli elementi di programmazione descritti nella documentazione della shell sono contenuti in due dll: Shell32.dll e Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="11a3b-110">All but a handful of the programming elements discussed in the Shell documentation are contained in two DLLs: Shell32.dll and Shlwapi.dll.</span></span> <span data-ttu-id="11a3b-111">A causa dei miglioramenti continui, le diverse versioni di queste DLL implementano funzionalità diverse.</span><span class="sxs-lookup"><span data-stu-id="11a3b-111">Because of ongoing enhancements, different versions of these DLLs implement different features.</span></span> <span data-ttu-id="11a3b-112">In tutta la documentazione di riferimento della shell ogni elemento di programmazione specifica un numero di versione di DLL minimo supportato.</span><span class="sxs-lookup"><span data-stu-id="11a3b-112">Throughout the Shell reference documentation, each programming element specifies a minimum supported DLL version number.</span></span> <span data-ttu-id="11a3b-113">Questo numero di versione indica che l'elemento di programmazione viene implementato in tale versione e nelle versioni successive della DLL se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="11a3b-113">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="11a3b-114">Se non viene specificato alcun numero di versione, l'elemento di programmazione viene implementato in tutte le versioni esistenti della DLL.</span><span class="sxs-lookup"><span data-stu-id="11a3b-114">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="11a3b-115">Prima di Windows XP, venivano talvolta fornite nuove versioni di Shell32.dll e Shlwapi.dll con le nuove versioni di Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="11a3b-115">Before Windows XP, new Shell32.dll and Shlwapi.dll versions were sometimes provided with new versions of Windows Internet Explorer.</span></span> <span data-ttu-id="11a3b-116">A partire da Windows XP, tali dll non venivano più fornite come file ridistribuibili al di fuori delle nuove versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="11a3b-116">As of Windows XP, those DLLs were no longer provided as redistributable files outside of new versions of Windows itself.</span></span> <span data-ttu-id="11a3b-117">Nella tabella seguente vengono descritte le diverse versioni di DLL e il modo in cui sono state distribuite, risalendo a Microsoft Internet Explorer 3,0, Windows 95 e Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="11a3b-117">The following table outlines the different DLL versions and how they were distributed dating back to Microsoft Internet Explorer 3.0, Windows 95, and Microsoft Windows NT 4.0.</span></span>

<span data-ttu-id="11a3b-118">Shell32.dll versione 4,0 è disponibile nelle versioni originali di Windows 95 e Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="11a3b-118">Shell32.dll version 4.0 is found in the original versions of Windows 95 and Microsoft Windows NT 4.0.</span></span> <span data-ttu-id="11a3b-119">La shell non è stata aggiornata con la versione di Internet Explorer 3,0, quindi Shell32.dll non dispone di una versione 4,70.</span><span class="sxs-lookup"><span data-stu-id="11a3b-119">The Shell was not updated with the Internet Explorer 3.0 release, so Shell32.dll does not have a version 4.70.</span></span> <span data-ttu-id="11a3b-120">Shell32.dll versioni 4,71 e 4,72 sono state fornite con le versioni corrispondenti di Internet Explorer, ma non sono state installate necessariamente (vedere la nota 1).</span><span class="sxs-lookup"><span data-stu-id="11a3b-120">Shell32.dll versions 4.71 and 4.72 were shipped with the corresponding Internet Explorer releases, but they were not necessarily installed (see note 1).</span></span> <span data-ttu-id="11a3b-121">Per le versioni successive a Microsoft Internet Explorer 4,01 e Windows 98, i numeri di versione per Shell32.dll e Shlwapi.dll divergenza.</span><span class="sxs-lookup"><span data-stu-id="11a3b-121">For releases subsequent to Microsoft Internet Explorer 4.01 and Windows 98, the version numbers for Shell32.dll and Shlwapi.dll diverge.</span></span> <span data-ttu-id="11a3b-122">In generale, è necessario presupporre che le dll abbiano numeri di versione diversi ed eseguirne il test separatamente.</span><span class="sxs-lookup"><span data-stu-id="11a3b-122">In general, you should assume that the DLLs have different version numbers and test each one separately.</span></span>

#### <a name="shell32dll"></a><span data-ttu-id="11a3b-123">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="11a3b-123">Shell32.dll</span></span>

| <span data-ttu-id="11a3b-124">Versione</span><span class="sxs-lookup"><span data-stu-id="11a3b-124">Version</span></span> | <span data-ttu-id="11a3b-125">Piattaforma di distribuzione</span><span class="sxs-lookup"><span data-stu-id="11a3b-125">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="11a3b-126">4.0</span><span class="sxs-lookup"><span data-stu-id="11a3b-126">4.0</span></span>     | <span data-ttu-id="11a3b-127">Windows 95 e Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="11a3b-127">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="11a3b-128">4,71</span><span class="sxs-lookup"><span data-stu-id="11a3b-128">4.71</span></span>    | <span data-ttu-id="11a3b-129">Microsoft Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="11a3b-129">Microsoft Internet Explorer 4.0.</span></span> <span data-ttu-id="11a3b-130">Vedere la nota 1.</span><span class="sxs-lookup"><span data-stu-id="11a3b-130">See note 1.</span></span>                                |
| <span data-ttu-id="11a3b-131">4,72</span><span class="sxs-lookup"><span data-stu-id="11a3b-131">4.72</span></span>    | <span data-ttu-id="11a3b-132">Internet Explorer 4,01 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="11a3b-132">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="11a3b-133">Vedere la nota 1.</span><span class="sxs-lookup"><span data-stu-id="11a3b-133">See note 1.</span></span>                          |
| <span data-ttu-id="11a3b-134">5.0</span><span class="sxs-lookup"><span data-stu-id="11a3b-134">5.0</span></span>     | <span data-ttu-id="11a3b-135">Windows 2000 e Windows Millennium Edition (Windows Me).</span><span class="sxs-lookup"><span data-stu-id="11a3b-135">Windows 2000 and Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="11a3b-136">Vedere la nota 2.</span><span class="sxs-lookup"><span data-stu-id="11a3b-136">See note 2.</span></span>       |
| <span data-ttu-id="11a3b-137">6.0</span><span class="sxs-lookup"><span data-stu-id="11a3b-137">6.0</span></span>     | <span data-ttu-id="11a3b-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="11a3b-138">Windows XP</span></span>                                                                  |
| <span data-ttu-id="11a3b-139">6.0.1</span><span class="sxs-lookup"><span data-stu-id="11a3b-139">6.0.1</span></span>   | <span data-ttu-id="11a3b-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11a3b-140">Windows Vista</span></span>                                                               |
| <span data-ttu-id="11a3b-141">6.1</span><span class="sxs-lookup"><span data-stu-id="11a3b-141">6.1</span></span>     | <span data-ttu-id="11a3b-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="11a3b-142">Windows 7</span></span>                                                                   |

#### <a name="shlwapidll"></a><span data-ttu-id="11a3b-143">Shlwapi.dll</span><span class="sxs-lookup"><span data-stu-id="11a3b-143">Shlwapi.dll</span></span>

| <span data-ttu-id="11a3b-144">Versione</span><span class="sxs-lookup"><span data-stu-id="11a3b-144">Version</span></span> | <span data-ttu-id="11a3b-145">Piattaforma di distribuzione</span><span class="sxs-lookup"><span data-stu-id="11a3b-145">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="11a3b-146">4.0</span><span class="sxs-lookup"><span data-stu-id="11a3b-146">4.0</span></span>     | <span data-ttu-id="11a3b-147">Windows 95 e Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="11a3b-147">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="11a3b-148">4,71</span><span class="sxs-lookup"><span data-stu-id="11a3b-148">4.71</span></span>    | <span data-ttu-id="11a3b-149">Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="11a3b-149">Internet Explorer 4.0.</span></span> <span data-ttu-id="11a3b-150">Vedere la nota 1.</span><span class="sxs-lookup"><span data-stu-id="11a3b-150">See note 1.</span></span>                                          |
| <span data-ttu-id="11a3b-151">4,72</span><span class="sxs-lookup"><span data-stu-id="11a3b-151">4.72</span></span>    | <span data-ttu-id="11a3b-152">Internet Explorer 4,01 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="11a3b-152">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="11a3b-153">Vedere la nota 1.</span><span class="sxs-lookup"><span data-stu-id="11a3b-153">See note 1.</span></span>                          |
| <span data-ttu-id="11a3b-154">4.7</span><span class="sxs-lookup"><span data-stu-id="11a3b-154">4.7</span></span>     | <span data-ttu-id="11a3b-155">Internet Explorer 3. x</span><span class="sxs-lookup"><span data-stu-id="11a3b-155">Internet Explorer 3.x</span></span>                                                       |
| <span data-ttu-id="11a3b-156">5.0</span><span class="sxs-lookup"><span data-stu-id="11a3b-156">5.0</span></span>     | <span data-ttu-id="11a3b-157">Microsoft Internet Explorer 5 e Windows 98 SE.</span><span class="sxs-lookup"><span data-stu-id="11a3b-157">Microsoft Internet Explorer 5 and Windows 98 SE.</span></span> <span data-ttu-id="11a3b-158">Vedere la nota 2.</span><span class="sxs-lookup"><span data-stu-id="11a3b-158">See note 2.</span></span>                |
| <span data-ttu-id="11a3b-159">5.5</span><span class="sxs-lookup"><span data-stu-id="11a3b-159">5.5</span></span>     | <span data-ttu-id="11a3b-160">Microsoft Internet Explorer 5,5 e Windows Millennium Edition (Windows Me)</span><span class="sxs-lookup"><span data-stu-id="11a3b-160">Microsoft Internet Explorer 5.5 and Windows Millennium Edition (Windows Me)</span></span> |
| <span data-ttu-id="11a3b-161">6.0</span><span class="sxs-lookup"><span data-stu-id="11a3b-161">6.0</span></span>     | <span data-ttu-id="11a3b-162">Windows XP e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11a3b-162">Windows XP and Windows Vista</span></span>                                                |



<span data-ttu-id="11a3b-163">**Nota 1:** A tutti i sistemi con Internet Explorer 4,0 o 4,01 è stata associata la versione di Shlwapi.dll (rispettivamente 4,71 o 4,72).</span><span class="sxs-lookup"><span data-stu-id="11a3b-163">**Note 1:** All systems with Internet Explorer 4.0 or 4.01 had the associated version of Shlwapi.dll (4.71 or 4.72, respectively).</span></span> <span data-ttu-id="11a3b-164">Tuttavia, per i sistemi precedenti a Windows 98, Internet Explorer 4,0 e 4,01 possono essere installati con o senza quello noto come *Shell integrata*.</span><span class="sxs-lookup"><span data-stu-id="11a3b-164">However, for systems prior to Windows 98, Internet Explorer 4.0 and 4.01 can be installed with or without what was known as the *integrated Shell*.</span></span> <span data-ttu-id="11a3b-165">Se Internet Explorer è stato installato con la shell integrata, è stata installata anche la versione associata di Shell32.dll (4,71 o 4,72).</span><span class="sxs-lookup"><span data-stu-id="11a3b-165">If Internet Explorer was installed with the integrated Shell, the associated version of Shell32.dll (4.71 or 4.72) was also installed.</span></span> <span data-ttu-id="11a3b-166">Se Internet Explorer è stato installato senza la shell integrata, Shell32.dll rimasto come versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="11a3b-166">If Internet Explorer was installed without the integrated Shell, Shell32.dll remained as version 4.0.</span></span> <span data-ttu-id="11a3b-167">In altre parole, la presenza della versione 4,71 o 4,72 di Shlwapi.dll in un sistema non garantisce che Shell32.dll abbia lo stesso numero di versione.</span><span class="sxs-lookup"><span data-stu-id="11a3b-167">In other words, the presence of version 4.71 or 4.72 of Shlwapi.dll on a system does not guarantee that Shell32.dll has the same version number.</span></span> <span data-ttu-id="11a3b-168">Tutti i sistemi Windows 98 hanno la versione 4,72 di Shell32.dll.</span><span class="sxs-lookup"><span data-stu-id="11a3b-168">All Windows 98 systems have version 4.72 of Shell32.dll.</span></span>

<span data-ttu-id="11a3b-169">**Nota 2:** La versione 5,0 di Shlwapi.dll è stata distribuita con Internet Explorer 5 ed è stata trovata in tutti i sistemi in cui è stato installato Internet Explorer 5, ad eccezione di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="11a3b-169">**Note 2:** Version 5.0 of Shlwapi.dll was distributed with Internet Explorer 5 and was found on all systems on which Internet Explorer 5 was installed, with the exception of Windows 2000.</span></span> <span data-ttu-id="11a3b-170">La versione 5,0 di Shell32.dll è stata distribuita in modo nativo con Windows 2000 e Windows Millennium Edition (Windows Me), insieme alla versione 5,0 di Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="11a3b-170">Version 5.0 of Shell32.dll was distributed natively with Windows 2000 and Windows Millennium Edition (Windows Me), together with version 5.0 of Shlwapi.dll.</span></span>

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="11a3b-171">Utilizzo di DllGetVersion per determinare il numero di versione</span><span class="sxs-lookup"><span data-stu-id="11a3b-171">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="11a3b-172">A partire dalla versione 4,71, le dll della shell, tra le altre, hanno iniziato a esportare [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="11a3b-172">Starting with version 4.71, the Shell DLLs, among others, began exporting [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="11a3b-173">Questa funzione può essere chiamata da un'applicazione per determinare quale versione DLL è presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="11a3b-173">This function can be called by an application to determine which DLL version is present on the system.</span></span>

> [!Note]  
> <span data-ttu-id="11a3b-174">Le dll non esportano necessariamente [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="11a3b-174">DLLs do not necessarily export [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="11a3b-175">Testarlo sempre prima di provare a usarlo.</span><span class="sxs-lookup"><span data-stu-id="11a3b-175">Always test for it before attempting to use it.</span></span>

<span data-ttu-id="11a3b-176">Per le versioni di Windows precedenti a Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) restituisce una struttura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) che contiene i numeri di versione principale e secondaria, il numero di build e un ID piattaforma.</span><span class="sxs-lookup"><span data-stu-id="11a3b-176">For Windows versions earlier than Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure that contains the major and minor version numbers, the build number, and a platform ID.</span></span> <span data-ttu-id="11a3b-177">Per i sistemi Windows 2000 e versioni successive, **DllGetVersion** potrebbe restituire invece una struttura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="11a3b-177">For Windows 2000 and later systems, **DllGetVersion** might instead return a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="11a3b-178">Oltre alle informazioni fornite tramite **DLLVERSIONINFO**, **DLLVERSIONINFO2** fornisce anche il numero di hotfix che identifica il Service Pack installato più recente, che fornisce un modo più efficace per confrontare i numeri di versione.</span><span class="sxs-lookup"><span data-stu-id="11a3b-178">In addition to the information provided through **DLLVERSIONINFO**, **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="11a3b-179">Poiché il primo membro di **DLLVERSIONINFO2** è una struttura **DLLVERSIONINFO** , la struttura successiva è compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="11a3b-179">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>

### <a name="using-dllgetversion"></a><span data-ttu-id="11a3b-180">Uso di DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="11a3b-180">Using DllGetVersion</span></span>

<span data-ttu-id="11a3b-181">La funzione di esempio seguente `GetVersion` carica una DLL specificata e tenta di chiamare la relativa funzione [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="11a3b-181">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="11a3b-182">Se ha esito positivo, usa una macro per comprimere i numeri di versione principale e secondaria dalla struttura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) in un **valore DWORD** restituito all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="11a3b-182">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="11a3b-183">Se la DLL non esporta **DllGetVersion**, la funzione restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="11a3b-183">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="11a3b-184">Con i sistemi Windows 2000 e versioni successive, è possibile modificare la funzione per gestire la possibilità che **DllGetVersion** restituisca una struttura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="11a3b-184">With Windows 2000 and later systems, you can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="11a3b-185">In tal caso, usare le informazioni contenute nel membro **ullVersion** della struttura **DLLVERSIONINFO2** per confrontare le versioni, i numeri di build e le versioni Service Pack.</span><span class="sxs-lookup"><span data-stu-id="11a3b-185">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="11a3b-186">La macro [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) semplifica l'attività di confronto di questi valori con quelli in **ullVersion**.</span><span class="sxs-lookup"><span data-stu-id="11a3b-186">The [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="11a3b-187">L'uso errato di [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) può causare rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="11a3b-187">Using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="11a3b-188">Per informazioni su come caricare correttamente le dll con versioni diverse di Windows, vedere la documentazione di **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="11a3b-188">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


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

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

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


<span data-ttu-id="11a3b-189">Nell'esempio di codice seguente viene illustrato come è possibile utilizzare `GetVersion` per verificare se Shell32.dll è la versione 6,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="11a3b-189">The following code example illustrates how you can use `GetVersion` to test whether Shell32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a><span data-ttu-id="11a3b-190">Versioni del progetto</span><span class="sxs-lookup"><span data-stu-id="11a3b-190">Project Versions</span></span>

<span data-ttu-id="11a3b-191">Per assicurarsi che l'applicazione sia compatibile con diverse versioni di destinazione di un file con estensione dll, le macro della versione sono presenti nei file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="11a3b-191">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="11a3b-192">Queste macro vengono utilizzate per definire, escludere o ridefinire determinate definizioni per versioni diverse della DLL.</span><span class="sxs-lookup"><span data-stu-id="11a3b-192">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="11a3b-193">Per una descrizione approfondita di queste macro, vedere [uso delle intestazioni di Windows](../winprog/using-the-windows-headers.md) .</span><span class="sxs-lookup"><span data-stu-id="11a3b-193">See [Using the Windows Headers](../winprog/using-the-windows-headers.md) for an in-depth description of these macros.</span></span>

<span data-ttu-id="11a3b-194">Ad esempio, il nome di macro **\_ Win32 \_ IE** si trova in genere nelle intestazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="11a3b-194">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="11a3b-195">L'utente è responsabile della definizione della macro come numero esadecimale.</span><span class="sxs-lookup"><span data-stu-id="11a3b-195">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="11a3b-196">Questo numero di versione definisce la versione di destinazione dell'applicazione che usa la DLL.</span><span class="sxs-lookup"><span data-stu-id="11a3b-196">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="11a3b-197">La tabella seguente illustra i numeri di versione disponibili e l'effetto di ogni utente sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="11a3b-197">The following table shows the available version numbers and the effect each has on your application.</span></span>


| <span data-ttu-id="11a3b-198">Versione</span><span class="sxs-lookup"><span data-stu-id="11a3b-198">Version</span></span> | <span data-ttu-id="11a3b-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11a3b-199">Description</span></span>                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a3b-200">0x0200</span><span class="sxs-lookup"><span data-stu-id="11a3b-200">0x0200</span></span>  | <span data-ttu-id="11a3b-201">L'applicazione è compatibile con Shell32.dll versione 4,00 e successive.</span><span class="sxs-lookup"><span data-stu-id="11a3b-201">The application is compatible with Shell32.dll version 4.00 and later.</span></span> <span data-ttu-id="11a3b-202">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,00.</span><span class="sxs-lookup"><span data-stu-id="11a3b-202">The application cannot implement features that were added after version 4.00.</span></span>                                              |
| <span data-ttu-id="11a3b-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="11a3b-203">0x0300</span></span>  | <span data-ttu-id="11a3b-204">L'applicazione è compatibile con Shell32.dll versione 4,70 e successive.</span><span class="sxs-lookup"><span data-stu-id="11a3b-204">The application is compatible with Shell32.dll version 4.70 and later.</span></span> <span data-ttu-id="11a3b-205">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,70.</span><span class="sxs-lookup"><span data-stu-id="11a3b-205">The application cannot implement features that were added after version 4.70.</span></span>                                              |
| <span data-ttu-id="11a3b-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="11a3b-206">0x0400</span></span>  | <span data-ttu-id="11a3b-207">L'applicazione è compatibile con Shell32.dll versione 4,71 e successive.</span><span class="sxs-lookup"><span data-stu-id="11a3b-207">The application is compatible with Shell32.dll version 4.71 and later.</span></span> <span data-ttu-id="11a3b-208">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,71.</span><span class="sxs-lookup"><span data-stu-id="11a3b-208">The application cannot implement features that were added after version 4.71.</span></span>                                              |
| <span data-ttu-id="11a3b-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="11a3b-209">0x0401</span></span>  | <span data-ttu-id="11a3b-210">L'applicazione è compatibile con Shell32.dll versione 4,72 e successive.</span><span class="sxs-lookup"><span data-stu-id="11a3b-210">The application is compatible with Shell32.dll version 4.72 and later.</span></span> <span data-ttu-id="11a3b-211">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,72.</span><span class="sxs-lookup"><span data-stu-id="11a3b-211">The application cannot implement features that were added after version 4.72.</span></span>                                              |
| <span data-ttu-id="11a3b-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="11a3b-212">0x0500</span></span>  | <span data-ttu-id="11a3b-213">L'applicazione è compatibile con Shell32.dll e Shlwapi.dll versione 5,0 e successive.</span><span class="sxs-lookup"><span data-stu-id="11a3b-213">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="11a3b-214">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 5,0 di Shell32.dll e Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="11a3b-214">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="11a3b-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="11a3b-215">0x0501</span></span>  | <span data-ttu-id="11a3b-216">L'applicazione è compatibile con Shell32.dll e Shlwapi.dll versione 5,0 e successive.</span><span class="sxs-lookup"><span data-stu-id="11a3b-216">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="11a3b-217">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 5,0 di Shell32.dll e Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="11a3b-217">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="11a3b-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="11a3b-218">0x0600</span></span>  | <span data-ttu-id="11a3b-219">L'applicazione è compatibile con Shell32.dll e Shlwapi.dll versione 6,0 e successive.</span><span class="sxs-lookup"><span data-stu-id="11a3b-219">The application is compatible with Shell32.dll and Shlwapi.dll version 6.0 and later.</span></span> <span data-ttu-id="11a3b-220">L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 6,0 di Shell32.dll e Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="11a3b-220">The application cannot implement features that were added after version 6.0 of Shell32.dll and Shlwapi.dll.</span></span> |


<span data-ttu-id="11a3b-221">Se non si definisce la macro di **\_ \_ IE Win32** nel progetto, questa viene definita automaticamente come 0x0500.</span><span class="sxs-lookup"><span data-stu-id="11a3b-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="11a3b-222">Per definire un valore diverso, è possibile aggiungere quanto segue alle direttive del compilatore nel file make; sostituire il numero di versione desiderato per 0x0400.</span><span class="sxs-lookup"><span data-stu-id="11a3b-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>

```
/D _WIN32_IE=0x0400
```

<span data-ttu-id="11a3b-223">Un altro metodo consiste nell'aggiungere una riga simile alla seguente nel codice sorgente prima di includere i file di intestazione della shell.</span><span class="sxs-lookup"><span data-stu-id="11a3b-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="11a3b-224">Sostituire il numero di versione desiderato per 0x0400.</span><span class="sxs-lookup"><span data-stu-id="11a3b-224">Substitute the desired version number for 0x0400.</span></span>

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
