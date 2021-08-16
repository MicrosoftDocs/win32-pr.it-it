---
title: MMIOM_CLOSE messaggio (Mmsystem.h)
description: Il messaggio MMIOM CLOSE viene inviato a una procedura di I/O dalla funzione mmioClose per richiedere la \_ chiusura di un file.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE di messaggi Windows multimediali
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a26b8b2ffa80c7c522fa5cdcbfc5da3334e0d2b5e258e090932147bf85438c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065391"
---
# <a name="mmiom_close-message"></a>Messaggio MMIOM \_ CLOSE

Il **messaggio MMIOM \_ CLOSE** viene inviato a una procedura di I/O dalla funzione [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) per richiedere la chiusura di un file.


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*
</dt> <dd>

Flag contenuti nel **parametro wFlags** di **mmioClose.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se il file viene chiuso correttamente o se in caso contrario si verifica un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



 

