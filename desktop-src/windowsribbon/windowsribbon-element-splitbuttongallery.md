---
title: Elemento SplitButtonGallery
description: Rappresenta un controllo raccolta di pulsanti di menu combinato con un menu a discesa basato sulla raccolta.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Barra multifunzione Windows elemento SplitButtonGallery
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68e90137325c16af6942f9f3929f8abfdf795660
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473782"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="bb143-104">Elemento SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="bb143-104">SplitButtonGallery element</span></span>

<span data-ttu-id="bb143-105">Rappresenta un controllo [raccolta di pulsanti](windowsribbon-controls-splitbuttongallery.md) di menu combinato con un menu a discesa basato sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bb143-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="bb143-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="bb143-106">Usage</span></span>

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
```

## <a name="attributes"></a><span data-ttu-id="bb143-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="bb143-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb143-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="bb143-108">Attribute</span></span></th>
<th><span data-ttu-id="bb143-109">Type</span><span class="sxs-lookup"><span data-stu-id="bb143-109">Type</span></span></th>
<th><span data-ttu-id="bb143-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="bb143-110">Required</span></span></th>
<th><span data-ttu-id="bb143-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb143-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb143-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="bb143-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="bb143-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="bb143-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="bb143-114">No</span><span class="sxs-lookup"><span data-stu-id="bb143-114">No</span></span><br/></td>
<td><span data-ttu-id="bb143-115">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="bb143-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="bb143-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="bb143-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bb143-117">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="bb143-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="bb143-118">Gli spazi vuoti sono validi e vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="bb143-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="bb143-119">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bb143-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb143-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="bb143-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="bb143-121">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="bb143-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="bb143-122">No</span><span class="sxs-lookup"><span data-stu-id="bb143-122">No</span></span><br/></td>
<td><span data-ttu-id="bb143-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb143-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="bb143-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="bb143-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bb143-125">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="bb143-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="bb143-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="bb143-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="bb143-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bb143-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb143-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="bb143-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="bb143-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="bb143-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="bb143-130">No</span><span class="sxs-lookup"><span data-stu-id="bb143-130">No</span></span><br/></td>
<td><span data-ttu-id="bb143-131">Determina se la risorsa immagine grande o piccola del comando viene visualizzata nel controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="bb143-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bb143-132">Si applica solo alle raccolte in cui il valore dell'attributo <em>Type</em> è uguale a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="bb143-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="bb143-133">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="bb143-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="bb143-134">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="bb143-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="bb143-135">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bb143-135">Default.</span></span> <br/> </dd> <span data-ttu-id="bb143-136"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="bb143-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb143-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="bb143-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="bb143-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bb143-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="bb143-139">No</span><span class="sxs-lookup"><span data-stu-id="bb143-139">No</span></span><br/></td>
<td><span data-ttu-id="bb143-140"><dt><span></span><span></span><strong></strong> (XS: Integer)</span><span class="sxs-lookup"><span data-stu-id="bb143-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="bb143-141">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="bb143-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb143-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="bb143-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="bb143-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bb143-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="bb143-144">No</span><span class="sxs-lookup"><span data-stu-id="bb143-144">No</span></span><br/></td>
<td><span data-ttu-id="bb143-145"><dt><span></span><span></span><strong></strong> (XS: Integer)</span><span class="sxs-lookup"><span data-stu-id="bb143-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="bb143-146">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="bb143-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb143-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="bb143-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="bb143-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="bb143-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="bb143-149">No</span><span class="sxs-lookup"><span data-stu-id="bb143-149">No</span></span><br/></td>
<td><span data-ttu-id="bb143-150">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb143-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="bb143-151">
<dt><span></span><span></span><strong></strong> Parte inferiore</span><span class="sxs-lookup"><span data-stu-id="bb143-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="bb143-152"><dt><span></span><span></span><strong></strong> Nascondere</span><span class="sxs-lookup"><span data-stu-id="bb143-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="bb143-153"><dt><span></span><span></span><strong></strong> Sinistra</span><span class="sxs-lookup"><span data-stu-id="bb143-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="bb143-154"><dt><span></span><span></span><strong></strong> Sovrapposizione</span><span class="sxs-lookup"><span data-stu-id="bb143-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="bb143-155"><dt><span></span><span></span><strong></strong> Destra</span><span class="sxs-lookup"><span data-stu-id="bb143-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="bb143-156"><dt><span></span><span></span><strong></strong> Top</span><span class="sxs-lookup"><span data-stu-id="bb143-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb143-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="bb143-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="bb143-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="bb143-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="bb143-159">No</span><span class="sxs-lookup"><span data-stu-id="bb143-159">No</span></span><br/></td>
<td><span data-ttu-id="bb143-160">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb143-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="bb143-161">
<dt><span></span><span></span><strong></strong> Elementi</span><span class="sxs-lookup"><span data-stu-id="bb143-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="bb143-162"><dt><span></span><span></span><strong></strong> Comandi</span><span class="sxs-lookup"><span data-stu-id="bb143-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="bb143-163">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bb143-163">Child elements</span></span>



| <span data-ttu-id="bb143-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="bb143-164">Element</span></span>                                                                                                 | <span data-ttu-id="bb143-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb143-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="bb143-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="bb143-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="bb143-167">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="bb143-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bb143-168">**Casella**</span><span class="sxs-lookup"><span data-stu-id="bb143-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="bb143-169">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="bb143-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bb143-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="bb143-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="bb143-171">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="bb143-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bb143-172">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="bb143-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="bb143-173">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="bb143-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="bb143-174">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="bb143-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="bb143-175">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="bb143-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="bb143-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="bb143-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="bb143-177">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="bb143-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bb143-178">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="bb143-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb143-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="bb143-179">Element</span></span></th>
<th><span data-ttu-id="bb143-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb143-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb143-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb143-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bb143-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb143-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bb143-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb143-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="bb143-184">Quando è contenuto in un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb143-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="bb143-185">Questo elemento è supportato solo al primo livello e non deve avere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="bb143-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb143-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb143-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="bb143-187">Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="bb143-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb143-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb143-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="bb143-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb143-189">Remarks</span></span>

<span data-ttu-id="bb143-190">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bb143-190">Optional.</span></span>

<span data-ttu-id="bb143-191">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="bb143-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="bb143-192">**SplitButtonGallery** supporta le [modalità di applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="bb143-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="bb143-193">[Interfaccia utente \_ PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) viene usato da un'applicazione per eseguire una query sullo stato di attivazione/disattivazione per il controllo Button di un **SplitButtonGallery**.</span><span class="sxs-lookup"><span data-stu-id="bb143-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="bb143-194">Lo screenshot seguente illustra il controllo raccolta dei [pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md) della barra multifunzione in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb143-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot di un controllo raccolta di pulsanti di suddivisione in Microsoft Paint per Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="bb143-196">Esempio</span><span class="sxs-lookup"><span data-stu-id="bb143-196">Examples</span></span>

<span data-ttu-id="bb143-197">Nell'esempio seguente viene illustrato il markup di base per la [raccolta dei pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="bb143-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="bb143-198">In questa sezione del codice vengono illustrate le dichiarazioni di comando **SplitButtonGallery** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButtonGallery** .</span><span class="sxs-lookup"><span data-stu-id="bb143-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



<span data-ttu-id="bb143-199">In questa sezione del codice vengono illustrate le dichiarazioni di controllo **SplitButtonGallery** .</span><span class="sxs-lookup"><span data-stu-id="bb143-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="bb143-200">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bb143-200">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="bb143-201">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb143-201">Minimum supported system</span></span><br/> | <span data-ttu-id="bb143-202">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb143-202">Windows 7</span></span> |
| <span data-ttu-id="bb143-203">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="bb143-203">Can be empty</span></span>                        | <span data-ttu-id="bb143-204">No</span><span class="sxs-lookup"><span data-stu-id="bb143-204">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="bb143-205">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bb143-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb143-206">Controllo raccolta pulsanti di suddivisione</span><span class="sxs-lookup"><span data-stu-id="bb143-206">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="bb143-207">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="bb143-207">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="bb143-208">**Modalità selettore**</span><span class="sxs-lookup"><span data-stu-id="bb143-208">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="bb143-209">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="bb143-209">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

