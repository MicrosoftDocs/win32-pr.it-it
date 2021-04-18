---
description: Si tratta di una combinazione degli attributi RTLRO, RightAligned e LeftScroll dell'ordine di lettura da destra a sinistra.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Attributo di controllo BiDi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556195c1b3170983083473598f69acb99cdcfaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311020"
---
# <a name="bidi-control-attribute"></a><span data-ttu-id="d1fee-103">Attributo di controllo BiDi</span><span class="sxs-lookup"><span data-stu-id="d1fee-103">BiDi Control Attribute</span></span>

<span data-ttu-id="d1fee-104">Si tratta di una combinazione degli attributi [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) dell'ordine di lettura da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="d1fee-104">This is a combination of the right-to-left reading order [RTLRO](rtlro-control-attribute.md), the [RightAligned](rightaligned-control-attribute.md), and [LeftScroll](leftscroll-control-attribute.md) attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="d1fee-105">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="d1fee-105">Valid Controls</span></span>

[<span data-ttu-id="d1fee-106">ScrollableText</span><span class="sxs-lookup"><span data-stu-id="d1fee-106">ScrollableText</span></span>](scrollabletext-control.md)

 

[<span data-ttu-id="d1fee-107">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="d1fee-107">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="d1fee-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="d1fee-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="d1fee-109">Elenco di directory</span><span class="sxs-lookup"><span data-stu-id="d1fee-109">DirectoryList</span></span>](directorylist-control.md)

 

[<span data-ttu-id="d1fee-110">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="d1fee-110">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="d1fee-111">Modifica</span><span class="sxs-lookup"><span data-stu-id="d1fee-111">Edit</span></span>](edit-control.md)

 

[<span data-ttu-id="d1fee-112">ListBox</span><span class="sxs-lookup"><span data-stu-id="d1fee-112">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="d1fee-113">ListView</span><span class="sxs-lookup"><span data-stu-id="d1fee-113">ListView</span></span>](listview-control.md)

 

[<span data-ttu-id="d1fee-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="d1fee-114">SelectionTree</span></span>](selectiontree-control.md)

 

[<span data-ttu-id="d1fee-115">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="d1fee-115">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="d1fee-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d1fee-116">Value</span></span>



| <span data-ttu-id="d1fee-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="d1fee-117">Decimal</span></span> | <span data-ttu-id="d1fee-118">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="d1fee-118">Hexadecimal</span></span> | <span data-ttu-id="d1fee-119">Costante</span><span class="sxs-lookup"><span data-stu-id="d1fee-119">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="d1fee-120">224</span><span class="sxs-lookup"><span data-stu-id="d1fee-120">224</span></span>     | <span data-ttu-id="d1fee-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="d1fee-121">0x000000E0</span></span>  | <span data-ttu-id="d1fee-122">**msidbControlAttributesBiDi**</span><span class="sxs-lookup"><span data-stu-id="d1fee-122">**msidbControlAttributesBiDi**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d1fee-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1fee-123">Remarks</span></span>

<span data-ttu-id="d1fee-124">Per impostare questo attributo su un controllo, includere il bit BiDi nella colonna attributi del record del controllo nella [tabella del controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="d1fee-124">To set this attribute on a control, include the BiDi bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="d1fee-125">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="d1fee-125">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



