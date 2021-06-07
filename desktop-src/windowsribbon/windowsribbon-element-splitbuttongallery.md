---
title: Elemento SplitButtonGallery
description: Rappresenta un controllo Split Button Gallery con un menu a discesa basato su raccolta.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Elemento SplitButtonGallery nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5f8767135b9472acba333b1cdfa6ab102e9b7f4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444832"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="eeebe-104">Elemento SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="eeebe-104">SplitButtonGallery element</span></span>

<span data-ttu-id="eeebe-105">Rappresenta un [controllo Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) con un menu a discesa basato su raccolta.</span><span class="sxs-lookup"><span data-stu-id="eeebe-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="eeebe-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="eeebe-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="eeebe-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="eeebe-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eeebe-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="eeebe-108">Attribute</span></span></th>
<th><span data-ttu-id="eeebe-109">Type</span><span class="sxs-lookup"><span data-stu-id="eeebe-109">Type</span></span></th>
<th><span data-ttu-id="eeebe-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="eeebe-110">Required</span></span></th>
<th><span data-ttu-id="eeebe-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeebe-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eeebe-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="eeebe-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="eeebe-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="eeebe-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="eeebe-114">No</span><span class="sxs-lookup"><span data-stu-id="eeebe-114">No</span></span><br/></td>
<td><span data-ttu-id="eeebe-115">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="eeebe-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="eeebe-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="eeebe-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eeebe-117">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="eeebe-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="eeebe-118">Gli spazi vuoti sono validi e ignorati.</span><span class="sxs-lookup"><span data-stu-id="eeebe-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="eeebe-119">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="eeebe-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeebe-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="eeebe-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="eeebe-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="eeebe-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="eeebe-122">No</span><span class="sxs-lookup"><span data-stu-id="eeebe-122">No</span></span><br/></td>
<td><span data-ttu-id="eeebe-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeebe-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="eeebe-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="eeebe-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eeebe-125">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="eeebe-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="eeebe-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="eeebe-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="eeebe-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="eeebe-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeebe-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="eeebe-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="eeebe-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="eeebe-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="eeebe-130">No</span><span class="sxs-lookup"><span data-stu-id="eeebe-130">No</span></span><br/></td>
<td><span data-ttu-id="eeebe-131">Determina se la risorsa immagine grande o piccola del comando viene visualizzata nel controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="eeebe-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eeebe-132">Si applica solo alle raccolte in cui il valore <em>dell'attributo Type</em> è uguale a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="eeebe-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="eeebe-133">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="eeebe-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="eeebe-134">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="eeebe-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="eeebe-135">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="eeebe-135">Default.</span></span> <br/> </dd> <span data-ttu-id="eeebe-136"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="eeebe-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeebe-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="eeebe-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="eeebe-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="eeebe-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="eeebe-139">No</span><span class="sxs-lookup"><span data-stu-id="eeebe-139">No</span></span><br/></td>
<td><span data-ttu-id="eeebe-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="eeebe-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="eeebe-141">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="eeebe-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeebe-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="eeebe-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="eeebe-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="eeebe-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="eeebe-144">No</span><span class="sxs-lookup"><span data-stu-id="eeebe-144">No</span></span><br/></td>
<td><span data-ttu-id="eeebe-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="eeebe-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="eeebe-146">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="eeebe-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeebe-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="eeebe-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="eeebe-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="eeebe-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="eeebe-149">No</span><span class="sxs-lookup"><span data-stu-id="eeebe-149">No</span></span><br/></td>
<td><span data-ttu-id="eeebe-150">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="eeebe-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="eeebe-151">
<dt><span></span><span></span><strong></strong> (Inferiore)</span><span class="sxs-lookup"><span data-stu-id="eeebe-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="eeebe-152"><dt><span></span><span></span><strong></strong> (Nascondi)</span><span class="sxs-lookup"><span data-stu-id="eeebe-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="eeebe-153"><dt><span></span><span></span><strong></strong> (A sinistra)</span><span class="sxs-lookup"><span data-stu-id="eeebe-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="eeebe-154"><dt><span></span><span></span><strong></strong> (Sovrapposizione)</span><span class="sxs-lookup"><span data-stu-id="eeebe-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="eeebe-155"><dt><span></span><span></span><strong></strong> (A destra)</span><span class="sxs-lookup"><span data-stu-id="eeebe-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="eeebe-156"><dt><span></span><span></span><strong></strong> (In alto)</span><span class="sxs-lookup"><span data-stu-id="eeebe-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeebe-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="eeebe-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="eeebe-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="eeebe-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="eeebe-159">No</span><span class="sxs-lookup"><span data-stu-id="eeebe-159">No</span></span><br/></td>
<td><span data-ttu-id="eeebe-160">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="eeebe-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="eeebe-161">
<dt><span></span><span></span><strong></strong> (Elementi)</span><span class="sxs-lookup"><span data-stu-id="eeebe-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="eeebe-162"><dt><span></span><span></span><strong></strong> (Comandi)</span><span class="sxs-lookup"><span data-stu-id="eeebe-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="eeebe-163">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="eeebe-163">Child elements</span></span>



| <span data-ttu-id="eeebe-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="eeebe-164">Element</span></span>                                                                                                 | <span data-ttu-id="eeebe-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeebe-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="eeebe-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="eeebe-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="eeebe-167">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="eeebe-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eeebe-168">**Casella**</span><span class="sxs-lookup"><span data-stu-id="eeebe-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="eeebe-169">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="eeebe-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eeebe-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="eeebe-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="eeebe-171">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="eeebe-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eeebe-172">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="eeebe-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="eeebe-173">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="eeebe-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="eeebe-174">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="eeebe-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="eeebe-175">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="eeebe-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="eeebe-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="eeebe-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="eeebe-177">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="eeebe-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="eeebe-178">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="eeebe-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eeebe-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="eeebe-179">Element</span></span></th>
<th><span data-ttu-id="eeebe-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeebe-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eeebe-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeebe-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="eeebe-182"><a href="windowsribbon-element-group.md"><strong>Gruppo</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeebe-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="eeebe-183"><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeebe-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="eeebe-184">Se contenuto in un <a href="windowsribbon-element-applicationmenu.md"><strong>oggetto ApplicationMenu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeebe-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="eeebe-185">Questo elemento è supportato solo nel primo livello e non deve avere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="eeebe-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeebe-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeebe-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="eeebe-187">Windows 8 e più recente.</span><span class="sxs-lookup"><span data-stu-id="eeebe-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeebe-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeebe-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="eeebe-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="eeebe-189">Remarks</span></span>

<span data-ttu-id="eeebe-190">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eeebe-190">Optional.</span></span>

<span data-ttu-id="eeebe-191">Può verificarsi una o più volte per [**ogni elemento ControlGroup,**](windowsribbon-element-controlgroup.md) [**Group,**](windowsribbon-element-group.md) [**MenuGroup**](windowsribbon-element-menugroup.md) [**o SplitButton.**](windowsribbon-element-splitbutton.md)</span><span class="sxs-lookup"><span data-stu-id="eeebe-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="eeebe-192">**SplitButtonGallery supporta** le [modalità applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="eeebe-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="eeebe-193">[Interfaccia utente \_ PKEY \_ BooleanValue viene](windowsribbon-reference-properties-uipkey-booleanvalue.md) usato da un'applicazione per eseguire una query sullo stato di attivazione/disattivazione per il controllo pulsante di un controllo **SplitButtonGallery.**</span><span class="sxs-lookup"><span data-stu-id="eeebe-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="eeebe-194">Lo screenshot seguente illustra il controllo Raccolta pulsanti di menu [suddivisi](windowsribbon-controls-splitbuttongallery.md) della barra multifunzione in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eeebe-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot di un controllo della raccolta di pulsanti divisi in Microsoft Paint per Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="eeebe-196">Esempio</span><span class="sxs-lookup"><span data-stu-id="eeebe-196">Examples</span></span>

<span data-ttu-id="eeebe-197">Nell'esempio seguente viene illustrato il markup di base per [la raccolta di pulsanti di menu suddivisi.](windowsribbon-controls-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="eeebe-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="eeebe-198">Questa sezione di codice illustra le dichiarazioni del comando **SplitButtonGallery,** con un oggetto [**Group**](windowsribbon-element-group.md) associato che funziona come contenitore padre per **l'elemento SplitButtonGallery.**</span><span class="sxs-lookup"><span data-stu-id="eeebe-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


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



<span data-ttu-id="eeebe-199">Questa sezione di codice mostra le **dichiarazioni del controllo SplitButtonGallery.**</span><span class="sxs-lookup"><span data-stu-id="eeebe-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="eeebe-200">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eeebe-200">Element information</span></span>


- <span data-ttu-id="eeebe-201">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="eeebe-201">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="eeebe-202">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="eeebe-202">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="eeebe-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eeebe-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeebe-204">Controllo Raccolta pulsanti di divisione</span><span class="sxs-lookup"><span data-stu-id="eeebe-204">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="eeebe-205">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="eeebe-205">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="eeebe-206">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="eeebe-206">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="eeebe-207">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="eeebe-207">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

