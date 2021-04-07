---
description: La struttura con etichetta \_ SYSTEMTIME definisce un'etichetta che viene visualizzata quando viene rilevato un valore specifico della Proprietà SYSTEMTIME.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Struttura LABELED_SYSTEMTIME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885470"
---
# <a name="labeled_systemtime-structure"></a><span data-ttu-id="ed79d-103">Struttura con etichetta \_ SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="ed79d-103">LABELED\_SYSTEMTIME structure</span></span>

<span data-ttu-id="ed79d-104">La struttura con **etichetta \_ SYSTEMTIME** definisce un'etichetta che viene visualizzata quando viene rilevato un valore specifico della Proprietà SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="ed79d-104">The **LABELED\_SYSTEMTIME** structure defines a label that is displayed when a specific SYSTEMTIME property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed79d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed79d-105">Syntax</span></span>


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a><span data-ttu-id="ed79d-106">Members</span><span class="sxs-lookup"><span data-stu-id="ed79d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed79d-107">**Valore**</span><span class="sxs-lookup"><span data-stu-id="ed79d-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="ed79d-108">Valore di SYSTEMTIME di una proprietà che si desidera rilevare.</span><span class="sxs-lookup"><span data-stu-id="ed79d-108">SYSTEMTIME value of a property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="ed79d-109">**Etichetta**</span><span class="sxs-lookup"><span data-stu-id="ed79d-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="ed79d-110">Descrizione testuale o etichetta visualizzata quando viene rilevato il valore SYSTEMTIME specificato nel membro **value** .</span><span class="sxs-lookup"><span data-stu-id="ed79d-110">Textual description or label that is displayed when the SYSTEMTIME value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed79d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed79d-111">Remarks</span></span>

<span data-ttu-id="ed79d-112">Il membro **lpLabeledSystemTimeTable** della struttura del [set](set.md) punta a una matrice di strutture **set** che definiscono una o più coppie di valori di etichetta.</span><span class="sxs-lookup"><span data-stu-id="ed79d-112">The **lpLabeledSystemTimeTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more label value pairs.</span></span> <span data-ttu-id="ed79d-113">Le coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di un valore LARGEINT specifico trovato nel pacchetto del protocollo.</span><span class="sxs-lookup"><span data-stu-id="ed79d-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed79d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed79d-114">Requirements</span></span>



| <span data-ttu-id="ed79d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed79d-115">Requirement</span></span> | <span data-ttu-id="ed79d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ed79d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed79d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed79d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ed79d-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed79d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ed79d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed79d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ed79d-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed79d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ed79d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed79d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed79d-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed79d-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed79d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed79d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed79d-124">SET</span><span class="sxs-lookup"><span data-stu-id="ed79d-124">SET</span></span>](set.md)
</dt> </dl>

 

 




