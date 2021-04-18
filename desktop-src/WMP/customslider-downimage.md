---
title: CUSTOMSLIDER.downImage
description: L'attributo downImage specifica o recupera l'immagine di stato inattivo del dispositivo di scorrimento personalizzato.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- Media Player Windows CUSTOMSLIDER. downImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8365043654bc3cca9fbf79162302cf804155956d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331755"
---
# <a name="customsliderdownimage"></a>CUSTOMSLIDER.downImage

L'attributo **downImage** specifica o recupera l'immagine di stato inattivo del dispositivo di scorrimento personalizzato.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Se non è specificato, verrà usato il file specificato nell'attributo **Image** .

**DownImage** rappresenta lo stato di inattività del controllo **CUSTOMSLIDER** . Può trattarsi di una singola immagine o di una serie di immagini che rappresentano i vari Stati del dispositivo di scorrimento. Se vengono usate più immagini, vengono disposte nello stesso modo del file di **immagine** .

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

 

 





