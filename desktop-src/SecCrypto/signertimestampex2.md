---
description: Timestamp l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del contesto del FIRMATARIo \_ che contiene un puntatore a un BLOB. Questa funzione può essere usata per eseguire l'infrastruttura a chiave pubblica X. 509, i timestamp RFC 3161&\# 8211; conformi.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316654"
---
# <a name="signertimestampex2-function"></a><span data-ttu-id="4e018-104">SignerTimeStampEx2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="4e018-104">SignerTimeStampEx2 function</span></span>

<span data-ttu-id="4e018-105">Il timestamp della funzione **SignerTimeStampEx2** indica l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene un puntatore a un [*BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4e018-105">The **SignerTimeStampEx2** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="4e018-106">Questa funzione può essere usata per eseguire l'infrastruttura a chiave pubblica X. 509, conforme a RFC 3161, timestamp.</span><span class="sxs-lookup"><span data-stu-id="4e018-106">This function can be used to perform X.509 Public Key Infrastructure, RFC 3161–compliant, time stamps.</span></span>

> [!Note]  
> <span data-ttu-id="4e018-107">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="4e018-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="4e018-108">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="4e018-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4e018-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e018-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="4e018-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e018-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e018-111">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e018-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e018-112">Valore che specifica il tipo di timestamp da generare.</span><span class="sxs-lookup"><span data-stu-id="4e018-112">Value that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="4e018-113">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4e018-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="4e018-114">I valori si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4e018-114">The values are mutually exclusive.</span></span>



| <span data-ttu-id="4e018-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4e018-115">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="4e018-116">Significato</span><span class="sxs-lookup"><span data-stu-id="4e018-116">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="4e018-117"><dt>**TIMESTAMP del FIRMATARIo \_ \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="4e018-117"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="4e018-118">Specifica un timestamp Authenticode.</span><span class="sxs-lookup"><span data-stu-id="4e018-118">Specifies an Authenticode time stamp.</span></span><br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="4e018-119"><dt>**TIMESTAMP del FIRMATARIo \_ \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="4e018-119"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="4e018-120">Specifica un timestamp conforme a RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="4e018-120">Specifies an RFC 3161–compliant time stamp.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4e018-121">*pSubjectInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e018-121">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e018-122">Indirizzo di una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che rappresenta l'oggetto di cui è stato indicato il timestamp.</span><span class="sxs-lookup"><span data-stu-id="4e018-122">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="4e018-123">*pwszHttpTimeStamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e018-123">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e018-124">Indirizzo di una stringa Unicode con terminazione null che contiene l'URL di un server di timestamp.</span><span class="sxs-lookup"><span data-stu-id="4e018-124">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="4e018-125">*dwAlgId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e018-125">*dwAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e018-126">Specifica un algoritmo hash da usare per l'esecuzione di timestamp conformi a RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="4e018-126">Specifies a hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="4e018-127">Questo parametro viene ignorato per gli indicatori di data e ora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="4e018-127">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="4e018-128">*psRequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e018-128">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e018-129">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4e018-129">Optional.</span></span> <span data-ttu-id="4e018-130">Indirizzo di una struttura [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi aggiunti alla richiesta del timestamp.</span><span class="sxs-lookup"><span data-stu-id="4e018-130">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="4e018-131">Questo parametro è facoltativo e può essere **null** se non è incluso.</span><span class="sxs-lookup"><span data-stu-id="4e018-131">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="4e018-132">*pSipData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e018-132">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e018-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4e018-133">Optional.</span></span> <span data-ttu-id="4e018-134">Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP ( [*Subject Interface Package*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="4e018-134">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="4e018-135">Il formato e il contenuto di questo parametro sono definiti dal provider SIP.</span><span class="sxs-lookup"><span data-stu-id="4e018-135">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="4e018-136">Questo parametro è facoltativo e può essere **null** se non è incluso.</span><span class="sxs-lookup"><span data-stu-id="4e018-136">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="4e018-137">*ppSignerContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4e018-137">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e018-138">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4e018-138">Optional.</span></span> <span data-ttu-id="4e018-139">Indirizzo di un puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene il BLOB firmato.</span><span class="sxs-lookup"><span data-stu-id="4e018-139">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="4e018-140">Al termine dell'uso della struttura del **\_ contesto del firmatario** , liberarla chiamando la funzione [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="4e018-140">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e018-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e018-141">Return value</span></span>

<span data-ttu-id="4e018-142">Se la funzione ha esito positivo, la funzione restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e018-142">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="4e018-143">Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="4e018-143">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4e018-144">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="4e018-144">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e018-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e018-145">Requirements</span></span>



| <span data-ttu-id="4e018-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e018-146">Requirement</span></span> | <span data-ttu-id="4e018-147">Valore</span><span class="sxs-lookup"><span data-stu-id="4e018-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e018-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e018-148">Minimum supported client</span></span><br/> | <span data-ttu-id="4e018-149">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e018-149">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4e018-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e018-150">Minimum supported server</span></span><br/> | <span data-ttu-id="4e018-151">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e018-151">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4e018-152">DLL</span><span class="sxs-lookup"><span data-stu-id="4e018-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e018-153"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e018-153"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e018-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e018-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e018-155">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="4e018-155">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="4e018-156">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="4e018-156">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> </dl>

 

 
