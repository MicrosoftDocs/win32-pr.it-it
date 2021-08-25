---
title: Funzione TLSKeyPackEnumNext
description: Continua da una chiamata precedente alla funzione TLSKeyPackEnumBegin e restituisce il key pack successivo installato in un server licenze Desktop remoto che corrisponde ai criteri di ricerca.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- Funzione TLSKeyPackEnumNext Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352d94204e4c590668018546f0d6304d4faa3836bcc7289b675b05b1ae2b825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869261"
---
# <a name="tlskeypackenumnext-function"></a>Funzione TLSKeyPackEnumNext

Continua da una chiamata precedente alla funzione [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e restituisce il key pack successivo installato in un server licenze Desktop remoto che corrisponde ai criteri di ricerca.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hHandle* \[ Pollici\]
</dt> <dd>

Handle a un Desktop remoto licenze. Specificare un handle aperto dalla funzione [**TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> <dt>

*lpKeyPack* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura LSKeyPack**](lskeypack.md) che riceve il key pack successivo che corrisponde ai criteri di ricerca.

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

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ I \_ NO \_ MORE \_ DATA** (4001)


</dt> <dd>

Nessun altro Key Pack corrisponde ai criteri di ricerca.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ ERRORE \_ INTERNO** (5001)


</dt> <dd>

Errore interno nel server licenze.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ SEQUENZA \_ NON VALIDA** (5006)


</dt> <dd>

Sequenza chiamante non valida. È necessario chiamare la [**funzione TLSKeyPackEnumBegin()**](tlskeypackenumbegin.md) prima di questo.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ SERVER \_ OCCUPATO** (5007)


</dt> <dd>

Il server licenze è troppo occupato per elaborare la richiesta.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

Impossibile elaborare la richiesta a causa di memoria insufficiente.

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

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

