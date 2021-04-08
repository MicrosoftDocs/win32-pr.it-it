---
title: attributo ms-DS-uscita-Claims-Transformation-Policy
description: Si tratta di un collegamento a un oggetto Criteri di trasformazione delle attestazioni per le attestazioni in uscita (attestazioni che lasciano questa foresta) al dominio trusted.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- ms-DS-uscita-Claims-Transformation-schema AD dell'attributo Policy
- attributo msDS-EgressClaimsTransformationPolicy-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965268"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a><span data-ttu-id="17b22-105">attributo ms-DS-uscita-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="17b22-105">ms-DS-Egress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="17b22-106">Si tratta di un collegamento a un oggetto Criteri di trasformazione delle attestazioni per le attestazioni in uscita (attestazioni che lasciano questa foresta) al dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="17b22-106">This is a link to a Claims Transformation Policy Object for the egress claims (claims leaving this forest) to the Trusted Domain.</span></span> <span data-ttu-id="17b22-107">Questa operazione è applicabile solo a un trust tra foreste in ingresso o bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="17b22-107">This is applicable only for an incoming or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="17b22-108">Quando questo collegamento non è presente, tutte le attestazioni possono essere in uscita così come sono.</span><span class="sxs-lookup"><span data-stu-id="17b22-108">When this link is not present, all claims are allowed to egress as-is.</span></span>



| <span data-ttu-id="17b22-109">Voce</span><span class="sxs-lookup"><span data-stu-id="17b22-109">Entry</span></span> | <span data-ttu-id="17b22-110">Valore</span><span class="sxs-lookup"><span data-stu-id="17b22-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="17b22-111">CN</span><span class="sxs-lookup"><span data-stu-id="17b22-111">CN</span></span>                | <span data-ttu-id="17b22-112">ms-DS-uscita-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="17b22-112">ms-DS-Egress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="17b22-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="17b22-113">Ldap-Display-Name</span></span> | <span data-ttu-id="17b22-114">msDS-EgressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="17b22-114">msDS-EgressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="17b22-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="17b22-115">Size</span></span>              | \-                                        |
| <span data-ttu-id="17b22-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="17b22-116">Update Privilege</span></span>  | \-                                        |
| <span data-ttu-id="17b22-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="17b22-117">Update Frequency</span></span>  | \-                                        |
| <span data-ttu-id="17b22-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17b22-118">Attribute-Id</span></span>      | <span data-ttu-id="17b22-119">1.2.840.113556.1.4.2192</span><span class="sxs-lookup"><span data-stu-id="17b22-119">1.2.840.113556.1.4.2192</span></span>                   |
| <span data-ttu-id="17b22-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="17b22-120">System-Id-Guid</span></span>    | <span data-ttu-id="17b22-121">c137427e-9a73-b040-9190-1b095bb43288</span><span class="sxs-lookup"><span data-stu-id="17b22-121">c137427e-9a73-b040-9190-1b095bb43288</span></span>      |
| <span data-ttu-id="17b22-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17b22-122">Syntax</span></span>            | [<span data-ttu-id="17b22-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="17b22-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)   |



## <a name="implementations"></a><span data-ttu-id="17b22-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="17b22-124">Implementations</span></span>

-   [<span data-ttu-id="17b22-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17b22-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="17b22-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17b22-126">Windows Server 2012</span></span>



| <span data-ttu-id="17b22-127">Voce</span><span class="sxs-lookup"><span data-stu-id="17b22-127">Entry</span></span> | <span data-ttu-id="17b22-128">Valore</span><span class="sxs-lookup"><span data-stu-id="17b22-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="17b22-129">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="17b22-129">Link-Id</span></span>                | <span data-ttu-id="17b22-130">2192</span><span class="sxs-lookup"><span data-stu-id="17b22-130">2192</span></span>                                                 |
| <span data-ttu-id="17b22-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17b22-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17b22-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="17b22-132">System-Only</span></span>            | <span data-ttu-id="17b22-133">Falso</span><span class="sxs-lookup"><span data-stu-id="17b22-133">False</span></span>                                                |
| <span data-ttu-id="17b22-134">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="17b22-134">Is-Single-Valued</span></span>       | <span data-ttu-id="17b22-135">Vero</span><span class="sxs-lookup"><span data-stu-id="17b22-135">True</span></span>                                                 |
| <span data-ttu-id="17b22-136">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="17b22-136">Is Indexed</span></span>             | <span data-ttu-id="17b22-137">Falso</span><span class="sxs-lookup"><span data-stu-id="17b22-137">False</span></span>                                                |
| <span data-ttu-id="17b22-138">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="17b22-138">In Global Catalog</span></span>      | <span data-ttu-id="17b22-139">Falso</span><span class="sxs-lookup"><span data-stu-id="17b22-139">False</span></span>                                                |
| <span data-ttu-id="17b22-140">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="17b22-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="17b22-141">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="17b22-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="17b22-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17b22-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="17b22-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17b22-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="17b22-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17b22-144">Search-Flags</span></span>           | <span data-ttu-id="17b22-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17b22-145">0x00000000</span></span>                                           |
| <span data-ttu-id="17b22-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17b22-146">System-Flags</span></span>           | <span data-ttu-id="17b22-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17b22-147">0x00000010</span></span>                                           |
| <span data-ttu-id="17b22-148">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="17b22-148">Classes used in</span></span>        | [<span data-ttu-id="17b22-149">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="17b22-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





