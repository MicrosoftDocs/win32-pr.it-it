---
title: AmbientAttributes.horizontalAlignment
description: L'attributo horizontalAlignment specifica o recupera un valore che indica la posizione orizzontale del controllo quando l'elemento VIEW o SUBVIEW padre viene ridimensionato.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- AmbientAttributes.horizontalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9daf64189735d79e1ad3eb4f7b3637ca68cfdae489cda9423bb60acdd1f9185c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055169"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes.horizontalAlignment

**L'attributo horizontalAlignment** specifica o recupera un valore che indica la posizione orizzontale del controllo quando l'elemento **VIEW** o **SUBVIEW** padre viene ridimensionato.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**



| Valore   | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sinistro    | Valore predefinito. Mantiene la posizione del controllo rispetto alla sinistra della vista **o** della visualizzazione **secondaria** padre quando la visualizzazione viene ridimensionata.                                                                                                                                                                                                                               |
| right   | Mantiene la posizione del controllo rispetto a destra della vista **o** della visualizzazione **secondaria** padre quando la visualizzazione viene ridimensionata.                                                                                                                                                                                                                                       |
| center  | Mantiene la posizione del controllo rispetto al centro orizzontale dell'oggetto **VIEW** o **subVIEW** padre quando la visualizzazione viene ridimensionata.                                                                                                                                                                                                                           |
| adattamento | Mantiene la posizione del controllo rispetto ai margini sinistro e destro dell'oggetto **VIEW** o **subVIEW** padre quando viene ridimensionato. Il controllo si adatta in modo da adattarsi quando **l'oggetto VIEW** **o SUBVIEW** viene allungato. L'immagine effettiva non aumenta o riduce a meno che non sia ridimensionabile, ma l'area selezionabile aumenta o si riduce se non è delimitata da **un oggetto clippingImage.** |



 

## <a name="remarks"></a>Commenti

A meno che **horizontalAlignment** non sia impostato su "center", il controllo mantiene la distanza originale dal bordo specificato o da entrambi i bordi se si specifica "stretch" e il controllo è ridimensionabile. Se il controllo non è ridimensionabile ed è specificato "stretch", l'area selezionabile viene estesa.

È possibile impostare qualsiasi combinazione **di horizontalAlignment** **e verticalAlignment.** Ad esempio, se vuoi centrare un controllo sia orizzontalmente che verticalmente, imposta horizontalAlignment="center" verticalAlignment="center".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





