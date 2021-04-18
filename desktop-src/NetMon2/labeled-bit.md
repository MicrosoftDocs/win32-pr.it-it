---
description: La \_ struttura di bit con etichetta definisce una coppia di bit etichetta.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Struttura LABELED_BIT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308163"
---
# <a name="labeled_bit-structure"></a><span data-ttu-id="b039d-103">Struttura di \_ bit con etichetta</span><span class="sxs-lookup"><span data-stu-id="b039d-103">LABELED\_BIT structure</span></span>

<span data-ttu-id="b039d-104">La struttura di **\_ bit con etichetta** definisce una coppia di bit etichetta.</span><span class="sxs-lookup"><span data-stu-id="b039d-104">The **LABELED\_BIT** structure defines a label BIT pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="b039d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b039d-105">Syntax</span></span>


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a><span data-ttu-id="b039d-106">Members</span><span class="sxs-lookup"><span data-stu-id="b039d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b039d-107">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="b039d-107">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="b039d-108">Numero di BIT della coppia di BIT dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="b039d-108">BIT number of the label BIT pair.</span></span> <span data-ttu-id="b039d-109">I valori sono compresi tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="b039d-109">Values range from 0 to 255.</span></span> <span data-ttu-id="b039d-110">Impostare il membro **bitnumber** sul bit utilizzato nel confronto del valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b039d-110">Set the **Bitnumber** member to the BIT used in the comparison of the property value.</span></span>

</dd> <dt>

<span data-ttu-id="b039d-111">**LabelOff**</span><span class="sxs-lookup"><span data-stu-id="b039d-111">**LabelOff**</span></span>
</dt> <dd>

<span data-ttu-id="b039d-112">Stringa o etichetta visualizzata quando il BIT specificato in **BitNumber** è uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="b039d-112">String or label that is displayed when the BIT specified in **BitNumber** equals zero.</span></span> <span data-ttu-id="b039d-113">Ad esempio, una possibile etichetta è "bit OFF".</span><span class="sxs-lookup"><span data-stu-id="b039d-113">For example, a possible label is "Bit OFF".</span></span>

</dd> <dt>

<span data-ttu-id="b039d-114">**Sconosciutain**</span><span class="sxs-lookup"><span data-stu-id="b039d-114">**LabelOn**</span></span>
</dt> <dd>

<span data-ttu-id="b039d-115">Stringa o etichetta visualizzata quando il BIT specificato in **BitNumber** è uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="b039d-115">String or label that is displayed when the BIT specified in **BitNumber** equals 1.</span></span> <span data-ttu-id="b039d-116">Ad esempio, una possibile etichetta è "bit ON".</span><span class="sxs-lookup"><span data-stu-id="b039d-116">For example, a possible label is "Bit ON".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b039d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b039d-117">Remarks</span></span>

<span data-ttu-id="b039d-118">Una matrice di strutture di **\_ bit con etichetta** viene utilizzata per definire un set di coppie di bit di etichette.</span><span class="sxs-lookup"><span data-stu-id="b039d-118">An array of **LABELED\_BIT** structures is used to define a set of label BIT pairs.</span></span> <span data-ttu-id="b039d-119">Un puntatore alla matrice viene specificato nel membro **lpLabeledBit** della struttura del [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="b039d-119">A pointer to the array is specified in the **lpLabeledBit** member of the [SET](set.md) structure.</span></span> <span data-ttu-id="b039d-120">Le coppie vengono utilizzate quando si desidera visualizzare un'etichetta basata sull'impostazione di ogni BIT.</span><span class="sxs-lookup"><span data-stu-id="b039d-120">The pairs are used when you want to display a label based on the setting of each BIT.</span></span> <span data-ttu-id="b039d-121">In genere, questo tipo di set viene utilizzato per indicare il valore di bit ON o OFF.</span><span class="sxs-lookup"><span data-stu-id="b039d-121">Typically, this type of set is used to indicate the ON or OFF value of BITs.</span></span>

<span data-ttu-id="b039d-122">Quando viene specificato un set di BIT, Network Monitor Visualizza solo i bit inclusi nella matrice di strutture **set** .</span><span class="sxs-lookup"><span data-stu-id="b039d-122">When a BIT set is specified, Network Monitor displays only the BITs included in the array of **SET** structures.</span></span> <span data-ttu-id="b039d-123">I bit non inclusi nella struttura del **set** non vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="b039d-123">BITs that are not in the **SET** structure are not displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b039d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b039d-124">Requirements</span></span>



| <span data-ttu-id="b039d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b039d-125">Requirement</span></span> | <span data-ttu-id="b039d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b039d-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b039d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b039d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b039d-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b039d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b039d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b039d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b039d-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b039d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b039d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b039d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b039d-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b039d-132"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b039d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b039d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b039d-134">SET</span><span class="sxs-lookup"><span data-stu-id="b039d-134">SET</span></span>](set.md)
</dt> </dl>

 

 




