---
description: Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi rimovibili. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Attributo di controllo RemovableVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751127"
---
# <a name="removablevolume-control-attribute"></a><span data-ttu-id="5df9a-104">Attributo di controllo RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="5df9a-104">RemovableVolume Control Attribute</span></span>

<span data-ttu-id="5df9a-105">Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi rimovibili.</span><span class="sxs-lookup"><span data-stu-id="5df9a-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the removable volumes.</span></span> <span data-ttu-id="5df9a-106">Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="5df9a-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="5df9a-107">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="5df9a-107">Valid Controls</span></span>

[<span data-ttu-id="5df9a-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="5df9a-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="5df9a-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="5df9a-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="5df9a-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="5df9a-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="5df9a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="5df9a-111">Value</span></span>



| <span data-ttu-id="5df9a-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="5df9a-112">Decimal</span></span> | <span data-ttu-id="5df9a-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="5df9a-113">Hexadecimal</span></span> | <span data-ttu-id="5df9a-114">Costante</span><span class="sxs-lookup"><span data-stu-id="5df9a-114">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="5df9a-115">65536</span><span class="sxs-lookup"><span data-stu-id="5df9a-115">65536</span></span>   | <span data-ttu-id="5df9a-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5df9a-116">0x00010000</span></span>  | <span data-ttu-id="5df9a-117">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="5df9a-117">**msidbControlAttributesRemovableVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5df9a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5df9a-118">Remarks</span></span>

<span data-ttu-id="5df9a-119">Per impostare questo attributo su un controllo, includere il bit RemovableVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="5df9a-119">To set this attribute on a control, include the RemovableVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="5df9a-120">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="5df9a-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



