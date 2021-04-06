---
title: TLSLicenseEnumBegin (funzione)
description: Inizia l'enumerazione delle licenze rilasciate dal server licenze Desktop remoto in base ai criteri di ricerca.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSLicenseEnumBegin
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743607"
---
# <a name="tlslicenseenumbegin-function"></a>TLSLicenseEnumBegin (funzione)

Inizia l'enumerazione delle licenze rilasciate dal server licenze Desktop remoto in base ai criteri di ricerca.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
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

Specifica i criteri di ricerca. Il parametro può essere costituito da una combinazione dei valori descritti nell'elenco seguente. Il parametro specifica il tipo di Key Pack e il Key Pack in cui eseguire la ricerca.

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ Cerca in \_ LICENSEID** (0x00000001)


</dt> <dd>

Cerca per ID licenza.

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ Cerca in \_ KEYPACKID** (0x00000002)


</dt> <dd>

Cerca per ID del Key Pack.

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ Cerca \_ machineName** (0x00000008)


</dt> <dd>

Cerca per nome computer.

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ Cerca \_ nome utente** (0x00000010)


</dt> <dd>

Cerca per nome utente.

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ RICERCA \_ rilasciata** (0x00000080)


</dt> <dd>

Cerca per data di rilascio.

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ RICERCA \_ scaduta** (0x00000100)


</dt> <dd>

Cerca per data di scadenza.

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ Cerca in \_ NUMLICENSES** (0x00000200)


</dt> <dd>

Eseguire una ricerca in base al numero di licenze.

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ \_ \_ Stato voce di ricerca** (0x20000000)


</dt> <dd>

Cerca per stato voce.

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ EXSEARCH \_ LICENSESTATUS** (0x00100000)


</dt> <dd>

Cerca per stato della licenza.

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ Cerca in \_ tutto** (0xFFFFFFFF)


</dt> <dd>

Eseguire una ricerca in tutte le licenze.

</dd> </dl> </dd> <dt>

*bMatchAll* \[ in\]
</dt> <dd>

Specifica se trovare la corrispondenza con tutti i valori di ricerca.

</dd> <dt>

*lpSearchParm* \[ in\]
</dt> <dd>

Puntatore a una struttura [**LSLicense**](lslicense.md) che specifica i parametri di ricerca da cercare.

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

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

