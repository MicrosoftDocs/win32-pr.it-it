---
title: LISTBOX (elemento)
description: LISTBOX (elemento)
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- Windows Media Player Skin, elemento LISTBOX
- interfacce, elemento LISTBOX
- LISTBOX (elemento)
- riferimento per le interfacce, elemento LISTBOX
- elementi, LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d9566d11586e995b289a0048dacb29a91921b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044501"
---
# <a name="listbox-element"></a><span data-ttu-id="b559d-108">LISTBOX (elemento)</span><span class="sxs-lookup"><span data-stu-id="b559d-108">LISTBOX Element</span></span>

<span data-ttu-id="b559d-109">L'elemento **ListBox** consente agli utenti di selezionare gli elementi da un elenco.</span><span class="sxs-lookup"><span data-stu-id="b559d-109">The **LISTBOX** element provides a way for users to select items from a list.</span></span> <span data-ttu-id="b559d-110">Questi elementi possono essere specificati usando gli elementi **elemento** come elementi figlio dell'elemento **ListBox** .</span><span class="sxs-lookup"><span data-stu-id="b559d-110">These items can be specified by using **ITEM** elements as children of the **LISTBOX** element.</span></span> <span data-ttu-id="b559d-111">Se è necessario un controllo casella di riepilogo visualizzato solo quando necessario, utilizzare l'elemento **popup** , che è identico all'elemento **ListBox** , ad eccezione del valore predefinito dell'attributo **popup** , che determina il comportamento di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b559d-111">If you need a list box control that is displayed only when needed, use the **POPUP** element, which is identical to the **LISTBOX** element except for the default value of the **popUp** attribute, which dictates its display behavior.</span></span>

<span data-ttu-id="b559d-112">L'elemento **ListBox** supporta gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b559d-112">The **LISTBOX** element supports the following attributes.</span></span>



| <span data-ttu-id="b559d-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="b559d-113">Attribute</span></span>                                        | <span data-ttu-id="b559d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b559d-114">Description</span></span>                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b559d-115">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b559d-115">backgroundColor</span></span>](listbox-backgroundcolor.md)   | <span data-ttu-id="b559d-116">Specifica o Recupera il colore di sfondo nel controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-116">Specifies or retrieves the background color in the list box control.</span></span>                                                  |
| [<span data-ttu-id="b559d-117">bordo</span><span class="sxs-lookup"><span data-stu-id="b559d-117">border</span></span>](listbox-border.md)                     | <span data-ttu-id="b559d-118">Specifica o recupera un valore che indica se il controllo casella di riepilogo presenta un bordo.</span><span class="sxs-lookup"><span data-stu-id="b559d-118">Specifies or retrieves a value indicating whether the list box control has a border.</span></span> <span data-ttu-id="b559d-119">Può essere impostato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="b559d-119">Can only be set at design time.</span></span>  |
| [<span data-ttu-id="b559d-120">firstVisibleItem</span><span class="sxs-lookup"><span data-stu-id="b559d-120">firstVisibleItem</span></span>](listbox-firstvisibleitem.md) | <span data-ttu-id="b559d-121">Specifica o recupera l'indice della prima riga visibile nel controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-121">Specifies or retrieves the index of the first visible line in the list box control.</span></span>                                   |
| [<span data-ttu-id="b559d-122">focusItem</span><span class="sxs-lookup"><span data-stu-id="b559d-122">focusItem</span></span>](listbox-focusitem.md)               | <span data-ttu-id="b559d-123">Specifica o recupera la riga che contiene lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b559d-123">Specifies or retrieves the line that contains focus.</span></span>                                                                  |
| [<span data-ttu-id="b559d-124">fontFace</span><span class="sxs-lookup"><span data-stu-id="b559d-124">fontFace</span></span>](listbox-fontface.md)                 | <span data-ttu-id="b559d-125">Specifica o Recupera il tipo di carattere per il controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-125">Specifies or retrieves the font for the list box control.</span></span>                                                             |
| [<span data-ttu-id="b559d-126">fontSize</span><span class="sxs-lookup"><span data-stu-id="b559d-126">fontSize</span></span>](listbox-fontsize.md)                 | <span data-ttu-id="b559d-127">Specifica o recupera le dimensioni del carattere per il controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-127">Specifies or retrieves the font size for the list box control.</span></span>                                                        |
| [<span data-ttu-id="b559d-128">fontStyle</span><span class="sxs-lookup"><span data-stu-id="b559d-128">fontStyle</span></span>](listbox-fontstyle.md)               | <span data-ttu-id="b559d-129">Specifica o recupera lo stile del carattere per il controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-129">Specifies or retrieves the font style for the list box control.</span></span>                                                       |
| [<span data-ttu-id="b559d-130">foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b559d-130">foregroundColor</span></span>](listbox-foregroundcolor.md)   | <span data-ttu-id="b559d-131">Specifica o Recupera il colore del testo nel controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-131">Specifies or retrieves the text color in the list box control.</span></span>                                                        |
| [<span data-ttu-id="b559d-132">itemCount</span><span class="sxs-lookup"><span data-stu-id="b559d-132">itemCount</span></span>](listbox-itemcount.md)               | <span data-ttu-id="b559d-133">Recupera il numero di elementi nel controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-133">Retrieves the number of items in the list box control.</span></span>                                                                |
| [<span data-ttu-id="b559d-134">multiSelect</span><span class="sxs-lookup"><span data-stu-id="b559d-134">multiSelect</span></span>](listbox-multiselect.md)           | <span data-ttu-id="b559d-135">Specifica o recupera un valore che indica se l'utente può selezionare più righe.</span><span class="sxs-lookup"><span data-stu-id="b559d-135">Specifies or retrieves a value indicating whether the user can select multiple lines.</span></span> <span data-ttu-id="b559d-136">Può essere impostato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="b559d-136">Can only be set at design time.</span></span> |
| [<span data-ttu-id="b559d-137">popUp</span><span class="sxs-lookup"><span data-stu-id="b559d-137">popUp</span></span>](listbox-popup.md)                       | <span data-ttu-id="b559d-138">Specifica un valore che indica se l'elemento rappresenta un controllo popup o una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-138">Specifies a value indicating whether the element represents a popup or list box control.</span></span>                              |
| [<span data-ttu-id="b559d-139">readOnly</span><span class="sxs-lookup"><span data-stu-id="b559d-139">readOnly</span></span>](listbox-readonly.md)                 | <span data-ttu-id="b559d-140">Specifica o recupera un valore che indica se il testo è di sola lettura o se il testo può essere selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b559d-140">Specifies or retrieves a value indicating whether text is read-only or text can be selected by the user.</span></span>              |
| [<span data-ttu-id="b559d-141">selectedItem</span><span class="sxs-lookup"><span data-stu-id="b559d-141">selectedItem</span></span>](listbox-selecteditem.md)         | <span data-ttu-id="b559d-142">Specifica o recupera l'indice dell'elemento selezionato nel controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-142">Specifies or retrieves the index of the item selected in the list box control.</span></span>                                        |
| [<span data-ttu-id="b559d-143">ordinati</span><span class="sxs-lookup"><span data-stu-id="b559d-143">sorted</span></span>](listbox-sorted.md)                     | <span data-ttu-id="b559d-144">Specifica o recupera un valore che indica se il controllo casella di riepilogo è ordinato in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="b559d-144">Specifies or retrieves a value indicating whether the list box control is sorted alphabetically.</span></span>                      |



 

<span data-ttu-id="b559d-145">L'elemento **ListBox** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b559d-145">The **LISTBOX** element supports the following methods.</span></span>



| <span data-ttu-id="b559d-146">Metodo</span><span class="sxs-lookup"><span data-stu-id="b559d-146">Method</span></span>                                                 | <span data-ttu-id="b559d-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b559d-147">Description</span></span>                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b559d-148">appendItem</span><span class="sxs-lookup"><span data-stu-id="b559d-148">appendItem</span></span>](listbox-appenditem.md)                   | <span data-ttu-id="b559d-149">Inserisce nuovo testo alla fine del controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-149">Inserts new text at the end of the list box control.</span></span>                                                                  |
| [<span data-ttu-id="b559d-150">deleteAll</span><span class="sxs-lookup"><span data-stu-id="b559d-150">deleteAll</span></span>](listbox-deleteall.md)                     | <span data-ttu-id="b559d-151">Elimina tutti gli elementi dal controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-151">Deletes all items from the list box control.</span></span>                                                                          |
| [<span data-ttu-id="b559d-152">deleteItem</span><span class="sxs-lookup"><span data-stu-id="b559d-152">deleteItem</span></span>](listbox-deleteitem.md)                   | <span data-ttu-id="b559d-153">Elimina l'elemento di controllo della casella di riepilogo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="b559d-153">Deletes the list box control item at the specified index.</span></span>                                                             |
| [<span data-ttu-id="b559d-154">respingere</span><span class="sxs-lookup"><span data-stu-id="b559d-154">dismiss</span></span>](listbox-dismiss.md)                         | <span data-ttu-id="b559d-155">Nasconde il controllo.</span><span class="sxs-lookup"><span data-stu-id="b559d-155">Hides the control.</span></span>                                                                                                    |
| [<span data-ttu-id="b559d-156">findItem</span><span class="sxs-lookup"><span data-stu-id="b559d-156">findItem</span></span>](listbox-finditem.md)                       | <span data-ttu-id="b559d-157">Cerca una determinata stringa a partire dall'elemento che segue l'indice dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="b559d-157">Searches for a given string starting with the item following the specified item index.</span></span>                                |
| [<span data-ttu-id="b559d-158">getItem</span><span class="sxs-lookup"><span data-stu-id="b559d-158">getItem</span></span>](listbox-getitem.md)                         | <span data-ttu-id="b559d-159">Recupera il testo per l'elemento con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="b559d-159">Retrieves the text for the item with the specified index.</span></span>                                                             |
| [<span data-ttu-id="b559d-160">getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="b559d-160">getNextSelectedItem</span></span>](listbox-getnextselecteditem.md) | <span data-ttu-id="b559d-161">Recupera il successivo elemento selezionato nel controllo casella di riepilogo a partire dall'elemento dopo quello con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="b559d-161">Retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span> |
| [<span data-ttu-id="b559d-162">insertItem</span><span class="sxs-lookup"><span data-stu-id="b559d-162">insertItem</span></span>](listbox-insertitem.md)                   | <span data-ttu-id="b559d-163">Inserisce il testo specificato in corrispondenza dell'indice specificato nel controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b559d-163">Inserts the specified text at the specified index in the list box control.</span></span>                                            |
| [<span data-ttu-id="b559d-164">replaceItem</span><span class="sxs-lookup"><span data-stu-id="b559d-164">replaceItem</span></span>](listbox-replaceitem.md)                 | <span data-ttu-id="b559d-165">Sostituisce il testo in corrispondenza dell'indice specificato con il testo specificato.</span><span class="sxs-lookup"><span data-stu-id="b559d-165">Replaces the text at the specified index with the specified text.</span></span>                                                     |
| [<span data-ttu-id="b559d-166">setSelectedState</span><span class="sxs-lookup"><span data-stu-id="b559d-166">setSelectedState</span></span>](listbox-setselectedstate.md)       | <span data-ttu-id="b559d-167">Seleziona o deseleziona l'elemento con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="b559d-167">Selects or unselects the item with the specified index.</span></span>                                                               |
| [<span data-ttu-id="b559d-168">show</span><span class="sxs-lookup"><span data-stu-id="b559d-168">show</span></span>](listbox-show.md)                               | <span data-ttu-id="b559d-169">Visualizza il controllo.</span><span class="sxs-lookup"><span data-stu-id="b559d-169">Displays the control.</span></span>                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="b559d-170">Questo elemento richiede Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b559d-170">This element requires Windows Media Player for Windows XP or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b559d-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b559d-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b559d-172">**Elemento POPUP**</span><span class="sxs-lookup"><span data-stu-id="b559d-172">**POPUP Element**</span></span>](popup-element.md)
</dt> <dt>

[<span data-ttu-id="b559d-173">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="b559d-173">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




