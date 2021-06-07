---
title: DropDownGallery - elemento
description: Rappresenta un Drop-Down raccolta con un menu basato su raccolta.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- Barra multifunzione di Windows per l'elemento DropDownGallery
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befe0624dfef5910625a0aa067f3ad8cd9882ca2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443422"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="008f1-104">DropDownGallery - elemento</span><span class="sxs-lookup"><span data-stu-id="008f1-104">DropDownGallery element</span></span>

<span data-ttu-id="008f1-105">Rappresenta un [controllo Raccolta a discesa](windowsribbon-controls-dropdowngallery.md) con un menu basato su raccolta.</span><span class="sxs-lookup"><span data-stu-id="008f1-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="008f1-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="008f1-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="008f1-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="008f1-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="008f1-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="008f1-108">Attribute</span></span></th>
<th><span data-ttu-id="008f1-109">Type</span><span class="sxs-lookup"><span data-stu-id="008f1-109">Type</span></span></th>
<th><span data-ttu-id="008f1-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="008f1-110">Required</span></span></th>
<th><span data-ttu-id="008f1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="008f1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="008f1-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="008f1-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="008f1-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="008f1-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="008f1-114">No</span><span class="sxs-lookup"><span data-stu-id="008f1-114">No</span></span><br/></td>
<td><span data-ttu-id="008f1-115">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="008f1-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="008f1-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="008f1-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="008f1-117">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="008f1-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="008f1-118">Gli spazi vuoti sono validi e ignorati.</span><span class="sxs-lookup"><span data-stu-id="008f1-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="008f1-119">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="008f1-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008f1-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="008f1-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="008f1-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="008f1-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="008f1-122">No</span><span class="sxs-lookup"><span data-stu-id="008f1-122">No</span></span><br/></td>
<td><span data-ttu-id="008f1-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="008f1-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="008f1-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="008f1-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="008f1-125">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="008f1-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="008f1-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="008f1-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="008f1-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="008f1-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="008f1-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="008f1-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="008f1-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="008f1-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="008f1-130">No</span><span class="sxs-lookup"><span data-stu-id="008f1-130">No</span></span><br/></td>
<td><span data-ttu-id="008f1-131">Determina se la risorsa immagine grande o piccola del comando viene visualizzata nel controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="008f1-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="008f1-132">Si applica solo alle raccolte in cui il valore <em>dell'attributo Type</em> è uguale a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="008f1-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="008f1-133">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="008f1-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="008f1-134">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="008f1-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="008f1-135">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="008f1-135">Default.</span></span> <br/> </dd> <span data-ttu-id="008f1-136"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="008f1-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008f1-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="008f1-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="008f1-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="008f1-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="008f1-139">No</span><span class="sxs-lookup"><span data-stu-id="008f1-139">No</span></span><br/></td>
<td><span data-ttu-id="008f1-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="008f1-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="008f1-141">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="008f1-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="008f1-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="008f1-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="008f1-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="008f1-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="008f1-144">No</span><span class="sxs-lookup"><span data-stu-id="008f1-144">No</span></span><br/></td>
<td><span data-ttu-id="008f1-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="008f1-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="008f1-146">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="008f1-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008f1-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="008f1-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="008f1-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="008f1-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="008f1-149">No</span><span class="sxs-lookup"><span data-stu-id="008f1-149">No</span></span><br/></td>
<td><span data-ttu-id="008f1-150">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="008f1-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="008f1-151">
<dt><span></span><span></span><strong></strong> (Inferiore)</span><span class="sxs-lookup"><span data-stu-id="008f1-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="008f1-152"><dt><span></span><span></span><strong></strong> (Nascondi)</span><span class="sxs-lookup"><span data-stu-id="008f1-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="008f1-153"><dt><span></span><span></span><strong></strong> (A sinistra)</span><span class="sxs-lookup"><span data-stu-id="008f1-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="008f1-154"><dt><span></span><span></span><strong></strong> (Sovrapposizione)</span><span class="sxs-lookup"><span data-stu-id="008f1-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="008f1-155"><dt><span></span><span></span><strong></strong> (A destra)</span><span class="sxs-lookup"><span data-stu-id="008f1-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="008f1-156"><dt><span></span><span></span><strong></strong> (In alto)</span><span class="sxs-lookup"><span data-stu-id="008f1-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="008f1-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="008f1-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="008f1-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="008f1-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="008f1-159">No</span><span class="sxs-lookup"><span data-stu-id="008f1-159">No</span></span><br/></td>
<td><span data-ttu-id="008f1-160">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="008f1-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="008f1-161">
<dt><span></span><span></span><strong></strong> (Elementi)</span><span class="sxs-lookup"><span data-stu-id="008f1-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="008f1-162"><dt><span></span><span></span><strong></strong> (Comandi)</span><span class="sxs-lookup"><span data-stu-id="008f1-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="008f1-163">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="008f1-163">Child elements</span></span>



| <span data-ttu-id="008f1-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="008f1-164">Element</span></span>                                                                                           | <span data-ttu-id="008f1-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="008f1-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="008f1-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="008f1-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="008f1-167">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="008f1-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="008f1-168">**Casella**</span><span class="sxs-lookup"><span data-stu-id="008f1-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="008f1-169">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="008f1-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="008f1-170">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="008f1-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="008f1-171">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="008f1-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="008f1-172">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="008f1-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="008f1-173">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="008f1-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="008f1-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="008f1-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="008f1-175">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="008f1-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="008f1-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="008f1-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="008f1-177">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="008f1-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="008f1-178">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="008f1-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="008f1-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="008f1-179">Element</span></span></th>
<th><span data-ttu-id="008f1-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="008f1-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="008f1-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="008f1-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="008f1-182"><a href="windowsribbon-element-group.md"><strong>Gruppo</strong></a></span><span class="sxs-lookup"><span data-stu-id="008f1-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="008f1-183"><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="008f1-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="008f1-184">Se contenuto in un <a href="windowsribbon-element-applicationmenu.md"><strong>oggetto ApplicationMenu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="008f1-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="008f1-185">Questo elemento è supportato solo nel primo livello e non deve avere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="008f1-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008f1-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="008f1-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="008f1-187">Windows 8 e più recente.</span><span class="sxs-lookup"><span data-stu-id="008f1-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="008f1-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="008f1-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="008f1-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="008f1-189">Remarks</span></span>

<span data-ttu-id="008f1-190">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="008f1-190">Optional.</span></span>

<span data-ttu-id="008f1-191">Può verificarsi una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButton.**](windowsribbon-element-splitbutton.md)</span><span class="sxs-lookup"><span data-stu-id="008f1-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="008f1-192">**DropDownGallery supporta** le [modalità applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="008f1-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="008f1-193">Lo screenshot seguente illustra il controllo [Raccolta a discesa della](windowsribbon-controls-dropdowngallery.md) barra multifunzione in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="008f1-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot di un controllo raccolta a discesa in Microsoft Paint per Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="008f1-195">Esempio</span><span class="sxs-lookup"><span data-stu-id="008f1-195">Examples</span></span>

<span data-ttu-id="008f1-196">Nell'esempio seguente viene illustrato il markup di base per **l'oggetto DropDownGallery.**</span><span class="sxs-lookup"><span data-stu-id="008f1-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="008f1-197">Questa sezione di codice illustra le **dichiarazioni di Comando DropDownGallery,** con un oggetto [**Group**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **DropDownGallery.**</span><span class="sxs-lookup"><span data-stu-id="008f1-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


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



<span data-ttu-id="008f1-198">Questa sezione di codice illustra le dichiarazioni del controllo **DropDownGallery.**</span><span class="sxs-lookup"><span data-stu-id="008f1-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="008f1-199">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="008f1-199">Element information</span></span>

* <span data-ttu-id="008f1-200">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="008f1-200">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="008f1-201">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="008f1-201">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="008f1-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="008f1-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="008f1-203">**Controllo Raccolta a discesa**</span><span class="sxs-lookup"><span data-stu-id="008f1-203">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="008f1-204">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="008f1-204">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="008f1-205">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="008f1-205">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="008f1-206">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="008f1-206">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

