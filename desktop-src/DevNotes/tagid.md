---
description: Contiene l'indice di una voce e le relative informazioni sui TAG in un database di shim.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966005"
---
# <a name="tagid"></a><span data-ttu-id="1b3ac-103">TAGID</span><span class="sxs-lookup"><span data-stu-id="1b3ac-103">TAGID</span></span>

<span data-ttu-id="1b3ac-104">Contiene l'indice di una voce e le relative informazioni sui TAG in un database di shim.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a><span data-ttu-id="1b3ac-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b3ac-105">Remarks</span></span>

<span data-ttu-id="1b3ac-106">Un **TagId** è specifico di un database.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-106">A **TAGID** is specific to a database.</span></span> <span data-ttu-id="1b3ac-107">Può essere un valore intero che rappresenta l'indice o uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b3ac-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1b3ac-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="1b3ac-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="1b3ac-109">Il **TagId** non esiste.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-109">The **TAGID** does not exist.</span></span> <span data-ttu-id="1b3ac-110">Questo valore viene restituito da una funzione quando non può restituire un **TagId** valido.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-110">This value is returned from a function when it cannot return a valid **TAGID**.</span></span>

</dd> <dt>

<span data-ttu-id="1b3ac-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>\_Radice TagId (0)</span><span class="sxs-lookup"><span data-stu-id="1b3ac-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="1b3ac-112">Indica un TAG dell'elenco radice che può essere utilizzato come elemento padre per ottenere un **TagId** figlio.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b3ac-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b3ac-113">Requirements</span></span>



| <span data-ttu-id="1b3ac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b3ac-114">Requirement</span></span> | <span data-ttu-id="1b3ac-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1b3ac-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b3ac-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b3ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1b3ac-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b3ac-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b3ac-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b3ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1b3ac-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b3ac-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b3ac-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b3ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b3ac-121">**TAG**</span><span class="sxs-lookup"><span data-stu-id="1b3ac-121">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="1b3ac-122">Tipi di TAG</span><span class="sxs-lookup"><span data-stu-id="1b3ac-122">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="1b3ac-123">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="1b3ac-123">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




