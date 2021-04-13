---
description: Se viene impostato il bit del controllo FloppyVolume, il controllo Mostra tutti i volumi necessari nell'installazione corrente più tutti i volumi floppy.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Attributo di controllo FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528183"
---
# <a name="floppyvolume-control-attribute"></a><span data-ttu-id="030e5-103">Attributo di controllo FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="030e5-103">FloppyVolume Control Attribute</span></span>

<span data-ttu-id="030e5-104">Se viene impostato il bit del controllo FloppyVolume, il controllo Mostra tutti i volumi necessari nell'installazione corrente più tutti i volumi floppy.</span><span class="sxs-lookup"><span data-stu-id="030e5-104">If the FloppyVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the floppy volumes.</span></span>

<span data-ttu-id="030e5-105">Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="030e5-105">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="030e5-106">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="030e5-106">Valid Controls</span></span>

[<span data-ttu-id="030e5-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="030e5-107">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="030e5-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="030e5-108">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="030e5-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="030e5-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="030e5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="030e5-110">Value</span></span>



| <span data-ttu-id="030e5-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="030e5-111">Decimal</span></span> | <span data-ttu-id="030e5-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="030e5-112">Hexadecimal</span></span> | <span data-ttu-id="030e5-113">Costante</span><span class="sxs-lookup"><span data-stu-id="030e5-113">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="030e5-114">2097152</span><span class="sxs-lookup"><span data-stu-id="030e5-114">2097152</span></span> | <span data-ttu-id="030e5-115">0x00200000</span><span class="sxs-lookup"><span data-stu-id="030e5-115">0x00200000</span></span>  | <span data-ttu-id="030e5-116">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="030e5-116">**msidbControlAttributesFloppyVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="030e5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="030e5-117">Remarks</span></span>

<span data-ttu-id="030e5-118">Per impostare questo attributo su un controllo, includere il bit FloppyVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="030e5-118">To set this attribute on a control, include the FloppyVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="030e5-119">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="030e5-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



