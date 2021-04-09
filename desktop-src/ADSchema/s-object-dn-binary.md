---
title: Sintassi Object (DN-Binary)
description: Stringa di ottetto che contiene un valore binario e un nome distinto (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Schema di AD Object (DN-Binary) per la sintassi
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104121786"
---
# <a name="objectdn-binary-syntax"></a><span data-ttu-id="a1ac6-104">Sintassi Object (DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="a1ac6-104">Object(DN-Binary) syntax</span></span>

<span data-ttu-id="a1ac6-105">Stringa di ottetto che contiene un valore binario e un nome distinto (DN).</span><span class="sxs-lookup"><span data-stu-id="a1ac6-105">An octet string that contains a binary value and a distinguished name (DN).</span></span>



| <span data-ttu-id="a1ac6-106">Voce</span><span class="sxs-lookup"><span data-stu-id="a1ac6-106">Entry</span></span> | <span data-ttu-id="a1ac6-107">Valore</span><span class="sxs-lookup"><span data-stu-id="a1ac6-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ac6-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a1ac6-108">Name</span></span>         | <span data-ttu-id="a1ac6-109">Object(DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="a1ac6-109">Object(DN-Binary)</span></span>                                                                  |
| <span data-ttu-id="a1ac6-110">ID sintassi</span><span class="sxs-lookup"><span data-stu-id="a1ac6-110">Syntax ID</span></span>    | <span data-ttu-id="a1ac6-111">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="a1ac6-111">2.5.5.7</span></span>                                                                            |
| <span data-ttu-id="a1ac6-112">ID OM</span><span class="sxs-lookup"><span data-stu-id="a1ac6-112">OM ID</span></span>        | <span data-ttu-id="a1ac6-113">127</span><span class="sxs-lookup"><span data-stu-id="a1ac6-113">127</span></span>                                                                                |
| <span data-ttu-id="a1ac6-114">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ac6-114">MAPI Type</span></span>    | <span data-ttu-id="a1ac6-115">TSTRING</span><span class="sxs-lookup"><span data-stu-id="a1ac6-115">TSTRING</span></span>                                                                            |
| <span data-ttu-id="a1ac6-116">Tipo di annunci</span><span class="sxs-lookup"><span data-stu-id="a1ac6-116">ADS Type</span></span>     | <span data-ttu-id="a1ac6-117">\_DN ADSTYPE \_ con \_ binario</span><span class="sxs-lookup"><span data-stu-id="a1ac6-117">ADSTYPE\_DN\_WITH\_BINARY</span></span>                                                          |
| <span data-ttu-id="a1ac6-118">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="a1ac6-118">Variant Type</span></span> | <span data-ttu-id="a1ac6-119">\_invio VT</span><span class="sxs-lookup"><span data-stu-id="a1ac6-119">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="a1ac6-120">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="a1ac6-120">SDS Type</span></span>     | <span data-ttu-id="a1ac6-121">Oggetto COM di cui è possibile eseguire il cast a un [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span><span class="sxs-lookup"><span data-stu-id="a1ac6-121">A COM object that can be cast to an [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span></span> |



## <a name="remarks"></a><span data-ttu-id="a1ac6-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1ac6-122">Remarks</span></span>

<span data-ttu-id="a1ac6-123">Un valore con questa sintassi ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="a1ac6-123">A value with this syntax has the following format:</span></span>

``` syntax
B:<char count>:<binary value>:<object DN>
```

<span data-ttu-id="a1ac6-124">dove " &lt; char count &gt; " è il numero di cifre esadecimali in " &lt; Binary value &gt; ", " &lt; Binary value &gt; " è la rappresentazione esadecimale del valore binario e " &lt; Object DN &gt; " è un nome distinto.</span><span class="sxs-lookup"><span data-stu-id="a1ac6-124">where "&lt;char count&gt;" is the number of hexadecimal digits in "&lt;binary value&gt;", "&lt;binary value&gt;" is the hexadecimal representation of the binary value, and "&lt;object DN&gt;" is a distinguished name.</span></span> <span data-ttu-id="a1ac6-125">Active Directory aggiorna automaticamente il DN se l'oggetto a cui fa riferimento è stato spostato o rinominato.</span><span class="sxs-lookup"><span data-stu-id="a1ac6-125">Active Directory automatically updates the DN if the object that it refers to is moved or renamed.</span></span> <span data-ttu-id="a1ac6-126">Per ulteriori informazioni e un esempio di codice in cui viene utilizzata questa sintassi, vedere [Abilitazione dell'associazione Rinomina-safe con la proprietà otherWellKnownObjects archiviato nel](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span><span class="sxs-lookup"><span data-stu-id="a1ac6-126">For more information and a code example that uses this syntax, see [Enabling Rename-safe Binding with the otherWellKnownObjects Property](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span></span>

## <a name="see-also"></a><span data-ttu-id="a1ac6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1ac6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1ac6-128">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="a1ac6-128">**IADsDNWithBinary**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
