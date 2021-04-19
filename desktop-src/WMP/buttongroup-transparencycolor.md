---
title: BUTTONGROUP. transparencyColor
description: L'attributo transparencyColor specifica o Recupera il colore trasparente delle immagini BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- Media Player Windows BUTTONGROUP. transparencyColor
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326479"
---
# <a name="buttongrouptransparencycolor"></a>BUTTONGROUP. transparencyColor

L'attributo **transparencyColor** specifica o Recupera il colore trasparente delle immagini **ButtonGroup** .

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura e non prevede alcun valore predefinito, contenente uno dei valori seguenti.



| Valore                                       | Descrizione                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Auto                                        | Il pixel nella posizione 0, 0 nell'immagine diventa il colore trasparente.                              |
| qualsiasi valore di colore di Microsoft Internet Explorer | Un valore di colore di Internet Explorer diventa il colore trasparente (ad esempio, "Red" o " \# FF0000"). |
| nessuno                                        | Valore predefinito. Nessuna trasparenza.                                                                          |



 

## <a name="remarks"></a>Commenti

Un colore trasparente in un'immagine consentirà tutto ciò che si trova dietro l'immagine per visualizzare le aree di trasparenza. L'area trasparente è selezionabile a meno che non venga troncata dal tag **clippingImage** .

Il colore può essere qualsiasi valore di colore di Microsoft Internet Explorer. Se il valore è auto, viene usato il colore del pixel nella posizione 0, 0 nell'immagine.

Se il colore specificato non è uno dei colori di Internet Explorer validi, viene restituito un avviso e viene mantenuto il valore precedente.

Poiché i jpg sono con perdita di tempo e pertanto sono soggetti a variazioni di colore impreviste, non sono consigliate quando si usa **transparencyColor** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**Riferimento ai colori**](color-reference.md)
</dt> </dl>

 

 





