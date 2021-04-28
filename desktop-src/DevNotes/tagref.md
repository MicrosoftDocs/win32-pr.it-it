---
description: "TAGREF: contiene l'indice di una voce e le relative informazioni TAG in un database shim."
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096629"
---
# <a name="tagref"></a><span data-ttu-id="2b1a0-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="2b1a0-103">TAGREF</span></span>

<span data-ttu-id="2b1a0-104">Contiene l'indice di una voce e le relative informazioni TAG in un database shim.</span><span class="sxs-lookup"><span data-stu-id="2b1a0-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="2b1a0-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b1a0-105">Remarks</span></span>

<span data-ttu-id="2b1a0-106">Un **TAGREF** è specifico di un database shim e valido in più database.</span><span class="sxs-lookup"><span data-stu-id="2b1a0-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="2b1a0-107">Può essere un valore intero che rappresenta l'indice o uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b1a0-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="2b1a0-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ NULL (0)</span><span class="sxs-lookup"><span data-stu-id="2b1a0-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="2b1a0-109">**TAGREF** inesistente.</span><span class="sxs-lookup"><span data-stu-id="2b1a0-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="2b1a0-110">Questo valore viene restituito da una funzione quando non può restituire un **tag TAGREF valido.**</span><span class="sxs-lookup"><span data-stu-id="2b1a0-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="2b1a0-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0)</span><span class="sxs-lookup"><span data-stu-id="2b1a0-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="2b1a0-112">Indica un TAG dell'elenco radice che può essere usato come elemento padre per ottenere un **TAGREF figlio.**</span><span class="sxs-lookup"><span data-stu-id="2b1a0-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b1a0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b1a0-113">Requirements</span></span>



| <span data-ttu-id="2b1a0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b1a0-114">Requirement</span></span> | <span data-ttu-id="2b1a0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2b1a0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2b1a0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b1a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2b1a0-117">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2b1a0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2b1a0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b1a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2b1a0-119">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b1a0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b1a0-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b1a0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b1a0-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="2b1a0-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="2b1a0-122">**TAG**</span><span class="sxs-lookup"><span data-stu-id="2b1a0-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="2b1a0-123">Tipi DI TAG</span><span class="sxs-lookup"><span data-stu-id="2b1a0-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="2b1a0-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="2b1a0-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




