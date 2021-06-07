---
title: Elemento DropDownColorPicker
description: Rappresenta un Drop-Down controllo Selezione colori che quando si fa clic visualizza una tavolozza di campioni di colore.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Barra multifunzione di Windows per l'elemento DropDownColorPicker
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442902"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="0d0af-104">Elemento DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="0d0af-104">DropDownColorPicker element</span></span>

<span data-ttu-id="0d0af-105">Rappresenta un [controllo elenco a Selezione colori](windowsribbon-controls-dropdowncolorpicker.md)che quando si fa clic visualizza una tavolozza di campioni di colore.</span><span class="sxs-lookup"><span data-stu-id="0d0af-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="0d0af-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0d0af-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="0d0af-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="0d0af-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0d0af-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="0d0af-108">Attribute</span></span></th>
<th><span data-ttu-id="0d0af-109">Type</span><span class="sxs-lookup"><span data-stu-id="0d0af-109">Type</span></span></th>
<th><span data-ttu-id="0d0af-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="0d0af-110">Required</span></span></th>
<th><span data-ttu-id="0d0af-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d0af-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d0af-112"><strong>ChipSize</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="0d0af-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="0d0af-114">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-114">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-115">Dimensioni di ogni chip o campione di colore.</span><span class="sxs-lookup"><span data-stu-id="0d0af-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="0d0af-116">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d0af-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="0d0af-117">
<dt><span></span><span></span><strong></strong> (Piccola)</span><span class="sxs-lookup"><span data-stu-id="0d0af-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-118">Ogni chip di colore è un quadrato di 11 x 11 pixel.</span><span class="sxs-lookup"><span data-stu-id="0d0af-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="0d0af-119"><dt><span></span><span></span><strong></strong> (Media)</span><span class="sxs-lookup"><span data-stu-id="0d0af-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-120">Ogni chip di colore è un quadrato di 16 x 16 pixel.</span><span class="sxs-lookup"><span data-stu-id="0d0af-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="0d0af-121"><dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="0d0af-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-122">Ogni chip di colore è un quadrato di 24 x 24 pixel.</span><span class="sxs-lookup"><span data-stu-id="0d0af-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d0af-123"><strong>ColorTemplate</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="0d0af-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="0d0af-125">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-125">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-126">Modelli di layout che specificano il tipo <a href="windowsribbon-controls-dropdowncolorpicker.md">di elenco a discesa Selezione colori</a>.</span><span class="sxs-lookup"><span data-stu-id="0d0af-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="0d0af-127">Limitato a uno dei valori seguenti (se non viene dichiarato alcun attributo facoltativo correlato a <em>un oggetto ColorTemplate,</em> viene visualizzata la visualizzazione predefinita):</span><span class="sxs-lookup"><span data-stu-id="0d0af-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="0d0af-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span><span class="sxs-lookup"><span data-stu-id="0d0af-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-129">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0d0af-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="0d0af-130">L'impostazione <em>dell'attributo ColorTemplate</em> <code>ThemeColors</code> su abilita le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d0af-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="0d0af-131">Ancoraggio SplitButton.</span><span class="sxs-lookup"><span data-stu-id="0d0af-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="0d0af-132"><strong>Il pulsante</strong> a colori automatico viene visualizzato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0d0af-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="0d0af-133">Griglia <strong>dei campioni dei colori</strong> del tema di Windows.</span><span class="sxs-lookup"><span data-stu-id="0d0af-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="0d0af-134"><strong>Griglia dei campioni</strong> di colori standard.</span><span class="sxs-lookup"><span data-stu-id="0d0af-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="0d0af-135"><strong>La griglia dei</strong> campioni colori recenti è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="0d0af-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="0d0af-136"><strong>Icona di avvio della finestra</strong> di dialogo Altri colori.</span><span class="sxs-lookup"><span data-stu-id="0d0af-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="0d0af-137"><strong>Per impostazione predefinita,</strong> non viene visualizzato alcun pulsante colore.</span><span class="sxs-lookup"><span data-stu-id="0d0af-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="0d0af-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span><span class="sxs-lookup"><span data-stu-id="0d0af-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="0d0af-139">L'impostazione <em>dell'attributo ColorTemplate</em> <code>StandardColors</code> su abilita le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d0af-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="0d0af-140">Ancoraggio SplitButton.</span><span class="sxs-lookup"><span data-stu-id="0d0af-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="0d0af-141"><strong>Il pulsante</strong> a colori automatico viene visualizzato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0d0af-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="0d0af-142"><strong>Griglia dei campioni</strong> di colori standard.</span><span class="sxs-lookup"><span data-stu-id="0d0af-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="0d0af-143"><strong>Icona di avvio della finestra</strong> di dialogo Altri colori.</span><span class="sxs-lookup"><span data-stu-id="0d0af-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="0d0af-144"><strong>Per impostazione predefinita,</strong> non viene visualizzato alcun pulsante colore.</span><span class="sxs-lookup"><span data-stu-id="0d0af-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="0d0af-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span><span class="sxs-lookup"><span data-stu-id="0d0af-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="0d0af-146">L'impostazione <em>dell'attributo ColorTemplate</em> <code>HighlightColors</code> su abilita le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d0af-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="0d0af-147">Ancoraggio SplitButton.</span><span class="sxs-lookup"><span data-stu-id="0d0af-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="0d0af-148"><strong>Griglia di campioni</strong> di colori standard senza intestazione.</span><span class="sxs-lookup"><span data-stu-id="0d0af-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="0d0af-149"><strong>Per impostazione predefinita,</strong> non viene visualizzato alcun pulsante colore.</span><span class="sxs-lookup"><span data-stu-id="0d0af-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d0af-150"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0d0af-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0d0af-152">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-152">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-153">Numero di colonne di chip di colore (o campione).</span><span class="sxs-lookup"><span data-stu-id="0d0af-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="0d0af-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0d0af-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-155">Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0d0af-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d0af-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-157">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="0d0af-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0d0af-158">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-158">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-159">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d0af-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="0d0af-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="0d0af-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-161">Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="0d0af-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="0d0af-162">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0d0af-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="0d0af-163">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0d0af-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d0af-164"><strong>IsAutomaticColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="0d0af-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="0d0af-166">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-166">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-167">Visualizza (o nasconde) il <strong>pulsante Colore</strong> automatico.</span><span class="sxs-lookup"><span data-stu-id="0d0af-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="0d0af-168">Valido solo quando <code>StandardColors</code> o viene specificato per <code>ThemeColors</code> <em>l'attributo ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="0d0af-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="0d0af-169">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="0d0af-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="0d0af-170">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="0d0af-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="0d0af-171"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="0d0af-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d0af-172"><strong>IsNoColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-173">Boolean</span><span class="sxs-lookup"><span data-stu-id="0d0af-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="0d0af-174">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-174">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-175">Visualizza (o nasconde) il <strong>pulsante Nessun</strong> colore.</span><span class="sxs-lookup"><span data-stu-id="0d0af-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="0d0af-176">Valido per tutti <em>i valori ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="0d0af-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="0d0af-177">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="0d0af-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="0d0af-178">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="0d0af-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="0d0af-179"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="0d0af-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d0af-180"><strong>RecentColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0d0af-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0d0af-182">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-182">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-183">Numero di righe di chip di colore (o campione) nell'area <strong>Colori</strong> recenti.</span><span class="sxs-lookup"><span data-stu-id="0d0af-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="0d0af-184">Valido solo quando <code>ThemeColors</code> viene specificato per <em>l'attributo ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="0d0af-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="0d0af-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0d0af-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-186">Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0d0af-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d0af-187"><strong>StandardColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0d0af-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0d0af-189">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-189">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-190">Numero di righe di chip di colore (o campione) nell'area <strong>Colori</strong> standard.</span><span class="sxs-lookup"><span data-stu-id="0d0af-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="0d0af-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0d0af-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-192">Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0d0af-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d0af-193"><strong>ThemeColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="0d0af-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0d0af-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0d0af-195">No</span><span class="sxs-lookup"><span data-stu-id="0d0af-195">No</span></span><br/></td>
<td><span data-ttu-id="0d0af-196">Numero di righe di chip di colore (o campione) nell'area <strong>Colori tema.</strong></span><span class="sxs-lookup"><span data-stu-id="0d0af-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="0d0af-197">Valido solo quando <code>ThemeColors</code> viene specificato per <em>l'attributo ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="0d0af-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="0d0af-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0d0af-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0d0af-199">Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0d0af-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0d0af-200">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0d0af-200">Child elements</span></span>

<span data-ttu-id="0d0af-201">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="0d0af-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0d0af-202">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0d0af-202">Parent elements</span></span>



| <span data-ttu-id="0d0af-203">Elemento</span><span class="sxs-lookup"><span data-stu-id="0d0af-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="0d0af-204">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="0d0af-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="0d0af-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="0d0af-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="0d0af-206">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="0d0af-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="0d0af-207">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="0d0af-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="0d0af-208">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="0d0af-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="0d0af-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="0d0af-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="0d0af-210">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="0d0af-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0d0af-211">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d0af-211">Remarks</span></span>

<span data-ttu-id="0d0af-212">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0d0af-212">Optional.</span></span>

<span data-ttu-id="0d0af-213">Può verificarsi una o più volte per ogni elemento [**ControlGroup,**](windowsribbon-element-controlgroup.md) [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**Group,**](windowsribbon-element-group.md) [**MenuGroup,**](windowsribbon-element-menugroup.md) [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="0d0af-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="0d0af-214">Esempio</span><span class="sxs-lookup"><span data-stu-id="0d0af-214">Examples</span></span>

<span data-ttu-id="0d0af-215">Nell'esempio seguente viene illustrato il markup di base per tutti e tre i tipi di elenco a [discesa Selezione colori](windowsribbon-controls-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="0d0af-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="0d0af-216">Questa sezione di codice illustra le dichiarazioni Command per tre **elementi DropDownColorPicker.**</span><span class="sxs-lookup"><span data-stu-id="0d0af-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


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



<span data-ttu-id="0d0af-217">Questa sezione di codice illustra i tre tipi di dichiarazioni di controllo **DropDownColorPicker.**</span><span class="sxs-lookup"><span data-stu-id="0d0af-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="0d0af-218">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0d0af-218">Element information</span></span>

* <span data-ttu-id="0d0af-219">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d0af-219">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="0d0af-220">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="0d0af-220">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="0d0af-221">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d0af-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0af-222">Elenco a discesa Selezione colori controllo</span><span class="sxs-lookup"><span data-stu-id="0d0af-222">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="0d0af-223">Esempio di DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="0d0af-223">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





