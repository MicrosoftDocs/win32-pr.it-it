---
title: Elemento DropDownColorPicker
description: Rappresenta un Pickercontrol colore Drop-Down che, quando selezionato, Visualizza una tavolozza dei campioni di colore.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Barra multifunzione Windows elemento DropDownColorPicker
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00185d14d9066b2cb85da4b23959e84df1827007
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "103720490"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="33936-104">Elemento DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="33936-104">DropDownColorPicker element</span></span>

<span data-ttu-id="33936-105">Rappresenta un controllo [selezione colori a discesa](windowsribbon-controls-dropdowncolorpicker.md)che, quando selezionato, Visualizza una tavolozza di campioni colore.</span><span class="sxs-lookup"><span data-stu-id="33936-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="33936-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="33936-106">Usage</span></span>

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="33936-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="33936-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33936-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="33936-108">Attribute</span></span></th>
<th><span data-ttu-id="33936-109">Type</span><span class="sxs-lookup"><span data-stu-id="33936-109">Type</span></span></th>
<th><span data-ttu-id="33936-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="33936-110">Required</span></span></th>
<th><span data-ttu-id="33936-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33936-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33936-112"><strong>ChipSize</strong></span><span class="sxs-lookup"><span data-stu-id="33936-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="33936-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="33936-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="33936-114">No</span><span class="sxs-lookup"><span data-stu-id="33936-114">No</span></span><br/></td>
<td><span data-ttu-id="33936-115">Dimensioni di ogni chip di colore o campione.</span><span class="sxs-lookup"><span data-stu-id="33936-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="33936-116">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="33936-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="33936-117">
<dt><span></span><span></span><strong></strong> Piccolo</span><span class="sxs-lookup"><span data-stu-id="33936-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-118">Ogni chip di colore è un quadrato di pixel 11x11.</span><span class="sxs-lookup"><span data-stu-id="33936-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="33936-119"><dt><span></span><span></span><strong></strong> Media</span><span class="sxs-lookup"><span data-stu-id="33936-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-120">Ogni chip di colore è un quadrato di pixel 16x16.</span><span class="sxs-lookup"><span data-stu-id="33936-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="33936-121"><dt><span></span><span></span><strong></strong> Grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="33936-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-122">Ogni chip di colore è un quadrato di pixel 24x24.</span><span class="sxs-lookup"><span data-stu-id="33936-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33936-123"><strong>ColorTemplate</strong></span><span class="sxs-lookup"><span data-stu-id="33936-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="33936-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="33936-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="33936-125">No</span><span class="sxs-lookup"><span data-stu-id="33936-125">No</span></span><br/></td>
<td><span data-ttu-id="33936-126">Modelli di layout che specificano il tipo di <a href="windowsribbon-controls-dropdowncolorpicker.md">selezione colori a discesa</a>.</span><span class="sxs-lookup"><span data-stu-id="33936-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="33936-127">Limitato a uno dei valori seguenti (se non sono dichiarati attributi facoltativi relativi a un <em>ColorTemplate</em> , viene visualizzata la visualizzazione predefinita):</span><span class="sxs-lookup"><span data-stu-id="33936-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="33936-128">
<dt><span></span><span></span><strong></strong> ThemeColors</span><span class="sxs-lookup"><span data-stu-id="33936-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-129">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="33936-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="33936-130">Impostando l'attributo <em>ColorTemplate</em> su <code>ThemeColors</code> sono abilitate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="33936-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="33936-131">Ancoraggio SplitButton.</span><span class="sxs-lookup"><span data-stu-id="33936-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="33936-132">Il pulsante colore <strong>automatico</strong> viene visualizzato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="33936-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="33936-133">Griglia campione <strong>colori del tema</strong> di Windows.</span><span class="sxs-lookup"><span data-stu-id="33936-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="33936-134">Griglia campioni <strong>colori standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="33936-135">La griglia di campioni <strong>colori recenti</strong> è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="33936-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="33936-136">Pulsante di avvio finestra di dialogo <strong>altri colori</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="33936-137">Per impostazione predefinita, non viene visualizzato alcun pulsante colore <strong>colore</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="33936-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span><span class="sxs-lookup"><span data-stu-id="33936-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="33936-139">Impostando l'attributo <em>ColorTemplate</em> su <code>StandardColors</code> sono abilitate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="33936-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="33936-140">Ancoraggio SplitButton.</span><span class="sxs-lookup"><span data-stu-id="33936-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="33936-141">Il pulsante colore <strong>automatico</strong> viene visualizzato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="33936-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="33936-142">Griglia campioni <strong>colori standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="33936-143">Pulsante di avvio finestra di dialogo <strong>altri colori</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="33936-144">Per impostazione predefinita, non viene visualizzato alcun pulsante colore <strong>colore</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="33936-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span><span class="sxs-lookup"><span data-stu-id="33936-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="33936-146">Impostando l'attributo <em>ColorTemplate</em> su <code>HighlightColors</code> sono abilitate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="33936-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="33936-147">Ancoraggio SplitButton.</span><span class="sxs-lookup"><span data-stu-id="33936-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="33936-148">Griglia campioni <strong>colori standard</strong> senza intestazione.</span><span class="sxs-lookup"><span data-stu-id="33936-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="33936-149">Per impostazione predefinita, non viene visualizzato alcun pulsante colore <strong>colore</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33936-150"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="33936-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="33936-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="33936-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="33936-152">No</span><span class="sxs-lookup"><span data-stu-id="33936-152">No</span></span><br/></td>
<td><span data-ttu-id="33936-153">Numero di colonne del chip di colore (o campione).</span><span class="sxs-lookup"><span data-stu-id="33936-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="33936-154">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="33936-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-155">Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.</span><span class="sxs-lookup"><span data-stu-id="33936-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33936-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="33936-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="33936-157">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="33936-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="33936-158">No</span><span class="sxs-lookup"><span data-stu-id="33936-158">No</span></span><br/></td>
<td><span data-ttu-id="33936-159">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="33936-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="33936-160">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="33936-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-161">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="33936-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="33936-162">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="33936-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="33936-163">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="33936-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33936-164"><strong>IsAutomaticColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="33936-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="33936-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="33936-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="33936-166">No</span><span class="sxs-lookup"><span data-stu-id="33936-166">No</span></span><br/></td>
<td><span data-ttu-id="33936-167">Consente di visualizzare o nascondere il pulsante colore <strong>automatico</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="33936-168">Valido solo quando <code>StandardColors</code> <code>ThemeColors</code> viene specificato o per l'attributo <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="33936-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="33936-169">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="33936-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="33936-170">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="33936-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="33936-171"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="33936-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33936-172"><strong>IsNoColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="33936-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="33936-173">Boolean</span><span class="sxs-lookup"><span data-stu-id="33936-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="33936-174">No</span><span class="sxs-lookup"><span data-stu-id="33936-174">No</span></span><br/></td>
<td><span data-ttu-id="33936-175">Consente di visualizzare o nascondere il pulsante <strong>nessun colore</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="33936-176">Valido per tutti i valori <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="33936-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="33936-177">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="33936-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="33936-178">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="33936-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="33936-179"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="33936-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33936-180"><strong>RecentColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="33936-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="33936-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="33936-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="33936-182">No</span><span class="sxs-lookup"><span data-stu-id="33936-182">No</span></span><br/></td>
<td><span data-ttu-id="33936-183">Numero di righe del chip di colore (o campione) nell'area dei <strong>colori recenti</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="33936-184">Valido solo quando <code>ThemeColors</code> viene specificato per l'attributo <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="33936-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="33936-185">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="33936-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-186">Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.</span><span class="sxs-lookup"><span data-stu-id="33936-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33936-187"><strong>StandardColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="33936-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="33936-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="33936-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="33936-189">No</span><span class="sxs-lookup"><span data-stu-id="33936-189">No</span></span><br/></td>
<td><span data-ttu-id="33936-190">Numero di righe del chip di colore (o campione) nell'area dei <strong>colori standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="33936-191">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="33936-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-192">Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.</span><span class="sxs-lookup"><span data-stu-id="33936-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33936-193"><strong>ThemeColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="33936-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="33936-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="33936-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="33936-195">No</span><span class="sxs-lookup"><span data-stu-id="33936-195">No</span></span><br/></td>
<td><span data-ttu-id="33936-196">Numero di righe del chip di colore (o campione) nell'area dei <strong>colori del tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="33936-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="33936-197">Valido solo quando <code>ThemeColors</code> viene specificato per l'attributo <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="33936-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="33936-198">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="33936-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="33936-199">Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.</span><span class="sxs-lookup"><span data-stu-id="33936-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="33936-200">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="33936-200">Child elements</span></span>

<span data-ttu-id="33936-201">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="33936-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="33936-202">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="33936-202">Parent elements</span></span>



| <span data-ttu-id="33936-203">Elemento</span><span class="sxs-lookup"><span data-stu-id="33936-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="33936-204">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="33936-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="33936-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="33936-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="33936-206">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="33936-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="33936-207">**Group**</span><span class="sxs-lookup"><span data-stu-id="33936-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="33936-208">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="33936-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="33936-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="33936-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="33936-210">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="33936-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="33936-211">Commenti</span><span class="sxs-lookup"><span data-stu-id="33936-211">Remarks</span></span>

<span data-ttu-id="33936-212">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="33936-212">Optional.</span></span>

<span data-ttu-id="33936-213">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="33936-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="33936-214">Esempio</span><span class="sxs-lookup"><span data-stu-id="33936-214">Examples</span></span>

<span data-ttu-id="33936-215">Nell'esempio seguente viene illustrato il markup di base per tutti e tre i tipi di [selezione colori a discesa](windowsribbon-controls-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="33936-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="33936-216">In questa sezione del codice vengono illustrate le dichiarazioni di comando per tre elementi **DropDownColorPicker** .</span><span class="sxs-lookup"><span data-stu-id="33936-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



<span data-ttu-id="33936-217">Questa sezione di codice mostra i tre tipi di dichiarazioni di controllo **DropDownColorPicker** .</span><span class="sxs-lookup"><span data-stu-id="33936-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="33936-218">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="33936-218">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="33936-219">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33936-219">Minimum supported system</span></span><br/> | <span data-ttu-id="33936-220">Windows 7</span><span class="sxs-lookup"><span data-stu-id="33936-220">Windows 7</span></span> |
| <span data-ttu-id="33936-221">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="33936-221">Can be empty</span></span>                        | <span data-ttu-id="33936-222">Sì</span><span class="sxs-lookup"><span data-stu-id="33936-222">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="33936-223">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33936-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33936-224">Controllo selezione colori a discesa</span><span class="sxs-lookup"><span data-stu-id="33936-224">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="33936-225">Esempio DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="33936-225">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





