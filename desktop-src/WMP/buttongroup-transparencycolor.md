---
title: BUTTONGROUP.transparencyColor
description: L'attributo transparencyColor specifica o recupera il colore trasparente delle immagini BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- PROPRIETÀ BUTTONGROUP.transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf97a25081e3f5c5729721bd675d9c59be1a4d52adc86acf6b9b75a0ee86dbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342664"
---
# <a name="buttongrouptransparencycolor"></a>BUTTONGROUP.transparencyColor

**L'attributo transparencyColor** specifica o recupera il colore trasparente delle **immagini BUTTONGROUP.**

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa **di** lettura/scrittura senza alcun valore predefinito, contenente uno dei valori seguenti.



| Valore                                       | Descrizione                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Auto                                        | Il pixel nella posizione 0,0 nell'immagine diventa il colore trasparente.                              |
| qualsiasi valore di colore Internet Explorer Microsoft | Un Internet Explorer colore diventa il colore trasparente(ad esempio, "red" o \# "FF0000"). |
| Nessuno                                        | Valore predefinito. Nessuna trasparenza.                                                                          |



 

## <a name="remarks"></a>Commenti

Un colore trasparente in un'immagine consentirà a tutto ciò che si trova dietro l'immagine di visualizzare attraverso le aree di trasparenza. L'area trasparente è selezionabile a meno che non venga ritagliata dal tag **clippingImage.**

Il colore può essere qualsiasi valore di Internet Explorer Microsoft. Se il valore è Auto, viene usato il colore del pixel nella posizione 0,0 nell'immagine.

Se il colore specificato non è uno dei colori Internet Explorer, viene restituito un avviso e viene mantenuto il valore precedente.

Poiché i file JPG sono persi e pertanto soggetti a modifiche di colore impreviste, non sono consigliati quando si usa **transparencyColor.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**Informazioni di riferimento sul colore**](color-reference.md)
</dt> </dl>

 

 





