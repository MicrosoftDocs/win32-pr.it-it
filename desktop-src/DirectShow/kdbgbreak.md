---
description: Causa un'eccezione del punto di interruzione e registra la stringa specificata utilizzando la macro DbgLog. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Macro KDbgBreak (Wxdebug. h)
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
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324789"
---
# <a name="kdbgbreak-macro"></a>KDbgBreak (macro)

Causa un'eccezione del punto di interruzione e registra la stringa specificata utilizzando la macro [**DbgLog**](dbglog.md) . Ignorato nelle compilazioni al dettaglio.

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

A differenza della macro [**DbgBreak**](dbgbreak.md) , questa macro non visualizza una finestra di messaggio che richiede all'utente. Nelle compilazioni di debug, causa automaticamente un'eccezione del punto di interruzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punti di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




