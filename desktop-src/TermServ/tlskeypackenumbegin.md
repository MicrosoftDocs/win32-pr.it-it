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
# <a name="tlskeypackenumbegin-function"></a><span data-ttu-id="6991c-104">TLSKeyPackEnumBegin (funzione)</span><span class="sxs-lookup"><span data-stu-id="6991c-104">TLSKeyPackEnumBegin function</span></span>

<span data-ttu-id="6991c-105">Inizia l'enumerazione tramite tutti i Key Pack installati in un server licenze Desktop remoto in base ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="6991c-105">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="6991c-106">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="6991c-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="6991c-107">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="6991c-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6991c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6991c-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="6991c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6991c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6991c-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6991c-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6991c-111">Handle per un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="6991c-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="6991c-112">Specificare un handle aperto dalla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="6991c-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6991c-113">*dwSearchParm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6991c-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6991c-114">Specifica i criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="6991c-114">Specifies the search criteria.</span></span> <span data-ttu-id="6991c-115">Questo parametro è riservato per utilizzi futuri e deve contenere 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="6991c-115">This parameter is reserved for future use and must contain 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="6991c-116">*bMatchAll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6991c-116">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6991c-117">Specifica se trovare la corrispondenza con tutti i valori di ricerca.</span><span class="sxs-lookup"><span data-stu-id="6991c-117">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="6991c-118">*lpSearchParm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6991c-118">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6991c-119">Puntatore a una struttura [**LSKeyPack**](lskeypack.md) che specifica i parametri di ricerca da cercare.</span><span class="sxs-lookup"><span data-stu-id="6991c-119">Pointer to a [**LSKeyPack**](lskeypack.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="6991c-120">*pdwErrCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6991c-120">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6991c-121">Puntatore a una variabile che riceve uno dei codici di errore seguenti alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="6991c-121">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="6991c-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ \_Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="6991c-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6991c-123">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6991c-123">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="6991c-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Errore interno di E** (5001)</span><span class="sxs-lookup"><span data-stu-id="6991c-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="6991c-125">Errore interno nel server licenze.</span><span class="sxs-lookup"><span data-stu-id="6991c-125">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="6991c-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequenza E non valida** (5006)</span><span class="sxs-lookup"><span data-stu-id="6991c-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="6991c-127">Sequenza di chiamata non valida.</span><span class="sxs-lookup"><span data-stu-id="6991c-127">The calling sequence was not valid.</span></span> <span data-ttu-id="6991c-128">Probabilmente, un'enumerazione precedente non è terminata.</span><span class="sxs-lookup"><span data-stu-id="6991c-128">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="6991c-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Server E \_ occupato** (5007)</span><span class="sxs-lookup"><span data-stu-id="6991c-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="6991c-130">Il server licenze è troppo occupato per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6991c-130">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="6991c-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OutOfMemory** (5008)</span><span class="sxs-lookup"><span data-stu-id="6991c-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="6991c-132">Impossibile elaborare la richiesta a causa di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="6991c-132">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="6991c-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ dati non validi** (5009)</span><span class="sxs-lookup"><span data-stu-id="6991c-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="6991c-134">I dati nel parametro di ricerca non sono validi.</span><span class="sxs-lookup"><span data-stu-id="6991c-134">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6991c-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6991c-135">Return value</span></span>

<span data-ttu-id="6991c-136">Questa funzione restituisce i valori restituiti possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="6991c-136">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="6991c-137">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="6991c-137">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="6991c-138">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6991c-138">The call succeeded.</span></span> <span data-ttu-id="6991c-139">Controllare il valore del parametro *pdwErrCode* per ottenere il codice restituito per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="6991c-139">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="6991c-140">**\_ \_ arg non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6991c-140">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="6991c-141">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="6991c-141">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6991c-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6991c-142">Requirements</span></span>



| <span data-ttu-id="6991c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="6991c-143">Requirement</span></span> | <span data-ttu-id="6991c-144">Valore</span><span class="sxs-lookup"><span data-stu-id="6991c-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6991c-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6991c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6991c-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6991c-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6991c-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6991c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6991c-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6991c-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6991c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6991c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6991c-150"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6991c-150"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6991c-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6991c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6991c-152">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="6991c-152">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="6991c-153">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="6991c-153">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="6991c-154">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="6991c-154">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="6991c-155">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="6991c-155">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

