---
description: La \_ struttura DWORD con etichetta definisce un'etichetta che viene visualizzata quando viene rilevato un valore di proprietà DWORD specifico.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Struttura LABELED_DWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232675"
---
# <a name="labeled_dword-structure"></a><span data-ttu-id="d0877-103">\_Struttura DWORD con etichetta</span><span class="sxs-lookup"><span data-stu-id="d0877-103">LABELED\_DWORD structure</span></span>

<span data-ttu-id="d0877-104">La struttura **\_ DWORD con etichetta** definisce un'etichetta che viene visualizzata quando viene rilevato un valore di proprietà DWORD specifico.</span><span class="sxs-lookup"><span data-stu-id="d0877-104">The **LABELED\_DWORD** structure defines a label that is displayed when a specific DWORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0877-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0877-105">Syntax</span></span>


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a><span data-ttu-id="d0877-106">Members</span><span class="sxs-lookup"><span data-stu-id="d0877-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0877-107">**Valore**</span><span class="sxs-lookup"><span data-stu-id="d0877-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="d0877-108">Valore DWORD della proprietà che si desidera rilevare.</span><span class="sxs-lookup"><span data-stu-id="d0877-108">DWORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="d0877-109">**Etichetta**</span><span class="sxs-lookup"><span data-stu-id="d0877-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="d0877-110">Descrizione testuale o etichetta visualizzata quando viene rilevato il valore DWORD specificato nel membro **value** .</span><span class="sxs-lookup"><span data-stu-id="d0877-110">Textual description or label that is displayed when the DWORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0877-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0877-111">Remarks</span></span>

<span data-ttu-id="d0877-112">Il membro **lpLabeledDwordTable** della struttura [set](set.md) punta a una matrice di strutture **set** che definiscono uno o più membri **Label** delle coppie valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="d0877-112">The **lpLabeledDwordTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the DWORD value pairs.</span></span> <span data-ttu-id="d0877-113">Le coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di uno specifico valore DWORD presente nel pacchetto del protocollo.</span><span class="sxs-lookup"><span data-stu-id="d0877-113">The pairs are used when you want to display a label in place of a specific DWORD value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0877-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0877-114">Requirements</span></span>



| <span data-ttu-id="d0877-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0877-115">Requirement</span></span> | <span data-ttu-id="d0877-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d0877-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d0877-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0877-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d0877-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0877-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d0877-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0877-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d0877-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0877-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d0877-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0877-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0877-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0877-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0877-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0877-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0877-124">SET</span><span class="sxs-lookup"><span data-stu-id="d0877-124">SET</span></span>](set.md)
</dt> </dl>

 

 




