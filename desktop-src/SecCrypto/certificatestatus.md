---
description: Contiene informazioni sulla creazione di una catena di certificati.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Oggetto CertificateStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e9a6cb31a00f4d2943e68670930e6cbc4436b6b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326528"
---
# <a name="certificatestatus-object"></a><span data-ttu-id="cd59f-103">Oggetto CertificateStatus</span><span class="sxs-lookup"><span data-stu-id="cd59f-103">CertificateStatus object</span></span>

<span data-ttu-id="cd59f-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd59f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cd59f-105">Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cd59f-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cd59f-106">L'oggetto **CertificateStatus** contiene informazioni su come costruire una catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="cd59f-106">The **CertificateStatus** object contains information about how to construct a certificate trust chain.</span></span>

## <a name="members"></a><span data-ttu-id="cd59f-107">Membri</span><span class="sxs-lookup"><span data-stu-id="cd59f-107">Members</span></span>

<span data-ttu-id="cd59f-108">L'oggetto **CertificateStatus** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cd59f-108">The **CertificateStatus** object has these types of members:</span></span>

-   [<span data-ttu-id="cd59f-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="cd59f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd59f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd59f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd59f-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="cd59f-111">Methods</span></span>

<span data-ttu-id="cd59f-112">L'oggetto **CertificateStatus** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cd59f-112">The **CertificateStatus** object has these methods.</span></span>



| <span data-ttu-id="cd59f-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="cd59f-113">Method</span></span>                                                               | <span data-ttu-id="cd59f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd59f-114">Description</span></span>                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd59f-115">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="cd59f-115">**ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md) | <span data-ttu-id="cd59f-116">Restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri di applicazione OID.</span><span class="sxs-lookup"><span data-stu-id="cd59f-116">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs.</span></span><br/>                                           |
| [<span data-ttu-id="cd59f-117">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="cd59f-117">**CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md) | <span data-ttu-id="cd59f-118">Restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri di certificato OID utilizzati durante la creazione della catena.</span><span class="sxs-lookup"><span data-stu-id="cd59f-118">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs used during chain building.</span></span><br/>                |
| [<span data-ttu-id="cd59f-119">**EKU**</span><span class="sxs-lookup"><span data-stu-id="cd59f-119">**EKU**</span></span>](certificatestatus-eku.md)                                 | <span data-ttu-id="cd59f-120">Restituisce l'oggetto [**EKU**](eku.md) utilizzato per impostare gli elementi EKU da archiviare per stabilire lo stato di validità di un certificato.</span><span class="sxs-lookup"><span data-stu-id="cd59f-120">Returns the [**EKU**](eku.md) object used to set the EKU elements to be checked in establishing a certificate's validity status.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cd59f-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd59f-121">Properties</span></span>

<span data-ttu-id="cd59f-122">L'oggetto **CertificateStatus** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd59f-122">The **CertificateStatus** object has these properties.</span></span>



| <span data-ttu-id="cd59f-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd59f-123">Property</span></span>                                                                        | <span data-ttu-id="cd59f-124">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="cd59f-124">Access type</span></span>           | <span data-ttu-id="cd59f-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd59f-125">Description</span></span>                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd59f-126">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="cd59f-126">**Certificates**</span></span>](certificatestatus-certificates.md)<br/>               | <span data-ttu-id="cd59f-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="cd59f-127">Read/write</span></span><br/> | <span data-ttu-id="cd59f-128">Imposta o recupera la raccolta di certificati che possono essere utilizzati per compilare la catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="cd59f-128">Sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span><br/> <span data-ttu-id="cd59f-129">**CAPICOM 2.0.0.3 e versioni precedenti:** La proprietà [**Certificates**](certificatestatus-certificates.md) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="cd59f-129">**CAPICOM 2.0.0.3 and earlier:** The [**Certificates**](certificatestatus-certificates.md) property is not supported.</span></span><br/>                    |
| [<span data-ttu-id="cd59f-130">**CheckFlag**</span><span class="sxs-lookup"><span data-stu-id="cd59f-130">**CheckFlag**</span></span>](certificatestatus-checkflag.md)<br/>                     | <span data-ttu-id="cd59f-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="cd59f-131">Read/write</span></span><br/> | <span data-ttu-id="cd59f-132">Flag di verifica validità.</span><span class="sxs-lookup"><span data-stu-id="cd59f-132">Validity check flag.</span></span> <span data-ttu-id="cd59f-133">I valori possono essere Uniti tramite **un operatore OR** logico.</span><span class="sxs-lookup"><span data-stu-id="cd59f-133">Values can be joined by using a logical **OR** operator.</span></span> <span data-ttu-id="cd59f-134">Il flag di controllo predefinito è [**CAPICOM \_ controllare \_ \_ tutti online**](capicom-check-flag.md).</span><span class="sxs-lookup"><span data-stu-id="cd59f-134">The default check flag is [**CAPICOM\_CHECK\_ONLINE\_ALL**](capicom-check-flag.md).</span></span><br/>                                                                                     |
| [<span data-ttu-id="cd59f-135">**Risultato**</span><span class="sxs-lookup"><span data-stu-id="cd59f-135">**Result**</span></span>](certificatestatus-result.md)<br/>                           | <span data-ttu-id="cd59f-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd59f-136">Read-only</span></span><br/>  | <span data-ttu-id="cd59f-137">Indica se il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="cd59f-137">Indicates whether the certificate is valid.</span></span> <span data-ttu-id="cd59f-138">La validità del certificato viene controllata usando l'impostazione corrente della proprietà [**CheckFlag**](certificatestatus-checkflag.md) e le impostazioni dei criteri del certificato.</span><span class="sxs-lookup"><span data-stu-id="cd59f-138">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the policy settings of the certificate.</span></span> <span data-ttu-id="cd59f-139">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="cd59f-139">This is the default property.</span></span><br/> |
| [<span data-ttu-id="cd59f-140">**UrlRetrievalTimeout**</span><span class="sxs-lookup"><span data-stu-id="cd59f-140">**UrlRetrievalTimeout**</span></span>](certificatestatus-urlretrievaltimeout.md)<br/> | <span data-ttu-id="cd59f-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="cd59f-141">Read/write</span></span><br/> | <span data-ttu-id="cd59f-142">Imposta o recupera l'intervallo di tempo prima che un URL venga determinato come irraggiungibile.</span><span class="sxs-lookup"><span data-stu-id="cd59f-142">Sets or retrieves the length of time before a URL is determined to be unreachable.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="cd59f-143">**VerificationTime**</span><span class="sxs-lookup"><span data-stu-id="cd59f-143">**VerificationTime**</span></span>](certificatestatus-verificationtime.md)<br/>       | <span data-ttu-id="cd59f-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="cd59f-144">Read/write</span></span><br/> | <span data-ttu-id="cd59f-145">Imposta o recupera l'ora in cui il certificato è stato verificato.</span><span class="sxs-lookup"><span data-stu-id="cd59f-145">Sets or retrieves the time that the certificate was verified.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="cd59f-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd59f-146">Remarks</span></span>

<span data-ttu-id="cd59f-147">Impossibile creare l'oggetto **CertificateStatus** .</span><span class="sxs-lookup"><span data-stu-id="cd59f-147">The **CertificateStatus** object cannot be created.</span></span>

<span data-ttu-id="cd59f-148">L'oggetto **CertificateStatus** viene restituito dal metodo [**Certificate. IsValid**](certificate-isvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="cd59f-148">The **CertificateStatus** object is returned by the [**Certificate.IsValid**](certificate-isvalid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd59f-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd59f-149">Requirements</span></span>



| <span data-ttu-id="cd59f-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd59f-150">Requirement</span></span> | <span data-ttu-id="cd59f-151">Valore</span><span class="sxs-lookup"><span data-stu-id="cd59f-151">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd59f-152">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cd59f-152">End of client support</span></span><br/> | <span data-ttu-id="cd59f-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd59f-153">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cd59f-154">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="cd59f-154">End of server support</span></span><br/> | <span data-ttu-id="cd59f-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd59f-155">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cd59f-156">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cd59f-156">Redistributable</span></span><br/>       | <span data-ttu-id="cd59f-157">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd59f-157">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cd59f-158">DLL</span><span class="sxs-lookup"><span data-stu-id="cd59f-158">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cd59f-159"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd59f-159"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd59f-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd59f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd59f-161">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="cd59f-161">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="cd59f-162">**Catena**</span><span class="sxs-lookup"><span data-stu-id="cd59f-162">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
