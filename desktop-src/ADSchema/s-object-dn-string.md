---
title: Sintassi Object (DN-String)
description: Stringa di ottetto che contiene un valore stringa e un DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Sintassi dell'oggetto (DN-String) AD schema
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302848"
---
# <a name="objectdn-string-syntax"></a><span data-ttu-id="b0366-104">Sintassi Object (DN-String)</span><span class="sxs-lookup"><span data-stu-id="b0366-104">Object(DN-String) syntax</span></span>

<span data-ttu-id="b0366-105">Stringa di ottetto che contiene un valore stringa e un DN.</span><span class="sxs-lookup"><span data-stu-id="b0366-105">An octet string that contains a string value and a DN.</span></span>



| <span data-ttu-id="b0366-106">Voce</span><span class="sxs-lookup"><span data-stu-id="b0366-106">Entry</span></span> | <span data-ttu-id="b0366-107">Valore</span><span class="sxs-lookup"><span data-stu-id="b0366-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0366-108">Nome</span><span class="sxs-lookup"><span data-stu-id="b0366-108">Name</span></span>         | <span data-ttu-id="b0366-109">Object(DN-String)</span><span class="sxs-lookup"><span data-stu-id="b0366-109">Object(DN-String)</span></span>                                                                  |
| <span data-ttu-id="b0366-110">ID sintassi</span><span class="sxs-lookup"><span data-stu-id="b0366-110">Syntax ID</span></span>    | <span data-ttu-id="b0366-111">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="b0366-111">2.5.5.14</span></span>                                                                           |
| <span data-ttu-id="b0366-112">ID OM</span><span class="sxs-lookup"><span data-stu-id="b0366-112">OM ID</span></span>        | <span data-ttu-id="b0366-113">127</span><span class="sxs-lookup"><span data-stu-id="b0366-113">127</span></span>                                                                                |
| <span data-ttu-id="b0366-114">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="b0366-114">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="b0366-115">Tipo di annunci</span><span class="sxs-lookup"><span data-stu-id="b0366-115">ADS Type</span></span>     | <span data-ttu-id="b0366-116">\_DN ADSTYPE \_ con \_ stringa</span><span class="sxs-lookup"><span data-stu-id="b0366-116">ADSTYPE\_DN\_WITH\_STRING</span></span>                                                          |
| <span data-ttu-id="b0366-117">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="b0366-117">Variant Type</span></span> | <span data-ttu-id="b0366-118">\_invio VT</span><span class="sxs-lookup"><span data-stu-id="b0366-118">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="b0366-119">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="b0366-119">SDS Type</span></span>     | <span data-ttu-id="b0366-120">Oggetto COM di cui è possibile eseguire il cast a un [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span><span class="sxs-lookup"><span data-stu-id="b0366-120">A COM object that can be cast to an [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span></span> |



## <a name="remarks"></a><span data-ttu-id="b0366-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0366-121">Remarks</span></span>

<span data-ttu-id="b0366-122">Un valore con questa sintassi ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="b0366-122">A value with this syntax has the following format:</span></span>

``` syntax
S:<char count>:<string value>:<object DN>
```

<span data-ttu-id="b0366-123">dove " &lt; char count &gt; " è il numero di caratteri nella stringa " &lt; Value String &gt; " e " &lt; Object DN &gt; " è un nome distinto di un oggetto in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b0366-123">where "&lt;char count&gt;" is the number of characters in the "&lt;string value&gt;" string, and "&lt;object DN&gt;" is a distinguished name of an object in Active Directory.</span></span> <span data-ttu-id="b0366-124">Active Directory aggiorna il DN se l'oggetto a cui fa riferimento è stato spostato o rinominato.</span><span class="sxs-lookup"><span data-stu-id="b0366-124">Active Directory updates the DN if the object that it refers to is moved or renamed.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0366-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0366-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0366-126">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="b0366-126">**IADsDNWithString**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
