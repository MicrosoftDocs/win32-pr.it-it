---
description: Valuta un'espressione e genera un'eccezione del punto di interruzione se l'espressione è FALSE. Il testo dell'espressione, il nome del file di origine e il numero di riga vengono registrati utilizzando la macro DbgLog. Ignorato nelle compilazioni al dettaglio.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro KASSERT (Wxdebug. h)
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
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333429"
---
# <a name="kassert-macro"></a>KASSERT (macro)

Valuta un'espressione e genera un'eccezione del punto di interruzione se l'espressione è **false**. Il testo dell'espressione, il nome del file di origine e il numero di riga vengono registrati utilizzando la macro [**DbgLog**](dbglog.md) . Ignorato nelle compilazioni al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cond* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Diversamente dalle macro [**Assert**](assert.md) ed [**Execute \_ Assert**](execute-assert.md) , questa macro non visualizza una finestra di messaggio che richiede all'utente. Nelle compilazioni di debug, se l'espressione è **false**, la macro causa automaticamente un'eccezione del punto di interruzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punti di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




