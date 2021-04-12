---
title: TLSLicenseEnumNext (funzione)
description: Continua da una precedente chiamata alla funzione TLSLicenseEnumBegin e restituisce la licenza successiva installata in un server licenze Desktop remoto corrispondente ai criteri di ricerca.
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSLicenseEnumNext
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c13b0a3137258015fe311c49b2cc9b999e3a13f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400922"
---
# <a name="tlslicenseenumnext-function"></a><span data-ttu-id="46dba-104">TLSLicenseEnumNext (funzione)</span><span class="sxs-lookup"><span data-stu-id="46dba-104">TLSLicenseEnumNext function</span></span>

<span data-ttu-id="46dba-105">Continua da una precedente chiamata alla funzione [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e restituisce la licenza successiva installata in un server licenze Desktop remoto corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="46dba-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="46dba-106">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="46dba-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="46dba-107">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="46dba-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="46dba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46dba-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="46dba-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="46dba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46dba-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46dba-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46dba-111">Handle per un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="46dba-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="46dba-112">Specificare un handle aperto dalla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="46dba-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="46dba-113">*lpLicense* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46dba-113">*lpLicense* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46dba-114">Puntatore a una struttura [**LSLicense**](lslicense.md) che riceve la licenza successiva corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="46dba-114">Pointer to a [**LSLicense**](lslicense.md) structure that receives the next license that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="46dba-115">*pdwErrCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="46dba-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46dba-116">Puntatore a una variabile che riceve uno dei codici di errore seguenti alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="46dba-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="46dba-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ \_Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="46dba-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="46dba-118">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="46dba-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="46dba-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ Non \_ sono \_ più \_ disponibili dati** (4001)</span><span class="sxs-lookup"><span data-stu-id="46dba-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="46dba-120">Nessuna licenza corrisponde ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="46dba-120">No more licenses match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="46dba-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Errore interno di E** (5001)</span><span class="sxs-lookup"><span data-stu-id="46dba-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="46dba-122">Errore interno nel server licenze.</span><span class="sxs-lookup"><span data-stu-id="46dba-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="46dba-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequenza E non valida** (5006)</span><span class="sxs-lookup"><span data-stu-id="46dba-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="46dba-124">Sequenza di chiamata non valida.</span><span class="sxs-lookup"><span data-stu-id="46dba-124">The calling sequence was not valid.</span></span> <span data-ttu-id="46dba-125">È necessario chiamare la funzione [**TLSLicenseEnumBegin ()**](tlslicenseenumbegin.md) prima di questa.</span><span class="sxs-lookup"><span data-stu-id="46dba-125">Must call the [**TLSLicenseEnumBegin()**](tlslicenseenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="46dba-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Server E \_ occupato** (5007)</span><span class="sxs-lookup"><span data-stu-id="46dba-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="46dba-127">Il server licenze è troppo occupato per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="46dba-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="46dba-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OutOfMemory** (5008)</span><span class="sxs-lookup"><span data-stu-id="46dba-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="46dba-129">Impossibile elaborare la richiesta a causa di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="46dba-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46dba-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46dba-130">Return value</span></span>

<span data-ttu-id="46dba-131">Questa funzione restituisce i valori restituiti possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="46dba-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="46dba-132">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="46dba-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="46dba-133">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="46dba-133">The call succeeded.</span></span> <span data-ttu-id="46dba-134">Controllare il valore del parametro *pdwErrCode* per ottenere il codice restituito per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="46dba-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="46dba-135">**\_ \_ arg non valido \_**</span><span class="sxs-lookup"><span data-stu-id="46dba-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="46dba-136">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="46dba-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46dba-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46dba-137">Requirements</span></span>



| <span data-ttu-id="46dba-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="46dba-138">Requirement</span></span> | <span data-ttu-id="46dba-139">Valore</span><span class="sxs-lookup"><span data-stu-id="46dba-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46dba-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46dba-140">Minimum supported client</span></span><br/> | <span data-ttu-id="46dba-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46dba-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46dba-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46dba-142">Minimum supported server</span></span><br/> | <span data-ttu-id="46dba-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46dba-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46dba-144">DLL</span><span class="sxs-lookup"><span data-stu-id="46dba-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46dba-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46dba-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46dba-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46dba-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46dba-147">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="46dba-147">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="46dba-148">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="46dba-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="46dba-149">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="46dba-149">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="46dba-150">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="46dba-150">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

