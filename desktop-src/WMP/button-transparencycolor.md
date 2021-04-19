---
title: BUTTON. transparencyColor
description: L'attributo transparencyColor specifica o Recupera il colore che sarà trasparente nelle immagini dei pulsanti.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332687"
---
# <a name="buttontransparencycolor"></a>BUTTON. transparencyColor

L'attributo **transparencyColor** specifica o Recupera il colore che sarà trasparente nelle immagini dei **pulsanti** .

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura e non prevede alcun valore predefinito contenente uno dei valori seguenti.



| Valore                                    | Descrizione                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Auto                                     | Il colore del pixel nella posizione 0, 0 nell'immagine diventa il colore trasparente.                        |
| Qualsiasi valore del formato di colore di Internet Explorer | Un valore in formato colore di Internet Explorer diventa il colore trasparente (ad esempio, "rosso" o " \# FF0000"). |
| nessuno                                     | Nessuna trasparenza.                                                                                          |



 

## <a name="remarks"></a>Commenti

Un colore trasparente in un'immagine consente la visualizzazione di qualsiasi oggetto dietro l'immagine attraverso le aree trasparenti. Il **pulsante** riceverà comunque i clic sull'area trasparente.

Il colore trasparente può essere qualsiasi valore di colore di Internet Explorer. Se il valore dell'attributo **transparencyColor** è impostato su "auto", viene usato il colore del pixel nella posizione 0, 0 nell'immagine.

Se il colore specificato non è uno dei colori di IE validi, viene mantenuto il valore precedente.

Poiché i jpg sono con perdita di tempo e pertanto sono soggetti a variazioni di colore impreviste, non sono consigliate quando si usa **transparencyColor** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON. image**](button-image.md)
</dt> <dt>

[**Riferimento ai colori**](color-reference.md)
</dt> </dl>

 

 





