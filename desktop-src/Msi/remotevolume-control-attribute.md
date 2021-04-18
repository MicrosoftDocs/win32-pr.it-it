---
description: Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi remoti. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Attributo di controllo RemoteVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306574"
---
# <a name="remotevolume-control-attribute"></a><span data-ttu-id="4e4aa-104">Attributo di controllo RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="4e4aa-104">RemoteVolume Control Attribute</span></span>

<span data-ttu-id="4e4aa-105">Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi remoti.</span><span class="sxs-lookup"><span data-stu-id="4e4aa-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the remote volumes.</span></span> <span data-ttu-id="4e4aa-106">Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="4e4aa-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="4e4aa-107">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="4e4aa-107">Valid Controls</span></span>

[<span data-ttu-id="4e4aa-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="4e4aa-108">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="4e4aa-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="4e4aa-109">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="4e4aa-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="4e4aa-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="4e4aa-111">Valore</span><span class="sxs-lookup"><span data-stu-id="4e4aa-111">Value</span></span>



| <span data-ttu-id="4e4aa-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="4e4aa-112">Decimal</span></span> | <span data-ttu-id="4e4aa-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="4e4aa-113">Hexadecimal</span></span> | <span data-ttu-id="4e4aa-114">Costante</span><span class="sxs-lookup"><span data-stu-id="4e4aa-114">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="4e4aa-115">262144</span><span class="sxs-lookup"><span data-stu-id="4e4aa-115">262144</span></span>  | <span data-ttu-id="4e4aa-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="4e4aa-116">0x00040000</span></span>  | <span data-ttu-id="4e4aa-117">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="4e4aa-117">**msidbControlAttributesRemoteVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4e4aa-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e4aa-118">Remarks</span></span>

<span data-ttu-id="4e4aa-119">Per impostare questo attributo su un controllo, includere il bit RemoteVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="4e4aa-119">To set this attribute on a control, include the RemoteVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="4e4aa-120">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="4e4aa-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



