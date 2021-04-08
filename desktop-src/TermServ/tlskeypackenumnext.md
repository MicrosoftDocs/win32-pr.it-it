---
title: TLSKeyPackEnumNext (funzione)
description: Continua da una precedente chiamata alla funzione TLSKeyPackEnumBegin e restituisce il key pack successivo installato in un server licenze Desktop remoto corrispondente ai criteri di ricerca.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSKeyPackEnumNext
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
ms.openlocfilehash: 897874f333ed7933ea1616f7f5ba5f1686736d0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047958"
---
# <a name="tlskeypackenumnext-function"></a><span data-ttu-id="43879-104">TLSKeyPackEnumNext (funzione)</span><span class="sxs-lookup"><span data-stu-id="43879-104">TLSKeyPackEnumNext function</span></span>

<span data-ttu-id="43879-105">Continua da una precedente chiamata alla funzione [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e restituisce il key pack successivo installato in un server licenze Desktop remoto corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="43879-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="43879-106">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="43879-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="43879-107">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="43879-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="43879-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43879-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="43879-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="43879-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43879-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43879-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43879-111">Handle per un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="43879-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="43879-112">Specificare un handle aperto dalla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="43879-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="43879-113">*lpKeyPack* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43879-113">*lpKeyPack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43879-114">Puntatore a una struttura [**LSKeyPack**](lskeypack.md) che riceve il key pack successivo corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="43879-114">Pointer to a [**LSKeyPack**](lskeypack.md) structure that receives the next key pack that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="43879-115">*pdwErrCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="43879-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43879-116">Puntatore a una variabile che riceve uno dei codici di errore seguenti alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="43879-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="43879-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ \_Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="43879-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="43879-118">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="43879-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="43879-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ Non \_ sono \_ più \_ disponibili dati** (4001)</span><span class="sxs-lookup"><span data-stu-id="43879-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="43879-120">Nessun altro Key Pack corrisponde ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="43879-120">No more key packs match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="43879-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Errore interno di E** (5001)</span><span class="sxs-lookup"><span data-stu-id="43879-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="43879-122">Errore interno nel server licenze.</span><span class="sxs-lookup"><span data-stu-id="43879-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="43879-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequenza E non valida** (5006)</span><span class="sxs-lookup"><span data-stu-id="43879-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="43879-124">Sequenza di chiamata non valida.</span><span class="sxs-lookup"><span data-stu-id="43879-124">The calling sequence was not valid.</span></span> <span data-ttu-id="43879-125">È necessario chiamare la funzione [**TLSKeyPackEnumBegin ()**](tlskeypackenumbegin.md) prima di questa.</span><span class="sxs-lookup"><span data-stu-id="43879-125">Must call the [**TLSKeyPackEnumBegin()**](tlskeypackenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="43879-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Server E \_ occupato** (5007)</span><span class="sxs-lookup"><span data-stu-id="43879-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="43879-127">Il server licenze è troppo occupato per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="43879-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="43879-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OutOfMemory** (5008)</span><span class="sxs-lookup"><span data-stu-id="43879-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="43879-129">Impossibile elaborare la richiesta a causa di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="43879-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43879-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43879-130">Return value</span></span>

<span data-ttu-id="43879-131">Questa funzione restituisce i valori restituiti possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="43879-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="43879-132">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="43879-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="43879-133">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="43879-133">The call succeeded.</span></span> <span data-ttu-id="43879-134">Controllare il valore del parametro *pdwErrCode* per ottenere il codice restituito per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="43879-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="43879-135">**\_ \_ arg non valido \_**</span><span class="sxs-lookup"><span data-stu-id="43879-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="43879-136">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="43879-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43879-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43879-137">Requirements</span></span>



| <span data-ttu-id="43879-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="43879-138">Requirement</span></span> | <span data-ttu-id="43879-139">Valore</span><span class="sxs-lookup"><span data-stu-id="43879-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43879-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43879-140">Minimum supported client</span></span><br/> | <span data-ttu-id="43879-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43879-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43879-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43879-142">Minimum supported server</span></span><br/> | <span data-ttu-id="43879-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43879-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43879-144">DLL</span><span class="sxs-lookup"><span data-stu-id="43879-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43879-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43879-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43879-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43879-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43879-147">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="43879-147">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="43879-148">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="43879-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="43879-149">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="43879-149">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="43879-150">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="43879-150">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

