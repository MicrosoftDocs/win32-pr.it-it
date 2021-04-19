---
title: CUSTOMSLIDER. image
description: L'attributo Image specifica o Recupera il nome del file contenente le immagini corrispondenti ai vari Stati del dispositivo di scorrimento personalizzato.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Media Player Windows CUSTOMSLIDER. image
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323910"
---
# <a name="customsliderimage"></a>CUSTOMSLIDER. image

L'attributo **Image** specifica o Recupera il nome del file contenente le immagini corrispondenti ai vari Stati del dispositivo di scorrimento personalizzato.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

L'attributo **Image** è obbligatorio. Specifica un file di immagine costituito da una o più immagini secondarie, disposte orizzontalmente o verticalmente, che rappresentano i vari Stati del dispositivo di scorrimento personalizzato. Ogni immagine secondaria deve avere le stesse dimensioni di **dimensione positionImage** o il dispositivo di scorrimento personalizzato non funzionerà correttamente. L'altezza o la larghezza dell'immagine complessiva deve quindi essere un multiplo pari dell'altezza o della larghezza del **dimensione positionImage**.

I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di un'immagine del dispositivo di scorrimento personalizzata. Il **dimensione positionImage** corrispondente viene visualizzato nella sezione esempio della proprietà **dimensione positionImage** .

![immagine customslider di esempio](images/dial.png)

L'attributo **dimensione positionImage** contiene anche un esempio di codice che illustra come vengono usati gli attributi dell'elemento **CUSTOMSLIDER** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. dimensione positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





