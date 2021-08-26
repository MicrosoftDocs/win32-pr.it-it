---
title: Funzione TLSLicenseEnumBegin
description: Avvia l'enumerazione delle licenze rilasciate dal server Desktop remoto in base ai criteri di ricerca.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Funzione TLSLicenseEnumBegin Servizi Desktop remoto
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
ms.openlocfilehash: 620f6487bb516a76ac5cb7f77da9983178933c24ac03151bd9a4c8455f694ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986881"
---
# <a name="tlslicenseenumbegin-function"></a>Funzione TLSLicenseEnumBegin

Avvia l'enumerazione delle licenze rilasciate dal server Desktop remoto in base ai criteri di ricerca.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mstlsapi.dll.

 

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

*hHandle* \[ Pollici\]
</dt> <dd>

Handle a un Desktop remoto licenze. Specificare un handle aperto dalla funzione [**TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> <dt>

*dwSearchParm* \[ Pollici\]
</dt> <dd>

Specifica i criteri di ricerca. Il parametro può essere uno o una combinazione dei valori descritti nell'elenco seguente. Il parametro specifica il tipo di key pack e il key pack da cercare.

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ CERCA \_ LICENSEID** (0x00000001)


</dt> <dd>

Cercare in base all'ID licenza.

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ SEARCH \_ KEYPACKID** (0x00000002)


</dt> <dd>

Cercare in base all'ID del key pack.

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ SEARCH \_ MACHINENAME** (0x00000008)


</dt> <dd>

Cercare in base al nome del computer.

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ NOME \_ UTENTE DI** RICERCA (0x00000010)


</dt> <dd>

Eseguire la ricerca in base al nome utente.

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ SEARCH \_ ISSUEDATE** (0x00000080)


</dt> <dd>

Eseguire la ricerca in base alla data di rilascio.

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ SEARCH \_ EXPIREDATE** (0x00000100)


</dt> <dd>

Eseguire la ricerca in base alla data di scadenza.

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ CERCA \_ NUMLICENSES** (0x00000200)


</dt> <dd>

Cercare in base al numero di licenze.

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ STATO \_ \_ VOCE DI RICERCA** (0x20000000)


</dt> <dd>

Eseguire la ricerca in base allo stato della voce.

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ EXSEARCH \_ LICENSESTATUS** (0x00100000)


</dt> <dd>

Cercare in base allo stato della licenza.

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ CERCA \_ TUTTO** (0xFFFFFFFF)


</dt> <dd>

Cercare tutte le licenze.

</dd> </dl> </dd> <dt>

*bMatchAll* \[ Pollici\]
</dt> <dd>

Specifica se trovare la corrispondenza con tutti i valori di ricerca.

</dd> <dt>

*lpSearchParm* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura LSLicense**](lslicense.md) che specifica i parametri di ricerca da cercare.

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

Sequenza chiamante non valida. Molto probabilmente, un'enumerazione precedente non è terminata.

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

Questa funzione restituisce i possibili valori restituiti seguenti.

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

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

