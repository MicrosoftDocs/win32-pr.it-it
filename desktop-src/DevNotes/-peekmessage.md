---
description: Invia i messaggi inviati in ingresso, verifica la presenza di un messaggio inviato nella coda dei messaggi del thread e recupera il messaggio (se presente).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage funzione
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
ms.openlocfilehash: 2a2fbfcf1903fcafba77227a6b2b9f51b9c6a45ef2e8a20f7482db1f3ec2a7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538891"
---
# <a name="_peekmessage-function"></a>\_Funzione PeekMessage

\[Questa funzione è un wrapper sulla **funzione PeekMessage.** Questa funzione potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono **chiamare direttamente PeekMessage.**\]

Invia i messaggi inviati in ingresso, verifica la presenza di un messaggio inviato nella coda dei messaggi del thread e recupera il messaggio (se presente). Vedere [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).

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

 

 
