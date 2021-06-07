---
title: Elemento InRibbonGallery
description: Rappresenta la In-Ribbon, un controllo basato su raccolta che espone un subset predefinito di elementi direttamente nella barra multifunzione. Tutti gli elementi rimanenti vengono visualizzati quando si fa clic su un pulsante di menu a discesa.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Elemento InRibbonGallery Barra multifunzione di Windows
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443372"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="3e04b-105">Elemento InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="3e04b-105">InRibbonGallery element</span></span>

<span data-ttu-id="3e04b-106">Rappresenta la [raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md), un controllo basato su raccolta che espone un subset predefinito di elementi direttamente nella barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="3e04b-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="3e04b-107">Tutti gli elementi rimanenti vengono visualizzati quando si fa clic su un pulsante di menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="3e04b-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="3e04b-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3e04b-108">Usage</span></span>

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
```

## <a name="attributes"></a><span data-ttu-id="3e04b-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="3e04b-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e04b-110">Attributo</span><span class="sxs-lookup"><span data-stu-id="3e04b-110">Attribute</span></span></th>
<th><span data-ttu-id="3e04b-111">Type</span><span class="sxs-lookup"><span data-stu-id="3e04b-111">Type</span></span></th>
<th><span data-ttu-id="3e04b-112">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="3e04b-112">Required</span></span></th>
<th><span data-ttu-id="3e04b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e04b-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e04b-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-115">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="3e04b-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3e04b-116">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-116">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-117">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e04b-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="3e04b-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="3e04b-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3e04b-119">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="3e04b-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="3e04b-120">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="3e04b-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="3e04b-121">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="3e04b-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e04b-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="3e04b-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="3e04b-124">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-124">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-125">Determina se la risorsa immagine grande o piccola del comando viene visualizzata nel controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e04b-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3e04b-126">Si applica solo alle raccolte in cui il valore <em>dell'attributo Type</em> è uguale a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="3e04b-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="3e04b-127">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="3e04b-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="3e04b-128">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="3e04b-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="3e04b-129">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3e04b-129">Default.</span></span> <br/> </dd> <span data-ttu-id="3e04b-130"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="3e04b-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e04b-131"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3e04b-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3e04b-133">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-133">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-134">Insieme a <em>ItemWidth,</em>determina le dimensioni dell'immagine dell'elemento visualizzata nel controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e04b-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3e04b-135">Si applica solo alle raccolte in cui il valore <em>dell'attributo Type</em> è uguale a</span><span class="sxs-lookup"><span data-stu-id="3e04b-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="3e04b-136">.</span><span class="sxs-lookup"><span data-stu-id="3e04b-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="3e04b-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3e04b-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3e04b-138">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="3e04b-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e04b-139"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3e04b-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3e04b-141">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-141">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-142">Insieme a <em>ItemHeight,</em>determina le dimensioni dell'immagine dell'elemento visualizzata nel controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e04b-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3e04b-143">Si applica solo alle raccolte in cui il valore <em>dell'attributo Type</em> è uguale a</span><span class="sxs-lookup"><span data-stu-id="3e04b-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="3e04b-144">.</span><span class="sxs-lookup"><span data-stu-id="3e04b-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="3e04b-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3e04b-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3e04b-146">Il valore predefinito è -1.</span><span class="sxs-lookup"><span data-stu-id="3e04b-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e04b-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3e04b-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3e04b-149">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-149">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-150">Specifica il numero massimo di colonne visualizzate da <strong>InRibbonGallery,</strong> ad esempio nell'elenco a discesa Layout gruppo di grandi dimensioni. <em></em></span><span class="sxs-lookup"><span data-stu-id="3e04b-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="3e04b-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3e04b-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e04b-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3e04b-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3e04b-154">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-154">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-155">Specifica il numero massimo di colonne visualizzate da <strong>InRibbonGallery</strong> nel layout gruppo Medio, prima di passare al layout <em>Large.</em> <em></em></span><span class="sxs-lookup"><span data-stu-id="3e04b-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="3e04b-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3e04b-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e04b-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3e04b-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3e04b-159">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-159">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-160">Specifica il numero massimo di righe per il layout degli <strong>elementi InRibbonGallery.</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="3e04b-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3e04b-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3e04b-162">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="3e04b-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e04b-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3e04b-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3e04b-165">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-165">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-166">Specifica il numero minimo di colonne visualizzate da <strong>InRibbonGallery</strong> nel layout Gruppo di grandi dimensioni, prima di passare a <em>Medio.</em> <em></em></span><span class="sxs-lookup"><span data-stu-id="3e04b-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="3e04b-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3e04b-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e04b-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3e04b-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3e04b-170">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-170">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-171">Specifica il numero minimo di colonne visualizzate da <strong>InRibbonGallery</strong> nel layout del gruppo <em>Medium,</em> prima di passare a <em>Small.</em></span><span class="sxs-lookup"><span data-stu-id="3e04b-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="3e04b-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3e04b-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e04b-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-174">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="3e04b-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="3e04b-175">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-175">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-176">Specifica dove viene visualizzata l'etichetta dell'elemento, rispetto all'immagine.</span><span class="sxs-lookup"><span data-stu-id="3e04b-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="3e04b-177">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e04b-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3e04b-178">
<dt><span></span><span></span><strong></strong> (Inferiore)</span><span class="sxs-lookup"><span data-stu-id="3e04b-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3e04b-179"><dt><span></span><span></span><strong></strong> (Nascondi)</span><span class="sxs-lookup"><span data-stu-id="3e04b-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3e04b-180"><dt><span></span><span></span><strong></strong> (A sinistra)</span><span class="sxs-lookup"><span data-stu-id="3e04b-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3e04b-181"><dt><span></span><span></span><strong></strong> (Sovrapposizione)</span><span class="sxs-lookup"><span data-stu-id="3e04b-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3e04b-182"><dt><span></span><span></span><strong></strong> (A destra)</span><span class="sxs-lookup"><span data-stu-id="3e04b-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3e04b-183"><dt><span></span><span></span><strong></strong> (In alto)</span><span class="sxs-lookup"><span data-stu-id="3e04b-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e04b-184"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="3e04b-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="3e04b-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="3e04b-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="3e04b-186">No</span><span class="sxs-lookup"><span data-stu-id="3e04b-186">No</span></span><br/></td>
<td><span data-ttu-id="3e04b-187">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e04b-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3e04b-188">
<dt><span></span><span></span><strong></strong> (Elementi)</span><span class="sxs-lookup"><span data-stu-id="3e04b-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3e04b-189"><dt><span></span><span></span><strong></strong> (Comandi)</span><span class="sxs-lookup"><span data-stu-id="3e04b-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3e04b-190">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3e04b-190">Child elements</span></span>



| <span data-ttu-id="3e04b-191">Elemento</span><span class="sxs-lookup"><span data-stu-id="3e04b-191">Element</span></span>                                                                                           | <span data-ttu-id="3e04b-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e04b-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="3e04b-193">**Casella**</span><span class="sxs-lookup"><span data-stu-id="3e04b-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="3e04b-194">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="3e04b-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3e04b-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="3e04b-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="3e04b-196">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="3e04b-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="3e04b-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="3e04b-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="3e04b-198">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="3e04b-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="3e04b-199">**Pulsante**</span><span class="sxs-lookup"><span data-stu-id="3e04b-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="3e04b-200">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="3e04b-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3e04b-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3e04b-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="3e04b-202">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="3e04b-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3e04b-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="3e04b-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="3e04b-204">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="3e04b-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3e04b-205">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3e04b-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e04b-206">Elemento</span><span class="sxs-lookup"><span data-stu-id="3e04b-206">Element</span></span></th>
<th><span data-ttu-id="3e04b-207">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e04b-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e04b-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e04b-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3e04b-209"><a href="windowsribbon-element-group.md"><strong>Gruppo</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e04b-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3e04b-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e04b-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="3e04b-211">Windows 8 e più recente.</span><span class="sxs-lookup"><span data-stu-id="3e04b-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="3e04b-212">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e04b-212">Remarks</span></span>

<span data-ttu-id="3e04b-213">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3e04b-213">Optional.</span></span>

<span data-ttu-id="3e04b-214">Può verificarsi al massimo una volta per [**ogni elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**o Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="3e04b-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="3e04b-215">La schermata seguente illustra il controllo [Raccolta barra](windowsribbon-controls-inribbongallery.md) multifunzione in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3e04b-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot di un controllo della raccolta nella barra multifunzione di Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="3e04b-217">Esempio</span><span class="sxs-lookup"><span data-stu-id="3e04b-217">Examples</span></span>

<span data-ttu-id="3e04b-218">Nell'esempio seguente viene illustrato il markup di base per [una raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="3e04b-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="3e04b-219">Questa sezione di codice illustra le dichiarazioni del comando **InRibbonGallery,** con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **InRibbonGallery.**</span><span class="sxs-lookup"><span data-stu-id="3e04b-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



<span data-ttu-id="3e04b-220">Questa sezione di codice illustra le **dichiarazioni di controllo InRibbonGallery.**</span><span class="sxs-lookup"><span data-stu-id="3e04b-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="3e04b-221">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3e04b-221">Element information</span></span>


* <span data-ttu-id="3e04b-222">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e04b-222">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="3e04b-223">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="3e04b-223">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="3e04b-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e04b-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e04b-225">Controllo Raccolta barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="3e04b-225">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="3e04b-226">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="3e04b-226">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="3e04b-227">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="3e04b-227">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





