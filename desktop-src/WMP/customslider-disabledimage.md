---
title: CUSTOMSLIDER.disabledImage
description: L'attributo disabledImage specifica o recupera l'immagine del dispositivo di scorrimento usato quando il dispositivo di scorrimento è disabilitato.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- Media Player Windows CUSTOMSLIDER. disabledImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331758"
---
# <a name="customsliderdisabledimage"></a>CUSTOMSLIDER.disabledImage

L'attributo **disabledImage** specifica o recupera l'immagine del dispositivo di scorrimento usato quando il dispositivo di scorrimento è disabilitato.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Se non è specificato, verrà usato il file specificato nell'attributo **Image** .

**DisabledImage** rappresenta lo stato disabilitato del controllo **CUSTOMSLIDER** . Può trattarsi di una singola immagine o di una serie di immagini che rappresentano i vari Stati del dispositivo di scorrimento. Se vengono usate più immagini, vengono disposte nello stesso modo del file di **immagine** .

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

 

 





