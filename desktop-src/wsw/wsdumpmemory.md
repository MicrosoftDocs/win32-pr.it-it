---
title: Funzione WsDumpMemory (WebServicesDebug. h)
description: Questa funzione consente di eseguire il dump di tutte le allocazioni di memoria alla console.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Servizi Web per la funzione WsDumpMemory per Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964694"
---
# <a name="wsdumpmemory-function"></a>WsDumpMemory (funzione)

Questa funzione consente di eseguire il dump di tutte le allocazioni di memoria alla console.

> [!Note]  
> Questa funzione è solo per il DEBUG.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*errore* \[ in, facoltativo\]
</dt> <dd>

Puntatore a un oggetto [WS \_ Error](ws-error.md) in cui è necessario archiviare informazioni aggiuntive sull'errore se la funzione ha esito negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                             |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





