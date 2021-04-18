---
title: TLSGetServerCertificate (funzione)
description: Restituisce il certificato del server licenze Desktop remoto.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSGetServerCertificate
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301292"
---
# <a name="tlsgetservercertificate-function"></a>TLSGetServerCertificate (funzione)

Restituisce il certificato del server licenze Desktop remoto.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hHandle* \[ in\]
</dt> <dd>

Handle per un server licenze Desktop remoto aperto da una chiamata alla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*bSignCert* \[ in\]
</dt> <dd>

**True** se il certificato di firma, **false** se il certificato di Exchange.

</dd> <dt>

*ppbCertBlob* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un puntatore a un buffer che contiene il certificato.

</dd> <dt>

*lpdwCertBlobLen* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni del certificato restituito.

</dd> <dt>

*pdwErrCode* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il codice di errore.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ \_Operazione riuscita** (0)


</dt> <dd>

La chiamata è riuscita.

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ \_ \_ Certificato SELFSIGN W** (4007)


</dt> <dd>

Il certificato restituito è un certificato autofirmato.

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ W \_ temp \_ SELFSIGN \_ CERT** (4009)


</dt> <dd>

Il certificato restituito è temporaneo.

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ E \_ accesso \_ negato** (5003)


</dt> <dd>

Accesso negato.

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ E \_ alloca \_ HANDLE** (5007)


</dt> <dd>

Il server è troppo occupato per elaborare la richiesta.

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ nessun \_ certificato** (5022)


</dt> <dd>

Impossibile recuperare un certificato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce i valori restituiti possibili seguenti.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

La chiamata è riuscita. Controllare il valore del parametro *pdwErrCode* per ottenere il codice restituito per la chiamata.

</dd> <dt>

**\_ \_ arg non valido \_**
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

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

