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
# <a name="tlslicenseenumbegin-function"></a><span data-ttu-id="13f47-104">TLSLicenseEnumBegin (funzione)</span><span class="sxs-lookup"><span data-stu-id="13f47-104">TLSLicenseEnumBegin function</span></span>

<span data-ttu-id="13f47-105">Inizia l'enumerazione delle licenze rilasciate dal server licenze Desktop remoto in base ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="13f47-105">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="13f47-106">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="13f47-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="13f47-107">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="13f47-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="13f47-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13f47-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="13f47-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="13f47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f47-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13f47-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f47-111">Handle per un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="13f47-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="13f47-112">Specificare un handle aperto dalla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="13f47-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="13f47-113">*dwSearchParm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13f47-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f47-114">Specifica i criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="13f47-114">Specifies the search criteria.</span></span> <span data-ttu-id="13f47-115">Il parametro può essere costituito da una combinazione dei valori descritti nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="13f47-115">The parameter can be one or a combination of the values that are described in the following list.</span></span> <span data-ttu-id="13f47-116">Il parametro specifica il tipo di Key Pack e il Key Pack in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="13f47-116">The parameter specifies the type of key pack and which key pack to search.</span></span>

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span data-ttu-id="13f47-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ Cerca in \_ LICENSEID** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="13f47-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE\_SEARCH\_LICENSEID** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-118">Cerca per ID licenza.</span><span class="sxs-lookup"><span data-stu-id="13f47-118">Search by license ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span data-ttu-id="13f47-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ Cerca in \_ KEYPACKID** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="13f47-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE\_SEARCH\_KEYPACKID** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-120">Cerca per ID del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="13f47-120">Search by key pack ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span data-ttu-id="13f47-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ Cerca \_ machineName** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="13f47-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE\_SEARCH\_MACHINENAME** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-122">Cerca per nome computer.</span><span class="sxs-lookup"><span data-stu-id="13f47-122">Search by machine name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span data-ttu-id="13f47-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ Cerca \_ nome utente** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="13f47-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE\_SEARCH\_USERNAME** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-124">Cerca per nome utente.</span><span class="sxs-lookup"><span data-stu-id="13f47-124">Search by user name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span data-ttu-id="13f47-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ RICERCA \_ rilasciata** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="13f47-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE\_SEARCH\_ISSUEDATE** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-126">Cerca per data di rilascio.</span><span class="sxs-lookup"><span data-stu-id="13f47-126">Search by issue date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span data-ttu-id="13f47-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ RICERCA \_ scaduta** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="13f47-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE\_SEARCH\_EXPIREDATE** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-128">Cerca per data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="13f47-128">Search by expiration date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span data-ttu-id="13f47-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ Cerca in \_ NUMLICENSES** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="13f47-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE\_SEARCH\_ NUMLICENSES** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-130">Eseguire una ricerca in base al numero di licenze.</span><span class="sxs-lookup"><span data-stu-id="13f47-130">Search by number of licenses.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span data-ttu-id="13f47-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ \_ \_ Stato voce di ricerca** (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="13f47-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE\_SEARCH\_ ENTRY\_STATUS** (0x20000000)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-132">Cerca per stato voce.</span><span class="sxs-lookup"><span data-stu-id="13f47-132">Search by entry status.</span></span>

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span data-ttu-id="13f47-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ EXSEARCH \_ LICENSESTATUS** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="13f47-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE\_EXSEARCH\_LICENSESTATUS** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-134">Cerca per stato della licenza.</span><span class="sxs-lookup"><span data-stu-id="13f47-134">Search by license status.</span></span>

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span data-ttu-id="13f47-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ Cerca in \_ tutto** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="13f47-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK\_SEARCH\_ALL** (0xFFFFFFFF)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-136">Eseguire una ricerca in tutte le licenze.</span><span class="sxs-lookup"><span data-stu-id="13f47-136">Search all licenses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="13f47-137">*bMatchAll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13f47-137">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f47-138">Specifica se trovare la corrispondenza con tutti i valori di ricerca.</span><span class="sxs-lookup"><span data-stu-id="13f47-138">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="13f47-139">*lpSearchParm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13f47-139">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f47-140">Puntatore a una struttura [**LSLicense**](lslicense.md) che specifica i parametri di ricerca da cercare.</span><span class="sxs-lookup"><span data-stu-id="13f47-140">Pointer to a [**LSLicense**](lslicense.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="13f47-141">*pdwErrCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="13f47-141">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13f47-142">Puntatore a una variabile che riceve uno dei codici di errore seguenti alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="13f47-142">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="13f47-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ \_Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="13f47-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-144">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="13f47-144">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="13f47-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Errore interno di E** (5001)</span><span class="sxs-lookup"><span data-stu-id="13f47-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-146">Errore interno nel server licenze.</span><span class="sxs-lookup"><span data-stu-id="13f47-146">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="13f47-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequenza E non valida** (5006)</span><span class="sxs-lookup"><span data-stu-id="13f47-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-148">Sequenza di chiamata non valida.</span><span class="sxs-lookup"><span data-stu-id="13f47-148">The calling sequence was not valid.</span></span> <span data-ttu-id="13f47-149">Probabilmente, un'enumerazione precedente non è terminata.</span><span class="sxs-lookup"><span data-stu-id="13f47-149">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="13f47-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Server E \_ occupato** (5007)</span><span class="sxs-lookup"><span data-stu-id="13f47-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-151">Il server licenze è troppo occupato per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="13f47-151">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="13f47-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OutOfMemory** (5008)</span><span class="sxs-lookup"><span data-stu-id="13f47-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-153">Impossibile elaborare la richiesta a causa di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="13f47-153">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="13f47-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ dati non validi** (5009)</span><span class="sxs-lookup"><span data-stu-id="13f47-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="13f47-155">I dati nel parametro di ricerca non sono validi.</span><span class="sxs-lookup"><span data-stu-id="13f47-155">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f47-156">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13f47-156">Return value</span></span>

<span data-ttu-id="13f47-157">Questa funzione restituisce i valori restituiti possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="13f47-157">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="13f47-158">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="13f47-158">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="13f47-159">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="13f47-159">The call succeeded.</span></span> <span data-ttu-id="13f47-160">Controllare il valore del parametro *pdwErrCode* per ottenere il codice restituito per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="13f47-160">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="13f47-161">**\_ \_ arg non valido \_**</span><span class="sxs-lookup"><span data-stu-id="13f47-161">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="13f47-162">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="13f47-162">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13f47-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13f47-163">Requirements</span></span>



| <span data-ttu-id="13f47-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="13f47-164">Requirement</span></span> | <span data-ttu-id="13f47-165">Valore</span><span class="sxs-lookup"><span data-stu-id="13f47-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13f47-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13f47-166">Minimum supported client</span></span><br/> | <span data-ttu-id="13f47-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13f47-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13f47-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13f47-168">Minimum supported server</span></span><br/> | <span data-ttu-id="13f47-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13f47-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13f47-170">DLL</span><span class="sxs-lookup"><span data-stu-id="13f47-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13f47-171"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13f47-171"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f47-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13f47-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f47-173">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="13f47-173">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="13f47-174">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="13f47-174">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="13f47-175">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="13f47-175">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="13f47-176">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="13f47-176">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

