---
title: CUSTOMSLIDER.downImage
description: L'attributo downImage specifica o recupera l'immagine dello stato verso il basso del dispositivo di scorrimento personalizzato.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- CUSTOMSLIDER.downImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e151f825dab7170c3e3678f280303265af0df91561c7dc709323dd8043809e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750340"
---
# <a name="customsliderdownimage"></a>CUSTOMSLIDER.downImage

**L'attributo downImage** specifica o recupera l'immagine dello stato verso il basso del dispositivo di scorrimento personalizzato.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Se non viene specificato, verrà  usato il file specificato nell'attributo image.

DownImage **rappresenta** lo stato in basso del **controllo CUSTOMSLIDER.** Può essere una singola immagine o una serie di immagini che rappresentano i vari stati del dispositivo di scorrimento. Se vengono usate più immagini, vengono disposte nello stesso modo del file **di** immagine.

I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (senza includere GIF animate).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.image**](customslider-image.md)
</dt> </dl>

 

 





