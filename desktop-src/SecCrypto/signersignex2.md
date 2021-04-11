---
description: Firma e timestamp del file specificato, consentendo più firme nidificate.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233122"
---
# <a name="signersignex2-function"></a><span data-ttu-id="3265c-103">SignerSignEx2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="3265c-103">SignerSignEx2 function</span></span>

<span data-ttu-id="3265c-104">La funzione **SignerSignEx2** firma e timbra il timestamp del file specificato, consentendo più firme nidificate.</span><span class="sxs-lookup"><span data-stu-id="3265c-104">The **SignerSignEx2** function signs and time stamps the specified file, allowing multiple nested signatures.</span></span>

> [!Note]  
> <span data-ttu-id="3265c-105">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="3265c-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="3265c-106">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="3265c-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3265c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3265c-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="3265c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3265c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3265c-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3265c-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-110">Modifica il comportamento di questa funzione.</span><span class="sxs-lookup"><span data-stu-id="3265c-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="3265c-111">Se il file da firmare è un file eseguibile portabile (PE), può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3265c-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="3265c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3265c-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="3265c-113">Significato</span><span class="sxs-lookup"><span data-stu-id="3265c-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="3265c-114"><dt>**SPC \_ \_Flag di \_ \_ hash \_ della pagina PE EXC**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="3265c-114"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="3265c-115">Escludere gli hash di pagina durante la creazione di dati SIP indiretti per il file PE.</span><span class="sxs-lookup"><span data-stu-id="3265c-115">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="3265c-116">Questo flag ha la precedenza sul flag del **flag di hash della \_ pagina del \_ PE \_ \_ \_ SPC Inc** .</span><span class="sxs-lookup"><span data-stu-id="3265c-116">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="3265c-117">Se non viene specificato né il flag di **hash della \_ \_ pagina del PE \_ \_ \_ di SPC** , né il flag del **\_ \_ \_ \_ \_ flag di hash della pagina del PE SPC Inc** , viene usato il valore impostato con la funzione [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) per questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="3265c-117">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="3265c-118">Il valore predefinito per questa impostazione consiste nell'escludere gli hash di pagina durante la creazione di dati SIP indiretti per i file PE.</span><span class="sxs-lookup"><span data-stu-id="3265c-118">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="3265c-119">Questo valore è definito nel file di intestazione Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="3265c-119">This value is defined in the Mssip.h header file.</span></span><br/> <span data-ttu-id="3265c-120">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3265c-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="3265c-121"><dt>**SPC \_ 0x20 \_ del \_ \_ flag di \_ tabella \_ IND Import PE**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3265c-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="3265c-122">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3265c-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="3265c-123"><dt>**SPC \_ 0x40 \_ di \_ \_ \_ informazioni di debug PE Inc**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3265c-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="3265c-124">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3265c-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="3265c-125"><dt>**SPC \_ 0x80 \_ \_ \_ flag risorse PE incl**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3265c-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="3265c-126">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3265c-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="3265c-127"><dt>**SPC \_ 0x100 \_ del \_ \_ \_ flag di hash delle pagine PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3265c-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="3265c-128">Includere gli hash di pagina quando si creano dati SIP indiretti per il file PE.</span><span class="sxs-lookup"><span data-stu-id="3265c-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="3265c-129">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3265c-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> <span data-ttu-id="3265c-130">Questo valore è definito nel file di intestazione Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="3265c-130">This value is defined in the Mssip.h header file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <span data-ttu-id="3265c-131"><dt>**Firma \_ Aggiungi**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="3265c-131"><dt>**SIG\_APPEND**</dt> <dt>0x1000</dt></span></span> </dl>                                                                         | <span data-ttu-id="3265c-132">La firma verrà nidificata.</span><span class="sxs-lookup"><span data-stu-id="3265c-132">The signature will be nested.</span></span> <span data-ttu-id="3265c-133">Se si imposta questo flag prima che venga aggiunta una firma, la firma generata verrà aggiunta come firma esterna.</span><span class="sxs-lookup"><span data-stu-id="3265c-133">If you set this flag before any signature has been added, the generated signature will be added as the outer signature.</span></span> <span data-ttu-id="3265c-134">Se non si imposta questo flag, la firma generata sostituisce la firma esterna, eliminando tutte le firme interne.</span><span class="sxs-lookup"><span data-stu-id="3265c-134">If you do not set this flag, the generated signature replaces the outer signature, deleting all inner signatures.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="3265c-135">*pSubjectInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3265c-135">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-136">Puntatore a una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che specifica l'oggetto da firmare.</span><span class="sxs-lookup"><span data-stu-id="3265c-136">Pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-137">*pSignerCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3265c-137">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-138">Puntatore a una struttura del certificato del [**firmatario \_**](signer-cert.md) che specifica il certificato da usare per creare la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="3265c-138">Pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-139">*pSignatureInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3265c-139">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-140">Puntatore a una struttura di [**\_ \_ informazioni sulla firma del firmatario**](signer-signature-info.md) che contiene informazioni sulla firma digitale.</span><span class="sxs-lookup"><span data-stu-id="3265c-140">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-141">*pProviderInfo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3265c-141">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-142">Puntatore a una struttura di [**\_ \_ informazioni del provider del firmatario**](signer-provider-info.md) che specifica le informazioni sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e sulla chiave privata utilizzate per creare la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="3265c-142">Pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="3265c-143">Se il valore di questo parametro è **null**, il parametro *pSignerCert* deve specificare un certificato associato a un CSP.</span><span class="sxs-lookup"><span data-stu-id="3265c-143">If the value of this parameter is **NULL**, the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-144">*dwTimestampFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3265c-144">*dwTimestampFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-145">Flag che verranno passati a [**SignerTimeStampEx3**](signertimestampex3.md) se il parametro *PwszHttpTimeStamp* non è **null**.</span><span class="sxs-lookup"><span data-stu-id="3265c-145">Flags that will be passed to [**SignerTimeStampEx3**](signertimestampex3.md) if the *pwszHttpTimeStamp* parameter is not **NULL**.</span></span> <span data-ttu-id="3265c-146">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3265c-146">This can be one of the following values.</span></span>



| <span data-ttu-id="3265c-147">Valore</span><span class="sxs-lookup"><span data-stu-id="3265c-147">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="3265c-148">Significato</span><span class="sxs-lookup"><span data-stu-id="3265c-148">Meaning</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="3265c-149"><dt>**TIMESTAMP del FIRMATARIo \_ \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="3265c-149"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="3265c-150">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3265c-150">Default value.</span></span> <span data-ttu-id="3265c-151">Specifica un timestamp Authenticode.</span><span class="sxs-lookup"><span data-stu-id="3265c-151">Specifies an Authenticode timestamp.</span></span><br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="3265c-152"><dt>**TIMESTAMP del FIRMATARIo \_ \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="3265c-152"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="3265c-153">Specifica un timestamp RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="3265c-153">Specifies an RFC 3161 timestamp.</span></span><br/>                    |



 

<span data-ttu-id="3265c-154">Questo parametro viene ignorato se il parametro *pwszHttpTimeStamp* è **null**.</span><span class="sxs-lookup"><span data-stu-id="3265c-154">This parameter is ignored if the *pwszHttpTimeStamp* parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-155">*pszTimestampAlgorithmOid* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3265c-155">*pszTimestampAlgorithmOid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-156">Identificatore di oggetto dell'algoritmo da usare per la creazione di un timestamp RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="3265c-156">Object identifier of the algorithm to be used for creating an RFC 3161 timestamp.</span></span> <span data-ttu-id="3265c-157">Questo parametro viene ignorato per gli indicatori di data e ora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="3265c-157">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-158">*pwszHttpTimeStamp* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3265c-158">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-159">URL del server di timestamp.</span><span class="sxs-lookup"><span data-stu-id="3265c-159">URL of the time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-160">*psRequest* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3265c-160">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-161">Puntatore a una matrice di strutture degli [**\_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) che vengono aggiunte a una richiesta di firma.</span><span class="sxs-lookup"><span data-stu-id="3265c-161">Pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="3265c-162">Questo parametro viene ignorato se il parametro *pwszHttpTimeStamp* non contiene un valore valido o è **null**.</span><span class="sxs-lookup"><span data-stu-id="3265c-162">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value or is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-163">*pSipData* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3265c-163">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-164">Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP.</span><span class="sxs-lookup"><span data-stu-id="3265c-164">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="3265c-165">Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.</span><span class="sxs-lookup"><span data-stu-id="3265c-165">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-166">*ppSignerContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3265c-166">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-167">Indirizzo di un puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene il [*BLOB*](../secgloss/b-gly.md)firmato.</span><span class="sxs-lookup"><span data-stu-id="3265c-167">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="3265c-168">Al termine dell'uso della struttura del **\_ contesto del firmatario** , liberare la struttura del **\_ contesto del firmatario** chiamando la funzione [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="3265c-168">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-169">*pCryptoPolicy* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3265c-169">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3265c-170">Se presente, puntatore a una struttura [**del \_ \_ segno \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) di firma forte del certificato che contiene i parametri utilizzati per verificare le firme sicure.</span><span class="sxs-lookup"><span data-stu-id="3265c-170">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="3265c-171">Se un certificato o la relativa catena non vengono superati, il file non viene modificato in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="3265c-171">If either a certificate or its chain does not pass, the file is not altered in any way.</span></span> <span data-ttu-id="3265c-172">Se viene passato un URL per specificare un'autorità di certificazione dell'ora (TSA), questo criterio viene applicato anche al timestamp.</span><span class="sxs-lookup"><span data-stu-id="3265c-172">If a URL is passed in to specify a Time Stamping Authority (TSA), this policy is also applied to the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="3265c-173">*Mantenuto*</span><span class="sxs-lookup"><span data-stu-id="3265c-173">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="3265c-174">Riservato.</span><span class="sxs-lookup"><span data-stu-id="3265c-174">Reserved.</span></span> <span data-ttu-id="3265c-175">Questo valore deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3265c-175">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3265c-176">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3265c-176">Return value</span></span>

<span data-ttu-id="3265c-177">Se la funzione ha esito positivo, la funzione restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3265c-177">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="3265c-178">Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="3265c-178">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="3265c-179">I codici di errore possibili restituiti da questa funzione includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="3265c-179">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="3265c-180">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="3265c-180">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



| <span data-ttu-id="3265c-181">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3265c-181">Return code</span></span>                                                                                  | <span data-ttu-id="3265c-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3265c-182">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3265c-183"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3265c-183"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3265c-184">Se si imposta il parametro *dwTimestampFlags* su **Signer \_ timestamp \_ AUTHENTICODE**, non è possibile impostare il parametro *dwFlags* su **sig \_ Append**.</span><span class="sxs-lookup"><span data-stu-id="3265c-184">If you set the *dwTimestampFlags* parameter to **SIGNER\_TIMESTAMP\_AUTHENTICODE**, you cannot set the *dwFlags* parameter to **SIG\_APPEND**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3265c-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3265c-185">Requirements</span></span>



| <span data-ttu-id="3265c-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="3265c-186">Requirement</span></span> | <span data-ttu-id="3265c-187">Valore</span><span class="sxs-lookup"><span data-stu-id="3265c-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3265c-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3265c-188">Minimum supported client</span></span><br/> | <span data-ttu-id="3265c-189">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3265c-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3265c-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3265c-190">Minimum supported server</span></span><br/> | <span data-ttu-id="3265c-191">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3265c-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3265c-192">DLL</span><span class="sxs-lookup"><span data-stu-id="3265c-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3265c-193"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3265c-193"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3265c-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3265c-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3265c-195">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="3265c-195">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="3265c-196">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="3265c-196">**SignerSignEx**</span></span>](signersignex.md)
</dt> <dt>

[<span data-ttu-id="3265c-197">**SignerFreeSignerContext**</span><span class="sxs-lookup"><span data-stu-id="3265c-197">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
