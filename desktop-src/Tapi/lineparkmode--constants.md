---
description: Le costanti del flag di bit LINEPARKMODE \_ descrivono diversi modi di chiamate di parcheggio.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: LINEPARKMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3070ad3f9e56de5e4e1a026b5f779c59469e947ff55b530e9d5b414a1b3b53b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140004"
---
# <a name="lineparkmode_-constants"></a>Costanti \_ LINEPARKMODE

Le costanti del flag di bit **LINEPARKMODE \_** descrivono diversi modi di chiamate di parcheggio.

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ DIRETTO**
</dt> <dd> <dl> <dt>



Specifica il parcheggio di chiamate diretto. L'indirizzo in cui deve essere parcheggiata la chiamata deve essere fornito all'interruttore.


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE \_ NON INDIRETTO**
</dt> <dd> <dl> <dt>



Specifica il parcheggio di chiamate non indirette. L'indirizzo in cui è stata parcheggiata la chiamata viene selezionato dall'opzione e fornito dal passaggio all'applicazione.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Le **costanti LINEPARKMODE \_ vengono usate** durante il parcheggio di una chiamata. Consultare le funzionalità del dispositivo indirizzo di una riga per scoprire quale modalità di parcheggio è disponibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




