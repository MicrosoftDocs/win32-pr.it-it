---
title: Funzione WsSetAutoFail (WebServicesDebug.h)
description: Imposta il punto successivo per inserire un errore. Si tratta di una funzione DEBUG ONLY.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Servizi Web della funzione WsSetAutoFail per Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae3ed731edce429aac78700d52d0e7504a5688d1bf35bbb9c64a5d34bc0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838541"
---
# <a name="wssetautofail-function"></a>Funzione WsSetAutoFail

Imposta il punto successivo per inserire un errore. Si tratta di una funzione DEBUG ONLY.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*count* \[ Pollici\]
</dt> <dd>

Specifica il numero di operazioni prima che inizino a verificarsi errori.

</dd> <dt>

*errore* \[ in, facoltativo\]
</dt> <dd>

Puntatore a un [oggetto WS \_ ERROR](ws-error.md) in cui devono essere archiviate informazioni aggiuntive sull'errore se la funzione non riesce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>WebServicesDebug.h</dt> </dl> |



 

 





