---
title: BUTTON. hoverImage
description: L'attributo hoverImage specifica o recupera l'immagine visualizzata quando il pulsante si trova nello stato up e l'utente posiziona il puntatore del mouse su di esso con il puntatore del mouse.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325449"
---
# <a name="buttonhoverimage"></a>BUTTON. hoverImage

L'attributo **hoverImage** specifica o recupera l'immagine visualizzata quando il **pulsante** si trova nello stato up e l'utente posiziona il puntatore del mouse su di esso con il puntatore del mouse.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF.

L'immagine predefinita è quella specificata nell'attributo **Image** oppure il valore predefinito.

Se l'immagine del passaggio del mouse è maggiore dell'area definita nell'attributo di ambiente, l'immagine del passaggio del mouse verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON. image**](button-image.md)
</dt> </dl>

 

 





