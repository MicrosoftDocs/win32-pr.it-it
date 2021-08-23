---
title: Evasore.disabledImage
description: L'attributo disabledImage specifica o recupera l'immagine del dispositivo di scorrimento usato quando il dispositivo di scorrimento è disabilitato.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- WINDOWS MEDIA PLAYER
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d75e26204fc362dfa714bc8720d6db87e511bbfda03096d60f58f91c3335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651561"
---
# <a name="customsliderdisabledimage"></a>Evasore.disabledImage

**L'attributo disabledImage** specifica o recupera l'immagine del dispositivo di scorrimento usato quando il dispositivo di scorrimento è disabilitato.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Se non viene specificato, verrà usato il file specificato **nell'attributo** image.

**disabledImage rappresenta** lo stato disabilitato del **controllo ELIDER.** Può trattarsi di una singola immagine o di una serie di immagini che rappresentano i vari stati del dispositivo di scorrimento. Se vengono usate più immagini, vengono disposte nello stesso modo del file **di** immagine.

I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (senza GIF animate).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento INSODELIDER**](customslider-element.md)
</dt> <dt>

[**ESEREZIONERI.immagine**](customslider-image.md)
</dt> </dl>

 

 





