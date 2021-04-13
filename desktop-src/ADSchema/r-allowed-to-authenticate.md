---
title: Consentito-autenticazione estesa a destra
description: Il controllo di accesso a destra controlla chi può eseguire l'autenticazione a un particolare computer o servizio.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Consentito per autenticare lo schema AD esteso a destra
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2fca1b6f4670fd340170ed5cfd1f0160d61945
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480448"
---
# <a name="allowed-to-authenticate-extended-right"></a><span data-ttu-id="e7a43-104">Consentito-autenticazione estesa a destra</span><span class="sxs-lookup"><span data-stu-id="e7a43-104">Allowed-To-Authenticate extended right</span></span>

<span data-ttu-id="e7a43-105">Il controllo di accesso a destra controlla chi può eseguire l'autenticazione a un particolare computer o servizio.</span><span class="sxs-lookup"><span data-stu-id="e7a43-105">The control access right controls who can authenticate to a particular computer or service.</span></span> <span data-ttu-id="e7a43-106">Sostanzialmente si trova negli oggetti computer, utente e InetOrgPerson.</span><span class="sxs-lookup"><span data-stu-id="e7a43-106">It basically lives on computer, user, and InetOrgPerson objects.</span></span> <span data-ttu-id="e7a43-107">È applicabile anche all'oggetto dominio se l'accesso è consentito per l'intero dominio.</span><span class="sxs-lookup"><span data-stu-id="e7a43-107">It is also applicable on the domain object if access is allowed for the entire domain.</span></span> <span data-ttu-id="e7a43-108">Può essere applicato alle unità organizzative per consentire agli utenti di impostare ACE ereditabili nelle unità organizzative che contengono un set di oggetti utente o computer.</span><span class="sxs-lookup"><span data-stu-id="e7a43-108">It can be applied to OUs to permit users to be able to set inheritable ACEs on OUs that contain a set of user or computer objects.</span></span>



| <span data-ttu-id="e7a43-109">Voce</span><span class="sxs-lookup"><span data-stu-id="e7a43-109">Entry</span></span> | <span data-ttu-id="e7a43-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a43-110">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="e7a43-111">CN</span><span class="sxs-lookup"><span data-stu-id="e7a43-111">CN</span></span>           | <span data-ttu-id="e7a43-112">Consentito per l'autenticazione</span><span class="sxs-lookup"><span data-stu-id="e7a43-112">Allowed-To-Authenticate</span></span>              |
| <span data-ttu-id="e7a43-113">Display-Name</span><span class="sxs-lookup"><span data-stu-id="e7a43-113">Display-Name</span></span> | <span data-ttu-id="e7a43-114">Autenticazione consentita</span><span class="sxs-lookup"><span data-stu-id="e7a43-114">Allowed to Authenticate</span></span>              |
| <span data-ttu-id="e7a43-115">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="e7a43-115">Rights-GUID</span></span>  | <span data-ttu-id="e7a43-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span><span class="sxs-lookup"><span data-stu-id="e7a43-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span></span> |



## <a name="implementations"></a><span data-ttu-id="e7a43-117">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e7a43-117">Implementations</span></span>

-   [<span data-ttu-id="e7a43-118">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e7a43-118">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e7a43-119">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e7a43-119">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e7a43-120">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e7a43-120">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e7a43-121">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e7a43-121">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e7a43-122">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e7a43-122">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e7a43-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7a43-123">Windows Server 2003</span></span>



| <span data-ttu-id="e7a43-124">Voce</span><span class="sxs-lookup"><span data-stu-id="e7a43-124">Entry</span></span> | <span data-ttu-id="e7a43-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a43-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a43-126">Applies-To</span><span class="sxs-lookup"><span data-stu-id="e7a43-126">Applies-To</span></span>              | [<span data-ttu-id="e7a43-127">**Computer**</span><span class="sxs-lookup"><span data-stu-id="e7a43-127">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e7a43-128">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7a43-128">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="e7a43-129">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e7a43-129">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="e7a43-130">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="e7a43-130">Localization-Display-ID</span></span> | <span data-ttu-id="e7a43-131">65</span><span class="sxs-lookup"><span data-stu-id="e7a43-131">65</span></span>                                                                                                                              |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e7a43-132">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e7a43-132">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e7a43-133">Voce</span><span class="sxs-lookup"><span data-stu-id="e7a43-133">Entry</span></span> | <span data-ttu-id="e7a43-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a43-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a43-135">Applies-To</span><span class="sxs-lookup"><span data-stu-id="e7a43-135">Applies-To</span></span>              | [<span data-ttu-id="e7a43-136">**Computer**</span><span class="sxs-lookup"><span data-stu-id="e7a43-136">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e7a43-137">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7a43-137">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="e7a43-138">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e7a43-138">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="e7a43-139">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="e7a43-139">Localization-Display-ID</span></span> | <span data-ttu-id="e7a43-140">65</span><span class="sxs-lookup"><span data-stu-id="e7a43-140">65</span></span>                                                                                                                              |



## <a name="windows-server-2008"></a><span data-ttu-id="e7a43-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7a43-141">Windows Server 2008</span></span>



| <span data-ttu-id="e7a43-142">Voce</span><span class="sxs-lookup"><span data-stu-id="e7a43-142">Entry</span></span> | <span data-ttu-id="e7a43-143">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a43-143">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a43-144">Applies-To</span><span class="sxs-lookup"><span data-stu-id="e7a43-144">Applies-To</span></span>              | [<span data-ttu-id="e7a43-145">**Computer**</span><span class="sxs-lookup"><span data-stu-id="e7a43-145">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e7a43-146">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7a43-146">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="e7a43-147">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e7a43-147">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="e7a43-148">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="e7a43-148">Localization-Display-ID</span></span> | <span data-ttu-id="e7a43-149">65</span><span class="sxs-lookup"><span data-stu-id="e7a43-149">65</span></span>                                                                                                                              |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e7a43-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7a43-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e7a43-151">Voce</span><span class="sxs-lookup"><span data-stu-id="e7a43-151">Entry</span></span> | <span data-ttu-id="e7a43-152">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a43-152">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a43-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="e7a43-153">Applies-To</span></span>              | [<span data-ttu-id="e7a43-154">**Computer**</span><span class="sxs-lookup"><span data-stu-id="e7a43-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e7a43-155">**ms-DS-Managed-Service-account**</span><span class="sxs-lookup"><span data-stu-id="e7a43-155">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="e7a43-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7a43-156">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="e7a43-157">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e7a43-157">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="e7a43-158">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="e7a43-158">Localization-Display-ID</span></span> | <span data-ttu-id="e7a43-159">65</span><span class="sxs-lookup"><span data-stu-id="e7a43-159">65</span></span>                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a><span data-ttu-id="e7a43-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7a43-160">Windows Server 2012</span></span>



| <span data-ttu-id="e7a43-161">Voce</span><span class="sxs-lookup"><span data-stu-id="e7a43-161">Entry</span></span> | <span data-ttu-id="e7a43-162">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a43-162">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a43-163">Applies-To</span><span class="sxs-lookup"><span data-stu-id="e7a43-163">Applies-To</span></span>              | [<span data-ttu-id="e7a43-164">**Computer**</span><span class="sxs-lookup"><span data-stu-id="e7a43-164">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e7a43-165">**ms-DS-Managed-Service-account**</span><span class="sxs-lookup"><span data-stu-id="e7a43-165">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="e7a43-166">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7a43-166">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="e7a43-167">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e7a43-167">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="e7a43-168">Localization-display-ID</span><span class="sxs-lookup"><span data-stu-id="e7a43-168">Localization-Display-ID</span></span> | <span data-ttu-id="e7a43-169">65</span><span class="sxs-lookup"><span data-stu-id="e7a43-169">65</span></span>                                                                                                                                                                                                               |



 

 





