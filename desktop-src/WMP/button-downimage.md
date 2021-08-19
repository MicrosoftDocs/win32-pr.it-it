---
title: BUTTON.downImage
description: L'attributo downImage specifica o recupera l'immagine che rappresenta lo stato verso il basso di BUTTON.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- Button.downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff24c568ae607b5b67d766f28eb7c221844f1434a959952628cc2ad5a5d6d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123741"
---
# <a name="buttondownimage"></a>BUTTON.downImage

**L'attributo downImage** specifica o recupera l'immagine che rappresenta lo stato down dell'elemento **BUTTON.**

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura contenente** il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF.

L'immagine predefinita è quella specificata **nell'attributo image** o il relativo valore predefinito.

Se l'immagine verso il basso è più grande dell'area definita nell'attributo di ambiente, l'immagine verso il basso verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita (l'immagine rossa-x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.down**](button-down.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 





