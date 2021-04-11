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
<td>XS: positiveInteger Union XS: String<br/></td>
<td>No<br/></td>
<td>ID di risorsa univoco. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Unione di XS: positiveInteger e xs: String)<br/> </dt> <dd> Valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo. <br/> La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Qualsiasi sequenza di cifre con un valore minimo pari a 96. <br/> Se MinDPI viene omesso, il valore predefinito è 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Origine</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: anyURI)<br/> </dt> <dd> Qualsiasi sequenza di caratteri che rappresenta un URI. Il valore URI è un percorso assoluto o relativo (per il file di markup della barra multifunzione) a una risorsa immagine di tipo BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Simbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Simbolo di risorsa per l'immagine.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di lettere, cifre o caratteri di sottolineatura fino a un massimo di 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Descrizione                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image. Source**](windowsribbon-element-image-source.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Comando. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Comando. LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Comando. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Comando. SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente una o più volte per ogni [**comando. SmallImages**](windowsribbon-element-command-smallimages.md), [**Command. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. LargeImages**](windowsribbon-element-command-largeimages.md)o [**Command. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) .

Quando una raccolta di risorse immagine progettate per supportare specifiche impostazioni dpi (screen punti per pollice) viene fornita al framework della barra multifunzione tramite un set di elementi **immagine** , il Framework usa l' **immagine** con un valore dell'attributo *MinDPI* che corrisponde all'impostazione DPI dello schermo corrente.

Se nessun elemento **Image** è dichiarato con un valore *MinDPI* che corrisponde all'impostazione DPI dello schermo corrente, il Framework seleziona l' **immagine** con il valore *MinDPI* più vicino inferiore rispetto all'impostazione DPI dello schermo corrente e ridimensiona la risorsa dell'immagine verso l'alto. In caso contrario, se non viene dichiarato alcun elemento **Image** con un valore dell'attributo *MinDPI* inferiore a quello della schermata corrente, il Framework sceglie il valore *MinDPI* più vicino maggiore dell'impostazione corrente DPI dello schermo e ridimensiona la risorsa immagine verso il basso.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato il markup necessario per dichiarare, tramite un set di elementi **immagine** , una raccolta di risorse immagine progettate per supportare quattro impostazioni DPI dello schermo specifiche.


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | No        |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Specifica delle risorse dell'immagine della barra multifunzione](windowsribbon-imageformats.md)
</dt> </dl>

 

 





