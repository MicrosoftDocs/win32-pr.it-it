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
# <a name="image-element"></a>Elemento Image

Rappresenta un'immagine.

## <a name="usage"></a>Utilizzo

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Type</th>
<th>Obbligatoria</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger union xs:string<br/></td>
<td>No<br/></td>
<td>ID risorsa univoco. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Unione di xs:positiveInteger e xs:string)<br/> </dt> <dd> Valore intero compreso tra 2 e 59999, inclusi o 0x2 e 0xea5f in formato esadecimale, inclusivo. <br/> La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualsiasi sequenza di cifre con un valore minimo di 96. <br/> Se MinDPI viene omesso, il valore predefinito è 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Origine</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:anyURI)<br/> </dt> <dd> Qualsiasi sequenza di caratteri che rappresenta un URI. Il valore URI è un percorso assoluto o relativo (al file di markup della barra multifunzione) di una risorsa immagine di tipo BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Simbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Simbolo della risorsa per l'immagine.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa composta da una lettera o un carattere di sottolineatura seguito da qualsiasi sequenza di lettere, cifre o caratteri di sottolineatura fino a un massimo di 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Descrizione                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image.Source**](windowsribbon-element-image-source.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Command.SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per ogni elemento [**Command.SmallImages,**](windowsribbon-element-command-smallimages.md) [**Command.SmallHighContrastImages,**](windowsribbon-element-command-smallhighcontrastimages.md) [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)o [**Command.LargeHighContrastImages.**](windowsribbon-element-command-largehighcontrastimages.md)

Quando al framework della barra multifunzione viene fornita una raccolta di risorse immagine progettate per supportare impostazioni specifiche dei punti  per pollice (dpi) dello schermo tramite un set di elementi **Image,** il framework usa l'immagine con un valore di *attributo MinDPI* corrispondente all'impostazione dpi dello schermo corrente.

Se nessun elemento **Image** viene dichiarato con un valore *MinDPI* corrispondente all'impostazione dpi dello schermo corrente, il framework seleziona l'immagine con il valore  *MinDPI* più vicino minore dell'impostazione dpi dello schermo corrente e ridimensiona la risorsa immagine. In caso contrario, se nessun elemento **Image** viene dichiarato con un valore di attributo *MinDPI* minore dell'impostazione dpi dello schermo corrente, il framework seleziona il valore *MinDPI* più vicino maggiore dell'impostazione dpi dello schermo corrente e ridimensiona la risorsa immagine.

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra il markup necessario per dichiarare, tramite un set di elementi **Image,** una raccolta di risorse immagine progettate per supportare quattro impostazioni dpi dello schermo specifiche.


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



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Specifica delle risorse immagine della barra multifunzione](windowsribbon-imageformats.md)
</dt> </dl>

 

 





