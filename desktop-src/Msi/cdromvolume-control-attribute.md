---
description: Se viene impostato il bit del controllo CDROMVolume, il controllo Mostra tutti i volumi nell'installazione corrente e tutti i volumi CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Attributo di controllo CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310996"
---
# <a name="cdromvolume-control-attribute"></a><span data-ttu-id="af103-103">Attributo di controllo CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="af103-103">CDROMVolume Control Attribute</span></span>

<span data-ttu-id="af103-104">Se viene impostato il bit del controllo CDROMVolume, il controllo Mostra tutti i volumi nell'installazione corrente e tutti i volumi CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="af103-104">If the CDROMVolume Control bit is set, the control shows all the volumes in the current installation plus all the CD-ROM volumes.</span></span>

<span data-ttu-id="af103-105">Se questo bit non è impostato, il controllo Mostra tutti i volumi nell'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="af103-105">If this bit is not set, the control shows all the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="af103-106">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="af103-106">Valid Controls</span></span>

[<span data-ttu-id="af103-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="af103-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="af103-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="af103-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="af103-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="af103-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="af103-110">Valore</span><span class="sxs-lookup"><span data-stu-id="af103-110">Value</span></span>



| <span data-ttu-id="af103-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="af103-111">Decimal</span></span> | <span data-ttu-id="af103-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="af103-112">Hexadecimal</span></span> | <span data-ttu-id="af103-113">Costante</span><span class="sxs-lookup"><span data-stu-id="af103-113">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="af103-114">524288</span><span class="sxs-lookup"><span data-stu-id="af103-114">524288</span></span>  | <span data-ttu-id="af103-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="af103-115">0x00080000</span></span>  | <span data-ttu-id="af103-116">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="af103-116">**msidbControlAttributesCDROMVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="af103-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="af103-117">Remarks</span></span>

<span data-ttu-id="af103-118">Per impostare questo attributo su un controllo, includere il bit CDROMVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="af103-118">To set this attribute on a control, include the CDROMVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="af103-119">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="af103-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



