---
title: TLSLicenseEnumEnd (funzione)
description: Continua da una precedente chiamata alla funzione TLSLicenseEnumBegin e termina l'enumerazione.
ms.assetid: b9cba03c-0f5a-41e8-ae13-bcdd0ac6dd99
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSLicenseEnumEnd
topic_type:
- apiref
api_name:
- TLSLicenseEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbd494ec539ee78008fa3df274282da1e9db6c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302442"
---
# <a name="tlslicenseenumend-function"></a><span data-ttu-id="de7c0-104">TLSLicenseEnumEnd (funzione)</span><span class="sxs-lookup"><span data-stu-id="de7c0-104">TLSLicenseEnumEnd function</span></span>

<span data-ttu-id="de7c0-105">Continua da una precedente chiamata alla funzione [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e termina l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="de7c0-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="de7c0-106">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="de7c0-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="de7c0-107">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="de7c0-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="de7c0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de7c0-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="de7c0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="de7c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de7c0-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de7c0-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de7c0-111">Handle per un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="de7c0-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="de7c0-112">Specificare un handle aperto dalla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="de7c0-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="de7c0-113">*pdwErrCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="de7c0-113">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de7c0-114">Puntatore a una variabile che riceve uno dei codici di errore seguenti alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="de7c0-114">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="de7c0-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ \_Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="de7c0-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="de7c0-116">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="de7c0-116">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span data-ttu-id="de7c0-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_ \_ \_ Handle E non valido** (5005)</span><span class="sxs-lookup"><span data-stu-id="de7c0-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER\_E\_INVALID\_HANDLE** (5005)</span></span>


</dt> <dd>

<span data-ttu-id="de7c0-118">Handle non valido.</span><span class="sxs-lookup"><span data-stu-id="de7c0-118">The handle is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de7c0-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de7c0-119">Return value</span></span>

<span data-ttu-id="de7c0-120">Questa funzione restituisce i valori restituiti possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="de7c0-120">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="de7c0-121">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="de7c0-121">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="de7c0-122">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="de7c0-122">The call succeeded.</span></span> <span data-ttu-id="de7c0-123">Controllare il valore del parametro *pdwErrCode* per ottenere il codice restituito per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="de7c0-123">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="de7c0-124">**\_ \_ arg non valido \_**</span><span class="sxs-lookup"><span data-stu-id="de7c0-124">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="de7c0-125">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="de7c0-125">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de7c0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de7c0-126">Requirements</span></span>



| <span data-ttu-id="de7c0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="de7c0-127">Requirement</span></span> | <span data-ttu-id="de7c0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="de7c0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de7c0-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de7c0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="de7c0-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de7c0-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de7c0-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de7c0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="de7c0-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de7c0-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de7c0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="de7c0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de7c0-134"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de7c0-134"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de7c0-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de7c0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de7c0-136">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="de7c0-136">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="de7c0-137">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="de7c0-137">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="de7c0-138">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="de7c0-138">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="de7c0-139">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="de7c0-139">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> </dl>

 

