---
description: Se questo bit è impostato su una casella di controllo o un gruppo di pulsanti di opzione, il pulsante viene disegnato con l'aspetto di un pulsante di comando, ma la logica rimane invariata. Se il bit non è impostato, i controlli vengono disegnati nello stile usuale.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Attributo di controllo PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311723"
---
# <a name="pushlike-control-attribute"></a><span data-ttu-id="0e9c4-104">Attributo di controllo PushLike</span><span class="sxs-lookup"><span data-stu-id="0e9c4-104">PushLike Control Attribute</span></span>

<span data-ttu-id="0e9c4-105">Se questo bit è impostato su una casella di controllo o un gruppo di pulsanti di opzione, il pulsante viene disegnato con l'aspetto di un pulsante di comando, ma la logica rimane invariata.</span><span class="sxs-lookup"><span data-stu-id="0e9c4-105">If this bit is set on a check box or a radio button group, the button is drawn with the appearance of a push button, but its logic stays the same.</span></span> <span data-ttu-id="0e9c4-106">Se il bit non è impostato, i controlli vengono disegnati nello stile usuale.</span><span class="sxs-lookup"><span data-stu-id="0e9c4-106">If the bit is not set, the controls are drawn in their usual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="0e9c4-107">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="0e9c4-107">Valid Controls</span></span>

<span data-ttu-id="0e9c4-108">[Casella](checkbox-control.md)di controllo[RadioButtonGroup](radiobuttongroup-control.md)</span><span class="sxs-lookup"><span data-stu-id="0e9c4-108">[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)</span></span>

## <a name="value"></a><span data-ttu-id="0e9c4-109">Valore</span><span class="sxs-lookup"><span data-stu-id="0e9c4-109">Value</span></span>



| <span data-ttu-id="0e9c4-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="0e9c4-110">Decimal</span></span> | <span data-ttu-id="0e9c4-111">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="0e9c4-111">Hexadecimal</span></span> | <span data-ttu-id="0e9c4-112">Costante</span><span class="sxs-lookup"><span data-stu-id="0e9c4-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="0e9c4-113">131072</span><span class="sxs-lookup"><span data-stu-id="0e9c4-113">131072</span></span>  | <span data-ttu-id="0e9c4-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="0e9c4-114">0x00020000</span></span>  | <span data-ttu-id="0e9c4-115">**msidbControlAttributesPushLike**</span><span class="sxs-lookup"><span data-stu-id="0e9c4-115">**msidbControlAttributesPushLike**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0e9c4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e9c4-116">Remarks</span></span>

<span data-ttu-id="0e9c4-117">Per impostare questo attributo su un controllo, includere il bit PushLike nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="0e9c4-117">To set this attribute on a control, include the PushLike bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="0e9c4-118">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="0e9c4-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



