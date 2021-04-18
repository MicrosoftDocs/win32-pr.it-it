---
title: CUSTOMSLIDER.hoverImage
description: L'attributo hoverImage specifica o recupera l'immagine visualizzata quando il mouse è posizionato sul dispositivo di scorrimento personalizzato.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- Media Player Windows CUSTOMSLIDER. hoverImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 361f7d903b6231e92f331ab38a3a9f51bc3ec679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331487"
---
# <a name="customsliderhoverimage"></a>CUSTOMSLIDER.hoverImage

L'attributo **hoverImage** specifica o recupera l'immagine visualizzata quando il mouse è posizionato sul dispositivo di scorrimento personalizzato.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Se non è specificato, verrà usato il file specificato nell'attributo **Image** .

**HoverImage** rappresenta lo stato del passaggio del mouse sul controllo CUSTOMSLIDER; ovvero lo stato visualizzato quando il cursore del mouse viene posizionato su di esso. Può trattarsi di una singola immagine o di una serie di immagini che rappresentano i vari Stati del dispositivo di scorrimento. Se vengono usate più immagini, vengono disposte nello stesso modo del file di **immagine**

I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. image**](customslider-image.md)
</dt> </dl>

 

 





