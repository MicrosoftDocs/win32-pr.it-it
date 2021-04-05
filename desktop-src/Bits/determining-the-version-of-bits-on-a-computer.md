---
title: Determinazione della versione dei bit in un computer
description: Per determinare la versione dei bit nel computer client, controllare la versione di QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707861"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a><span data-ttu-id="9c555-103">Determinazione della versione dei bit in un computer</span><span class="sxs-lookup"><span data-stu-id="9c555-103">Determining the Version of BITS on a Computer</span></span>

<span data-ttu-id="9c555-104">Per determinare la versione dei bit nel computer client, controllare la versione di QMgr.dll.</span><span class="sxs-lookup"><span data-stu-id="9c555-104">To determine the version of BITS on the client computer, check the version of QMgr.dll.</span></span> <span data-ttu-id="9c555-105">Per trovare il numero di versione della DLL:</span><span class="sxs-lookup"><span data-stu-id="9c555-105">To find the version number of the DLL:</span></span>

-   <span data-ttu-id="9c555-106">Individuare QMgr.dll in% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="9c555-106">Locate QMgr.dll in %windir%\\System32.</span></span>
-   <span data-ttu-id="9c555-107">Fare clic con il pulsante destro del mouse su QMgr.dll e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="9c555-107">Right-click QMgr.dll and click **Properties**.</span></span>
-   <span data-ttu-id="9c555-108">Fare clic sulla scheda **Version** .</span><span class="sxs-lookup"><span data-stu-id="9c555-108">Click the **Version** tab.</span></span>
-   <span data-ttu-id="9c555-109">Annotare il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="9c555-109">Note the version number.</span></span>

<span data-ttu-id="9c555-110">È anche possibile usare il codice PowerShell seguente per determinare la versione del file dll nel sistema:</span><span class="sxs-lookup"><span data-stu-id="9c555-110">You can also use the following PowerShell code to determine the version of the .dll on your system:</span></span>

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

<span data-ttu-id="9c555-111">Se la DLL esiste anche in% windir% \\ system32 \\ bit, ripetere i passaggi precedenti.</span><span class="sxs-lookup"><span data-stu-id="9c555-111">If the DLL also exists in %windir%\\System32\\Bits, repeat the previous steps.</span></span> <span data-ttu-id="9c555-112">BITS usa la DLL con il numero di versione superiore.</span><span class="sxs-lookup"><span data-stu-id="9c555-112">BITS uses the DLL with the higher version number.</span></span>

<span data-ttu-id="9c555-113">Nella tabella seguente sono elencate le versioni di BITS e i numeri di versione del file QMgr.dll corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="9c555-113">The following table lists the versions of BITS and their corresponding QMgr.dll file version numbers.</span></span>



| <span data-ttu-id="9c555-114">Versione BITS</span><span class="sxs-lookup"><span data-stu-id="9c555-114">BITS version</span></span> | <span data-ttu-id="9c555-115">Numero di versione del file di QMgr.dll</span><span class="sxs-lookup"><span data-stu-id="9c555-115">QMgr.dll file version number</span></span> |
|--------------|------------------------------|
| <span data-ttu-id="9c555-116">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="9c555-116">BITS 10.1</span></span>    | <span data-ttu-id="9c555-117">7.8. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-117">7.8.xxxx.xxxx</span></span>                |
| <span data-ttu-id="9c555-118">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="9c555-118">BITS 5.0</span></span>     | <span data-ttu-id="9c555-119">7.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-119">7.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="9c555-120">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="9c555-120">BITS 4.0</span></span>     | <span data-ttu-id="9c555-121">7.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-121">7.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="9c555-122">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="9c555-122">BITS 3.0</span></span>     | <span data-ttu-id="9c555-123">7.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-123">7.0.xxxx.xxxx</span></span>                |
| <span data-ttu-id="9c555-124">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="9c555-124">BITS 2.5</span></span>     | <span data-ttu-id="9c555-125">6.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-125">6.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="9c555-126">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="9c555-126">BITS 2.0</span></span>     | <span data-ttu-id="9c555-127">6.6. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-127">6.6.xxxx.xxxx</span></span>                |
| <span data-ttu-id="9c555-128">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="9c555-128">BITS 1.5</span></span>     | <span data-ttu-id="9c555-129">6.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-129">6.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="9c555-130">BITS 1,2</span><span class="sxs-lookup"><span data-stu-id="9c555-130">BITS 1.2</span></span>     | <span data-ttu-id="9c555-131">6.2. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-131">6.2.xxxx.xxxx</span></span>                |
| <span data-ttu-id="9c555-132">BITS 1,0</span><span class="sxs-lookup"><span data-stu-id="9c555-132">BITS 1.0</span></span>     | <span data-ttu-id="9c555-133">6.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="9c555-133">6.0.xxxx.xxxx</span></span>                |



 

<span data-ttu-id="9c555-134">È inoltre possibile utilizzare gli identificatori di classe simbolici per determinare la versione di bit registrata nel computer.</span><span class="sxs-lookup"><span data-stu-id="9c555-134">You can also use the symbolic class identifiers to determine the version of BITS that is registered on the computer.</span></span> <span data-ttu-id="9c555-135">La tabella seguente elenca le versioni di BITS e i corrispondenti identificatori di classe simbolici.</span><span class="sxs-lookup"><span data-stu-id="9c555-135">The following table lists the versions of BITS and their corresponding symbolic class identifiers.</span></span> <span data-ttu-id="9c555-136">La funzione **CoCreateInstance** restituisce **REGDB \_ E \_ CLASSNOTREG** se la classe non è registrata.</span><span class="sxs-lookup"><span data-stu-id="9c555-136">The **CoCreateInstance** function returns **REGDB\_E\_CLASSNOTREG** if the class is not registered.</span></span>



| <span data-ttu-id="9c555-137">Versione BITS</span><span class="sxs-lookup"><span data-stu-id="9c555-137">BITS version</span></span>  | <span data-ttu-id="9c555-138">Identificatore di classe simbolico</span><span class="sxs-lookup"><span data-stu-id="9c555-138">Symbolic class identifier</span></span>         |
|---------------|-----------------------------------|
| <span data-ttu-id="9c555-139">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="9c555-139">BITS 10.1</span></span>     | <span data-ttu-id="9c555-140">CLSID \_ BackgroundCopyManager10 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9c555-140">CLSID\_BackgroundCopyManager10\_1</span></span> |
| <span data-ttu-id="9c555-141">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="9c555-141">BITS 5.0</span></span>      | <span data-ttu-id="9c555-142">CLSID \_ BackgroundCopyManager5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c555-142">CLSID\_BackgroundCopyManager5\_0</span></span>  |
| <span data-ttu-id="9c555-143">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="9c555-143">BITS 4.0</span></span>      | <span data-ttu-id="9c555-144">CLSID \_ BackgroundCopyManager4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c555-144">CLSID\_BackgroundCopyManager4\_0</span></span>  |
| <span data-ttu-id="9c555-145">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="9c555-145">BITS 3.0</span></span>      | <span data-ttu-id="9c555-146">CLSID \_ BackgroundCopyManager3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c555-146">CLSID\_BackgroundCopyManager3\_0</span></span>  |
| <span data-ttu-id="9c555-147">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="9c555-147">BITS 2.5</span></span>      | <span data-ttu-id="9c555-148">CLSID \_ BackgroundCopyManager2 \_ 5</span><span class="sxs-lookup"><span data-stu-id="9c555-148">CLSID\_BackgroundCopyManager2\_5</span></span>  |
| <span data-ttu-id="9c555-149">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="9c555-149">BITS 2.0</span></span>      | <span data-ttu-id="9c555-150">CLSID \_ BackgroundCopyManager2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c555-150">CLSID\_BackgroundCopyManager2\_0</span></span>  |
| <span data-ttu-id="9c555-151">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="9c555-151">BITS 1.5</span></span>      | <span data-ttu-id="9c555-152">CLSID \_ BackgroundCopyManager1 \_ 5</span><span class="sxs-lookup"><span data-stu-id="9c555-152">CLSID\_BackgroundCopyManager1\_5</span></span>  |
| <span data-ttu-id="9c555-153">BITS 1,2, 1,0</span><span class="sxs-lookup"><span data-stu-id="9c555-153">BITS 1.2, 1.0</span></span> | <span data-ttu-id="9c555-154">\_BACKGROUNDCOPYMANAGER CLSID</span><span class="sxs-lookup"><span data-stu-id="9c555-154">CLSID\_BackgroundCopyManager</span></span>      |



 

 

 




