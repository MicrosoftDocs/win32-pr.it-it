---
title: TLSKeyPackEnumBegin (funzione)
description: Inizia l'enumerazione tramite tutti i Key Pack installati in un server licenze Desktop remoto in base ai criteri di ricerca.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSKeyPackEnumBegin
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
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341253"
---
# <a name="tlskeypackenumbegin-function"></a>TLSKeyPackEnumBegin (funzione)

Inizia l'enumerazione tramite tutti i Key Pack installati in un server licenze Desktop remoto in base ai criteri di ricerca.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.

 

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

*hHandle* \[ in\]
</dt> <dd>

Handle per un server licenze Desktop remoto. Specificare un handle aperto dalla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*dwSearchParm* \[ in\]
</dt> <dd>

Specifica i criteri di ricerca. Questo parametro è riservato per utilizzi futuri e deve contenere 0xFFFFFFFF.

</dd> <dt>

*bMatchAll* \[ in\]
</dt> <dd>

Specifica se trovare la corrispondenza con tutti i valori di ricerca.

</dd> <dt>

*lpSearchParm* \[ in\]
</dt> <dd>

Puntatore a una struttura [**LSKeyPack**](lskeypack.md) che specifica i parametri di ricerca da cercare.

</dd> <dt>

*pdwErrCode* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve uno dei codici di errore seguenti alla restituzione.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ \_Operazione riuscita** (0)


</dt> <dd>

La chiamata è riuscita.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Errore interno di E** (5001)


</dt> <dd>

Errore interno nel server licenze.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequenza E non valida** (5006)


</dt> <dd>

Sequenza di chiamata non valida. Probabilmente, un'enumerazione precedente non è terminata.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Server E \_ occupato** (5007)


</dt> <dd>

Il server licenze è troppo occupato per elaborare la richiesta.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OutOfMemory** (5008)


</dt> <dd>

Impossibile elaborare la richiesta a causa di memoria insufficiente.

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ dati non validi** (5009)


</dt> <dd>

I dati nel parametro di ricerca non sono validi.

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

Argomento non valido.

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

 

