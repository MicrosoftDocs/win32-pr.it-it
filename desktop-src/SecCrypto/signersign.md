---
description: Firma il file specificato.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314690"
---
# <a name="signersign-function"></a><span data-ttu-id="48fce-103">SignerSign (funzione)</span><span class="sxs-lookup"><span data-stu-id="48fce-103">SignerSign function</span></span>

<span data-ttu-id="48fce-104">La funzione **SignerSign** firma il file specificato.</span><span class="sxs-lookup"><span data-stu-id="48fce-104">The **SignerSign** function signs the specified file.</span></span>

> [!Note]  
> <span data-ttu-id="48fce-105">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="48fce-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="48fce-106">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="48fce-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="48fce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48fce-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="48fce-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="48fce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48fce-109">*pSubjectInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48fce-109">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48fce-110">Puntatore a una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che specifica l'oggetto da firmare.</span><span class="sxs-lookup"><span data-stu-id="48fce-110">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="48fce-111">*pSignerCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48fce-111">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48fce-112">Puntatore a una struttura del certificato del [**firmatario \_**](signer-cert.md) che specifica il certificato da usare per creare la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="48fce-112">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="48fce-113">*pSignatureInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48fce-113">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48fce-114">Puntatore a una struttura di [**\_ \_ informazioni sulla firma del firmatario**](signer-signature-info.md) che contiene informazioni sulla firma digitale.</span><span class="sxs-lookup"><span data-stu-id="48fce-114">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="48fce-115">*pProviderInfo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="48fce-115">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48fce-116">Puntatore a una struttura di [**\_ \_ informazioni del provider del firmatario**](signer-provider-info.md) che specifica le informazioni sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e sulla [*chiave privata*](../secgloss/p-gly.md) utilizzate per creare la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="48fce-116">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and [*private key*](../secgloss/p-gly.md) information used to create the digital signature.</span></span>

<span data-ttu-id="48fce-117">Se il valore di questo parametro è **null**, il valore del parametro *pSignerCert* deve specificare un certificato associato a un CSP.</span><span class="sxs-lookup"><span data-stu-id="48fce-117">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="48fce-118">*pwszHttpTimeStamp* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="48fce-118">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48fce-119">URL di un server di timestamp.</span><span class="sxs-lookup"><span data-stu-id="48fce-119">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="48fce-120">*psRequest* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="48fce-120">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48fce-121">Puntatore a una matrice di strutture [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) che vengono aggiunte a una richiesta di firma.</span><span class="sxs-lookup"><span data-stu-id="48fce-121">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="48fce-122">Questo parametro viene ignorato se il parametro *pwszHttpTimeStamp* non contiene un valore valido che non è **null**.</span><span class="sxs-lookup"><span data-stu-id="48fce-122">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48fce-123">*pSipData* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="48fce-123">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48fce-124">Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP.</span><span class="sxs-lookup"><span data-stu-id="48fce-124">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="48fce-125">Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.</span><span class="sxs-lookup"><span data-stu-id="48fce-125">The format and content of this is defined by the SIP provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48fce-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48fce-126">Return value</span></span>

<span data-ttu-id="48fce-127">Se la funzione ha esito positivo, la funzione restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48fce-127">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="48fce-128">Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="48fce-128">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="48fce-129">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="48fce-129">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48fce-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48fce-130">Requirements</span></span>



| <span data-ttu-id="48fce-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="48fce-131">Requirement</span></span> | <span data-ttu-id="48fce-132">Valore</span><span class="sxs-lookup"><span data-stu-id="48fce-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48fce-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48fce-133">Minimum supported client</span></span><br/> | <span data-ttu-id="48fce-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="48fce-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="48fce-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48fce-135">Minimum supported server</span></span><br/> | <span data-ttu-id="48fce-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48fce-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48fce-137">DLL</span><span class="sxs-lookup"><span data-stu-id="48fce-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48fce-138"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48fce-138"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48fce-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48fce-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48fce-140">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="48fce-140">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
