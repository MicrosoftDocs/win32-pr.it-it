---
title: Image.Source - proprietà
description: Rappresenta il percorso di directory di un'immagine.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Proprietà Image.Source Windows barra multifunzione
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20612f0d25f914cb4c80ae77bb001a678af79e4605c3e1358ed7e33f6b19d805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202406"
---
# <a name="imagesource-property"></a>Image.Source - proprietà

Rappresenta il percorso di directory di un'immagine.

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

Può verificarsi al massimo una volta per ogni [**immagine**](windowsribbon-element-image.md).

Questo elemento contiene un valore di tipo *xs:anyURI* o qualsiasi sequenza di caratteri che rappresenta un Uniform Resource Identifier (URI). Il valore URI è un percorso di directory assoluto o relativo (al file di markup della barra multifunzione) di una risorsa immagine di tipo bitmap (BMP).

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra il markup necessario per dichiarare, tramite un set di elementi [**Image,**](windowsribbon-element-image.md) una raccolta di risorse immagine progettate per supportare quattro impostazioni dpi dello schermo specifiche. La **proprietà Image.Source** viene usata per specificare il percorso della risorsa immagine.


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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





