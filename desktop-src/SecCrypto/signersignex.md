---
description: Firma il file specificato e restituisce un puntatore ai dati firmati.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: SignerSignEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755562"
---
# <a name="signersignex-function"></a><span data-ttu-id="4dd6e-103">SignerSignEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="4dd6e-103">SignerSignEx function</span></span>

<span data-ttu-id="4dd6e-104">La funzione **SignerSignEx** firma il file specificato e restituisce un puntatore ai dati firmati.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-104">The **SignerSignEx** function signs the specified file and returns a pointer to the signed data.</span></span>

> [!Note]  
> <span data-ttu-id="4dd6e-105">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="4dd6e-106">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4dd6e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dd6e-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="4dd6e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4dd6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd6e-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-110">Modifica il comportamento di questa funzione.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="4dd6e-111">Se il file da firmare è un file eseguibile portabile (PE), può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="4dd6e-112">Questi identificatori sono definiti in Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-112">These identifiers are defined in Mssip.h.</span></span>



| <span data-ttu-id="4dd6e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd6e-113">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="4dd6e-114">Significato</span><span class="sxs-lookup"><span data-stu-id="4dd6e-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="4dd6e-115"><dt>**SPC \_ \_Flag di \_ \_ hash \_ della pagina PE EXC**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="4dd6e-115"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="4dd6e-116">Escludere gli hash di pagina durante la creazione di dati SIP indiretti per il file PE.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-116">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="4dd6e-117">Questo flag ha la precedenza sul flag del **flag di hash della \_ pagina del \_ PE \_ \_ \_ SPC Inc** .</span><span class="sxs-lookup"><span data-stu-id="4dd6e-117">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="4dd6e-118">Se non viene specificato né il flag di **hash della \_ \_ pagina del PE \_ \_ \_ di SPC** , né il flag del **\_ \_ \_ \_ \_ flag di hash della pagina del PE SPC Inc** , viene usato il valore impostato con la funzione [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) per questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-118">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="4dd6e-119">Il valore predefinito per questa impostazione consiste nell'escludere gli hash di pagina durante la creazione di dati SIP indiretti per i file PE.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-119">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="4dd6e-120">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="4dd6e-121"><dt>**SPC \_ 0x20 \_ del \_ \_ flag di \_ tabella \_ IND Import PE**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4dd6e-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="4dd6e-122">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="4dd6e-123"><dt>**SPC \_ 0x40 \_ di \_ \_ \_ informazioni di debug PE Inc**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4dd6e-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="4dd6e-124">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="4dd6e-125"><dt>**SPC \_ 0x80 \_ \_ \_ flag risorse PE incl**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4dd6e-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="4dd6e-126">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="4dd6e-127"><dt>**SPC \_ 0x100 \_ del \_ \_ \_ flag di hash delle pagine PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4dd6e-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="4dd6e-128">Includere gli hash di pagina quando si creano dati SIP indiretti per il file PE.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="4dd6e-129">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="4dd6e-130">*pSubjectInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-130">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-131">Puntatore a una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che specifica l'oggetto da firmare.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-131">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="4dd6e-132">*pSignerCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-132">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-133">Puntatore a una struttura del certificato del [**firmatario \_**](signer-cert.md) che specifica il certificato da usare per creare la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-133">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="4dd6e-134">*pSignatureInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-134">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-135">Puntatore a una struttura di [**\_ \_ informazioni sulla firma del firmatario**](signer-signature-info.md) che contiene informazioni sulla firma digitale.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-135">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="4dd6e-136">*pProviderInfo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-136">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-137">Puntatore a una struttura di [**\_ \_ informazioni del provider del firmatario**](signer-provider-info.md) che specifica le informazioni sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e sulla chiave privata utilizzate per creare la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-137">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="4dd6e-138">Se il valore di questo parametro è **null**, il valore del parametro *pSignerCert* deve specificare un certificato associato a un CSP.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-138">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="4dd6e-139">*pwszHttpTimeStamp* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-139">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-140">URL di un server di timestamp.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-140">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="4dd6e-141">*psRequest* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-141">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-142">Puntatore a una matrice di strutture [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) che vengono aggiunte a una richiesta di firma.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-142">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="4dd6e-143">Questo parametro viene ignorato se il parametro *pwszHttpTimeStamp* non contiene un valore valido che non è **null**.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-143">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4dd6e-144">*pSipData* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-144">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-145">Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-145">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="4dd6e-146">Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-146">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="4dd6e-147">*ppSignerContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-147">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd6e-148">Indirizzo di un puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene il [*BLOB*](../secgloss/b-gly.md)firmato.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-148">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="4dd6e-149">Al termine dell'uso della struttura del **\_ contesto del firmatario** , liberare la struttura del **\_ contesto del firmatario** chiamando la funzione [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd6e-149">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd6e-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4dd6e-150">Return value</span></span>

<span data-ttu-id="4dd6e-151">Se la funzione ha esito positivo, la funzione restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-151">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="4dd6e-152">Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="4dd6e-152">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4dd6e-153">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="4dd6e-153">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd6e-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dd6e-154">Requirements</span></span>



| <span data-ttu-id="4dd6e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dd6e-155">Requirement</span></span> | <span data-ttu-id="4dd6e-156">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd6e-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd6e-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dd6e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd6e-158">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4dd6e-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dd6e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd6e-160">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4dd6e-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4dd6e-161">DLL</span><span class="sxs-lookup"><span data-stu-id="4dd6e-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dd6e-162"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dd6e-162"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dd6e-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dd6e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd6e-164">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="4dd6e-164">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="4dd6e-165">**SignerFreeSignerContext**</span><span class="sxs-lookup"><span data-stu-id="4dd6e-165">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
