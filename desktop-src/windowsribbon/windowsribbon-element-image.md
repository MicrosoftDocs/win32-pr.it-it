---
title: Elemento Image (Windows Ribbon Framework)
description: Rappresenta un'immagine.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Elemento Image della barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442892"
---
# <a name="image-element"></a><span data-ttu-id="8995f-104">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="8995f-104">Image element</span></span>

<span data-ttu-id="8995f-105">Rappresenta un'immagine.</span><span class="sxs-lookup"><span data-stu-id="8995f-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="8995f-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8995f-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="8995f-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="8995f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8995f-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="8995f-108">Attribute</span></span></th>
<th><span data-ttu-id="8995f-109">Type</span><span class="sxs-lookup"><span data-stu-id="8995f-109">Type</span></span></th>
<th><span data-ttu-id="8995f-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="8995f-110">Required</span></span></th>
<th><span data-ttu-id="8995f-111">Description</span><span class="sxs-lookup"><span data-stu-id="8995f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8995f-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="8995f-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="8995f-113">xs:positiveInteger union xs:string</span><span class="sxs-lookup"><span data-stu-id="8995f-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="8995f-114">No</span><span class="sxs-lookup"><span data-stu-id="8995f-114">No</span></span><br/></td>
<td><span data-ttu-id="8995f-115">ID risorsa univoco.</span><span class="sxs-lookup"><span data-stu-id="8995f-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="8995f-116">
<dt><span></span><span></span><strong></strong> (Unione di xs:positiveInteger e xs:string)</span><span class="sxs-lookup"><span data-stu-id="8995f-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8995f-117">Valore intero compreso tra 2 e 59999, inclusi o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="8995f-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="8995f-118">La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi.</span><span class="sxs-lookup"><span data-stu-id="8995f-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8995f-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="8995f-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="8995f-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="8995f-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="8995f-121">No</span><span class="sxs-lookup"><span data-stu-id="8995f-121">No</span></span><br/></td>
<td><span data-ttu-id="8995f-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="8995f-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="8995f-123">Qualsiasi sequenza di cifre con un valore minimo di 96.</span><span class="sxs-lookup"><span data-stu-id="8995f-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="8995f-124">Se MinDPI viene omesso, il valore predefinito è 96.</span><span class="sxs-lookup"><span data-stu-id="8995f-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8995f-125"><strong>Origine</strong></span><span class="sxs-lookup"><span data-stu-id="8995f-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="8995f-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="8995f-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="8995f-127">No</span><span class="sxs-lookup"><span data-stu-id="8995f-127">No</span></span><br/></td>
<td><span data-ttu-id="8995f-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span><span class="sxs-lookup"><span data-stu-id="8995f-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="8995f-129">Qualsiasi sequenza di caratteri che rappresenta un URI.</span><span class="sxs-lookup"><span data-stu-id="8995f-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="8995f-130">Il valore URI è un percorso assoluto o relativo (al file di markup della barra multifunzione) di una risorsa immagine di tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="8995f-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8995f-131"><strong>Simbolo</strong></span><span class="sxs-lookup"><span data-stu-id="8995f-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="8995f-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="8995f-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="8995f-133">No</span><span class="sxs-lookup"><span data-stu-id="8995f-133">No</span></span><br/></td>
<td><span data-ttu-id="8995f-134">Simbolo della risorsa per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="8995f-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="8995f-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="8995f-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8995f-136">Stringa composta da una lettera o un carattere di sottolineatura seguito da qualsiasi sequenza di lettere, cifre o caratteri di sottolineatura fino a un massimo di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="8995f-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="8995f-137">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8995f-137">Child elements</span></span>



| <span data-ttu-id="8995f-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="8995f-138">Element</span></span>                                                               | <span data-ttu-id="8995f-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8995f-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="8995f-140">**Image.Source**</span><span class="sxs-lookup"><span data-stu-id="8995f-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="8995f-141">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="8995f-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8995f-142">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8995f-142">Parent elements</span></span>



| <span data-ttu-id="8995f-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="8995f-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8995f-144">**Command.LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="8995f-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="8995f-145">**Command.LargeImages**</span><span class="sxs-lookup"><span data-stu-id="8995f-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="8995f-146">**Command.SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="8995f-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="8995f-147">**Command.SmallImages**</span><span class="sxs-lookup"><span data-stu-id="8995f-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="8995f-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="8995f-148">Remarks</span></span>

<span data-ttu-id="8995f-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8995f-149">Optional.</span></span>

<span data-ttu-id="8995f-150">Può verificarsi una o più volte per ogni elemento [**Command.SmallImages,**](windowsribbon-element-command-smallimages.md) [**Command.SmallHighContrastImages,**](windowsribbon-element-command-smallhighcontrastimages.md) [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)o [**Command.LargeHighContrastImages.**](windowsribbon-element-command-largehighcontrastimages.md)</span><span class="sxs-lookup"><span data-stu-id="8995f-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="8995f-151">Quando al framework della barra multifunzione viene fornita una raccolta di risorse immagine progettate per supportare impostazioni specifiche dei punti  per pollice (dpi) dello schermo tramite un set di elementi **Image,** il framework usa l'immagine con un valore di *attributo MinDPI* corrispondente all'impostazione dpi dello schermo corrente.</span><span class="sxs-lookup"><span data-stu-id="8995f-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="8995f-152">Se nessun elemento **Image** viene dichiarato con un valore *MinDPI* corrispondente all'impostazione dpi dello schermo corrente, il framework seleziona l'immagine con il valore  *MinDPI* più vicino minore dell'impostazione dpi dello schermo corrente e ridimensiona la risorsa immagine.</span><span class="sxs-lookup"><span data-stu-id="8995f-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="8995f-153">In caso contrario, se nessun elemento **Image** viene dichiarato con un valore di attributo *MinDPI* minore dell'impostazione dpi dello schermo corrente, il framework seleziona il valore *MinDPI* più vicino maggiore dell'impostazione dpi dello schermo corrente e ridimensiona la risorsa immagine.</span><span class="sxs-lookup"><span data-stu-id="8995f-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="8995f-154">Esempio</span><span class="sxs-lookup"><span data-stu-id="8995f-154">Examples</span></span>

<span data-ttu-id="8995f-155">L'esempio di codice seguente illustra il markup necessario per dichiarare, tramite un set di elementi **Image,** una raccolta di risorse immagine progettate per supportare quattro impostazioni dpi dello schermo specifiche.</span><span class="sxs-lookup"><span data-stu-id="8995f-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="8995f-156">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8995f-156">Element information</span></span>

* <span data-ttu-id="8995f-157">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="8995f-157">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="8995f-158">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="8995f-158">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="8995f-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8995f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8995f-160">Specifica delle risorse immagine della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="8995f-160">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





