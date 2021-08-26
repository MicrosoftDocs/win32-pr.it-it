---
title: Funzione TLSLicenseEnumEnd
description: Continua da una chiamata precedente alla funzione TLSLicenseEnumBegin e termina l'enumerazione.
ms.assetid: b9cba03c-0f5a-41e8-ae13-bcdd0ac6dd99
ms.tgt_platform: multiple
keywords:
- Funzione TLSLicenseEnumEnd Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TLSLicenseEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0518b9c27b01484b7fb92dd254ae6f1ccdf01d36ef602541209b9f38abd205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869211"
---
# <a name="tlslicenseenumend-function"></a>Funzione TLSLicenseEnumEnd

Continua da una chiamata precedente alla [**funzione TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e termina l'enumerazione.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hHandle* \[ Pollici\]
</dt> <dd>

Handle a un Desktop remoto licenze. Specificare un handle aperto dalla funzione [**TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> <dt>

*pdwErrCode* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve uno dei codici di errore seguenti al ritorno.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ SUCCESS** (0)


</dt> <dd>

La chiamata ha esito positivo.

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_ E \_ HANDLE \_ NON VALIDO** (5005)


</dt> <dd>

L'handle non è valido.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce i valori restituiti possibili seguenti.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

La chiamata ha avuto esito positivo. Controllare il valore del *parametro pdwErrCode* per ottenere il codice restituito per la chiamata.

</dd> <dt>

**RPC \_ S NON VALIDA \_ \_ ARG**
</dt> <dd>

L'argomento non è valido.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> </dl>

 

