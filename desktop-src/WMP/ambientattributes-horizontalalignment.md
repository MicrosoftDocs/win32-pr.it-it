---
title: AmbientAttributes. horizontalAlignment
description: L'attributo horizontalAlignment specifica o recupera un valore che indica la posizione orizzontale del controllo quando la visualizzazione o la Sottovisualizzazione padre viene ridimensionata.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Media Player di Windows AmbientAttributes. horizontalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324752"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes. horizontalAlignment

L'attributo **HorizontalAlignment** specifica o recupera un valore che indica la posizione orizzontale del controllo quando la **visualizzazione** o la **Sottovisualizzazione** padre viene ridimensionata.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.



| Valore   | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sinistro    | Valore predefinito. Mantiene la posizione del controllo rispetto a sinistra della **visualizzazione** o della **Sottovisualizzazione** padre quando la vista viene ridimensionata.                                                                                                                                                                                                                               |
| right   | Mantiene la posizione del controllo rispetto a destra della visualizzazione o della **Sottovisualizzazione** padre quando **la vista viene** ridimensionata.                                                                                                                                                                                                                                       |
| center  | Mantiene la posizione del controllo in relazione al centro orizzontale della **vista** o della **Sottovisualizzazione** padre quando la visualizzazione viene ridimensionata.                                                                                                                                                                                                                           |
| adattamento | Mantiene il posizionamento del controllo in relazione ai margini sinistro e destro della **vista** o della **Sottovisualizzazione** padre quando viene ridimensionato. Il controllo si adatta al momento in cui la **visualizzazione** o la **Sottovisualizzazione** è allungata. L'immagine effettiva non aumenta o diminuisce a meno che non sia ridimensionabile, ma l'area selezionabile aumenta o diminuisce se non è vincolata da un **clippingImage**. |



 

## <a name="remarks"></a>Commenti

A meno che **HorizontalAlignment** non sia impostato su "Center", il controllo mantiene la distanza originale dal bordo specificato oppure da entrambi i bordi se si specifica "Stretch" e il controllo è ridimensionabile. Se il controllo non è ridimensionabile e si specifica "Stretch", viene invece estesa l'area selezionabile.

È possibile impostare qualsiasi combinazione di **HorizontalAlignment** e **VerticalAlignment**. Ad esempio, se si desidera centrare un controllo sia orizzontalmente che verticalmente, impostare horizontalAlignment = "Center" verticalAlignment = "Center".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





