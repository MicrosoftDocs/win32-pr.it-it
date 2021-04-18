---
title: Struttura ICONRESDIR
description: Contiene le dimensioni e il formato colori di una singola immagine dell'icona in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Menu struttura ICONRESDIR e altre risorse
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301768"
---
# <a name="iconresdir-structure"></a><span data-ttu-id="96fa0-105">Struttura ICONRESDIR</span><span class="sxs-lookup"><span data-stu-id="96fa0-105">ICONRESDIR structure</span></span>

<span data-ttu-id="96fa0-106">Contiene le dimensioni e il formato colori di una singola immagine dell'icona in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96fa0-106">Contains the dimensions and color format of an individual icon image in a resource group.</span></span> <span data-ttu-id="96fa0-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="96fa0-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="96fa0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96fa0-108">Syntax</span></span>


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a><span data-ttu-id="96fa0-109">Members</span><span class="sxs-lookup"><span data-stu-id="96fa0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="96fa0-110">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="96fa0-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="96fa0-111">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="96fa0-111">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="96fa0-112">Larghezza, in pixel, dell'icona.</span><span class="sxs-lookup"><span data-stu-id="96fa0-112">The width of the icon, in pixels.</span></span> <span data-ttu-id="96fa0-113">I valori accettabili sono 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="96fa0-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="96fa0-114">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="96fa0-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="96fa0-115">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="96fa0-115">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="96fa0-116">Altezza, in pixel, dell'icona.</span><span class="sxs-lookup"><span data-stu-id="96fa0-116">The height of the icon, in pixels.</span></span> <span data-ttu-id="96fa0-117">I valori accettabili sono 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="96fa0-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="96fa0-118">**ColorCount**</span><span class="sxs-lookup"><span data-stu-id="96fa0-118">**ColorCount**</span></span>
</dt> <dd>

<span data-ttu-id="96fa0-119">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="96fa0-119">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="96fa0-120">Il numero di colori nell'icona.</span><span class="sxs-lookup"><span data-stu-id="96fa0-120">The number of colors in the icon.</span></span> <span data-ttu-id="96fa0-121">I valori accettabili sono 2, 8 e 16.</span><span class="sxs-lookup"><span data-stu-id="96fa0-121">Acceptable values are 2, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="96fa0-122">**riservati**</span><span class="sxs-lookup"><span data-stu-id="96fa0-122">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="96fa0-123">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="96fa0-123">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="96fa0-124">Riservati deve essere impostato sullo stesso valore di quello del campo riservato nell'intestazione del file icona.</span><span class="sxs-lookup"><span data-stu-id="96fa0-124">Reserved; must be set to the same value as that of the reserved field in the icon file header.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96fa0-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="96fa0-125">Remarks</span></span>

<span data-ttu-id="96fa0-126">La struttura **ICONRESDIR** viene passata nella struttura [**RESDIR**](resdir.md) se la struttura **RESDIR** descrive un'icona.</span><span class="sxs-lookup"><span data-stu-id="96fa0-126">The **ICONRESDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes an icon.</span></span>

## <a name="requirements"></a><span data-ttu-id="96fa0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96fa0-127">Requirements</span></span>



| <span data-ttu-id="96fa0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="96fa0-128">Requirement</span></span> | <span data-ttu-id="96fa0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="96fa0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="96fa0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96fa0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="96fa0-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96fa0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="96fa0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96fa0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="96fa0-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96fa0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="96fa0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96fa0-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="96fa0-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="96fa0-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96fa0-136">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="96fa0-136">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="96fa0-137">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="96fa0-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="96fa0-138">Risorse</span><span class="sxs-lookup"><span data-stu-id="96fa0-138">Resources</span></span>](resources.md)
</dt> </dl>

 

 





