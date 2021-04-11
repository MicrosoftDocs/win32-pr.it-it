---
description: Timestamp l'oggetto specificato e supporta l'impostazione di timestamp su più firme.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128090"
---
# <a name="signertimestampex3-function"></a><span data-ttu-id="9e5a8-103">SignerTimeStampEx3 (funzione)</span><span class="sxs-lookup"><span data-stu-id="9e5a8-103">SignerTimeStampEx3 function</span></span>

<span data-ttu-id="9e5a8-104">Il timestamp della funzione **SignerTimeStampEx3** timbra l'oggetto specificato e supporta l'impostazione dei timestamp su più firme.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-104">The **SignerTimeStampEx3** function time stamps the specified subject and supports setting time stamps on multiple signatures.</span></span>

> [!Note]  
> <span data-ttu-id="9e5a8-105">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="9e5a8-106">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9e5a8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e5a8-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="9e5a8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e5a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5a8-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-110">Flag che specifica il tipo di timestamp da generare.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-110">Flag that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="9e5a8-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="9e5a8-112">I valori si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-112">The values are mutually exclusive.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e5a8-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9e5a8-113">Value</span></span></th>
<th><span data-ttu-id="9e5a8-114">Significato</span><span class="sxs-lookup"><span data-stu-id="9e5a8-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="9e5a8-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9e5a8-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9e5a8-116">Specifica un timestamp Authenticode.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-116">Specifies an Authenticode time stamp.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9e5a8-117">Authenticode non è più il tipo di timestamp preferito.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-117">Authenticode is no longer the preferred type of time stamp.</span></span> <span data-ttu-id="9e5a8-118">Il supporto per i timestamp Authenticode potrebbe essere rimosso in futuro.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-118">Support for Authenticode time stamps may be removed in the future.</span></span> <span data-ttu-id="9e5a8-119">Si consiglia di usare invece RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-119">We recommend that you use RFC 3161 instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="9e5a8-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9e5a8-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9e5a8-121">Specifica un timestamp conforme a RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-121">Specifies an RFC 3161–compliant time stamp.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="9e5a8-122">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-122">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-123">Specifica il numero di sequenza della firma a cui verrà aggiunto il timestamp.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-123">Specifies the sequence number of the signature to which the timestamp will be added.</span></span> <span data-ttu-id="9e5a8-124">Se questo valore è zero (0), la firma esterna verrà contrassegnata con il timestamp.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-124">If this value is zero (0), the outer signature will be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="9e5a8-125">*pSubjectInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-125">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-126">Indirizzo di una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che rappresenta l'oggetto di cui è stato indicato il timestamp.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-126">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="9e5a8-127">*pwszHttpTimeStamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-127">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-128">Indirizzo di una stringa Unicode con terminazione null che contiene l'URL di un server di timestamp.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-128">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="9e5a8-129">*pszAlgorithmOid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-129">*pszAlgorithmOid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-130">Algoritmo hash da utilizzare per l'esecuzione di indicatori di tempo conformi a RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-130">A hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="9e5a8-131">Questo parametro viene ignorato per gli indicatori di data e ora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-131">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="9e5a8-132">*psRequest* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-132">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-133">Optional.</span></span> <span data-ttu-id="9e5a8-134">Indirizzo di una struttura [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi aggiunti alla richiesta del timestamp.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-134">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="9e5a8-135">Questo parametro è facoltativo e può essere **null** se non è incluso.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-135">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="9e5a8-136">*pSipData* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-136">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-137">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-137">Optional.</span></span> <span data-ttu-id="9e5a8-138">Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP ( [*Subject Interface Package*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="9e5a8-138">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="9e5a8-139">Il formato e il contenuto di questo parametro sono definiti dal provider SIP.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-139">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="9e5a8-140">Questo parametro è facoltativo e può essere **null** se non è incluso.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-140">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="9e5a8-141">*ppSignerContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-141">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-142">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-142">Optional.</span></span> <span data-ttu-id="9e5a8-143">Indirizzo di un puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene il BLOB firmato.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-143">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="9e5a8-144">Al termine dell'uso della struttura del **\_ contesto del firmatario** , liberarla chiamando la funzione [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="9e5a8-144">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9e5a8-145">*pCryptoPolicy* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-145">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5a8-146">Se presente, puntatore a una struttura [**del \_ \_ segno \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) di firma forte del certificato che contiene i parametri utilizzati per verificare le firme sicure.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-146">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="9e5a8-147">Il timestamp deve superare questo criterio di crittografia.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-147">The time stamp must pass this cryptographic policy.</span></span>

</dd> <dt>

<span data-ttu-id="9e5a8-148">*Mantenuto*</span><span class="sxs-lookup"><span data-stu-id="9e5a8-148">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="9e5a8-149">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-149">Reserved.</span></span> <span data-ttu-id="9e5a8-150">Questo valore deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-150">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5a8-151">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e5a8-151">Return value</span></span>

<span data-ttu-id="9e5a8-152">Se la funzione ha esito positivo, la funzione restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-152">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="9e5a8-153">Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-153">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="9e5a8-154">I codici di errore possibili restituiti da questa funzione includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-154">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="9e5a8-155">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="9e5a8-155">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e5a8-156">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9e5a8-156">Return code</span></span></th>
<th><span data-ttu-id="9e5a8-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e5a8-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="9e5a8-158"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9e5a8-158"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9e5a8-159">Questo errore può essere restituito per le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e5a8-159">This error can be returned for the following conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="9e5a8-160">Per il parametro <em>dwFlags</em> è necessario impostare <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> o <strong>SIGNER_TIMESTAMP_RFC3161</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e5a8-160">You must set either <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> or <strong>SIGNER_TIMESTAMP_RFC3161</strong> for the <em>dwFlags</em> parameter.</span></span></li>
<li><span data-ttu-id="9e5a8-161">Il parametro <em>mantenuto</em> deve essere <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-161">The <em>pReserved</em> parameter must be <strong>NULL</strong>.</span></span></li>
<li><span data-ttu-id="9e5a8-162">Se si imposta il flag di <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> nel parametro <em>dwFlags</em> , è necessario impostare il parametro <em>dwIndex</em> su zero.</span><span class="sxs-lookup"><span data-stu-id="9e5a8-162">If you set the <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> flag in the <em>dwFlags</em> parameter, you must set the <em>dwIndex</em> parameter to zero.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9e5a8-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e5a8-163">Requirements</span></span>



| <span data-ttu-id="9e5a8-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e5a8-164">Requirement</span></span> | <span data-ttu-id="9e5a8-165">Valore</span><span class="sxs-lookup"><span data-stu-id="9e5a8-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5a8-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e5a8-166">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5a8-167">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-167">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9e5a8-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e5a8-168">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5a8-169">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9e5a8-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9e5a8-170">DLL</span><span class="sxs-lookup"><span data-stu-id="9e5a8-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e5a8-171"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e5a8-171"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e5a8-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e5a8-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5a8-173">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="9e5a8-173">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="9e5a8-174">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="9e5a8-174">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> <dt>

[<span data-ttu-id="9e5a8-175">**SignerTimeStampEx2**</span><span class="sxs-lookup"><span data-stu-id="9e5a8-175">**SignerTimeStampEx2**</span></span>](signertimestampex2.md)
</dt> </dl>

 

 
