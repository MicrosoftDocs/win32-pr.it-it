---
description: Valuta un'espressione e genera un'eccezione del punto di interruzione se l'espressione è FALSE. Il testo dell'espressione, il nome del file di origine e il numero di riga vengono registrati usando la macro DbgLog. Ignorato nelle build per la vendita al dettaglio.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro KASSERT (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: a1eb6738ea3e9d4535bf9f8291dc71349d67bb51d143b6bc73e83290f36657cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817058"
---
# <a name="kassert-macro"></a>Macro KASSERT

Valuta un'espressione e genera un'eccezione del punto di interruzione se l'espressione è **FALSE.** Il testo dell'espressione, il nome del file di origine e il numero di riga vengono registrati usando la macro [**DbgLog.**](dbglog.md) Ignorato nelle build per la vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cond* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

A differenza [**delle**](assert.md) macro ASSERT [**ed EXECUTE \_ ASSERT,**](execute-assert.md) questa macro non visualizza una finestra di messaggio in cui viene richiesto all'utente. Nelle compilazioni di debug, se l'espressione è **FALSE,** la macro genera automaticamente un'eccezione del punto di interruzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e di punto di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




