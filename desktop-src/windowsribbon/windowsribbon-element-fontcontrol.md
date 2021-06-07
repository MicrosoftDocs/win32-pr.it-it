---
title: Elemento FontControl
description: Rappresenta un controllo Tipo di carattere, un contenitore specializzato di singoli controlli dedicati alla manipolazione del tipo di carattere.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Barra multifunzione di Windows per l'elemento FontControl
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c9d900c2af4f7f8ba26f5ac8dbbdc0d055668d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443402"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="1f5b3-104">Elemento FontControl</span><span class="sxs-lookup"><span data-stu-id="1f5b3-104">FontControl element</span></span>

<span data-ttu-id="1f5b3-105">Rappresenta un [controllo Tipo di carattere](windowsribbon-controls-fontcontrol.md), che è un contenitore specializzato di singoli controlli dedicati alla manipolazione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="1f5b3-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="1f5b3-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="1f5b3-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="1f5b3-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f5b3-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="1f5b3-108">Attribute</span></span></th>
<th><span data-ttu-id="1f5b3-109">Type</span><span class="sxs-lookup"><span data-stu-id="1f5b3-109">Type</span></span></th>
<th><span data-ttu-id="1f5b3-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="1f5b3-110">Required</span></span></th>
<th><span data-ttu-id="1f5b3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f5b3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f5b3-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="1f5b3-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="1f5b3-114">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-114">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="1f5b3-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="1f5b3-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="1f5b3-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f5b3-120"><strong>Tipo di carattere</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="1f5b3-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="1f5b3-122">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-122">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-123">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f5b3-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="1f5b3-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="1f5b3-126">L'impostazione <em>dell'attributo FontType</em> <code>FontOnly</code> su abilita le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f5b3-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="1f5b3-127"><strong>Casella combinata della famiglia</strong> di caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="1f5b3-128"><strong>Casella combinata Dimensioni</strong> carattere.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="1f5b3-129"><strong>Pulsanti di</strong> <strong>attivazione/disattivazione</strong> <strong>grassetto,</strong>corsivo, <strong>sottolineatura e barrato.</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-130">I pulsanti <strong></strong> <strong>di</strong> attivazione/disattivazione Barrato e Sottolineatura vengono visualizzati per impostazione predefinita, ma possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="1f5b3-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="1f5b3-132">L'impostazione <em>dell'attributo FontType</em> <code>FontWithColor</code> su abilita le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f5b3-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="1f5b3-133"><strong>Casella combinata della famiglia</strong> di caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="1f5b3-134"><strong>Casella combinata Dimensioni</strong> carattere.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="1f5b3-135"><strong>Pulsanti Aumenta dimensioni carattere</strong> <strong>e Riduci dimensioni</strong> carattere incrementa e decrementa.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="1f5b3-136"><strong>Pulsanti di</strong> <strong>attivazione/disattivazione</strong> <strong>grassetto,</strong>corsivo, <strong>sottolineatura e barrato.</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-137">I pulsanti <strong></strong> <strong>di</strong> attivazione/disattivazione Barrato e Sottolineatura vengono visualizzati per impostazione predefinita, ma possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="1f5b3-138"><strong>Selezione colori</strong> testo.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="1f5b3-139"><strong>Selezione colori evidenziazione</strong> testo.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-140">Questo controllo è nascosto per impostazione predefinita, ma può essere visualizzato impostando <em>l'attributo IsHighlightButtonVisible</em> su <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="1f5b3-141"><dt><span></span><span></span><strong></strong> (RichFont)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="1f5b3-142">L'impostazione <em>dell'attributo FontType</em> <code>RichFont</code> su abilita le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f5b3-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="1f5b3-143"><strong>Casella combinata della famiglia</strong> di caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="1f5b3-144"><strong>Casella combinata Dimensioni</strong> carattere.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="1f5b3-145"><strong>Pulsanti Aumenta dimensioni carattere</strong> <strong>e Riduci dimensioni</strong> carattere incrementa e decrementa.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="1f5b3-146"><strong>Pulsanti di</strong> <strong>attivazione/disattivazione</strong> <strong>grassetto,</strong>corsivo, <strong>sottolineatura e barrato.</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-147">I pulsanti <strong></strong> <strong>di</strong> attivazione/disattivazione barrato e sottolineatura vengono visualizzati per impostazione predefinita e non possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="1f5b3-148"><strong>Selezione colori</strong> testo.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="1f5b3-149"><strong>Selezione colori evidenziazione</strong> testo.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-150">Questo controllo viene visualizzato per impostazione predefinita e non può essere nascosto impostando <em>l'attributo IsHighlightButtonVisible</em> su <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="1f5b3-151"><strong>Pulsanti di attivazione/disattivazione</strong> <strong>pedice</strong> e apice.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f5b3-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f5b3-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="1f5b3-154">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-154">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-155"><strong>Windows 8 e più recente</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="1f5b3-156">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f5b3-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-157">I pulsanti Aumenta/Riduci non vengono mai visualizzati in <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="1f5b3-158">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-159">Impostazione predefinita quando il valore di <em>FontType</em> è uguale <code>FontWithColor</code> a o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="1f5b3-160"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-161">Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f5b3-162"><strong>IsHighlightButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f5b3-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="1f5b3-164">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-164">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-165">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="1f5b3-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-166">L'evidenziazione dei colori è disponibile solo da <strong>un oggetto FontControl</strong> quando il valore dell'attributo <em>FontType</em> è uguale <code>FontWithColor</code> a o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="1f5b3-167">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-168">Impostazione predefinita quando il valore di <em>FontType</em> è uguale <code>FontWithColor</code> a o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="1f5b3-169">Valido solo quando il valore di <em>FontType</em> è uguale <code>FontWithColor</code> a o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="1f5b3-170"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-171">Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="1f5b3-172">Valido solo quando il valore di <em>FontType</em> è uguale <code>FontOnly</code> a o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f5b3-173"><strong>IsStrikethroughButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f5b3-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="1f5b3-175">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-175">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-176">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="1f5b3-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="1f5b3-177">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-178">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-178">Default.</span></span> <br/> </dd> <span data-ttu-id="1f5b3-179"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-180">Valido solo quando il valore di <em>FontType</em> è uguale <code>FontOnly</code> a o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f5b3-181"><strong>IsUnderlineButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-182">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f5b3-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="1f5b3-183">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-183">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-184">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="1f5b3-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="1f5b3-185">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-186">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-186">Default.</span></span> <br/> </dd> <span data-ttu-id="1f5b3-187"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-188">Valido solo quando il valore di <em>FontType</em> è uguale <code>FontOnly</code> a o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f5b3-189"><strong>MaximumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="1f5b3-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="1f5b3-191">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-191">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-192">Dimensione massima del punto da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="1f5b3-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-194">Valore intero compreso tra 1 e 9999, inclusi.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="1f5b3-195">Il valore predefinito <strong>è 9999.</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f5b3-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="1f5b3-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="1f5b3-198">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-198">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-199">Dimensione minima in punti da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="1f5b3-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-201">Valore intero compreso tra 1 e 9999 inclusi.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="1f5b3-202">Il valore predefinito <strong>è 1</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f5b3-203"><strong>ShowTrueTypeOnly</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f5b3-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="1f5b3-205">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-205">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-206">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="1f5b3-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="1f5b3-207">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-208">Visualizza solo i tipi di carattere TrueType e OpenType.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="1f5b3-209"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-210">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-210">Default.</span></span> <span data-ttu-id="1f5b3-211">Non viene impostata alcuna restrizione sul tipo di carattere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f5b3-212"><strong>ShowVerticalFonts</strong></span><span class="sxs-lookup"><span data-stu-id="1f5b3-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="1f5b3-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f5b3-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="1f5b3-214">No</span><span class="sxs-lookup"><span data-stu-id="1f5b3-214">No</span></span><br/></td>
<td><span data-ttu-id="1f5b3-215">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="1f5b3-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-216">I tipi di carattere verticali sono preceduti da un simbolo @ <strong>nell'elenco Famiglia di</strong> caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="1f5b3-217">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-218">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-218">Default.</span></span> <span data-ttu-id="1f5b3-219">Visualizza i tipi di carattere verticali impostati su <strong>Mostra nel</strong> pannello di <strong>controllo Tipi</strong> di carattere.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="1f5b3-220"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="1f5b3-221">Consente a un'applicazione che non supporta il testo verticale di nascondere i tipi di carattere verticali impostati su <strong>Mostra</strong> nel pannello <strong>di controllo Tipi di</strong> carattere.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f5b3-222">In Windows Vista il pannello <strong>di controllo Tipi</strong> di carattere non offre la <strong>funzionalità</strong> Mostra <strong>o</strong> Nascondi.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="1f5b3-223">In questo caso, <em>l'attributo ShowVerticalFonts</em> deve essere impostato su <code>False</code> .</span><span class="sxs-lookup"><span data-stu-id="1f5b3-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1f5b3-224">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1f5b3-224">Child elements</span></span>

<span data-ttu-id="1f5b3-225">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1f5b3-226">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="1f5b3-226">Parent elements</span></span>



| <span data-ttu-id="1f5b3-227">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f5b3-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="1f5b3-228">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="1f5b3-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="1f5b3-229">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="1f5b3-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="1f5b3-230">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="1f5b3-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="1f5b3-231">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f5b3-231">Remarks</span></span>

<span data-ttu-id="1f5b3-232">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-232">Optional.</span></span>

<span data-ttu-id="1f5b3-233">Può verificarsi al massimo una volta per [**ogni elemento ControlGroup,**](windowsribbon-element-controlgroup.md) [**Group**](windowsribbon-element-group.md) [**o MenuGroup.**](windowsribbon-element-menugroup.md)</span><span class="sxs-lookup"><span data-stu-id="1f5b3-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="1f5b3-234">Tutti gli attributi del comando **FontControl** dichiarati nel markup, ad esempio [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command.TooltipTitle,**](windowsribbon-element-command-tooltiptitle.md)vengono sottoposti a override dagli attributi dei singoli controlli che comprendono **FontControl.**</span><span class="sxs-lookup"><span data-stu-id="1f5b3-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="1f5b3-235">Qualsiasi tentativo di selezionare un campione di colore [](windowsribbon-controls-fontcontrol.md) dalla selezione colori di un controllo Tipo di carattere può comportare una violazione di accesso se al controllo non è associato alcun gestore comando.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="1f5b3-236">Esempio</span><span class="sxs-lookup"><span data-stu-id="1f5b3-236">Examples</span></span>

<span data-ttu-id="1f5b3-237">Nell'esempio seguente viene illustrato il markup di base per i tre tipi di [controllo Del tipo di carattere](windowsribbon-controls-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="1f5b3-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="1f5b3-238">Questa sezione di codice illustra le dichiarazioni **del comando FontControl,** ognuna con una dichiarazione [**del contenitore**](windowsribbon-element-group.md) Group.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


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



<span data-ttu-id="1f5b3-239">Questa sezione di codice illustra le **dichiarazioni del controllo FontControl** in cui ogni **fontControl** e [**gruppo**](windowsribbon-element-group.md) viene dichiarato in un'unica scheda.</span><span class="sxs-lookup"><span data-stu-id="1f5b3-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1f5b3-240">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1f5b3-240">Element information</span></span>

* <span data-ttu-id="1f5b3-241">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="1f5b3-241">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="1f5b3-242">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="1f5b3-242">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="1f5b3-243">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f5b3-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f5b3-244">Controllo Font</span><span class="sxs-lookup"><span data-stu-id="1f5b3-244">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="1f5b3-245">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="1f5b3-245">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="1f5b3-246">Esempio di FontControl</span><span class="sxs-lookup"><span data-stu-id="1f5b3-246">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





