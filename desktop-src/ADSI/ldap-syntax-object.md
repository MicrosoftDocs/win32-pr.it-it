---
title: Oggetto sintassi LDAP
description: Il provider LDAP usa il mapping seguente tra la sintassi LDAP e la sintassi ADSI.
ms.assetid: a82cf8ab-9591-4489-87a6-ccfab0e01d61
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, provider di servizi, sintassi di mapping a sintassi LDAP
- mapping della sintassi ADSI alla sintassi LDAP ADSI
- sintassi e mapping da ADSI a LDAP ADSI
- Provider di servizi LDAP ADSI, mapping della sintassi ADSI alla sintassi LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2272a0805ec32fd7ade9c4584feefb64fb1467f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116685"
---
# <a name="ldap-syntax-object"></a><span data-ttu-id="19ad6-107">Oggetto sintassi LDAP</span><span class="sxs-lookup"><span data-stu-id="19ad6-107">LDAP Syntax Object</span></span>

<span data-ttu-id="19ad6-108">Il provider LDAP usa il mapping seguente tra la sintassi LDAP e la sintassi ADSI.</span><span class="sxs-lookup"><span data-stu-id="19ad6-108">The LDAP provider uses the following mapping between the LDAP syntax and ADSI syntax.</span></span>



| <span data-ttu-id="19ad6-109">Sintassi LDAP</span><span class="sxs-lookup"><span data-stu-id="19ad6-109">LDAP Syntax</span></span>   | <span data-ttu-id="19ad6-110">Sintassi ADSI (automazione)</span><span class="sxs-lookup"><span data-stu-id="19ad6-110">ADSI Syntax (Automation)</span></span>            |
|---------------|-------------------------------------|
| <span data-ttu-id="19ad6-111">ADsPath</span><span class="sxs-lookup"><span data-stu-id="19ad6-111">ADsPath</span></span>       | <span data-ttu-id="19ad6-112">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-112">VT\_BSTR</span></span>                            |
| <span data-ttu-id="19ad6-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="19ad6-113">Boolean</span></span>       | <span data-ttu-id="19ad6-114">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-114">VT\_BOOL</span></span>                            |
| <span data-ttu-id="19ad6-115">Contatore</span><span class="sxs-lookup"><span data-stu-id="19ad6-115">Counter</span></span>       | <span data-ttu-id="19ad6-116">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="19ad6-116">VT\_I4</span></span>                              |
| <span data-ttu-id="19ad6-117">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="19ad6-117">EmailAddress</span></span>  | <span data-ttu-id="19ad6-118">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-118">VT\_BSTR</span></span>                            |
| <span data-ttu-id="19ad6-119">NumeroFax</span><span class="sxs-lookup"><span data-stu-id="19ad6-119">FaxNumber</span></span>     | <span data-ttu-id="19ad6-120">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-120">VT\_BSTR</span></span>                            |
| <span data-ttu-id="19ad6-121">Integer</span><span class="sxs-lookup"><span data-stu-id="19ad6-121">Integer</span></span>       | <span data-ttu-id="19ad6-122">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="19ad6-122">VT\_I4</span></span>                              |
| <span data-ttu-id="19ad6-123">Interval</span><span class="sxs-lookup"><span data-stu-id="19ad6-123">Interval</span></span>      | <span data-ttu-id="19ad6-124">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="19ad6-124">VT\_I4</span></span>                              |
| <span data-ttu-id="19ad6-125">Elenco</span><span class="sxs-lookup"><span data-stu-id="19ad6-125">List</span></span>          | <span data-ttu-id="19ad6-126">\_variante VT ( \_ Array VT BSTR VT \| \_ )</span><span class="sxs-lookup"><span data-stu-id="19ad6-126">VT\_VARIANT (VT\_BSTR \| VT\_ARRAY)</span></span> |
| <span data-ttu-id="19ad6-127">NetAddress</span><span class="sxs-lookup"><span data-stu-id="19ad6-127">NetAddress</span></span>    | <span data-ttu-id="19ad6-128">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-128">VT\_BSTR</span></span>                            |
| <span data-ttu-id="19ad6-129">OctetString</span><span class="sxs-lookup"><span data-stu-id="19ad6-129">OctetString</span></span>   | <span data-ttu-id="19ad6-130">\_variante VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-130">VT\_VARIANT</span></span>                         |
| <span data-ttu-id="19ad6-131">Percorso</span><span class="sxs-lookup"><span data-stu-id="19ad6-131">Path</span></span>          | <span data-ttu-id="19ad6-132">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-132">VT\_BSTR</span></span>                            |
| <span data-ttu-id="19ad6-133">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="19ad6-133">PhoneNumber</span></span>   | <span data-ttu-id="19ad6-134">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-134">VT\_BSTR</span></span>                            |
| <span data-ttu-id="19ad6-135">PostalAddress</span><span class="sxs-lookup"><span data-stu-id="19ad6-135">PostalAddress</span></span> | <span data-ttu-id="19ad6-136">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-136">VT\_BSTR</span></span>                            |
| <span data-ttu-id="19ad6-137">SmallInterval</span><span class="sxs-lookup"><span data-stu-id="19ad6-137">SmallInterval</span></span> | <span data-ttu-id="19ad6-138">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="19ad6-138">VT\_I4</span></span>                              |
| <span data-ttu-id="19ad6-139">string</span><span class="sxs-lookup"><span data-stu-id="19ad6-139">String</span></span>        | <span data-ttu-id="19ad6-140">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-140">VT\_BSTR</span></span>                            |
| <span data-ttu-id="19ad6-141">Tempo</span><span class="sxs-lookup"><span data-stu-id="19ad6-141">Time</span></span>          | <span data-ttu-id="19ad6-142">\_Data VT</span><span class="sxs-lookup"><span data-stu-id="19ad6-142">VT\_DATE</span></span>                            |



 

 

 




