---
title: DS-Execute-Intentions-script esteso a destra
description: Controllare l'accesso a destra, che deve essere concesso al contenitore partizioni, che consente l'utilizzo dell'operazione di Rendom.exe o preparazione in una ridenominazione del dominio.
ms.assetid: 39e9e76c-55c5-4514-ad4d-102844bcbc5a
ms.tgt_platform: multiple
keywords:
- DS-Execute-Intentions-schema AD esteso destro dello script
topic_type:
- apiref
api_name:
- DS-Execute-Intentions-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b34765db2063688ccc8fced0a1e25cac23b98ded
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123123"
---
# <a name="ds-execute-intentions-script-extended-right"></a><span data-ttu-id="8243b-104">DS-Execute-Intentions-script esteso a destra</span><span class="sxs-lookup"><span data-stu-id="8243b-104">DS-Execute-Intentions-Script extended right</span></span>

<span data-ttu-id="8243b-105">Controllare l'accesso a destra, che deve essere concesso al contenitore partizioni, che consente l'utilizzo dell'operazione di Rendom.exe o preparazione in una ridenominazione del dominio.</span><span class="sxs-lookup"><span data-stu-id="8243b-105">Control access right, which should be granted to the partitions container, that allows the Rendom.exe or prepare operation to be used in a domain rename.</span></span> <span data-ttu-id="8243b-106">Questo diritto di accesso al controllo viene inoltre visualizzato come diritto di controllo solo quando viene eseguita l'operazione di Rendom.exe o di esecuzione del passaggio.</span><span class="sxs-lookup"><span data-stu-id="8243b-106">This control access right also appears as an audit-only right when the Rendom.exe or execute step operation is performed.</span></span>



| <span data-ttu-id="8243b-107">Voce</span><span class="sxs-lookup"><span data-stu-id="8243b-107">Entry</span></span> | <span data-ttu-id="8243b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="8243b-108">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="8243b-109">CN</span><span class="sxs-lookup"><span data-stu-id="8243b-109">CN</span></span>           | <span data-ttu-id="8243b-110">DS-Execute-Intentions-script</span><span class="sxs-lookup"><span data-stu-id="8243b-110">DS-Execute-Intentions-Script</span></span>         |
| <span data-ttu-id="8243b-111">Display-Name</span><span class="sxs-lookup"><span data-stu-id="8243b-111">Display-Name</span></span> | <span data-ttu-id="8243b-112">Esegui script di aggiornamento foresta</span><span class="sxs-lookup"><span data-stu-id="8243b-112">Execute Forest Update Script</span></span>         |
| <span data-ttu-id="8243b-113">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="8243b-113">Rights-GUID</span></span>  | <span data-ttu-id="8243b-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span><span class="sxs-lookup"><span data-stu-id="8243b-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span></span> |



## <a name="implementations"></a><span data-ttu-id="8243b-115">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="8243b-115">Implementations</span></span>

-   [<span data-ttu-id="8243b-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8243b-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8243b-117">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8243b-117">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8243b-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8243b-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8243b-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8243b-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8243b-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8243b-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8243b-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8243b-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8243b-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8243b-122">Windows Server 2003</span></span>



| <span data-ttu-id="8243b-123">Voce</span><span class="sxs-lookup"><span data-stu-id="8243b-123">Entry</span></span> | <span data-ttu-id="8243b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8243b-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8243b-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8243b-125">Applies-To</span></span>              | [<span data-ttu-id="8243b-126">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="8243b-126">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8243b-127">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="8243b-127">Localization-Display-ID</span></span> | <span data-ttu-id="8243b-128">66</span><span class="sxs-lookup"><span data-stu-id="8243b-128">66</span></span>                                                            |



## <a name="adam"></a><span data-ttu-id="8243b-129">ADAM</span><span class="sxs-lookup"><span data-stu-id="8243b-129">ADAM</span></span>



| <span data-ttu-id="8243b-130">Voce</span><span class="sxs-lookup"><span data-stu-id="8243b-130">Entry</span></span> | <span data-ttu-id="8243b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8243b-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8243b-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8243b-132">Applies-To</span></span>              | [<span data-ttu-id="8243b-133">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="8243b-133">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8243b-134">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="8243b-134">Localization-Display-ID</span></span> | <span data-ttu-id="8243b-135">66</span><span class="sxs-lookup"><span data-stu-id="8243b-135">66</span></span>                                                            |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8243b-136">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8243b-136">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8243b-137">Voce</span><span class="sxs-lookup"><span data-stu-id="8243b-137">Entry</span></span> | <span data-ttu-id="8243b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8243b-138">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8243b-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8243b-139">Applies-To</span></span>              | [<span data-ttu-id="8243b-140">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="8243b-140">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8243b-141">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="8243b-141">Localization-Display-ID</span></span> | <span data-ttu-id="8243b-142">66</span><span class="sxs-lookup"><span data-stu-id="8243b-142">66</span></span>                                                            |



## <a name="windows-server-2008"></a><span data-ttu-id="8243b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8243b-143">Windows Server 2008</span></span>



| <span data-ttu-id="8243b-144">Voce</span><span class="sxs-lookup"><span data-stu-id="8243b-144">Entry</span></span> | <span data-ttu-id="8243b-145">Valore</span><span class="sxs-lookup"><span data-stu-id="8243b-145">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8243b-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8243b-146">Applies-To</span></span>              | [<span data-ttu-id="8243b-147">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="8243b-147">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8243b-148">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="8243b-148">Localization-Display-ID</span></span> | <span data-ttu-id="8243b-149">66</span><span class="sxs-lookup"><span data-stu-id="8243b-149">66</span></span>                                                            |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8243b-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8243b-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8243b-151">Voce</span><span class="sxs-lookup"><span data-stu-id="8243b-151">Entry</span></span> | <span data-ttu-id="8243b-152">Valore</span><span class="sxs-lookup"><span data-stu-id="8243b-152">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8243b-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8243b-153">Applies-To</span></span>              | [<span data-ttu-id="8243b-154">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="8243b-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8243b-155">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="8243b-155">Localization-Display-ID</span></span> | <span data-ttu-id="8243b-156">66</span><span class="sxs-lookup"><span data-stu-id="8243b-156">66</span></span>                                                            |



## <a name="windows-server-2012"></a><span data-ttu-id="8243b-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8243b-157">Windows Server 2012</span></span>



| <span data-ttu-id="8243b-158">Voce</span><span class="sxs-lookup"><span data-stu-id="8243b-158">Entry</span></span> | <span data-ttu-id="8243b-159">Valore</span><span class="sxs-lookup"><span data-stu-id="8243b-159">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8243b-160">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8243b-160">Applies-To</span></span>              | [<span data-ttu-id="8243b-161">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="8243b-161">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8243b-162">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="8243b-162">Localization-Display-ID</span></span> | <span data-ttu-id="8243b-163">66</span><span class="sxs-lookup"><span data-stu-id="8243b-163">66</span></span>                                                            |



 

 





