---
title: CUSTOMSLIDER.image
description: L'attributo image specifica o recupera il nome del file contenente le immagini corrispondenti ai vari stati del dispositivo di scorrimento personalizzato.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- CUSTOMSLIDER.image Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b169bbdcac0e251a161c8e09f352caf460280b23e0198167a641721caa6c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936250"
---
# <a name="customsliderimage"></a>CUSTOMSLIDER.image

**L'attributo** image specifica o recupera il nome del file contenente le immagini corrispondenti ai vari stati del dispositivo di scorrimento personalizzato.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

**L'attributo image** è obbligatorio. Specifica un file di immagine costituito da una o più immagini secondarie, disposte orizzontalmente o verticalmente, che rappresentano i vari stati del dispositivo di scorrimento personalizzato. Ogni immagine secondaria deve avere le stesse dimensioni di **positionImage** oppure il dispositivo di scorrimento personalizzato non funzionerà correttamente. L'altezza o la larghezza dell'immagine complessiva deve quindi essere un multiplo pari dell'altezza o della larghezza **dell'oggetto positionImage.**

I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (senza includere GIF animate).

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di un'immagine del dispositivo di scorrimento personalizzata. **L'immagine positionImage** corrispondente è illustrata nella sezione di esempio della **proprietà positionImage.**

![immagine dogana di esempio](images/dial.png)

**L'attributo positionImage** contiene anche un esempio di codice che illustra come vengono usati gli attributi dell'elemento **CUSTOMSLIDER.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





