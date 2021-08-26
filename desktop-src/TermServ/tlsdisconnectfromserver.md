---
title: Funzione TLSDisconnectFromServer
description: Chiude un handle aperto per un server Desktop remoto licenze.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Funzione TLSDisconnectFromServer Servizi Desktop remoto
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
ms.openlocfilehash: 95911536eda4bd87e45fd034626cf83d88f4d9fc768e4837316ee93abfe3c3d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869411"
---
# <a name="tlsdisconnectfromserver-function"></a>Funzione TLSDisconnectFromServer

Chiude un handle aperto per un server Desktop remoto licenze.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hHandle* \[ Pollici\]
</dt> <dd>

Handle a un Desktop remoto licenze aperto da una chiamata alla [**funzione TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Chiamare la **funzione TLSDisconnectFromServer** come parte della routine di pulizia del programma per chiudere tutti gli handle del server aperti dalle chiamate alla [**funzione TLSConnectToLsServer.**](tlsconnecttolsserver.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TLS \_ HANDLE**](tls-handle.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

