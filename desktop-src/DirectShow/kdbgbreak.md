---
description: Genera un'eccezione del punto di interruzione e registra la stringa specificata usando la macro DbgLog. Ignorato nelle build di vendita al dettaglio.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Macro KDbgBreak (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 3339e69bb10876fe326f5960e6012849664fdbfcb4fe06fffd4029e6170af8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952360"
---
# <a name="kdbgbreak-macro"></a>Macro KDbgBreak

Genera un'eccezione del punto di interruzione e registra la stringa specificata usando la macro [**DbgLog.**](dbglog.md) Ignorato nelle build di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strLiteral* 
</dt> <dd>

Stringa di testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

A differenza della macro [**DbgBreak,**](dbgbreak.md) questa macro non visualizza una finestra di messaggio che richiede all'utente. Nelle compilazioni di debug viene generata automaticamente un'eccezione del punto di interruzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punto di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




