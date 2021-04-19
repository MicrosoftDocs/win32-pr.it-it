---
description: Le righe di un controllo ListView non vengono considerate come singoli controlli, ma fanno parte di un ListView che funge da controllo. La tabella ListView definisce i valori per tutti i ListView.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tabella ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310796"
---
# <a name="listview-table"></a><span data-ttu-id="8fb12-104">Tabella ListView</span><span class="sxs-lookup"><span data-stu-id="8fb12-104">ListView Table</span></span>

<span data-ttu-id="8fb12-105">Le righe di un controllo ListView non vengono considerate come singoli controlli, ma fanno parte di un ListView che funge da controllo.</span><span class="sxs-lookup"><span data-stu-id="8fb12-105">The lines of a listview are not treated as individual controls, but they are part of a listview that functions as a control.</span></span> <span data-ttu-id="8fb12-106">La tabella ListView definisce i valori per tutti i ListView.</span><span class="sxs-lookup"><span data-stu-id="8fb12-106">The ListView table defines the values for all listviews.</span></span>

<span data-ttu-id="8fb12-107">La tabella ListView contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="8fb12-107">The ListView table has the following columns.</span></span>



| <span data-ttu-id="8fb12-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="8fb12-108">Column</span></span>   | <span data-ttu-id="8fb12-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fb12-109">Type</span></span>                         | <span data-ttu-id="8fb12-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="8fb12-110">Key</span></span> | <span data-ttu-id="8fb12-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="8fb12-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="8fb12-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8fb12-112">Property</span></span> | [<span data-ttu-id="8fb12-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8fb12-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="8fb12-114">S</span><span class="sxs-lookup"><span data-stu-id="8fb12-114">Y</span></span>   | <span data-ttu-id="8fb12-115">N</span><span class="sxs-lookup"><span data-stu-id="8fb12-115">N</span></span>        |
| <span data-ttu-id="8fb12-116">JSON</span><span class="sxs-lookup"><span data-stu-id="8fb12-116">Order</span></span>    | [<span data-ttu-id="8fb12-117">Integer</span><span class="sxs-lookup"><span data-stu-id="8fb12-117">Integer</span></span>](integer.md)       | <span data-ttu-id="8fb12-118">S</span><span class="sxs-lookup"><span data-stu-id="8fb12-118">Y</span></span>   | <span data-ttu-id="8fb12-119">N</span><span class="sxs-lookup"><span data-stu-id="8fb12-119">N</span></span>        |
| <span data-ttu-id="8fb12-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb12-120">Value</span></span>    | [<span data-ttu-id="8fb12-121">Formattato</span><span class="sxs-lookup"><span data-stu-id="8fb12-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8fb12-122">N</span><span class="sxs-lookup"><span data-stu-id="8fb12-122">N</span></span>   | <span data-ttu-id="8fb12-123">N</span><span class="sxs-lookup"><span data-stu-id="8fb12-123">N</span></span>        |
| <span data-ttu-id="8fb12-124">Testo</span><span class="sxs-lookup"><span data-stu-id="8fb12-124">Text</span></span>     | [<span data-ttu-id="8fb12-125">Formattato</span><span class="sxs-lookup"><span data-stu-id="8fb12-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8fb12-126">N</span><span class="sxs-lookup"><span data-stu-id="8fb12-126">N</span></span>   | <span data-ttu-id="8fb12-127">S</span><span class="sxs-lookup"><span data-stu-id="8fb12-127">Y</span></span>        |
| <span data-ttu-id="8fb12-128">Binary\_</span><span class="sxs-lookup"><span data-stu-id="8fb12-128">Binary\_</span></span> | [<span data-ttu-id="8fb12-129">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8fb12-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="8fb12-130">N</span><span class="sxs-lookup"><span data-stu-id="8fb12-130">N</span></span>   | <span data-ttu-id="8fb12-131">S</span><span class="sxs-lookup"><span data-stu-id="8fb12-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8fb12-132">Colonne</span><span class="sxs-lookup"><span data-stu-id="8fb12-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8fb12-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà</span><span class="sxs-lookup"><span data-stu-id="8fb12-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="8fb12-134">Proprietà denominata da associare a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="8fb12-134">A named property to be tied to this item.</span></span> <span data-ttu-id="8fb12-135">Tutti gli elementi collegati alla stessa proprietà diventano parte dello stesso ListView.</span><span class="sxs-lookup"><span data-stu-id="8fb12-135">All the items tied to the same property become part of the same listview.</span></span>

</dd> <dt>

<span data-ttu-id="8fb12-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine</span><span class="sxs-lookup"><span data-stu-id="8fb12-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="8fb12-137">Intero positivo utilizzato per determinare l'ordinamento degli elementi visualizzati in un singolo elenco ListView.</span><span class="sxs-lookup"><span data-stu-id="8fb12-137">A positive integer used to determine the ordering of the items that appear in a single listview list.</span></span> <span data-ttu-id="8fb12-138">I numeri interi non devono essere consecutivi.</span><span class="sxs-lookup"><span data-stu-id="8fb12-138">The integers do not have to be consecutive.</span></span> <span data-ttu-id="8fb12-139">Se un ListView viene definito come ordinato, tutti gli elementi devono avere un valore di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="8fb12-139">If a listview is defined as ordered, then all the items should have an Ordering value.</span></span> <span data-ttu-id="8fb12-140">Se ListView è definito come non ordinato, la colonna viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="8fb12-140">If the listview is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="8fb12-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="8fb12-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="8fb12-142">Stringa del valore associata a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="8fb12-142">The value string associated with this item.</span></span> <span data-ttu-id="8fb12-143">Selezionando la riga, la proprietà associata verrà impostata su questo valore.</span><span class="sxs-lookup"><span data-stu-id="8fb12-143">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="8fb12-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo</span><span class="sxs-lookup"><span data-stu-id="8fb12-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="8fb12-145">Testo visibile e localizzabile da assegnare all'elemento.</span><span class="sxs-lookup"><span data-stu-id="8fb12-145">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="8fb12-146">Se questa voce o l'intera colonna risulta mancante, per impostazione predefinita il testo viene impostato sulla voce corrispondente in value.</span><span class="sxs-lookup"><span data-stu-id="8fb12-146">If this entry or the entire column is missing, then the text defaults to the corresponding entry in Value.</span></span>

</dd> <dt>

<span data-ttu-id="8fb12-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binario\_</span><span class="sxs-lookup"><span data-stu-id="8fb12-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binary\_</span></span>
</dt> <dd>

<span data-ttu-id="8fb12-148">Dati dell'immagine per l'icona.</span><span class="sxs-lookup"><span data-stu-id="8fb12-148">The image data for the icon.</span></span> <span data-ttu-id="8fb12-149">Si tratta di una chiave esterna per la [tabella binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="8fb12-149">This is a foreign key to the [Binary table](binary-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fb12-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fb12-150">Remarks</span></span>

<span data-ttu-id="8fb12-151">Il contenuto del valore e i campi di testo vengono formattati dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo, pertanto possono contenere qualsiasi espressione che la funzione MsiFormatRecord possa interpretare.</span><span class="sxs-lookup"><span data-stu-id="8fb12-151">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the MsiFormatRecord function can interpret.</span></span> <span data-ttu-id="8fb12-152">La formattazione si verifica solo quando viene creato il controllo e non viene aggiornata se una proprietà richiesta nell'espressione viene modificata durante il ciclo di vita del controllo.</span><span class="sxs-lookup"><span data-stu-id="8fb12-152">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="8fb12-153">Convalida</span><span class="sxs-lookup"><span data-stu-id="8fb12-153">Validation</span></span>

<dl>

[<span data-ttu-id="8fb12-154">ICE03</span><span class="sxs-lookup"><span data-stu-id="8fb12-154">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8fb12-155">ICE06</span><span class="sxs-lookup"><span data-stu-id="8fb12-155">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8fb12-156">ICE17</span><span class="sxs-lookup"><span data-stu-id="8fb12-156">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="8fb12-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="8fb12-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



