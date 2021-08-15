---
description: Valuta un'espressione nelle build di debug e di vendita al dettaglio. Nelle build di debug visualizza un messaggio di diagnostica se l'espressione è FALSE.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: EXECUTE_ASSERT macro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 871a8e4a04ec1dc31f3240b539a943c9c1733f083166fa4b7e6f6b52d14a466c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401794"
---
# <a name="execute_assert-macro"></a>\_Execute ASSERT - macro

Valuta un'espressione nelle build di debug e di vendita al dettaglio. Nelle build di debug visualizza un messaggio di diagnostica se l'espressione è **FALSE.**

## <a name="syntax"></a>Sintassi


```C++
void EXECUTE_ASSERT(
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

A differenza della macro [**ASSERT,**](assert.md) questa macro valuta l'espressione nelle build per la vendita al dettaglio. Nelle build di debug, se l'espressione è **FALSE,** la macro visualizza una finestra di messaggio con il testo dell'espressione, il nome del file di origine e il numero di riga. L'utente può ignorare l'asserzione, accedere al debugger o uscire dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e di punto di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




