---
description: Se questo bit è impostato, il testo nel controllo viene visualizzato su una sola riga. Se il testo si estende oltre i margini del controllo, viene troncato e i puntini di sospensione (&\# 0034;... &\# 0034;) viene inserito alla fine per indicare il troncamento. Se questo bit non è impostato, il testo viene incapsulato.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Attributo di controllo nowrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313339"
---
# <a name="nowrap-control-attribute"></a><span data-ttu-id="80530-105">Attributo di controllo nowrap</span><span class="sxs-lookup"><span data-stu-id="80530-105">NoWrap Control Attribute</span></span>

<span data-ttu-id="80530-106">Se questo bit è impostato, il testo nel controllo viene visualizzato su una sola riga.</span><span class="sxs-lookup"><span data-stu-id="80530-106">If this bit is set the text in the control is displayed on a single line.</span></span> <span data-ttu-id="80530-107">Se il testo si estende oltre i margini del controllo, viene troncato e al termine vengono inseriti i puntini di sospensione ("...") per indicare il troncamento.</span><span class="sxs-lookup"><span data-stu-id="80530-107">If the text extends beyond the control's margins it is truncated and an ellipsis ("...") is inserted at the end to indicate the truncation.</span></span> <span data-ttu-id="80530-108">Se questo bit non è impostato, il testo viene incapsulato.</span><span class="sxs-lookup"><span data-stu-id="80530-108">If this bit is not set, text wraps.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="80530-109">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="80530-109">Valid Controls</span></span>

[<span data-ttu-id="80530-110">Text</span><span class="sxs-lookup"><span data-stu-id="80530-110">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="80530-111">Valore</span><span class="sxs-lookup"><span data-stu-id="80530-111">Value</span></span>



| <span data-ttu-id="80530-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="80530-112">Decimal</span></span> | <span data-ttu-id="80530-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="80530-113">Hexadecimal</span></span> | <span data-ttu-id="80530-114">Costante</span><span class="sxs-lookup"><span data-stu-id="80530-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="80530-115">262144</span><span class="sxs-lookup"><span data-stu-id="80530-115">262144</span></span>  | <span data-ttu-id="80530-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="80530-116">0x00040000</span></span>  | <span data-ttu-id="80530-117">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="80530-117">**msidbControlAttributesNoWrap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="80530-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="80530-118">Remarks</span></span>

<span data-ttu-id="80530-119">Per impostare questo attributo su un controllo, includere il bit nowrap nella colonna attributi del record del controllo nella [tabella dei controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="80530-119">To set this attribute on a control, include the NoWrap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="80530-120">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="80530-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



