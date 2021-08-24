---
title: Funzione TLSKeyPackEnumBegin
description: Inizia l'enumerazione tramite tutti i Key Pack installati in un server licenze Desktop remoto in base ai criteri di ricerca.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- Funzione TLSKeyPackEnumBegin Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469e4e255f3bdd64749060fcb712df480a8a1f6fc3683ebb25916be44856e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869331"
---
# <a name="tlskeypackenumbegin-function"></a>Funzione TLSKeyPackEnumBegin

Inizia l'enumerazione tramite tutti i Key Pack installati in un server licenze Desktop remoto in base ai criteri di ricerca.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hHandle* \[ Pollici\]
</dt> <dd>

Handle a un server Desktop remoto licenze. Specificare un handle aperto dalla [**funzione TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> <dt>

*dwSearchParm* \[ Pollici\]
</dt> <dd>

Specifica i criteri di ricerca. Questo parametro è riservato per un uso futuro e deve contenere 0xFFFFFFFF.

</dd> <dt>

*bMatchAll* \[ Pollici\]
</dt> <dd>

Specifica se trovare la corrispondenza con tutti i valori di ricerca.

</dd> <dt>

*lpSearchParm* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura LSKeyPack**](lskeypack.md) che specifica i parametri di ricerca da cercare.

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

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ ERRORE \_ INTERNO** (5001)


</dt> <dd>

Errore interno nel server licenze.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ SEQUENZA \_ NON VALIDA** (5006)


</dt> <dd>

La sequenza chiamante non è valida. Molto probabilmente, un'enumerazione precedente non è terminata.

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

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ DATI \_ NON VALIDI** (5009)


</dt> <dd>

I dati nel parametro di ricerca non sono validi.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce i valori restituiti possibili seguenti.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

La chiamata è riuscita. Controllare il valore del *parametro pdwErrCode* per ottenere il codice restituito per la chiamata.

</dd> <dt>

**RPC \_ S NON VALIDO \_ \_ ARG**
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

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

