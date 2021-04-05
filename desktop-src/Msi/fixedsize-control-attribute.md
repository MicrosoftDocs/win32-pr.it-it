---
description: Se viene impostato il bit del controllo FixedSize, l'immagine viene ritagliata o centrata nel controllo senza modificarne la forma o la dimensione.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Attributo di controllo FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751143"
---
# <a name="fixedsize-control-attribute"></a><span data-ttu-id="935c9-103">Attributo di controllo FixedSize</span><span class="sxs-lookup"><span data-stu-id="935c9-103">FixedSize Control Attribute</span></span>

<span data-ttu-id="935c9-104">Se viene impostato il bit del controllo FixedSize, l'immagine viene ritagliata o centrata nel controllo senza modificarne la forma o la dimensione.</span><span class="sxs-lookup"><span data-stu-id="935c9-104">If the FixedSize Control bit is set, the picture is cropped or centered in the control without changing its shape or size.</span></span>

<span data-ttu-id="935c9-105">Se questo bit non è impostato, l'immagine viene allungata per adattarsi al controllo.</span><span class="sxs-lookup"><span data-stu-id="935c9-105">If this bit is not set the picture is stretched to fit the control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="935c9-106">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="935c9-106">Valid Controls</span></span>

[<span data-ttu-id="935c9-107">Bitmap</span><span class="sxs-lookup"><span data-stu-id="935c9-107">Bitmap</span></span>](bitmap-control.md)

[<span data-ttu-id="935c9-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="935c9-108">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="935c9-109">Icona</span><span class="sxs-lookup"><span data-stu-id="935c9-109">Icon</span></span>](icon-control.md)

[<span data-ttu-id="935c9-110">Pulsante</span><span class="sxs-lookup"><span data-stu-id="935c9-110">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="935c9-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="935c9-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="935c9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="935c9-112">Value</span></span>



| <span data-ttu-id="935c9-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="935c9-113">Decimal</span></span> | <span data-ttu-id="935c9-114">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="935c9-114">Hexadecimal</span></span> | <span data-ttu-id="935c9-115">Costante</span><span class="sxs-lookup"><span data-stu-id="935c9-115">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="935c9-116">1048576</span><span class="sxs-lookup"><span data-stu-id="935c9-116">1048576</span></span> | <span data-ttu-id="935c9-117">0x00100000</span><span class="sxs-lookup"><span data-stu-id="935c9-117">0x00100000</span></span>  | <span data-ttu-id="935c9-118">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="935c9-118">**msidbControlAttributesFixedSize**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="935c9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="935c9-119">Remarks</span></span>

<span data-ttu-id="935c9-120">Per impostare questo attributo su un controllo, includere il bit FixedSize nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="935c9-120">To set this attribute on a control, include the FixedSize bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="935c9-121">L'impostazione del bit FixedSize non ha alcun effetto su una [casella](checkbox-control.md)di controllo, un [pulsante](pushbutton-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) se non è stata impostata né la [bitmap](bitmap-control-attribute.md) né l' [icona](icon-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="935c9-121">Setting the FixedSize bit has no effect on a [CheckBox](checkbox-control.md), [PushButton](pushbutton-control.md), or [RadioButtonGroup](radiobuttongroup-control.md) if neither the [Bitmap](bitmap-control-attribute.md) or the [Icon](icon-control-attribute.md) have been set.</span></span>

<span data-ttu-id="935c9-122">L'impostazione del bit FixedSize non ha alcun effetto su un controllo Icon o su un pulsante associato a un'icona se i bit [iconSize](iconsize-control-attribute.md) non sono impostati.</span><span class="sxs-lookup"><span data-stu-id="935c9-122">Setting the FixedSize bit has no effect on an Icon control, or a PushButton associated with an icon, if the [IconSize](iconsize-control-attribute.md) bits is not set.</span></span>

<span data-ttu-id="935c9-123">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="935c9-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



