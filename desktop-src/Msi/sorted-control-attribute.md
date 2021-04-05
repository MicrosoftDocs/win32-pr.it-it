---
description: Se questo bit è impostato, gli elementi elencati nel controllo vengono visualizzati in un ordine specificato. Se il bit non è impostato, gli elementi vengono visualizzati in ordine alfabetico.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Attributo di controllo ordinato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049368"
---
# <a name="sorted-control-attribute"></a><span data-ttu-id="b124a-104">Attributo di controllo ordinato</span><span class="sxs-lookup"><span data-stu-id="b124a-104">Sorted Control Attribute</span></span>

<span data-ttu-id="b124a-105">Se questo bit è impostato, gli elementi elencati nel controllo vengono visualizzati in un ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="b124a-105">If this bit is set, the items listed in the control are displayed in a specified order.</span></span> <span data-ttu-id="b124a-106">Se il bit non è impostato, gli elementi vengono visualizzati in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="b124a-106">If the bit is not set, items are displayed in alphabetical order.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b124a-107">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="b124a-107">Valid Controls</span></span>

[<span data-ttu-id="b124a-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="b124a-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="b124a-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="b124a-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="b124a-110">Controllo ListView</span><span class="sxs-lookup"><span data-stu-id="b124a-110">ListView Control</span></span>](listview-control.md)

## <a name="value"></a><span data-ttu-id="b124a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b124a-111">Value</span></span>



| <span data-ttu-id="b124a-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="b124a-112">Decimal</span></span> | <span data-ttu-id="b124a-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b124a-113">Hexadecimal</span></span> | <span data-ttu-id="b124a-114">Costante</span><span class="sxs-lookup"><span data-stu-id="b124a-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="b124a-115">65536</span><span class="sxs-lookup"><span data-stu-id="b124a-115">65536</span></span>   | <span data-ttu-id="b124a-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="b124a-116">0x00010000</span></span>  | <span data-ttu-id="b124a-117">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="b124a-117">**msidbControlAttributesSorted**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b124a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b124a-118">Remarks</span></span>

<span data-ttu-id="b124a-119">Per ordinare gli elementi in una [casella combinata](combobox-control.md), includere il bit ordinato nella colonna attributi della [tabella dei controlli](control-table.md) e specificare l'ordine degli elementi nella colonna Order della [tabella ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="b124a-119">To sort the items in a [ComboBox](combobox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="b124a-120">Per ordinare gli elementi in una [casella di riepilogo](listbox-control.md), includere il bit ordinato nella colonna Attributes della [tabella dei controlli](control-table.md) e specificare l'ordine degli elementi nella colonna Order della [tabella ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="b124a-120">To sort the items in a [ListBox](listbox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="b124a-121">Per ordinare gli elementi in un controllo [ListView](listview-control.md), includere il bit ordinato nella colonna attributi della [tabella dei controlli](control-table.md) e specificare l'ordine degli elementi nella [tabella ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="b124a-121">To sort the items in a [ListView](listview-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the order of items in the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="b124a-122">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="b124a-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



