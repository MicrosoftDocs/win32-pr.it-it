---
title: AmbientAttributes.verticalAlignment
description: L'attributo verticalAlignment specifica o recupera un valore che indica la posizione verticale del controllo quando l'elemento VIEW o subVIEW padre viene allungato.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- AmbientAttributes.verticalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a116a8883fe1d591f5c68050e4a5ab738a3cf913322ae7c671c71a507f2c924d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956391"
---
# <a name="ambientattributesverticalalignment"></a>AmbientAttributes.verticalAlignment

**L'attributo verticalAlignment** specifica o recupera un valore che indica la posizione verticale del controllo quando l'elemento **VIEW** o **subVIEW** padre viene allungato.

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**



| Valore   | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | Valore predefinito. Mantiene la posizione del controllo rispetto alla parte superiore dell'oggetto **VIEW** o **subVIEW** padre quando la visualizzazione viene ridimensionata.                                                                                                                                                                                                             |
| bottom  | Mantiene la posizione del controllo rispetto alla parte inferiore dell'oggetto **VIEW** o **subVIEW** padre quando la visualizzazione viene ridimensionata.                                                                                                                                                                                                                   |
| center  | Mantiene la posizione del controllo rispetto al centro verticale dell'oggetto **VIEW** o **subVIEW** padre quando la visualizzazione viene ridimensionata.                                                                                                                                                                                                          |
| adattamento | Mantiene la posizione del controllo rispetto ai margini superiore e inferiore della visualizzazione quando viene ridimensionata. Il controllo si adatta in modo da adattarsi quando **l'elemento VIEW** o **subVIEW padre** viene allungato. L'immagine effettiva non aumenta o riduce a meno che non sia ridimensionabile, ma l'area selezionabile aumenta o si riduce se non è delimitata da **un oggetto clippingImage.** |



 

## <a name="remarks"></a>Commenti

A meno che **verticalAlignment** non sia impostato su "center", il controllo mantiene la distanza originale dal bordo specificato o da entrambi i bordi se si specifica "stretch" e il controllo è ridimensionabile. Se il controllo non è ridimensionabile ed è specificato "stretch", l'area selezionabile viene estesa.

È possibile impostare qualsiasi combinazione degli **attributi horizontalAlignment** **e verticalAlignment.** Ad esempio, se vuoi che un controllo sia centrato sia orizzontalmente che verticalmente, imposta **horizontalAlignment** su "center" e **verticalAlignment** su "center".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.horizontalAlignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





