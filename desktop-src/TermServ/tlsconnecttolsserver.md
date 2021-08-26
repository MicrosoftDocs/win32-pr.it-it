---
title: Funzione TLSConnectToLsServer
description: Apre un handle per il server licenze Desktop remoto specificato.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Funzione TLSConnectToLsServer Servizi Desktop remoto
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
ms.openlocfilehash: dbfc3c1e365a97b8199df34c2e55a8362f48b7f6a2a43e524e3c6e937de5cb0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986971"
---
# <a name="tlsconnecttolsserver-function"></a>Funzione TLSConnectToLsServer

Apre un handle per il server licenze Desktop remoto specificato.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszLsServer* \[ Pollici\]
</dt> <dd>

Puntatore a **una stringa** con terminazione Null che specifica il nome NetBIOS del server Desktop remoto licenze. Se il valore di questo parametro è **NULL,** il server specificato è il computer locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il server specificato.

Se la funzione ha esito negativo, il valore restituito è **NULL.** Per ottenere informazioni estese sull'errore, chiamare [**la funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Commenti

Dopo aver terminato di usare l'handle restituito dalla funzione **TLSConnectToLsServer,** rilasciarlo chiamando la [**funzione TLSDisconnectFromServer.**](tlsdisconnectfromserver.md)

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

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

