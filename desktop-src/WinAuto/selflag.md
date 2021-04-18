---
title: Costanti SELFLAG (oleacc. h)
description: In questo argomento vengono descritti i valori costanti utilizzati per specificare la modalità di selezione di un oggetto accessibile o lo stato attivo.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327702"
---
# <a name="selflag-constants"></a><span data-ttu-id="e9945-103">Costanti SELFLAG</span><span class="sxs-lookup"><span data-stu-id="e9945-103">SELFLAG Constants</span></span>

<span data-ttu-id="e9945-104">In questo argomento vengono descritti i valori costanti utilizzati per specificare la modalità di selezione di un oggetto accessibile o lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="e9945-104">This topic describes the constant values used to specify how an accessible object becomes selected or takes the focus.</span></span> <span data-ttu-id="e9945-105">Le costanti sono definite in oleacc. h e vengono usate con il metodo [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .</span><span class="sxs-lookup"><span data-stu-id="e9945-105">The constants are defined in oleacc.h and are used with the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method.</span></span>

<span data-ttu-id="e9945-106">Non sono consentite le combinazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9945-106">The following combinations are not allowed:</span></span>

-   <span data-ttu-id="e9945-107">SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-107">SELFLAG\_ADDSELECTION \| SELFLAG\_REMOVESELECTION</span></span>
-   <span data-ttu-id="e9945-108">SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-108">SELFLAG\_ADDSELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="e9945-109">SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-109">SELFLAG\_REMOVESELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="e9945-110">SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-110">SELFLAG\_EXTENDSELECTION \| SELFLAG\_TAKESELECTION</span></span>

<span data-ttu-id="e9945-111">**Nota ai client:** Microsoft Active Accessibility non supporta la selezione del testo contenuto nei controlli Edit e Rich Edit perché il testo viene esposto come stringa nella [proprietà Value](value-property.md)dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9945-111">**Note to clients :** Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a string in the object's [Value property](value-property.md).</span></span>

<span data-ttu-id="e9945-112">Per informazioni su come eseguire operazioni di selezione complesse, vedere [selezione di oggetti figlio](selecting-child-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e9945-112">For information on how to perform complex selection operations, see [Selecting Child Objects](selecting-child-objects.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e9945-113">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="e9945-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e9945-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9945-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <span data-ttu-id="e9945-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="e9945-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9945-116">Non esegue alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="e9945-116">Performs no action.</span></span> <span data-ttu-id="e9945-117">Microsoft Active Accessibility non modifica la selezione o lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="e9945-117">Microsoft Active Accessibility does not change the selection or focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <span data-ttu-id="e9945-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span><span class="sxs-lookup"><span data-stu-id="e9945-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9945-119">Imposta lo stato attivo sull'oggetto e lo rende l'ancoraggio della selezione.</span><span class="sxs-lookup"><span data-stu-id="e9945-119">Sets the focus to the object and makes it the selection anchor.</span></span> <span data-ttu-id="e9945-120">Usato da solo, questo flag non modifica la selezione.</span><span class="sxs-lookup"><span data-stu-id="e9945-120">Used by itself, this flag does not alter the selection.</span></span> <span data-ttu-id="e9945-121">L'effetto è simile allo spostare lo stato attivo manualmente premendo un tasto di direzione tenendo premuto il tasto CTRL in Esplora risorse o in qualsiasi casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="e9945-121">The effect is similar to moving the focus manually by pressing an ARROW key while holding down the CTRL key in Windows Explorer or in any multiple-selection list box.</span></span> <br/> <span data-ttu-id="e9945-122">Con gli oggetti con il <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS viene combinato con i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9945-122">With objects that have the <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS is combined with the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="e9945-123">SELFLAG_TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-123">SELFLAG_TAKESELECTION</span></span></li>
<li><span data-ttu-id="e9945-124">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-124">SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="e9945-125">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-125">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="e9945-126">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-126">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="e9945-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="e9945-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
</ul>
<span data-ttu-id="e9945-129">Se si chiama <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: accSelect</strong></a> con il flag SELFLAG_TAKEFOCUS su un oggetto con <strong>HWND</strong>, il flag diviene effettivo solo se l'elemento padre dell'oggetto ha già lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="e9945-129">If you call <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> with the SELFLAG_TAKEFOCUS flag on an object that has an <strong>HWND</strong>, the flag will take effect only if the object's parent already has the focus.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <span data-ttu-id="e9945-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span><span class="sxs-lookup"><span data-stu-id="e9945-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9945-131">Seleziona l'oggetto e rimuove la selezione da tutti gli altri oggetti nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="e9945-131">Selects the object and removes the selection from all other objects in the container.</span></span> <br/> <span data-ttu-id="e9945-132">A meno che non sia combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio della selezione.</span><span class="sxs-lookup"><span data-stu-id="e9945-132">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="e9945-133">SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinazione è equivalente a un solo clic su un elemento in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e9945-133">The SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to single-clicking an item in Windows Explorer.</span></span><br/> <span data-ttu-id="e9945-134">Questo flag non deve essere combinato con i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9945-134">This flag must not be combined with the following flags:</span></span><br/>
<ul>
<li><span data-ttu-id="e9945-135">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-135">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="e9945-136">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-136">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="e9945-137">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="e9945-137">SELFLAG_EXTENDSELECTION</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <span data-ttu-id="e9945-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span><span class="sxs-lookup"><span data-stu-id="e9945-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9945-139">Modifica la selezione in modo che tutti gli oggetti tra l'ancoraggio di selezione e questo oggetto prendano lo stato di selezione dell'oggetto di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="e9945-139">Alters the selection so that all objects between the selection anchor and this object take on the anchor object's selection state.</span></span> <span data-ttu-id="e9945-140">Se tale oggetto non è selezionato, gli oggetti verranno rimossi dalla selezione.</span><span class="sxs-lookup"><span data-stu-id="e9945-140">If the anchor object is not selected, the objects are removed from the selection.</span></span> <span data-ttu-id="e9945-141">Se l'oggetto di ancoraggio è selezionato, la selezione viene estesa in modo da includere questo oggetto e tutti gli oggetti in.</span><span class="sxs-lookup"><span data-stu-id="e9945-141">If the anchor object is selected, the selection is extended to include this object and all the objects in between.</span></span> <span data-ttu-id="e9945-142">Impostare lo stato di selezione combinando questo flag con SELFLAG_ADDSELECTION o SELFLAG_REMOVESELECTION.</span><span class="sxs-lookup"><span data-stu-id="e9945-142">Set the selection state by combining this flag with SELFLAG_ADDSELECTION or SELFLAG_REMOVESELECTION.</span></span> <br/> <span data-ttu-id="e9945-143">A meno che non sia combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio della selezione.</span><span class="sxs-lookup"><span data-stu-id="e9945-143">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="e9945-144">SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinazione equivale all'aggiunta manuale di un elemento a una selezione tenendo premuto il tasto MAIUSC e facendo clic su un oggetto non selezionato in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e9945-144">The SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the SHIFT key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="e9945-145">Questo flag non è combinato con SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="e9945-145">This flag is not combined with SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <span data-ttu-id="e9945-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span><span class="sxs-lookup"><span data-stu-id="e9945-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9945-147">Aggiunge l'oggetto alla selezione corrente. il risultato possibile è una selezione non contigua.</span><span class="sxs-lookup"><span data-stu-id="e9945-147">Adds the object to the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="e9945-148">A meno che non sia combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio della selezione.</span><span class="sxs-lookup"><span data-stu-id="e9945-148">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="e9945-149">SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinazione equivale all'aggiunta manuale di un elemento a una selezione tenendo premuto il tasto CTRL e facendo clic su un oggetto non selezionato in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e9945-149">The SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the CTRL key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="e9945-150">Questo flag non è combinato con SELFLAG_REMOVESELECTION o SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="e9945-150">This flag is not combined with SELFLAG_REMOVESELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <span data-ttu-id="e9945-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span><span class="sxs-lookup"><span data-stu-id="e9945-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9945-152">Rimuove l'oggetto dalla selezione corrente. il risultato possibile è una selezione non contigua.</span><span class="sxs-lookup"><span data-stu-id="e9945-152">Removes the object from the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="e9945-153">A meno che non sia combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio della selezione.</span><span class="sxs-lookup"><span data-stu-id="e9945-153">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="e9945-154">SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinazione equivale a rimuovere un elemento da una selezione manualmente, tenendo premuto il tasto CTRL mentre si fa clic su un oggetto selezionato in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e9945-154">The SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to removing an item from a selection manually, by holding down the CTRL key while clicking a selected object in Windows Explorer.</span></span><br/> <span data-ttu-id="e9945-155">Questo flag non è combinato con SELFLAG_ADDSELECTION o SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="e9945-155">This flag is not combined with SELFLAG_ADDSELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e9945-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9945-156">Requirements</span></span>



| <span data-ttu-id="e9945-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9945-157">Requirement</span></span> | <span data-ttu-id="e9945-158">Valore</span><span class="sxs-lookup"><span data-stu-id="e9945-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9945-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9945-159">Header</span></span><br/> | <dl> <span data-ttu-id="e9945-160"><dt>Oleacc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9945-160"><dt>Oleacc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9945-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9945-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9945-162">**IAccessible:: accSelect**</span><span class="sxs-lookup"><span data-stu-id="e9945-162">**IAccessible::accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[<span data-ttu-id="e9945-163">Selezione di oggetti figlio</span><span class="sxs-lookup"><span data-stu-id="e9945-163">Selecting Child Objects</span></span>](selecting-child-objects.md)
</dt> </dl>

 

 





