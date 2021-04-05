---
title: Proprietà Image. Source
description: Rappresenta il percorso della directory di un'immagine.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Proprietà Image. Source-barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740999"
---
# <a name="imagesource-property"></a>Proprietà Image. Source

Rappresenta il percorso della directory di un'immagine.

## <a name="usage"></a>Utilizzo

``` syntax
<Image.Source/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                 |
|---------------------------------------------------------|
| [**Immagine**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente al massimo una volta per ogni [**immagine**](windowsribbon-element-image.md).

Questo elemento contiene un valore di tipo *xs: anyURI* o qualsiasi sequenza di caratteri che rappresenta un Uniform Resource Identifier (URI). Il valore URI è un percorso di directory assoluto o relativo (al file di markup della barra multifunzione) di una risorsa immagine di tipo bitmap (BMP).

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato il markup necessario per dichiarare, tramite un set di elementi [**immagine**](windowsribbon-element-image.md) , una raccolta di risorse immagine progettate per supportare quattro impostazioni DPI dello schermo specifiche. La proprietà **Image. Source** viene utilizzata per specificare il percorso della risorsa immagine.


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





