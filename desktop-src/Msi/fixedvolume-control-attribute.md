---
description: Se viene impostato il bit del controllo FixedVolume, il controllo Mostra tutti i volumi necessari nell'installazione corrente più tutti i dischi rigidi interni fissi.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Attributo di controllo FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880194"
---
# <a name="fixedvolume-control-attribute"></a><span data-ttu-id="ee3b5-103">Attributo di controllo FixedVolume</span><span class="sxs-lookup"><span data-stu-id="ee3b5-103">FixedVolume Control Attribute</span></span>

<span data-ttu-id="ee3b5-104">Se viene impostato il bit del controllo FixedVolume, il controllo Mostra tutti i volumi necessari nell'installazione corrente più tutti i dischi rigidi interni fissi.</span><span class="sxs-lookup"><span data-stu-id="ee3b5-104">If the FixedVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the fixed internal hard drives.</span></span>

<span data-ttu-id="ee3b5-105">Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="ee3b5-105">If this bit is not set, the control lists the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ee3b5-106">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="ee3b5-106">Valid Controls</span></span>

[<span data-ttu-id="ee3b5-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="ee3b5-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="ee3b5-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="ee3b5-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="ee3b5-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="ee3b5-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)



| <span data-ttu-id="ee3b5-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="ee3b5-110">Decimal</span></span> | <span data-ttu-id="ee3b5-111">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="ee3b5-111">Hexadecimal</span></span> | <span data-ttu-id="ee3b5-112">Costante</span><span class="sxs-lookup"><span data-stu-id="ee3b5-112">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="ee3b5-113">131072</span><span class="sxs-lookup"><span data-stu-id="ee3b5-113">131072</span></span>  | <span data-ttu-id="ee3b5-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="ee3b5-114">0x00020000</span></span>  | <span data-ttu-id="ee3b5-115">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="ee3b5-115">**msidbControlAttributesFixedVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ee3b5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee3b5-116">Remarks</span></span>

<span data-ttu-id="ee3b5-117">Per impostare questo attributo su un controllo, includere il bit FixedVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee3b5-117">To set this attribute on a control, include the FixedVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="ee3b5-118">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ee3b5-118">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



