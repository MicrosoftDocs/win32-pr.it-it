---
title: attributo ms-DS-ingress-Claims-Transformation-Policy
description: Si tratta di un collegamento a un oggetto Criteri di trasformazione delle attestazioni per le attestazioni in ingresso (attestazioni che accedono a questa foresta) dal dominio trusted.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- ms-DS-ingress-Claims-Transformation-schema AD dell'attributo Policy
- attributo msDS-IngressClaimsTransformationPolicy-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519853"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a><span data-ttu-id="96d9b-105">attributo ms-DS-ingress-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="96d9b-105">ms-DS-Ingress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="96d9b-106">Si tratta di un collegamento a un oggetto Criteri di trasformazione delle attestazioni per le attestazioni in ingresso (attestazioni che accedono a questa foresta) dal dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="96d9b-106">This is a link to a Claims Transformation Policy Object for the ingress claims (claims entering this forest) from the Trusted Domain.</span></span> <span data-ttu-id="96d9b-107">Questa operazione è applicabile solo per un trust tra foreste in uscita o bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="96d9b-107">This is applicable only for an outgoing or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="96d9b-108">Se questo collegamento è assente, vengono eliminate tutte le attestazioni in ingresso.</span><span class="sxs-lookup"><span data-stu-id="96d9b-108">If this link is absent, all the ingress claims are dropped.</span></span>



| <span data-ttu-id="96d9b-109">Voce</span><span class="sxs-lookup"><span data-stu-id="96d9b-109">Entry</span></span> | <span data-ttu-id="96d9b-110">Valore</span><span class="sxs-lookup"><span data-stu-id="96d9b-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="96d9b-111">CN</span><span class="sxs-lookup"><span data-stu-id="96d9b-111">CN</span></span>                | <span data-ttu-id="96d9b-112">ms-DS-ingress-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="96d9b-112">ms-DS-Ingress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="96d9b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="96d9b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="96d9b-114">msDS-IngressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="96d9b-114">msDS-IngressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="96d9b-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="96d9b-115">Size</span></span>              | \-                                         |
| <span data-ttu-id="96d9b-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="96d9b-116">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="96d9b-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="96d9b-117">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="96d9b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="96d9b-118">Attribute-Id</span></span>      | <span data-ttu-id="96d9b-119">1.2.840.113556.1.4.2191</span><span class="sxs-lookup"><span data-stu-id="96d9b-119">1.2.840.113556.1.4.2191</span></span>                    |
| <span data-ttu-id="96d9b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="96d9b-120">System-Id-Guid</span></span>    | <span data-ttu-id="96d9b-121">86284c08-0c6e-1540-8b15-75147d23d20d</span><span class="sxs-lookup"><span data-stu-id="96d9b-121">86284c08-0c6e-1540-8b15-75147d23d20d</span></span>       |
| <span data-ttu-id="96d9b-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96d9b-122">Syntax</span></span>            | [<span data-ttu-id="96d9b-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="96d9b-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)    |



## <a name="implementations"></a><span data-ttu-id="96d9b-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="96d9b-124">Implementations</span></span>

-   [<span data-ttu-id="96d9b-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="96d9b-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="96d9b-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96d9b-126">Windows Server 2012</span></span>



| <span data-ttu-id="96d9b-127">Voce</span><span class="sxs-lookup"><span data-stu-id="96d9b-127">Entry</span></span> | <span data-ttu-id="96d9b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="96d9b-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="96d9b-129">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="96d9b-129">Link-Id</span></span>                | <span data-ttu-id="96d9b-130">2190</span><span class="sxs-lookup"><span data-stu-id="96d9b-130">2190</span></span>                                                 |
| <span data-ttu-id="96d9b-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96d9b-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="96d9b-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="96d9b-132">System-Only</span></span>            | <span data-ttu-id="96d9b-133">Falso</span><span class="sxs-lookup"><span data-stu-id="96d9b-133">False</span></span>                                                |
| <span data-ttu-id="96d9b-134">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="96d9b-134">Is-Single-Valued</span></span>       | <span data-ttu-id="96d9b-135">Vero</span><span class="sxs-lookup"><span data-stu-id="96d9b-135">True</span></span>                                                 |
| <span data-ttu-id="96d9b-136">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="96d9b-136">Is Indexed</span></span>             | <span data-ttu-id="96d9b-137">Falso</span><span class="sxs-lookup"><span data-stu-id="96d9b-137">False</span></span>                                                |
| <span data-ttu-id="96d9b-138">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="96d9b-138">In Global Catalog</span></span>      | <span data-ttu-id="96d9b-139">Falso</span><span class="sxs-lookup"><span data-stu-id="96d9b-139">False</span></span>                                                |
| <span data-ttu-id="96d9b-140">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="96d9b-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="96d9b-141">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="96d9b-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="96d9b-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96d9b-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="96d9b-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96d9b-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="96d9b-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96d9b-144">Search-Flags</span></span>           | <span data-ttu-id="96d9b-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96d9b-145">0x00000000</span></span>                                           |
| <span data-ttu-id="96d9b-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96d9b-146">System-Flags</span></span>           | <span data-ttu-id="96d9b-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96d9b-147">0x00000010</span></span>                                           |
| <span data-ttu-id="96d9b-148">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="96d9b-148">Classes used in</span></span>        | [<span data-ttu-id="96d9b-149">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="96d9b-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





