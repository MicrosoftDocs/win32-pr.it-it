---
description: La \_ struttura largeInt con etichetta definisce un'etichetta che viene visualizzata quando viene rilevato un valore specifico della proprietà LARGEINT.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Struttura LABELED_LARGEINT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050081"
---
# <a name="labeled_largeint-structure"></a><span data-ttu-id="e6427-103">\_Struttura largeInt con etichetta</span><span class="sxs-lookup"><span data-stu-id="e6427-103">LABELED\_LARGEINT structure</span></span>

<span data-ttu-id="e6427-104">La struttura **\_ largeInt con etichetta** definisce un'etichetta che viene visualizzata quando viene rilevato un valore specifico della proprietà LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="e6427-104">The **LABELED\_LARGEINT** structure defines a label that is displayed when a specific LARGEINT property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6427-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6427-105">Syntax</span></span>


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a><span data-ttu-id="e6427-106">Members</span><span class="sxs-lookup"><span data-stu-id="e6427-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6427-107">**Valore**</span><span class="sxs-lookup"><span data-stu-id="e6427-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="e6427-108">Valore LARGEINT della proprietà che si desidera rilevare.</span><span class="sxs-lookup"><span data-stu-id="e6427-108">LARGEINT value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="e6427-109">**Etichetta**</span><span class="sxs-lookup"><span data-stu-id="e6427-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="e6427-110">Descrizione testuale o etichetta visualizzata quando viene rilevato il valore LARGEINT specificato nel membro **value** .</span><span class="sxs-lookup"><span data-stu-id="e6427-110">Textual description or label that is displayed when the LARGEINT value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6427-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6427-111">Remarks</span></span>

<span data-ttu-id="e6427-112">Il membro **lpLabeledLargeIntTable** della struttura [set](set.md) punta a una matrice di strutture **set** che definiscono uno o più membri **Label** delle coppie valore LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="e6427-112">The **lpLabeledLargeIntTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the LARGEINT value pairs.</span></span> <span data-ttu-id="e6427-113">Le coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di un valore LARGEINT specifico presente in un pacchetto di protocollo.</span><span class="sxs-lookup"><span data-stu-id="e6427-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6427-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6427-114">Requirements</span></span>



| <span data-ttu-id="e6427-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6427-115">Requirement</span></span> | <span data-ttu-id="e6427-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e6427-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6427-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6427-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e6427-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6427-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e6427-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6427-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e6427-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6427-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e6427-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6427-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6427-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6427-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6427-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6427-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6427-124">SET</span><span class="sxs-lookup"><span data-stu-id="e6427-124">SET</span></span>](set.md)
</dt> </dl>

 

 




