---
description: La struttura di \_ parole con etichetta definisce un'etichetta che viene visualizzata quando viene rilevato un valore della proprietà Word specifico.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Struttura LABELED_WORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315453"
---
# <a name="labeled_word-structure"></a><span data-ttu-id="83b32-103">Struttura di \_ parole con etichetta</span><span class="sxs-lookup"><span data-stu-id="83b32-103">LABELED\_WORD structure</span></span>

<span data-ttu-id="83b32-104">La struttura di **\_ parole con etichetta** definisce un'etichetta che viene visualizzata quando viene rilevato un valore della proprietà Word specifico.</span><span class="sxs-lookup"><span data-stu-id="83b32-104">The **LABELED\_WORD** structure defines a label that is displayed when a specific WORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83b32-105">Syntax</span></span>


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a><span data-ttu-id="83b32-106">Members</span><span class="sxs-lookup"><span data-stu-id="83b32-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="83b32-107">**Valore**</span><span class="sxs-lookup"><span data-stu-id="83b32-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="83b32-108">Valore di parola della proprietà che si desidera rilevare.</span><span class="sxs-lookup"><span data-stu-id="83b32-108">WORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="83b32-109">**Etichetta**</span><span class="sxs-lookup"><span data-stu-id="83b32-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="83b32-110">Descrizione testuale o etichetta visualizzata quando viene rilevato il valore WORD specificato nel membro **value** .</span><span class="sxs-lookup"><span data-stu-id="83b32-110">Textual description or label that is displayed when the WORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83b32-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="83b32-111">Remarks</span></span>

<span data-ttu-id="83b32-112">Il membro **lpLabeledWordTable** della struttura del [set](set.md) punta a una matrice di strutture set per definire una o più coppie di valori di etichetta.</span><span class="sxs-lookup"><span data-stu-id="83b32-112">The **lpLabeledWordTable** member of the [SET](set.md) structure points to an array of SET structures to define one or more label value pairs.</span></span> <span data-ttu-id="83b32-113">Queste coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di un valore WORD specifico presente in un pacchetto di protocollo.</span><span class="sxs-lookup"><span data-stu-id="83b32-113">These pairs are used when you want to display a label in place of a specific WORD value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="83b32-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83b32-114">Requirements</span></span>



| <span data-ttu-id="83b32-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b32-115">Requirement</span></span> | <span data-ttu-id="83b32-116">Valore</span><span class="sxs-lookup"><span data-stu-id="83b32-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="83b32-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83b32-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83b32-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83b32-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="83b32-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83b32-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83b32-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83b32-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="83b32-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83b32-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="83b32-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="83b32-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83b32-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83b32-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b32-124">SET</span><span class="sxs-lookup"><span data-stu-id="83b32-124">SET</span></span>](set.md)
</dt> </dl>

 

 




