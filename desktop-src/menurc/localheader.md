---
title: Struttura LOCALHEADER
description: Contiene le coordinate x e y di un hotspot associato al cursore identificato da una struttura RESDIR. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Menu struttura LOCALHEADER e altre risorse
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400719"
---
# <a name="localheader-structure"></a><span data-ttu-id="1edf5-105">Struttura LOCALHEADER</span><span class="sxs-lookup"><span data-stu-id="1edf5-105">LOCALHEADER structure</span></span>

<span data-ttu-id="1edf5-106">Contiene le coordinate x e y di un hotspot associato al cursore identificato da una struttura [**RESDIR**](resdir.md) .</span><span class="sxs-lookup"><span data-stu-id="1edf5-106">Contains the x- and y-coordinates of a hotspot associated with the cursor identified by a [**RESDIR**](resdir.md) structure.</span></span> <span data-ttu-id="1edf5-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="1edf5-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1edf5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1edf5-108">Syntax</span></span>


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a><span data-ttu-id="1edf5-109">Members</span><span class="sxs-lookup"><span data-stu-id="1edf5-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1edf5-110">**xHotSpot**</span><span class="sxs-lookup"><span data-stu-id="1edf5-110">**xHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="1edf5-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="1edf5-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1edf5-112">Coordinata x dell'area sensibile del cursore, in pixel.</span><span class="sxs-lookup"><span data-stu-id="1edf5-112">The x-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1edf5-113">**yHotSpot**</span><span class="sxs-lookup"><span data-stu-id="1edf5-113">**yHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="1edf5-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="1edf5-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1edf5-115">Coordinata y dell'area sensibile del cursore, in pixel.</span><span class="sxs-lookup"><span data-stu-id="1edf5-115">The y-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1edf5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1edf5-116">Remarks</span></span>

<span data-ttu-id="1edf5-117">La struttura **LOCALHEADER** è il primo dato scritto nella risorsa [del \_ cursore RT](/windows/desktop/menurc/resource-types) se una struttura [**RESDIR**](resdir.md) contiene informazioni su un cursore.</span><span class="sxs-lookup"><span data-stu-id="1edf5-117">The **LOCALHEADER** structure is the first data written to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource if a [**RESDIR**](resdir.md) structure contains information about a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="1edf5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1edf5-118">Requirements</span></span>



| <span data-ttu-id="1edf5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1edf5-119">Requirement</span></span> | <span data-ttu-id="1edf5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1edf5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1edf5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1edf5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1edf5-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1edf5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1edf5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1edf5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1edf5-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1edf5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1edf5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1edf5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1edf5-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1edf5-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1edf5-127">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="1edf5-127">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="1edf5-128">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="1edf5-128">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="1edf5-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1edf5-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1edf5-130">Risorse</span><span class="sxs-lookup"><span data-stu-id="1edf5-130">Resources</span></span>](resources.md)
</dt> </dl>

 

