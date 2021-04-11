---
description: Se questo bit è impostato, il controllo viene visualizzato con un aspetto incassato a tre dimensioni.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Attributo di controllo incassato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130274"
---
# <a name="sunken-control-attribute"></a><span data-ttu-id="44170-103">Attributo di controllo incassato</span><span class="sxs-lookup"><span data-stu-id="44170-103">Sunken Control Attribute</span></span>

<span data-ttu-id="44170-104">Se questo bit è impostato, il controllo viene visualizzato con un aspetto incassato a tre dimensioni.</span><span class="sxs-lookup"><span data-stu-id="44170-104">If this bit is set, the control is displayed with a sunken, three dimensional look.</span></span> <span data-ttu-id="44170-105">L'effetto di questo bit di stile è diverso per i diversi controlli e versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="44170-105">The effect of this style bit is different on different controls and versions of Windows.</span></span> <span data-ttu-id="44170-106">In alcuni controlli non ha alcun effetto visibile.</span><span class="sxs-lookup"><span data-stu-id="44170-106">On some controls it has no visible effect.</span></span> <span data-ttu-id="44170-107">Se il sistema non supporta l'attributo di controllo incassato, il controllo viene visualizzato nello stile di visualizzazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="44170-107">If the system does not support the Sunken control attribute, the control is displayed in the default visual style.</span></span> <span data-ttu-id="44170-108">Se questo bit non è impostato, il controllo viene visualizzato con lo stile di visualizzazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="44170-108">If this bit is not set, the control is displayed with the default visual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="44170-109">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="44170-109">Valid Controls</span></span>

<span data-ttu-id="44170-110">Tutti i controlli.</span><span class="sxs-lookup"><span data-stu-id="44170-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="44170-111">Valore</span><span class="sxs-lookup"><span data-stu-id="44170-111">Value</span></span>



| <span data-ttu-id="44170-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="44170-112">Decimal</span></span> | <span data-ttu-id="44170-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="44170-113">Hexadecimal</span></span> | <span data-ttu-id="44170-114">Costante</span><span class="sxs-lookup"><span data-stu-id="44170-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="44170-115">4</span><span class="sxs-lookup"><span data-stu-id="44170-115">4</span></span>       | <span data-ttu-id="44170-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="44170-116">0x00000004</span></span>  | <span data-ttu-id="44170-117">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="44170-117">**msidbControlAttributesSunken**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="44170-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="44170-118">Remarks</span></span>

<span data-ttu-id="44170-119">Per impostare questo attributo su un controllo, includere il bit incassato nella colonna attributi del record del controllo nella [tabella dei controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="44170-119">To set this attribute on a control, include the Sunken bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="44170-120">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="44170-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



