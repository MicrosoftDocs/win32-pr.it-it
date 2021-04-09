---
description: Le righe di una casella di riepilogo non vengono considerate come singoli controlli, ma fanno parte di una casella di riepilogo che funge da controllo. La tabella ListBox definisce i valori per tutte le caselle di riepilogo.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Tabella ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967788"
---
# <a name="listbox-table"></a><span data-ttu-id="3fcb6-104">Tabella ListBox</span><span class="sxs-lookup"><span data-stu-id="3fcb6-104">ListBox Table</span></span>

<span data-ttu-id="3fcb6-105">Le righe di una casella di riepilogo non vengono considerate come singoli controlli, ma fanno parte di una casella di riepilogo che funge da controllo.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-105">The lines of a list box are not treated as individual controls, but they are part of a list box that functions as a control.</span></span> <span data-ttu-id="3fcb6-106">La tabella ListBox definisce i valori per tutte le caselle di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-106">The ListBox table defines the values for all list boxes.</span></span>

<span data-ttu-id="3fcb6-107">La tabella ListBox contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-107">The ListBox table has the following columns.</span></span>



| <span data-ttu-id="3fcb6-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="3fcb6-108">Column</span></span>   | <span data-ttu-id="3fcb6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fcb6-109">Type</span></span>                         | <span data-ttu-id="3fcb6-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="3fcb6-110">Key</span></span> | <span data-ttu-id="3fcb6-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="3fcb6-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="3fcb6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fcb6-112">Property</span></span> | [<span data-ttu-id="3fcb6-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3fcb6-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="3fcb6-114">S</span><span class="sxs-lookup"><span data-stu-id="3fcb6-114">Y</span></span>   | <span data-ttu-id="3fcb6-115">N</span><span class="sxs-lookup"><span data-stu-id="3fcb6-115">N</span></span>        |
| <span data-ttu-id="3fcb6-116">JSON</span><span class="sxs-lookup"><span data-stu-id="3fcb6-116">Order</span></span>    | [<span data-ttu-id="3fcb6-117">Integer</span><span class="sxs-lookup"><span data-stu-id="3fcb6-117">Integer</span></span>](integer.md)       | <span data-ttu-id="3fcb6-118">S</span><span class="sxs-lookup"><span data-stu-id="3fcb6-118">Y</span></span>   | <span data-ttu-id="3fcb6-119">N</span><span class="sxs-lookup"><span data-stu-id="3fcb6-119">N</span></span>        |
| <span data-ttu-id="3fcb6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3fcb6-120">Value</span></span>    | [<span data-ttu-id="3fcb6-121">Formattato</span><span class="sxs-lookup"><span data-stu-id="3fcb6-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3fcb6-122">N</span><span class="sxs-lookup"><span data-stu-id="3fcb6-122">N</span></span>   | <span data-ttu-id="3fcb6-123">N</span><span class="sxs-lookup"><span data-stu-id="3fcb6-123">N</span></span>        |
| <span data-ttu-id="3fcb6-124">Testo</span><span class="sxs-lookup"><span data-stu-id="3fcb6-124">Text</span></span>     | [<span data-ttu-id="3fcb6-125">Formattato</span><span class="sxs-lookup"><span data-stu-id="3fcb6-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3fcb6-126">N</span><span class="sxs-lookup"><span data-stu-id="3fcb6-126">N</span></span>   | <span data-ttu-id="3fcb6-127">S</span><span class="sxs-lookup"><span data-stu-id="3fcb6-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3fcb6-128">Colonne</span><span class="sxs-lookup"><span data-stu-id="3fcb6-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3fcb6-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fcb6-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="3fcb6-130">Proprietà denominata da associare a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-130">A named property to be tied to this item.</span></span> <span data-ttu-id="3fcb6-131">Tutti gli elementi collegati alla stessa proprietà diventano parte della stessa casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-131">All the items tied to the same property become part of the same list box.</span></span>

</dd> <dt>

<span data-ttu-id="3fcb6-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine</span><span class="sxs-lookup"><span data-stu-id="3fcb6-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="3fcb6-133">Intero positivo utilizzato per determinare l'ordinamento degli elementi visualizzati in una singola casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-133">A positive integer used to determine the ordering of the items that appear in a single list box.</span></span> <span data-ttu-id="3fcb6-134">Se la casella di riepilogo è definita come ordinata, tutti gli elementi devono avere un valore di ordine.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-134">If the list box is defined as ordered, then all items should have an Order value.</span></span> <span data-ttu-id="3fcb6-135">I numeri interi non devono essere consecutivi.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-135">The integers do not have to be consecutive.</span></span> <span data-ttu-id="3fcb6-136">Se la casella di riepilogo è definita come non ordinata, la colonna viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-136">If the list box is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3fcb6-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="3fcb6-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="3fcb6-138">Stringa del valore associata a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-138">The value string associated with this item.</span></span> <span data-ttu-id="3fcb6-139">Selezionando la riga, la proprietà associata verrà impostata su questo valore.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-139">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="3fcb6-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo</span><span class="sxs-lookup"><span data-stu-id="3fcb6-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="3fcb6-141">Testo visibile e localizzabile da assegnare all'elemento.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-141">The localizable, visible text to be assigned to the item.</span></span> <span data-ttu-id="3fcb6-142">Se questa voce o l'intera colonna risulta mancante, per impostazione predefinita il testo viene impostato sulla voce corrispondente in value.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-142">If this entry or the entire column is missing, the text defaults to the corresponding entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fcb6-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fcb6-143">Remarks</span></span>

<span data-ttu-id="3fcb6-144">Il contenuto del valore e i campi di testo vengono formattati dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo, pertanto possono contenere qualsiasi espressione che la funzione **MsiFormatRecord** possa interpretare.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-144">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="3fcb6-145">La formattazione si verifica solo quando viene creato il controllo e non viene aggiornata se una proprietà richiesta nell'espressione viene modificata durante il ciclo di vita del controllo.</span><span class="sxs-lookup"><span data-stu-id="3fcb6-145">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="3fcb6-146">Convalida</span><span class="sxs-lookup"><span data-stu-id="3fcb6-146">Validation</span></span>

<dl>

[<span data-ttu-id="3fcb6-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="3fcb6-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3fcb6-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="3fcb6-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3fcb6-149">ICE17</span><span class="sxs-lookup"><span data-stu-id="3fcb6-149">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="3fcb6-150">ICE20</span><span class="sxs-lookup"><span data-stu-id="3fcb6-150">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="3fcb6-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="3fcb6-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



