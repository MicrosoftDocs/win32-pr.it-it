---
title: AmbientAttributes. verticalAlignment
description: L'attributo verticalAlignment specifica o recupera un valore che indica la posizione verticale del controllo quando la visualizzazione o la Sottovisualizzazione padre è allungata.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Media Player Windows AmbientAttributes. verticalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332142"
---
# <a name="ambientattributesverticalalignment"></a>AmbientAttributes. verticalAlignment

L'attributo **VerticalAlignment** specifica o recupera un valore che indica la posizione verticale del controllo quando la **visualizzazione** o la **Sottovisualizzazione** padre è allungata.

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.



| Valore   | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | Valore predefinito. Mantiene la posizione del controllo rispetto alla parte superiore della **visualizzazione** o della **Sottovisualizzazione** padre quando la vista viene ridimensionata.                                                                                                                                                                                                             |
| bottom  | Mantiene la posizione del controllo rispetto alla parte inferiore della **visualizzazione** o della **Sottovisualizzazione** padre quando la vista viene ridimensionata.                                                                                                                                                                                                                   |
| center  | Mantiene il posizionamento del controllo in relazione al centro verticale della **visualizzazione** o della **Sottovisualizzazione** padre quando la visualizzazione viene ridimensionata.                                                                                                                                                                                                          |
| adattamento | Mantiene la posizione del controllo rispetto ai margini superiore e inferiore della visualizzazione quando viene ridimensionato. Il controllo si adatta al momento in cui la **visualizzazione** o la **Sottovisualizzazione** padre è allungata. L'immagine effettiva non aumenta o diminuisce a meno che non sia ridimensionabile, ma l'area selezionabile aumenta o diminuisce se non è vincolata da un **clippingImage**. |



 

## <a name="remarks"></a>Commenti

A meno che **VerticalAlignment** non sia impostato su "Center", il controllo mantiene la distanza originale dal bordo specificato oppure da entrambi i bordi se viene specificato "Stretch" e il controllo è ridimensionabile. Se il controllo non è ridimensionabile e si specifica "Stretch", viene invece estesa l'area selezionabile.

È possibile impostare qualsiasi combinazione degli attributi **HorizontalAlignment** e **VerticalAlignment** . Se ad esempio si desidera che un controllo sia centrato orizzontalmente e verticalmente, impostare **HorizontalAlignment** su "Center" e **VerticalAlignment** su "Center".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. horizontalAlignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





