---
title: BUTTON. downImage
description: L'attributo downImage specifica o recupera l'immagine che rappresenta lo stato di inattività del pulsante.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324583"
---
# <a name="buttondownimage"></a>BUTTON. downImage

L'attributo **downImage** specifica o recupera l'immagine che rappresenta lo stato di inattività del **pulsante**.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF.

L'immagine predefinita è quella specificata nell'attributo **Image** oppure il valore predefinito.

Se l'immagine inattiva è più grande dell'area definita nell'attributo di ambiente, l'immagine in giù verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**PULSANTE in basso**](button-down.md)
</dt> <dt>

[**BUTTON. image**](button-image.md)
</dt> </dl>

 

 





