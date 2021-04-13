---
title: Elemento FontControl
description: Rappresenta un controllo del tipo di carattere, ovvero un contenitore specializzato di singoli controlli dedicati alla manipolazione dei tipi di carattere.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Barra multifunzione Windows elemento FontControl
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa080b58e3a9d53fa044e7dbbb6598d5b7be7c49
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2020
ms.locfileid: "104398823"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="0c600-104">Elemento FontControl</span><span class="sxs-lookup"><span data-stu-id="0c600-104">FontControl element</span></span>

<span data-ttu-id="0c600-105">Rappresenta un [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md), ovvero un contenitore specializzato di singoli controlli dedicati alla manipolazione dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="0c600-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="0c600-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0c600-106">Usage</span></span>

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
```

## <a name="attributes"></a><span data-ttu-id="0c600-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="0c600-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c600-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="0c600-108">Attribute</span></span></th>
<th><span data-ttu-id="0c600-109">Type</span><span class="sxs-lookup"><span data-stu-id="0c600-109">Type</span></span></th>
<th><span data-ttu-id="0c600-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="0c600-110">Required</span></span></th>
<th><span data-ttu-id="0c600-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c600-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c600-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="0c600-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0c600-114">No</span><span class="sxs-lookup"><span data-stu-id="0c600-114">No</span></span><br/></td>
<td><span data-ttu-id="0c600-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0c600-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="0c600-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="0c600-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="0c600-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="0c600-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0c600-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="0c600-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0c600-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c600-120"><strong>FontType</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c600-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="0c600-122">No</span><span class="sxs-lookup"><span data-stu-id="0c600-122">No</span></span><br/></td>
<td><span data-ttu-id="0c600-123">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c600-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="0c600-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span><span class="sxs-lookup"><span data-stu-id="0c600-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0c600-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="0c600-126">Impostando l'attributo <em>FontType</em> su <code>FontOnly</code> sono abilitate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c600-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="0c600-127">Casella combinata della <strong>famiglia di caratteri</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="0c600-128">Casella combinata <strong>dimensioni carattere</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="0c600-129">Pulsanti di attivazione con <strong>grassetto</strong>, <strong>corsivo</strong>, <strong>sottolineatura</strong>e <strong>barrato</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-130">I pulsanti per l'interruttore <strong>barrato</strong> e <strong>sottolineatura</strong> vengono visualizzati per impostazione predefinita, ma possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="0c600-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span><span class="sxs-lookup"><span data-stu-id="0c600-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="0c600-132">Impostando l'attributo <em>FontType</em> su <code>FontWithColor</code> sono abilitate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c600-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="0c600-133">Casella combinata della <strong>famiglia di caratteri</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="0c600-134">Casella combinata <strong>dimensioni carattere</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="0c600-135"><strong>Aumentare</strong> le dimensioni del carattere e <strong>ridurre</strong> i pulsanti di incremento e decremento del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="0c600-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="0c600-136">Pulsanti di attivazione con <strong>grassetto</strong>, <strong>corsivo</strong>, <strong>sottolineatura</strong>e <strong>barrato</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-137">I pulsanti per l'interruttore <strong>barrato</strong> e <strong>sottolineatura</strong> vengono visualizzati per impostazione predefinita, ma possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="0c600-138">Selezione colori <strong>colore testo</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="0c600-139">Selezione colore colore <strong>evidenziazione testo</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-140">Questo controllo è nascosto per impostazione predefinita, ma può essere visualizzato impostando l'attributo <em>IsHighlightButtonVisible</em> su <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="0c600-141"><dt><span></span><span></span><strong></strong> (RichFont)</span><span class="sxs-lookup"><span data-stu-id="0c600-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="0c600-142">Impostando l'attributo <em>FontType</em> su <code>RichFont</code> sono abilitate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c600-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="0c600-143">Casella combinata della <strong>famiglia di caratteri</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="0c600-144">Casella combinata <strong>dimensioni carattere</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="0c600-145"><strong>Aumentare</strong> le dimensioni del carattere e <strong>ridurre</strong> i pulsanti di incremento e decremento del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="0c600-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="0c600-146">Pulsanti di attivazione con <strong>grassetto</strong>, <strong>corsivo</strong>, <strong>sottolineatura</strong>e <strong>barrato</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-147">I pulsanti per l'interruttore <strong>barrato</strong> e <strong>sottolineatura</strong> vengono visualizzati per impostazione predefinita e non possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="0c600-148">Selezione colori <strong>colore testo</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="0c600-149">Selezione colore colore <strong>evidenziazione testo</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-150">Questo controllo viene visualizzato per impostazione predefinita e non può essere nascosto impostando l'attributo <em>IsHighlightButtonVisible</em> su <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="0c600-151">Pulsanti <strong>per l'attivazione di pedice</strong> <strong>e pedice</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c600-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="0c600-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="0c600-154">No</span><span class="sxs-lookup"><span data-stu-id="0c600-154">No</span></span><br/></td>
<td><span data-ttu-id="0c600-155"><strong>Windows 8 e versioni successive</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="0c600-156">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c600-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-157">I pulsanti di espansione/compattazione non vengono mai visualizzati in <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0c600-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="0c600-158">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="0c600-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-159">Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontWithColor</code> o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="0c600-160"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="0c600-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-161">Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c600-162"><strong>IsHighlightButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="0c600-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="0c600-164">No</span><span class="sxs-lookup"><span data-stu-id="0c600-164">No</span></span><br/></td>
<td><span data-ttu-id="0c600-165">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="0c600-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-166">L'evidenziazione dei colori è disponibile solo da un <strong>FontControl</strong> quando il valore dell'attributo <em>FontType</em> è uguale a <code>FontWithColor</code> o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="0c600-167">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="0c600-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-168">Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontWithColor</code> o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="0c600-169">Valido solo quando il valore di <em>FontType</em> è uguale a <code>FontWithColor</code> o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="0c600-170"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="0c600-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-171">Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="0c600-172">Valido solo quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c600-173"><strong>IsStrikethroughButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="0c600-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="0c600-175">No</span><span class="sxs-lookup"><span data-stu-id="0c600-175">No</span></span><br/></td>
<td><span data-ttu-id="0c600-176">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="0c600-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="0c600-177">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="0c600-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-178">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0c600-178">Default.</span></span> <br/> </dd> <span data-ttu-id="0c600-179"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="0c600-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-180">Valido solo quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c600-181"><strong>IsUnderlineButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-182">Boolean</span><span class="sxs-lookup"><span data-stu-id="0c600-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="0c600-183">No</span><span class="sxs-lookup"><span data-stu-id="0c600-183">No</span></span><br/></td>
<td><span data-ttu-id="0c600-184">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="0c600-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="0c600-185">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="0c600-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-186">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0c600-186">Default.</span></span> <br/> </dd> <span data-ttu-id="0c600-187"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="0c600-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-188">Valido solo quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c600-189"><strong>MaximumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0c600-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0c600-191">No</span><span class="sxs-lookup"><span data-stu-id="0c600-191">No</span></span><br/></td>
<td><span data-ttu-id="0c600-192">Dimensioni massime del punto da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="0c600-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="0c600-193">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0c600-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-194">Valore intero compreso tra 1 e 9999 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0c600-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="0c600-195">Il valore predefinito è <strong>9999</strong>.</span><span class="sxs-lookup"><span data-stu-id="0c600-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c600-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0c600-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0c600-198">No</span><span class="sxs-lookup"><span data-stu-id="0c600-198">No</span></span><br/></td>
<td><span data-ttu-id="0c600-199">Dimensioni minime del punto da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="0c600-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="0c600-200">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0c600-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-201">Valore intero compreso tra 1 e 9999 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0c600-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="0c600-202">Il valore predefinito è <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="0c600-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c600-203"><strong>ShowTrueTypeOnly</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="0c600-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="0c600-205">No</span><span class="sxs-lookup"><span data-stu-id="0c600-205">No</span></span><br/></td>
<td><span data-ttu-id="0c600-206">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="0c600-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="0c600-207">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="0c600-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-208">Consente di visualizzare solo i tipi di carattere TrueType e OpenType.</span><span class="sxs-lookup"><span data-stu-id="0c600-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="0c600-209"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="0c600-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-210">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0c600-210">Default.</span></span> <span data-ttu-id="0c600-211">Nessuna restrizione viene posizionata sul tipo di carattere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="0c600-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c600-212"><strong>ShowVerticalFonts</strong></span><span class="sxs-lookup"><span data-stu-id="0c600-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="0c600-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="0c600-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="0c600-214">No</span><span class="sxs-lookup"><span data-stu-id="0c600-214">No</span></span><br/></td>
<td><span data-ttu-id="0c600-215">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="0c600-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-216">I tipi di carattere verticali sono preceduti da un simbolo @ nell'elenco della <strong>famiglia di caratteri</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="0c600-217">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="0c600-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-218">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0c600-218">Default.</span></span> <span data-ttu-id="0c600-219">Consente di visualizzare i tipi di carattere verticali impostati per la <strong>visualizzazione</strong> nel pannello di controllo dei <strong>tipi di carattere</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="0c600-220"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="0c600-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="0c600-221">Consente a un'applicazione che non supporta il testo verticale di nascondere i tipi di carattere verticali impostati per la <strong>visualizzazione</strong> nel pannello di controllo dei <strong>tipi di carattere</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c600-222">In Windows Vista, il pannello di controllo dei <strong>tipi di carattere</strong> non offre funzionalità <strong>Mostra</strong> o <strong>Nascondi</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c600-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="0c600-223">In questo caso, l'attributo <em>ShowVerticalFonts</em> deve essere impostato su <code>False</code> .</span><span class="sxs-lookup"><span data-stu-id="0c600-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0c600-224">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0c600-224">Child elements</span></span>

<span data-ttu-id="0c600-225">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="0c600-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0c600-226">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0c600-226">Parent elements</span></span>



| <span data-ttu-id="0c600-227">Elemento</span><span class="sxs-lookup"><span data-stu-id="0c600-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="0c600-228">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="0c600-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="0c600-229">**Group**</span><span class="sxs-lookup"><span data-stu-id="0c600-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="0c600-230">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="0c600-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="0c600-231">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c600-231">Remarks</span></span>

<span data-ttu-id="0c600-232">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0c600-232">Optional.</span></span>

<span data-ttu-id="0c600-233">Può verificarsi al massimo una volta per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md)o [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="0c600-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="0c600-234">Tutti gli attributi del comando **FontControl** dichiarati nel markup, ad esempio [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), vengono sottoposti a override dagli attributi dei singoli controlli che comprendono **FontControl**.</span><span class="sxs-lookup"><span data-stu-id="0c600-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="0c600-235">Qualsiasi tentativo di selezionare un campione di colore dalla selezione colori di un [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md) può causare una violazione di accesso se al controllo non è associato alcun gestore di comando.</span><span class="sxs-lookup"><span data-stu-id="0c600-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="0c600-236">Esempio</span><span class="sxs-lookup"><span data-stu-id="0c600-236">Examples</span></span>

<span data-ttu-id="0c600-237">Nell'esempio seguente viene illustrato il markup di base per i tre tipi di [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="0c600-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="0c600-238">In questa sezione del codice vengono illustrate le dichiarazioni di comando **FontControl** , ognuna con una dichiarazione del contenitore di [**gruppo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="0c600-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



<span data-ttu-id="0c600-239">Questa sezione di codice mostra le dichiarazioni di controllo **FontControl** in cui ogni **FontControl** e [**gruppo**](windowsribbon-element-group.md) viene dichiarato in una singola scheda.</span><span class="sxs-lookup"><span data-stu-id="0c600-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a><span data-ttu-id="0c600-240">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0c600-240">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="0c600-241">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c600-241">Minimum supported system</span></span><br/> | <span data-ttu-id="0c600-242">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c600-242">Windows 7</span></span> |
| <span data-ttu-id="0c600-243">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0c600-243">Can be empty</span></span>                        | <span data-ttu-id="0c600-244">Sì</span><span class="sxs-lookup"><span data-stu-id="0c600-244">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="0c600-245">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c600-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c600-246">Controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="0c600-246">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="0c600-247">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="0c600-247">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="0c600-248">Esempio FontControl</span><span class="sxs-lookup"><span data-stu-id="0c600-248">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





