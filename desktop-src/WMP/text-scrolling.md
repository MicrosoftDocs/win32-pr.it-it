---
title: TESTO. scorrimento
description: L'attributo di scorrimento specifica o recupera un valore che indica se lo scorrimento del testo viene eseguito.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- TESTO. scorrimento di Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328589"
---
# <a name="textscrolling"></a>TESTO. scorrimento

L'attributo di **scorrimento** specifica o recupera un valore che indica se lo scorrimento del testo viene eseguito.

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                     |
|-------|---------------------------------|
| true  | Lo scorrimento è abilitato.           |
| false | Valore predefinito. Lo scorrimento è disabilitato. |



 

## <a name="remarks"></a>Commenti

La funzionalità di scorrimento fornisce un buffer di due spazi tra la fine del testo e l'inizio della riga ripetuta.

L'attributo **giustificazione** specifica il punto in cui il testo viene visualizzato prima dell'inizio dello scorrimento.

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. giustificazione**](text-justification.md)
</dt> <dt>

[**TESTO. scrollingAmount**](text-scrollingamount.md)
</dt> <dt>

[**TESTO. scrollingDelay**](text-scrollingdelay.md)
</dt> <dt>

[**TESTO. scrollingDirection**](text-scrollingdirection.md)
</dt> </dl>

 

 





