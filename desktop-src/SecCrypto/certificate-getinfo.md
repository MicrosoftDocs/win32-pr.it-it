---
description: Recupera le informazioni dal certificato.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'Metodo ICertificate2:: GetInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325606"
---
# <a name="icertificate2getinfo-method"></a><span data-ttu-id="3f359-103">Metodo ICertificate2:: GetInfo</span><span class="sxs-lookup"><span data-stu-id="3f359-103">ICertificate2::GetInfo method</span></span>

<span data-ttu-id="3f359-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f359-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3f359-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3f359-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3f359-106">Il metodo **GetInfo** recupera le informazioni dal [*certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3f359-106">The **GetInfo** method retrieves information from the [*certificate*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f359-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f359-107">Syntax</span></span>


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a><span data-ttu-id="3f359-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f359-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f359-109">*InfoType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f359-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f359-110">Valore dell'enumerazione del [**\_ \_ \_ tipo di informazioni del certificato capicol**](capicom-cert-info-type.md) che specifica il tipo di dati che viene recuperato dal certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-110">A value of the [**CAPICOM\_CERT\_INFO\_TYPE**](capicom-cert-info-type.md) enumeration that specifies what type of data is retrieved from the certificate.</span></span> <span data-ttu-id="3f359-111">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="3f359-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="3f359-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3f359-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="3f359-113">Significato</span><span class="sxs-lookup"><span data-stu-id="3f359-113">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <span data-ttu-id="3f359-114"><dt>**\_ \_ \_ \_ nome semplice soggetto informazioni sul certificato capicot \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-114"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</dt></span></span> </dl> | <span data-ttu-id="3f359-115">Restituisce il nome visualizzato dal soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-115">Returns the display name from the certificate subject.</span></span><br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <span data-ttu-id="3f359-116"><dt>**\_ \_ \_ nome semplice dell'emittente informazioni \_ sul certificato capicot \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-116"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="3f359-117">Restituisce il nome visualizzato dell'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-117">Returns the display name of the issuer of the certificate.</span></span><br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <span data-ttu-id="3f359-118"><dt>**\_ \_ \_ nome di \_ posta elettronica dell'oggetto \_ del certificato di capicol**</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-118"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="3f359-119">Restituisce l'indirizzo di posta elettronica del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-119">Returns the email address of the certificate subject.</span></span><br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <span data-ttu-id="3f359-120"><dt>**\_ \_ \_ nome di \_ posta elettronica dell'autorità emittente informazioni sul certificato CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-120"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</dt></span></span> </dl>       | <span data-ttu-id="3f359-121">Restituisce l'indirizzo di posta elettronica dell'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-121">Returns the email address of the issuer of the certificate.</span></span><br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <span data-ttu-id="3f359-122"><dt>**nome \_ \_ \_ UPN oggetto informazioni del certificato \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-122"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</dt></span></span> </dl>                          | <span data-ttu-id="3f359-123">Restituisce l'UPN dell'oggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-123">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="3f359-124">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="3f359-124">Introduced in CAPICOM 2.0.</span></span><br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <span data-ttu-id="3f359-125"><dt>**nome UPN dell' \_ \_ \_ autorità emittente informazioni sul certificato capicot \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-125"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</dt></span></span> </dl>                             | <span data-ttu-id="3f359-126">Restituisce l'UPN dell'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="3f359-127">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="3f359-127">Introduced in CAPICOM 2.0.</span></span><br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <span data-ttu-id="3f359-128"><dt>**\_ \_ \_ nome DNS dell'oggetto informazioni \_ sul certificato capicol \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-128"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="3f359-129">Restituisce il nome DNS del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-129">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="3f359-130">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="3f359-130">Introduced in CAPICOM 2.0.</span></span><br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <span data-ttu-id="3f359-131"><dt>**\_ \_ \_ nome DNS dell'autorità emittente informazioni sul \_ certificato \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-131"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</dt></span></span> </dl>             | <span data-ttu-id="3f359-132">Restituisce il nome DNS dell'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="3f359-132">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="3f359-133">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="3f359-133">Introduced in CAPICOM 2.0.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f359-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f359-134">Return value</span></span>

<span data-ttu-id="3f359-135">Stringa che contiene le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="3f359-135">A string that contains the requested information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f359-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f359-136">Requirements</span></span>



| <span data-ttu-id="3f359-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f359-137">Requirement</span></span> | <span data-ttu-id="3f359-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3f359-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f359-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3f359-139">End of client support</span></span><br/> | <span data-ttu-id="3f359-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f359-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3f359-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="3f359-141">End of server support</span></span><br/> | <span data-ttu-id="3f359-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f359-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3f359-143">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3f359-143">Redistributable</span></span><br/>       | <span data-ttu-id="3f359-144">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="3f359-144">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3f359-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3f359-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3f359-146"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f359-146"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f359-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f359-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f359-148">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="3f359-148">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="3f359-149">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="3f359-149">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
