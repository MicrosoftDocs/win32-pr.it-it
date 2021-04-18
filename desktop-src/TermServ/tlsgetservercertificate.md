---
title: TLSGetServerCertificate (funzione)
description: Restituisce il certificato del server licenze Desktop remoto.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSGetServerCertificate
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301292"
---
# <a name="tlsgetservercertificate-function"></a><span data-ttu-id="d9858-104">TLSGetServerCertificate (funzione)</span><span class="sxs-lookup"><span data-stu-id="d9858-104">TLSGetServerCertificate function</span></span>

<span data-ttu-id="d9858-105">Restituisce il certificato del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="d9858-105">Returns the certificate of the Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="d9858-106">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="d9858-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="d9858-107">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="d9858-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d9858-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9858-108">Syntax</span></span>


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="d9858-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9858-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9858-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9858-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9858-111">Handle per un server licenze Desktop remoto aperto da una chiamata alla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="d9858-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d9858-112">*bSignCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9858-112">*bSignCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9858-113">**True** se il certificato di firma, **false** se il certificato di Exchange.</span><span class="sxs-lookup"><span data-stu-id="d9858-113">**TRUE** if signature certificate, **FALSE** if exchange certificate.</span></span>

</dd> <dt>

<span data-ttu-id="d9858-114">*ppbCertBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d9858-114">*ppbCertBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9858-115">Puntatore a una variabile che riceve un puntatore a un buffer che contiene il certificato.</span><span class="sxs-lookup"><span data-stu-id="d9858-115">Pointer to a variable that receives a pointer to a buffer that contains the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="d9858-116">*lpdwCertBlobLen* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d9858-116">*lpdwCertBlobLen* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9858-117">Puntatore a una variabile che riceve le dimensioni del certificato restituito.</span><span class="sxs-lookup"><span data-stu-id="d9858-117">Pointer to a variable that receives the size of the certificate that is returned.</span></span>

</dd> <dt>

<span data-ttu-id="d9858-118">*pdwErrCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d9858-118">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9858-119">Puntatore a una variabile che riceve il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="d9858-119">Pointer to a variable that receives the error code.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="d9858-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ \_Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="d9858-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d9858-121">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="d9858-121">Call is successful.</span></span>

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span data-ttu-id="d9858-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ \_ \_ Certificato SELFSIGN W** (4007)</span><span class="sxs-lookup"><span data-stu-id="d9858-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS\_W\_SELFSIGN\_CERTIFICATE** (4007)</span></span>


</dt> <dd>

<span data-ttu-id="d9858-123">Il certificato restituito è un certificato autofirmato.</span><span class="sxs-lookup"><span data-stu-id="d9858-123">Certificate returned is a self-signed certificate.</span></span>

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span data-ttu-id="d9858-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ W \_ temp \_ SELFSIGN \_ CERT** (4009)</span><span class="sxs-lookup"><span data-stu-id="d9858-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS\_W\_TEMP\_SELFSIGN\_CERT** (4009)</span></span>


</dt> <dd>

<span data-ttu-id="d9858-125">Il certificato restituito è temporaneo.</span><span class="sxs-lookup"><span data-stu-id="d9858-125">Certificate returned is temporary.</span></span>

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span data-ttu-id="d9858-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ E \_ accesso \_ negato** (5003)</span><span class="sxs-lookup"><span data-stu-id="d9858-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS\_E\_ACCESS\_DENIED** (5003)</span></span>


</dt> <dd>

<span data-ttu-id="d9858-127">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d9858-127">Access denied.</span></span>

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span data-ttu-id="d9858-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ E \_ alloca \_ HANDLE** (5007)</span><span class="sxs-lookup"><span data-stu-id="d9858-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS\_E\_ALLOCATE\_HANDLE** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="d9858-129">Il server è troppo occupato per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d9858-129">Server is too busy to process the request.</span></span>

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span data-ttu-id="d9858-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ nessun \_ certificato** (5022)</span><span class="sxs-lookup"><span data-stu-id="d9858-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS\_E\_NO\_CERTIFICATE** (5022)</span></span>


</dt> <dd>

<span data-ttu-id="d9858-131">Impossibile recuperare un certificato.</span><span class="sxs-lookup"><span data-stu-id="d9858-131">Cannot retrieve a certificate.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9858-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9858-132">Return value</span></span>

<span data-ttu-id="d9858-133">Questa funzione restituisce i valori restituiti possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9858-133">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="d9858-134">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="d9858-134">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="d9858-135">La chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="d9858-135">The call succeeded.</span></span> <span data-ttu-id="d9858-136">Controllare il valore del parametro *pdwErrCode* per ottenere il codice restituito per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="d9858-136">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="d9858-137">**\_ \_ arg non valido \_**</span><span class="sxs-lookup"><span data-stu-id="d9858-137">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="d9858-138">L'argomento non è valido.</span><span class="sxs-lookup"><span data-stu-id="d9858-138">The argument was invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9858-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9858-139">Requirements</span></span>



| <span data-ttu-id="d9858-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9858-140">Requirement</span></span> | <span data-ttu-id="d9858-141">Valore</span><span class="sxs-lookup"><span data-stu-id="d9858-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9858-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9858-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d9858-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9858-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9858-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9858-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d9858-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9858-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9858-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d9858-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9858-147"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9858-147"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9858-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9858-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9858-149">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="d9858-149">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

