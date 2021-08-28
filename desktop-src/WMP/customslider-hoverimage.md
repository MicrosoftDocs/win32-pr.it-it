---
title: CUSTOMSLIDER.hoverImage
description: L'attributo hoverImage specifica o recupera l'immagine visualizzata quando il mouse si trova sul dispositivo di scorrimento personalizzato.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- CUSTOMSLIDER.hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d12f337c8d4889e0d2e94bac0c0a4dce74f3a80fda9261d245b91ce5612754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651401"
---
# <a name="customsliderhoverimage"></a>CUSTOMSLIDER.hoverImage

**L'attributo hoverImage** specifica o recupera l'immagine visualizzata quando il mouse si trova sul dispositivo di scorrimento personalizzato.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Se non viene specificato, verrà usato il file specificato nell'attributo **image.**

HoverImage **rappresenta** lo stato del passaggio del mouse del controllo CUSTOMSLIDER. cio, lo stato visualizzato quando il cursore del mouse passa su di esso. Può essere una singola immagine o una serie di immagini che rappresentano i vari stati del dispositivo di scorrimento. Se vengono usate più immagini, vengono disposte nello stesso modo del file **di** immagine

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

 

 





