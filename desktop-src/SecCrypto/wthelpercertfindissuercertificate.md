---
description: Trova un certificato dell'autorità emittente dagli archivi certificati specificati che corrisponde al certificato dell'oggetto specificato.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231701"
---
# <a name="wthelpercertfindissuercertificate-function"></a><span data-ttu-id="93235-103">WTHelperCertFindIssuerCertificate (funzione)</span><span class="sxs-lookup"><span data-stu-id="93235-103">WTHelperCertFindIssuerCertificate function</span></span>

<span data-ttu-id="93235-104">\[La funzione **WTHelperCertFindIssuerCertificate** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="93235-104">\[The **WTHelperCertFindIssuerCertificate** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="93235-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="93235-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="93235-106">La funzione **WTHelperCertFindIssuerCertificate** trova un certificato dell'autorità emittente dagli archivi certificati specificati che corrisponde al certificato dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="93235-106">The **WTHelperCertFindIssuerCertificate** function finds an issuer certificate from the specified certificate stores that matches the specified subject certificate.</span></span>

> [!Note]  
> <span data-ttu-id="93235-107">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="93235-107">This function has no associated import library.</span></span> <span data-ttu-id="93235-108">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Wintrust.dll.</span><span class="sxs-lookup"><span data-stu-id="93235-108">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="93235-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93235-109">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a><span data-ttu-id="93235-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="93235-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93235-111">*pChildContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93235-111">*pChildContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93235-112">Certificato dell'oggetto per il quale trovare un certificato dell'autorità emittente corrispondente.</span><span class="sxs-lookup"><span data-stu-id="93235-112">The subject certificate for which to find a matching issuer certificate.</span></span>

</dd> <dt>

<span data-ttu-id="93235-113">*chStores* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93235-113">*chStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93235-114">Numero di elementi nella matrice *pahStores* .</span><span class="sxs-lookup"><span data-stu-id="93235-114">The number of elements in the *pahStores* array.</span></span>

</dd> <dt>

<span data-ttu-id="93235-115">*pahStores* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93235-115">*pahStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93235-116">Matrice di archivi certificati in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="93235-116">An array of certificate stores in which to search.</span></span>

</dd> <dt>

<span data-ttu-id="93235-117">*psftVerifyAsOf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93235-117">*psftVerifyAsOf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93235-118">Ora della verifica.</span><span class="sxs-lookup"><span data-stu-id="93235-118">The time of verification.</span></span>

</dd> <dt>

<span data-ttu-id="93235-119">*dwEncoding* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93235-119">*dwEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93235-120">Valore **DWORD** che specifica i tipi di codifica del certificato da verificare.</span><span class="sxs-lookup"><span data-stu-id="93235-120">A **DWORD** value that specifies the encoding types of the certificate to check.</span></span> <span data-ttu-id="93235-121">Per informazioni sui possibili tipi di codifica, vedere [tipi di codifica di certificati e messaggi](certificate-and-message-encoding-types.md).</span><span class="sxs-lookup"><span data-stu-id="93235-121">For information about possible encoding types, see [Certificate and Message Encoding Types](certificate-and-message-encoding-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="93235-122">*pdwConfidence* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="93235-122">*pdwConfidence* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93235-123">Questo parametro può essere una combinazione bit per bit di zero o più dei valori di confidenza seguenti.</span><span class="sxs-lookup"><span data-stu-id="93235-123">This parameter can be a bitwise combination of zero or more of the following confidence values.</span></span>



| <span data-ttu-id="93235-124">Valore</span><span class="sxs-lookup"><span data-stu-id="93235-124">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="93235-125">Significato</span><span class="sxs-lookup"><span data-stu-id="93235-125">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <span data-ttu-id="93235-126"><dt>**Certificato \_ \_Firma di sicurezza**</dt> <dt> 0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="93235-126"><dt>**CERT\_CONFIDENCE\_SIG**</dt> <dt> 0x10000000</dt></span></span> </dl>                     | <span data-ttu-id="93235-127">La firma del certificato è valida.</span><span class="sxs-lookup"><span data-stu-id="93235-127">The signature of the certificate is valid.</span></span><br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <span data-ttu-id="93235-128"><dt>**Certificato \_ \_Tempo di confidenza**</dt> <dt> 0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="93235-128"><dt>**CERT\_CONFIDENCE\_TIME**</dt> <dt> 0x01000000</dt></span></span> </dl>                  | <span data-ttu-id="93235-129">Il tempo dell'emittente del certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="93235-129">The time of the certificate issuer is valid.</span></span><br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <span data-ttu-id="93235-130"><dt>0x00100000</dt> di <dt> **sicurezza del certificato \_ \_ TIMENEST**</dt></span><span class="sxs-lookup"><span data-stu-id="93235-130"><dt> **CERT\_CONFIDENCE\_TIMENEST**</dt> <dt>0x00100000</dt></span></span> </dl>    | <span data-ttu-id="93235-131">L'ora del certificato è valida.</span><span class="sxs-lookup"><span data-stu-id="93235-131">The time of the certificate is valid.</span></span><br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <span data-ttu-id="93235-132"><dt>0x00010000</dt> di <dt> **sicurezza del certificato \_ \_ AUTHIDEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="93235-132"><dt> **CERT\_CONFIDENCE\_AUTHIDEXT**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="93235-133">Estensione ID autorità valida.</span><span class="sxs-lookup"><span data-stu-id="93235-133">The authority ID extension is valid.</span></span><br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <span data-ttu-id="93235-134"><dt>0x00001000</dt> <dt> **\_ \_ igiene certificati attendibilità**</dt></span><span class="sxs-lookup"><span data-stu-id="93235-134"><dt> **CERT\_CONFIDENCE\_HYGIENE**</dt> <dt>0x00001000</dt></span></span> </dl>       | <span data-ttu-id="93235-135">Come minimo, la firma del certificato e l'estensione ID autorità sono validi.</span><span class="sxs-lookup"><span data-stu-id="93235-135">At a minimum, the signature of the certificate and authority ID extension are valid.</span></span><br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <span data-ttu-id="93235-136"><dt>0x11111000</dt> di <dt> **sicurezza del certificato \_ \_ più alto**</dt></span><span class="sxs-lookup"><span data-stu-id="93235-136"><dt> **CERT\_CONFIDENCE\_HIGHEST**</dt> <dt>0x11111000</dt></span></span> </dl>       | <span data-ttu-id="93235-137">Combinazione di tutti gli altri valori di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="93235-137">A combination of all of the other confidence values.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="93235-138">*dwError* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="93235-138">*dwError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93235-139">Puntatore a una variabile **DWORD** che contiene il valore di errore per il certificato, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="93235-139">A pointer to a **DWORD** variable that contains the error value for this certificate, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93235-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93235-140">Return value</span></span>

<span data-ttu-id="93235-141">Un certificato dell'autorità emittente che corrisponde al certificato dell'oggetto specificato dal parametro *pChildContext* .</span><span class="sxs-lookup"><span data-stu-id="93235-141">An issuer certificate that matches the subject certificate specified by the *pChildContext* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="93235-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="93235-142">Remarks</span></span>

<span data-ttu-id="93235-143">Per trovare correttamente un certificato dell'autorità emittente corrispondente, è necessario soddisfare i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="93235-143">To successfully find a matching issuer certificate, the following requirements must be met:</span></span>

-   <span data-ttu-id="93235-144">La firma del certificato dell'oggetto specificato dal parametro *pChildContext* deve essere valida.</span><span class="sxs-lookup"><span data-stu-id="93235-144">The signature of the subject certificate specified by the *pChildContext* parameter must be valid.</span></span>
-   <span data-ttu-id="93235-145">Il membro **rgExtension** del membro **PCertInfo** del parametro *pChildContext* deve contenere una struttura [**\_ \_ \_ \_ info ID chiave dell'autorità di certificazione**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) .</span><span class="sxs-lookup"><span data-stu-id="93235-145">The **rgExtension** member of the **pCertInfo** member of the *pChildContext* parameter must contain a [**CERT\_AUTHORITY\_KEY\_ID\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) structure.</span></span> <span data-ttu-id="93235-146">I membri di **CertIssuer** e **CertSerialMember** di questa struttura corrispondono in gran parte ai membri corrispondenti per il certificato dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="93235-146">The **CertIssuer** and **CertSerialMember** members of this structure much match the corresponding members for the issuer certificate.</span></span>
-   <span data-ttu-id="93235-147">Il valore del parametro *psftVerifyAsOf* deve essere compreso nel periodo di validità del certificato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93235-147">The value of the *psftVerifyAsOf* parameter must be within the period of validity of the subject certificate.</span></span>
-   <span data-ttu-id="93235-148">Il periodo di validità del certificato del soggetto deve essere compreso nel periodo di validità del certificato dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="93235-148">The period of validity of the subject certificate must be within the period of validity of the issuer certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="93235-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93235-149">Requirements</span></span>



| <span data-ttu-id="93235-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="93235-150">Requirement</span></span> | <span data-ttu-id="93235-151">Valore</span><span class="sxs-lookup"><span data-stu-id="93235-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93235-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93235-152">Minimum supported client</span></span><br/> | <span data-ttu-id="93235-153">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93235-153">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="93235-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93235-154">Minimum supported server</span></span><br/> | <span data-ttu-id="93235-155">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93235-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93235-156">DLL</span><span class="sxs-lookup"><span data-stu-id="93235-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93235-157"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93235-157"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
