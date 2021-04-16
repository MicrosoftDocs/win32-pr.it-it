---
title: Elemento DropDownGallery
description: Rappresenta un controllo raccolta Drop-Down con un menu basato su raccolta.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- Barra multifunzione Windows elemento DropDownGallery
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dfc2890e33fa7f5d93919e7361465e163dadcb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516840"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="6fb3f-104">Elemento DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="6fb3f-104">DropDownGallery element</span></span>

<span data-ttu-id="6fb3f-105">Rappresenta un controllo [raccolta a discesa](windowsribbon-controls-dropdowngallery.md) con un menu basato su raccolta.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="6fb3f-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="6fb3f-106">Usage</span></span>

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
```

## <a name="attributes"></a><span data-ttu-id="6fb3f-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="6fb3f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fb3f-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="6fb3f-108">Attribute</span></span></th>
<th><span data-ttu-id="6fb3f-109">Type</span><span class="sxs-lookup"><span data-stu-id="6fb3f-109">Type</span></span></th>
<th><span data-ttu-id="6fb3f-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="6fb3f-110">Required</span></span></th>
<th><span data-ttu-id="6fb3f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fb3f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fb3f-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="6fb3f-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="6fb3f-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="6fb3f-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="6fb3f-114">No</span><span class="sxs-lookup"><span data-stu-id="6fb3f-114">No</span></span><br/></td>
<td><span data-ttu-id="6fb3f-115">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="6fb3f-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="6fb3f-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6fb3f-117">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="6fb3f-118">Gli spazi vuoti sono validi e vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="6fb3f-119">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fb3f-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="6fb3f-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="6fb3f-121">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="6fb3f-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="6fb3f-122">No</span><span class="sxs-lookup"><span data-stu-id="6fb3f-122">No</span></span><br/></td>
<td><span data-ttu-id="6fb3f-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="6fb3f-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="6fb3f-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6fb3f-125">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="6fb3f-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6fb3f-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fb3f-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="6fb3f-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="6fb3f-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="6fb3f-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="6fb3f-130">No</span><span class="sxs-lookup"><span data-stu-id="6fb3f-130">No</span></span><br/></td>
<td><span data-ttu-id="6fb3f-131">Determina se la risorsa immagine grande o piccola del comando viene visualizzata nel controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6fb3f-132">Si applica solo alle raccolte in cui il valore dell'attributo <em>Type</em> è uguale a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="6fb3f-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="6fb3f-133">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="6fb3f-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="6fb3f-134">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="6fb3f-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="6fb3f-135">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-135">Default.</span></span> <br/> </dd> <span data-ttu-id="6fb3f-136"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="6fb3f-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fb3f-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="6fb3f-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="6fb3f-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6fb3f-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="6fb3f-139">No</span><span class="sxs-lookup"><span data-stu-id="6fb3f-139">No</span></span><br/></td>
<td><span data-ttu-id="6fb3f-140"><dt><span></span><span></span><strong></strong> (XS: Integer)</span><span class="sxs-lookup"><span data-stu-id="6fb3f-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="6fb3f-141">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fb3f-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="6fb3f-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="6fb3f-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6fb3f-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="6fb3f-144">No</span><span class="sxs-lookup"><span data-stu-id="6fb3f-144">No</span></span><br/></td>
<td><span data-ttu-id="6fb3f-145"><dt><span></span><span></span><strong></strong> (XS: Integer)</span><span class="sxs-lookup"><span data-stu-id="6fb3f-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="6fb3f-146">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fb3f-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="6fb3f-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="6fb3f-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="6fb3f-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="6fb3f-149">No</span><span class="sxs-lookup"><span data-stu-id="6fb3f-149">No</span></span><br/></td>
<td><span data-ttu-id="6fb3f-150">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6fb3f-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="6fb3f-151">
<dt><span></span><span></span><strong></strong> Parte inferiore</span><span class="sxs-lookup"><span data-stu-id="6fb3f-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="6fb3f-152"><dt><span></span><span></span><strong></strong> Nascondere</span><span class="sxs-lookup"><span data-stu-id="6fb3f-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="6fb3f-153"><dt><span></span><span></span><strong></strong> Sinistra</span><span class="sxs-lookup"><span data-stu-id="6fb3f-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="6fb3f-154"><dt><span></span><span></span><strong></strong> Sovrapposizione</span><span class="sxs-lookup"><span data-stu-id="6fb3f-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="6fb3f-155"><dt><span></span><span></span><strong></strong> Destra</span><span class="sxs-lookup"><span data-stu-id="6fb3f-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="6fb3f-156"><dt><span></span><span></span><strong></strong> Top</span><span class="sxs-lookup"><span data-stu-id="6fb3f-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fb3f-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="6fb3f-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="6fb3f-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="6fb3f-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="6fb3f-159">No</span><span class="sxs-lookup"><span data-stu-id="6fb3f-159">No</span></span><br/></td>
<td><span data-ttu-id="6fb3f-160">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6fb3f-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="6fb3f-161">
<dt><span></span><span></span><strong></strong> Elementi</span><span class="sxs-lookup"><span data-stu-id="6fb3f-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="6fb3f-162"><dt><span></span><span></span><strong></strong> Comandi</span><span class="sxs-lookup"><span data-stu-id="6fb3f-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6fb3f-163">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6fb3f-163">Child elements</span></span>



| <span data-ttu-id="6fb3f-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="6fb3f-164">Element</span></span>                                                                                           | <span data-ttu-id="6fb3f-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fb3f-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="6fb3f-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="6fb3f-167">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6fb3f-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6fb3f-168">**Casella**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="6fb3f-169">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6fb3f-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6fb3f-170">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="6fb3f-171">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="6fb3f-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="6fb3f-172">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="6fb3f-173">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="6fb3f-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="6fb3f-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="6fb3f-175">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6fb3f-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6fb3f-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="6fb3f-177">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6fb3f-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6fb3f-178">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="6fb3f-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fb3f-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="6fb3f-179">Element</span></span></th>
<th><span data-ttu-id="6fb3f-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fb3f-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fb3f-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fb3f-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6fb3f-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fb3f-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6fb3f-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fb3f-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="6fb3f-184">Quando è contenuto in un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="6fb3f-185">Questo elemento è supportato solo al primo livello e non deve avere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fb3f-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fb3f-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="6fb3f-187">Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fb3f-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fb3f-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="6fb3f-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fb3f-189">Remarks</span></span>

<span data-ttu-id="6fb3f-190">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-190">Optional.</span></span>

<span data-ttu-id="6fb3f-191">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="6fb3f-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="6fb3f-192">**DropDownGallery** supporta le [modalità di applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="6fb3f-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="6fb3f-193">Lo screenshot seguente illustra il controllo raccolta a [discesa](windowsribbon-controls-dropdowngallery.md) della barra multifunzione in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot di un controllo raccolta a discesa in Microsoft Paint per Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="6fb3f-195">Esempio</span><span class="sxs-lookup"><span data-stu-id="6fb3f-195">Examples</span></span>

<span data-ttu-id="6fb3f-196">Nell'esempio seguente viene illustrato il markup di base per **DropDownGallery**.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="6fb3f-197">In questa sezione del codice vengono illustrate le dichiarazioni di comando **DropDownGallery** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **DropDownGallery** .</span><span class="sxs-lookup"><span data-stu-id="6fb3f-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



<span data-ttu-id="6fb3f-198">In questa sezione del codice vengono illustrate le dichiarazioni di controllo **DropDownGallery** .</span><span class="sxs-lookup"><span data-stu-id="6fb3f-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="6fb3f-199">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6fb3f-199">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="6fb3f-200">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fb3f-200">Minimum supported system</span></span><br/> | <span data-ttu-id="6fb3f-201">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6fb3f-201">Windows 7</span></span> |
| <span data-ttu-id="6fb3f-202">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="6fb3f-202">Can be empty</span></span>                        | <span data-ttu-id="6fb3f-203">No</span><span class="sxs-lookup"><span data-stu-id="6fb3f-203">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="6fb3f-204">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6fb3f-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb3f-205">**Controllo raccolta a discesa**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-205">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="6fb3f-206">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="6fb3f-206">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="6fb3f-207">**Modalità selettore**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-207">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="6fb3f-208">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="6fb3f-208">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

