---
title: TLSDisconnectFromServer (funzione)
description: Chiude un handle aperto per un server licenze Desktop remoto.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSDisconnectFromServer
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302594"
---
# <a name="tlsdisconnectfromserver-function"></a>TLSDisconnectFromServer (funzione)

Chiude un handle aperto per un server licenze Desktop remoto.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hHandle* \[ in\]
</dt> <dd>

Handle per un server licenze Desktop remoto aperto da una chiamata alla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Chiamare la funzione **TLSDisconnectFromServer** come parte della routine di pulizia del programma per chiudere tutti gli handle del server aperti dalle chiamate alla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_handle TLS**](tls-handle.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

