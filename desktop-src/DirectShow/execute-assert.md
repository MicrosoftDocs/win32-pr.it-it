---
description: Valuta un'espressione nelle compilazioni di debug e di vendita al dettaglio. Nelle build di debug, Visualizza un messaggio di diagnostica se l'espressione è FALSE.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: EXECUTE_ASSERT macro (Wxdebug. h)
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
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333599"
---
# <a name="execute_assert-macro"></a>Esegui la \_ macro ASSERT

Valuta un'espressione nelle compilazioni di debug e di vendita al dettaglio. Nelle build di debug, Visualizza un messaggio di diagnostica se l'espressione è **false**.

## <a name="syntax"></a>Sintassi


```C++
void EXECUTE_ASSERT(
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

A differenza della macro [**Assert**](assert.md) , questa macro valuta l'espressione nelle compilazioni al dettaglio. Nelle compilazioni di debug, se l'espressione è **false**, la macro Visualizza una finestra di messaggio con il testo dell'espressione, il nome del file di origine e il numero di riga. L'utente può ignorare l'asserzione, immettere il debugger o chiudere l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punti di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




