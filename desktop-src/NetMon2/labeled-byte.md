---
description: La \_ struttura di byte con etichetta definisce una coppia di bit con etichetta. L'etichetta della coppia di BIT con etichetta viene visualizzata quando viene rilevato un valore di proprietà byte specifico.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Struttura LABELED_BYTE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315454"
---
# <a name="labeled_byte-structure"></a><span data-ttu-id="bb991-104">Struttura di \_ byte con etichetta</span><span class="sxs-lookup"><span data-stu-id="bb991-104">LABELED\_BYTE structure</span></span>

<span data-ttu-id="bb991-105">La struttura di **\_ byte con etichetta** definisce una coppia di bit con etichetta.</span><span class="sxs-lookup"><span data-stu-id="bb991-105">The **LABELED\_BYTE** structure defines a labeled BIT pair.</span></span> <span data-ttu-id="bb991-106">L' **etichetta** della coppia di bit con etichetta viene visualizzata quando viene rilevato un valore di proprietà byte specifico.</span><span class="sxs-lookup"><span data-stu-id="bb991-106">The **Label** of the labeled BIT pair is displayed when a specific byte property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb991-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb991-107">Syntax</span></span>


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a><span data-ttu-id="bb991-108">Members</span><span class="sxs-lookup"><span data-stu-id="bb991-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb991-109">**Valore**</span><span class="sxs-lookup"><span data-stu-id="bb991-109">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="bb991-110">Valore BYTE della proprietà che si desidera rilevare.</span><span class="sxs-lookup"><span data-stu-id="bb991-110">BYTE value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="bb991-111">**Etichetta**</span><span class="sxs-lookup"><span data-stu-id="bb991-111">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="bb991-112">Descrizione testuale o etichetta visualizzata quando viene rilevato il valore specificato nel membro **value** .</span><span class="sxs-lookup"><span data-stu-id="bb991-112">Textual description or label that is displayed when the value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb991-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb991-113">Remarks</span></span>

<span data-ttu-id="bb991-114">Il membro **lpLabeledByteTable** della struttura [set](set.md) punta a una matrice di strutture **set** che definiscono uno o più membri **Label** delle coppie valore byte.</span><span class="sxs-lookup"><span data-stu-id="bb991-114">The **lpLabeledByteTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the BYTE value pairs.</span></span> <span data-ttu-id="bb991-115">Queste coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di uno specifico valore BYTE trovato nel pacchetto del protocollo.</span><span class="sxs-lookup"><span data-stu-id="bb991-115">These pairs are used when you want to display a label in place of a specific BYTE value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb991-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb991-116">Requirements</span></span>



| <span data-ttu-id="bb991-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb991-117">Requirement</span></span> | <span data-ttu-id="bb991-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bb991-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bb991-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb991-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb991-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb991-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bb991-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb991-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb991-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb991-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bb991-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb991-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb991-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb991-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb991-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb991-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb991-126">SET</span><span class="sxs-lookup"><span data-stu-id="bb991-126">SET</span></span>](set.md)
</dt> </dl>

 

 




