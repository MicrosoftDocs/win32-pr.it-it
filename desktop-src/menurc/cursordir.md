---
title: Struttura CURSORDIR
description: Contiene le dimensioni di una singola immagine del cursore in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menu struttura CURSORDIR e altre risorse
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400858"
---
# <a name="cursordir-structure"></a><span data-ttu-id="fdb2d-105">Struttura CURSORDIR</span><span class="sxs-lookup"><span data-stu-id="fdb2d-105">CURSORDIR structure</span></span>

<span data-ttu-id="fdb2d-106">Contiene le dimensioni di una singola immagine del cursore in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fdb2d-106">Contains the dimensions of an individual cursor image in a resource group.</span></span> <span data-ttu-id="fdb2d-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="fdb2d-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb2d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fdb2d-108">Syntax</span></span>


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a><span data-ttu-id="fdb2d-109">Members</span><span class="sxs-lookup"><span data-stu-id="fdb2d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="fdb2d-110">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="fdb2d-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="fdb2d-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="fdb2d-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fdb2d-112">Larghezza, in pixel, del cursore.</span><span class="sxs-lookup"><span data-stu-id="fdb2d-112">The width of the cursor, in pixels.</span></span> <span data-ttu-id="fdb2d-113">I valori accettabili sono 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="fdb2d-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="fdb2d-114">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="fdb2d-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="fdb2d-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="fdb2d-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fdb2d-116">Altezza, in pixel, del cursore.</span><span class="sxs-lookup"><span data-stu-id="fdb2d-116">The height of the cursor, in pixels.</span></span> <span data-ttu-id="fdb2d-117">I valori accettabili sono 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="fdb2d-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdb2d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdb2d-118">Remarks</span></span>

<span data-ttu-id="fdb2d-119">La struttura **CURSORDIR** viene passata nella struttura [**RESDIR**](resdir.md) se la struttura **RESDIR** descrive un cursore.</span><span class="sxs-lookup"><span data-stu-id="fdb2d-119">The **CURSORDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb2d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdb2d-120">Requirements</span></span>



| <span data-ttu-id="fdb2d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdb2d-121">Requirement</span></span> | <span data-ttu-id="fdb2d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fdb2d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fdb2d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdb2d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fdb2d-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fdb2d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fdb2d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdb2d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fdb2d-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fdb2d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fdb2d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdb2d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="fdb2d-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fdb2d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fdb2d-129">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="fdb2d-129">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="fdb2d-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="fdb2d-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fdb2d-131">Risorse</span><span class="sxs-lookup"><span data-stu-id="fdb2d-131">Resources</span></span>](resources.md)
</dt> </dl>

 

 





