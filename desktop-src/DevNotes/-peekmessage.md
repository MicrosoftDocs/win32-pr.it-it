---
description: Invia messaggi in ingresso inviati, controlla la coda di messaggi del thread per un messaggio inviato e recupera il messaggio (se presente).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: Funzione _PeekMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325678"
---
# <a name="_peekmessage-function"></a>\_PeekMessage (funzione)

\[Questa funzione è un wrapper per la funzione **PeekMessage** . Questa funzione può essere modificata o non disponibile in futuro. Le applicazioni devono chiamare direttamente **PeekMessage** .\]

Invia messaggi in ingresso inviati, controlla la coda di messaggi del thread per un messaggio inviato e recupera il messaggio (se presente). Vedere [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).

## <a name="syntax"></a>Sintassi


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
