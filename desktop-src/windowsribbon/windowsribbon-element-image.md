---
title: Elemento Image (Framework della barra multifunzione di Windows)
description: Rappresenta un'immagine.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Barra multifunzione di Windows elemento immagine
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d33f6710da2261a359aa7fd0a3b493871155cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104117165"
---
# <a name="image-element"></a><span data-ttu-id="5af86-104">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="5af86-104">Image element</span></span>

<span data-ttu-id="5af86-105">Rappresenta un'immagine.</span><span class="sxs-lookup"><span data-stu-id="5af86-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="5af86-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5af86-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="5af86-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="5af86-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5af86-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="5af86-108">Attribute</span></span></th>
<th><span data-ttu-id="5af86-109">Type</span><span class="sxs-lookup"><span data-stu-id="5af86-109">Type</span></span></th>
<th><span data-ttu-id="5af86-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="5af86-110">Required</span></span></th>
<th><span data-ttu-id="5af86-111">Description</span><span class="sxs-lookup"><span data-stu-id="5af86-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5af86-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="5af86-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="5af86-113">XS: positiveInteger Union XS: String</span><span class="sxs-lookup"><span data-stu-id="5af86-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="5af86-114">No</span><span class="sxs-lookup"><span data-stu-id="5af86-114">No</span></span><br/></td>
<td><span data-ttu-id="5af86-115">ID di risorsa univoco.</span><span class="sxs-lookup"><span data-stu-id="5af86-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="5af86-116">
<dt><span></span><span></span><strong></strong> (Unione di XS: positiveInteger e xs: String)</span><span class="sxs-lookup"><span data-stu-id="5af86-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="5af86-117">Valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="5af86-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="5af86-118">La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi.</span><span class="sxs-lookup"><span data-stu-id="5af86-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5af86-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="5af86-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="5af86-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="5af86-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="5af86-121">No</span><span class="sxs-lookup"><span data-stu-id="5af86-121">No</span></span><br/></td>
<td><span data-ttu-id="5af86-122"><dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="5af86-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="5af86-123">Qualsiasi sequenza di cifre con un valore minimo pari a 96.</span><span class="sxs-lookup"><span data-stu-id="5af86-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="5af86-124">Se MinDPI viene omesso, il valore predefinito è 96.</span><span class="sxs-lookup"><span data-stu-id="5af86-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5af86-125"><strong>Origine</strong></span><span class="sxs-lookup"><span data-stu-id="5af86-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="5af86-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="5af86-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="5af86-127">No</span><span class="sxs-lookup"><span data-stu-id="5af86-127">No</span></span><br/></td>
<td><span data-ttu-id="5af86-128"><dt><span></span><span></span><strong></strong> (XS: anyURI)</span><span class="sxs-lookup"><span data-stu-id="5af86-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="5af86-129">Qualsiasi sequenza di caratteri che rappresenta un URI.</span><span class="sxs-lookup"><span data-stu-id="5af86-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="5af86-130">Il valore URI è un percorso assoluto o relativo (per il file di markup della barra multifunzione) a una risorsa immagine di tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="5af86-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5af86-131"><strong>Simbolo</strong></span><span class="sxs-lookup"><span data-stu-id="5af86-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="5af86-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="5af86-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="5af86-133">No</span><span class="sxs-lookup"><span data-stu-id="5af86-133">No</span></span><br/></td>
<td><span data-ttu-id="5af86-134">Simbolo di risorsa per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="5af86-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="5af86-135">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="5af86-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="5af86-136">Stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di lettere, cifre o caratteri di sottolineatura fino a un massimo di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5af86-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="5af86-137">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5af86-137">Child elements</span></span>



| <span data-ttu-id="5af86-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="5af86-138">Element</span></span>                                                               | <span data-ttu-id="5af86-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5af86-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="5af86-140">**Image. Source**</span><span class="sxs-lookup"><span data-stu-id="5af86-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="5af86-141">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="5af86-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5af86-142">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5af86-142">Parent elements</span></span>



| <span data-ttu-id="5af86-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="5af86-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5af86-144">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="5af86-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="5af86-145">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="5af86-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="5af86-146">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="5af86-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="5af86-147">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="5af86-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="5af86-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="5af86-148">Remarks</span></span>

<span data-ttu-id="5af86-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5af86-149">Optional.</span></span>

<span data-ttu-id="5af86-150">Può essere presente una o più volte per ogni [**comando. SmallImages**](windowsribbon-element-command-smallimages.md), [**Command. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. LargeImages**](windowsribbon-element-command-largeimages.md)o [**Command. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) .</span><span class="sxs-lookup"><span data-stu-id="5af86-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="5af86-151">Quando una raccolta di risorse immagine progettate per supportare specifiche impostazioni dpi (screen punti per pollice) viene fornita al framework della barra multifunzione tramite un set di elementi **immagine** , il Framework usa l' **immagine** con un valore dell'attributo *MinDPI* che corrisponde all'impostazione DPI dello schermo corrente.</span><span class="sxs-lookup"><span data-stu-id="5af86-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="5af86-152">Se nessun elemento **Image** è dichiarato con un valore *MinDPI* che corrisponde all'impostazione DPI dello schermo corrente, il Framework seleziona l' **immagine** con il valore *MinDPI* più vicino inferiore rispetto all'impostazione DPI dello schermo corrente e ridimensiona la risorsa dell'immagine verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="5af86-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="5af86-153">In caso contrario, se non viene dichiarato alcun elemento **Image** con un valore dell'attributo *MinDPI* inferiore a quello della schermata corrente, il Framework sceglie il valore *MinDPI* più vicino maggiore dell'impostazione corrente DPI dello schermo e ridimensiona la risorsa immagine verso il basso.</span><span class="sxs-lookup"><span data-stu-id="5af86-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="5af86-154">Esempio</span><span class="sxs-lookup"><span data-stu-id="5af86-154">Examples</span></span>

<span data-ttu-id="5af86-155">Nell'esempio di codice seguente viene illustrato il markup necessario per dichiarare, tramite un set di elementi **immagine** , una raccolta di risorse immagine progettate per supportare quattro impostazioni DPI dello schermo specifiche.</span><span class="sxs-lookup"><span data-stu-id="5af86-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a><span data-ttu-id="5af86-156">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5af86-156">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="5af86-157">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5af86-157">Minimum supported system</span></span><br/> | <span data-ttu-id="5af86-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5af86-158">Windows 7</span></span> |
| <span data-ttu-id="5af86-159">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="5af86-159">Can be empty</span></span>                        | <span data-ttu-id="5af86-160">No</span><span class="sxs-lookup"><span data-stu-id="5af86-160">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="5af86-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5af86-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af86-162">Specifica delle risorse dell'immagine della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="5af86-162">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





