---
title: TLSConnectToLsServer (funzione)
description: Apre un handle per il server licenze Desktop remoto specificato.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSConnectToLsServer
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400727"
---
# <a name="tlsconnecttolsserver-function"></a>TLSConnectToLsServer (funzione)

Apre un handle per il server licenze Desktop remoto specificato.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszLsServer* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione **null** che specifica il nome NetBIOS del server licenze Desktop remoto. Se il valore di questo parametro è **null**, il server specificato è il computer locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il server specificato.

Se la funzione ha esito negativo, il valore restituito è **null**. Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Commenti

Al termine dell'utilizzo dell'handle restituito dalla funzione **TLSConnectToLsServer** , rilasciarlo chiamando la funzione [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) .

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

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

