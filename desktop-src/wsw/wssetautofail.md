---
title: Funzione WsSetAutoFail (WebServicesDebug. h)
description: Imposta il punto successivo in cui inserire un errore. Si tratta di una funzione di solo DEBUG.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Servizi Web per la funzione WsSetAutoFail per Windows
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
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518538"
---
# <a name="wssetautofail-function"></a>WsSetAutoFail (funzione)

Imposta il punto successivo in cui inserire un errore. Si tratta di una funzione di solo DEBUG.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ di in\]
</dt> <dd>

Specifica il numero di operazioni prima che inizino a verificarsi degli errori.

</dd> <dt>

*errore* \[ in, facoltativo\]
</dt> <dd>

Puntatore a un oggetto [WS \_ Error](ws-error.md) in cui è necessario archiviare informazioni aggiuntive sull'errore se la funzione ha esito negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





