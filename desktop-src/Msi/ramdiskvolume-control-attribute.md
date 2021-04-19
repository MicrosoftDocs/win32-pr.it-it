---
description: Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi del disco RAM. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Attributo di controllo RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311720"
---
# <a name="ramdiskvolume-control-attribute"></a><span data-ttu-id="6fda9-104">Attributo di controllo RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="6fda9-104">RAMDiskVolume Control Attribute</span></span>

<span data-ttu-id="6fda9-105">Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi del disco RAM.</span><span class="sxs-lookup"><span data-stu-id="6fda9-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the RAM disk volumes.</span></span> <span data-ttu-id="6fda9-106">Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="6fda9-106">If this bit is not set the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="6fda9-107">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="6fda9-107">Valid Controls</span></span>

[<span data-ttu-id="6fda9-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="6fda9-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="6fda9-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="6fda9-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="6fda9-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="6fda9-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="6fda9-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6fda9-111">Value</span></span>



| <span data-ttu-id="6fda9-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="6fda9-112">Decimal</span></span> | <span data-ttu-id="6fda9-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="6fda9-113">Hexadecimal</span></span> | <span data-ttu-id="6fda9-114">Costante</span><span class="sxs-lookup"><span data-stu-id="6fda9-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="6fda9-115">1048567</span><span class="sxs-lookup"><span data-stu-id="6fda9-115">1048567</span></span> | <span data-ttu-id="6fda9-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="6fda9-116">0x00100000</span></span>  | <span data-ttu-id="6fda9-117">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="6fda9-117">**msidbControlAttributesRAMDiskVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6fda9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fda9-118">Remarks</span></span>

<span data-ttu-id="6fda9-119">Per impostare questo attributo su un controllo, includere il bit RAMDiskVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="6fda9-119">To set this attribute on a control, include the RAMDiskVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="6fda9-120">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="6fda9-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



