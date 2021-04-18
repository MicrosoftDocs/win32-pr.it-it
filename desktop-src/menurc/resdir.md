---
title: Struttura RESDIR
description: Contiene informazioni su un singolo componente icona o cursore in un gruppo di risorse. Esiste una struttura RESDIR per ogni componente del gruppo. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menu struttura RESDIR e altre risorse
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301195"
---
# <a name="resdir-structure"></a><span data-ttu-id="f7017-106">Struttura RESDIR</span><span class="sxs-lookup"><span data-stu-id="f7017-106">RESDIR structure</span></span>

<span data-ttu-id="f7017-107">Contiene informazioni su un singolo componente icona o cursore in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7017-107">Contains information about an individual icon or cursor component in a resource group.</span></span> <span data-ttu-id="f7017-108">Esiste una struttura **RESDIR** per ogni componente del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f7017-108">There is one **RESDIR** structure for each group component.</span></span> <span data-ttu-id="f7017-109">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="f7017-109">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7017-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7017-110">Syntax</span></span>


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a><span data-ttu-id="f7017-111">Members</span><span class="sxs-lookup"><span data-stu-id="f7017-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="f7017-112">**Icona**</span><span class="sxs-lookup"><span data-stu-id="f7017-112">**Icon**</span></span>
</dt> <dd>

<span data-ttu-id="f7017-113">Tipo: **[ **ICONRESDIR**](iconresdir.md)**</span><span class="sxs-lookup"><span data-stu-id="f7017-113">Type: **[**ICONRESDIR**](iconresdir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7017-114">Larghezza, altezza e numero di colori dell'icona indicata.</span><span class="sxs-lookup"><span data-stu-id="f7017-114">The width, height, and color count of the indicated icon.</span></span>

</dd> <dt>

<span data-ttu-id="f7017-115">**Cursore**</span><span class="sxs-lookup"><span data-stu-id="f7017-115">**Cursor**</span></span>
</dt> <dd>

<span data-ttu-id="f7017-116">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f7017-116">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7017-117">Larghezza e altezza del cursore indicato.</span><span class="sxs-lookup"><span data-stu-id="f7017-117">The width and height of the indicated cursor.</span></span>

</dd> <dt>

<span data-ttu-id="f7017-118">**Aerei**</span><span class="sxs-lookup"><span data-stu-id="f7017-118">**Planes**</span></span>
</dt> <dd>

<span data-ttu-id="f7017-119">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f7017-119">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7017-120">Numero di piani di colore nell'icona o nella bitmap del cursore.</span><span class="sxs-lookup"><span data-stu-id="f7017-120">The number of color planes in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f7017-121">**BitCount**</span><span class="sxs-lookup"><span data-stu-id="f7017-121">**BitCount**</span></span>
</dt> <dd>

<span data-ttu-id="f7017-122">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f7017-122">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7017-123">Numero di bit per pixel nell'icona o nella bitmap del cursore.</span><span class="sxs-lookup"><span data-stu-id="f7017-123">The number of bits per pixel in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f7017-124">**BytesInRes**</span><span class="sxs-lookup"><span data-stu-id="f7017-124">**BytesInRes**</span></span>
</dt> <dd>

<span data-ttu-id="f7017-125">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f7017-125">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7017-126">Dimensioni in byte della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f7017-126">The size of the resource, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f7017-127">**IconCursorId**</span><span class="sxs-lookup"><span data-stu-id="f7017-127">**IconCursorId**</span></span>
</dt> <dd>

<span data-ttu-id="f7017-128">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f7017-128">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7017-129">Icona o cursore con un identificatore ordinale univoco.</span><span class="sxs-lookup"><span data-stu-id="f7017-129">The icon or cursor with a unique ordinal identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7017-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7017-130">Remarks</span></span>

<span data-ttu-id="f7017-131">Una o più strutture **RESDIR** seguono immediatamente la struttura [**NEWHEADER**](newheader.md) nel file res.</span><span class="sxs-lookup"><span data-stu-id="f7017-131">One or more **RESDIR** structures immediately follow the [**NEWHEADER**](newheader.md) structure in the .res file.</span></span> <span data-ttu-id="f7017-132">Il membro **ResCount** della struttura **NEWHEADER** specifica il numero di strutture **RESDIR** .</span><span class="sxs-lookup"><span data-stu-id="f7017-132">The **ResCount** member of the **NEWHEADER** structure specifies the number of **RESDIR** structures.</span></span> <span data-ttu-id="f7017-133">Si noti che la struttura **RESDIR** è costituita da una struttura [**ICONRESDIR**](iconresdir.md) o da una struttura [**CURSORDIR**](cursordir.md) seguita dai membri **Planes**, **BitCount**, **BytesInRes** e **IconCursorId** .</span><span class="sxs-lookup"><span data-stu-id="f7017-133">Note that the **RESDIR** structure consists of either an [**ICONRESDIR**](iconresdir.md) structure or a [**CURSORDIR**](cursordir.md) structure followed by the **Planes**, **BitCount**, **BytesInRes**, and **IconCursorId** members.</span></span> <span data-ttu-id="f7017-134">Se la struttura **RESDIR** contiene informazioni su un cursore, le prime due **parole** il compilatore di risorse scrive nella risorsa [del \_ cursore RT](/windows/desktop/menurc/resource-types) sono i membri **xHotSpot** e **yHotSpot** della struttura [**LOCALHEADER**](localheader.md) .</span><span class="sxs-lookup"><span data-stu-id="f7017-134">If the **RESDIR** structure contains information about a cursor, the first two **WORD** s the resource compiler writes to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource are the **xHotSpot** and **yHotSpot** members of the [**LOCALHEADER**](localheader.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7017-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7017-135">Requirements</span></span>



| <span data-ttu-id="f7017-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7017-136">Requirement</span></span> | <span data-ttu-id="f7017-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f7017-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f7017-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7017-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f7017-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7017-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f7017-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7017-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f7017-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7017-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f7017-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7017-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7017-143">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f7017-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f7017-144">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="f7017-144">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="f7017-145">**ICONRESDIR**</span><span class="sxs-lookup"><span data-stu-id="f7017-145">**ICONRESDIR**</span></span>](iconresdir.md)
</dt> <dt>

[<span data-ttu-id="f7017-146">**LOCALHEADER**</span><span class="sxs-lookup"><span data-stu-id="f7017-146">**LOCALHEADER**</span></span>](localheader.md)
</dt> <dt>

[<span data-ttu-id="f7017-147">**NEWHEADER**</span><span class="sxs-lookup"><span data-stu-id="f7017-147">**NEWHEADER**</span></span>](newheader.md)
</dt> <dt>

<span data-ttu-id="f7017-148">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f7017-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f7017-149">Risorse</span><span class="sxs-lookup"><span data-stu-id="f7017-149">Resources</span></span>](resources.md)
</dt> </dl>

 

