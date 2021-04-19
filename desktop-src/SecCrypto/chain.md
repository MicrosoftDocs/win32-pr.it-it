---
description: Rappresenta una catena di certificati attendibili.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chain (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326769"
---
# <a name="chain-object"></a><span data-ttu-id="2ae04-103">Chain (oggetto)</span><span class="sxs-lookup"><span data-stu-id="2ae04-103">Chain object</span></span>

<span data-ttu-id="2ae04-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2ae04-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2ae04-105">Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2ae04-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2ae04-106">L'oggetto **Chain** rappresenta una catena di certificati attendibili.</span><span class="sxs-lookup"><span data-stu-id="2ae04-106">The **Chain** object represents a certificate trust chain.</span></span>

<span data-ttu-id="2ae04-107">Questo oggetto fornisce proprietà e metodi per compilare una catena di certificati attendibili per verificare la validità dei certificati.</span><span class="sxs-lookup"><span data-stu-id="2ae04-107">This object provides properties and methods to build a certificate trust chain to check the validity of certificates.</span></span> <span data-ttu-id="2ae04-108">La catena viene compilata usando il valore della proprietà [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) e le impostazioni dei criteri di un oggetto [**CertificateStatus**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae04-108">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property value and the policy settings of a [**CertificateStatus**](certificatestatus.md) object.</span></span>

<span data-ttu-id="2ae04-109">L'oggetto **Chain** espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ae04-109">The **Chain** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="2ae04-110">**IChain2**: introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="2ae04-110">**IChain2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="2ae04-111">**IChain**: introdotta in capicol 1,0.</span><span class="sxs-lookup"><span data-stu-id="2ae04-111">**IChain**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2ae04-112">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="2ae04-112">When to use</span></span>

<span data-ttu-id="2ae04-113">L'oggetto **Chain** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ae04-113">The **Chain** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="2ae04-114">Compilare una catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="2ae04-114">Build a certificate trust chain.</span></span>
-   <span data-ttu-id="2ae04-115">Ottenere il OID di tutti i criteri del certificato e dell'applicazione validi per la catena.</span><span class="sxs-lookup"><span data-stu-id="2ae04-115">Obtain the OIDs of all the certificate and application policies valid for the chain.</span></span>
-   <span data-ttu-id="2ae04-116">Verificare lo stato dei certificati nella catena.</span><span class="sxs-lookup"><span data-stu-id="2ae04-116">Verify the status of the certificates in the chain.</span></span>
-   <span data-ttu-id="2ae04-117">Ottenere informazioni estese sull'errore.</span><span class="sxs-lookup"><span data-stu-id="2ae04-117">Obtain extended error information.</span></span>
-   <span data-ttu-id="2ae04-118">Recuperare la raccolta di certificati nella catena.</span><span class="sxs-lookup"><span data-stu-id="2ae04-118">Retrieve the collection of certificates in the chain.</span></span>

## <a name="members"></a><span data-ttu-id="2ae04-119">Membri</span><span class="sxs-lookup"><span data-stu-id="2ae04-119">Members</span></span>

<span data-ttu-id="2ae04-120">L'oggetto **Chain** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2ae04-120">The **Chain** object has these types of members:</span></span>

-   [<span data-ttu-id="2ae04-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="2ae04-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="2ae04-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ae04-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2ae04-123">Metodi</span><span class="sxs-lookup"><span data-stu-id="2ae04-123">Methods</span></span>

<span data-ttu-id="2ae04-124">L'oggetto **Chain** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2ae04-124">The **Chain** object has these methods.</span></span>



| <span data-ttu-id="2ae04-125">Metodo</span><span class="sxs-lookup"><span data-stu-id="2ae04-125">Method</span></span>                                                   | <span data-ttu-id="2ae04-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ae04-126">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ae04-127">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="2ae04-127">**ApplicationPolicies**</span></span>](chain-applicationpolicies.md) | <span data-ttu-id="2ae04-128">Restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri dell'applicazione OID validi per la catena.</span><span class="sxs-lookup"><span data-stu-id="2ae04-128">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="2ae04-129">(Ereditato da **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="2ae04-129">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="2ae04-130">**Compilazione**</span><span class="sxs-lookup"><span data-stu-id="2ae04-130">**Build**</span></span>](chain-build.md)                             | <span data-ttu-id="2ae04-131">Compila una catena di verifica dei certificati da un certificato finale al [*certificato radice*](../secgloss/r-gly.md)attendibile, restituendo un valore booleano che indica la validità complessiva della catena.</span><span class="sxs-lookup"><span data-stu-id="2ae04-131">Builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md), returning a Boolean value that indicates the overall validity of the chain.</span></span><br/> <span data-ttu-id="2ae04-132">(Ereditato da **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="2ae04-132">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="2ae04-133">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="2ae04-133">**CertificatePolicies**</span></span>](chain-certificatepolicies.md) | <span data-ttu-id="2ae04-134">Restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri di certificato OID validi per la catena.</span><span class="sxs-lookup"><span data-stu-id="2ae04-134">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="2ae04-135">(Ereditato da **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="2ae04-135">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="2ae04-136">**ExtendedErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2ae04-136">**ExtendedErrorInfo**</span></span>](chain-extendederrorinfo.md)     | <span data-ttu-id="2ae04-137">Restituisce una stringa che contiene informazioni aggiuntive sull'errore relative alla voce indicizzata.</span><span class="sxs-lookup"><span data-stu-id="2ae04-137">Returns a string that contains additional error information about the indexed entry.</span></span><br/> <span data-ttu-id="2ae04-138">(Ereditato da **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="2ae04-138">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="2ae04-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ae04-139">Properties</span></span>

<span data-ttu-id="2ae04-140">L'oggetto **Chain** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2ae04-140">The **Chain** object has these properties.</span></span>



| <span data-ttu-id="2ae04-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ae04-141">Property</span></span>                                              | <span data-ttu-id="2ae04-142">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2ae04-142">Access type</span></span>          | <span data-ttu-id="2ae04-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ae04-143">Description</span></span>                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ae04-144">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="2ae04-144">**Certificates**</span></span>](chain-certificates.md)<br/> | <span data-ttu-id="2ae04-145">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2ae04-145">Read-only</span></span><br/> | <span data-ttu-id="2ae04-146">Recupera una raccolta di [**certificati**](certificates.md) che rappresenta i certificati nella catena.</span><span class="sxs-lookup"><span data-stu-id="2ae04-146">Retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="2ae04-147">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="2ae04-147">This is the default property.</span></span><br/> <span data-ttu-id="2ae04-148">(Ereditato da **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="2ae04-148">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="2ae04-149">**Stato**</span><span class="sxs-lookup"><span data-stu-id="2ae04-149">**Status**</span></span>](chain-status.md)<br/>             | <span data-ttu-id="2ae04-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2ae04-150">Read-only</span></span><br/> | <span data-ttu-id="2ae04-151">Recupera lo stato di validità della catena o di un certificato specifico nella catena.</span><span class="sxs-lookup"><span data-stu-id="2ae04-151">Retrieves the validity status of the chain or a specific certificate in the chain.</span></span><br/> <span data-ttu-id="2ae04-152">(Ereditato da **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="2ae04-152">(Inherited from **ChainIChain2IChain**)</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="2ae04-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ae04-153">Remarks</span></span>

<span data-ttu-id="2ae04-154">È possibile creare l'oggetto **Chain** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="2ae04-154">The **Chain** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="2ae04-155">Il ProgID per l'oggetto **Chain** è "CAPICOM. Chain. 2 ".</span><span class="sxs-lookup"><span data-stu-id="2ae04-155">The ProgID for the **Chain** object is "CAPICOM.Chain.2".</span></span>

<span data-ttu-id="2ae04-156">**CAPICOM 1. *x*:** il ProgID per l'oggetto **Chain** è capicom. Chain. 1.</span><span class="sxs-lookup"><span data-stu-id="2ae04-156">**CAPICOM 1.*x*:** The ProgID for the **Chain** object is CAPICOM.Chain.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae04-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ae04-157">Requirements</span></span>



| <span data-ttu-id="2ae04-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae04-158">Requirement</span></span> | <span data-ttu-id="2ae04-159">Valore</span><span class="sxs-lookup"><span data-stu-id="2ae04-159">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae04-160">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2ae04-160">End of client support</span></span><br/> | <span data-ttu-id="2ae04-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ae04-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2ae04-162">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2ae04-162">End of server support</span></span><br/> | <span data-ttu-id="2ae04-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ae04-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2ae04-164">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="2ae04-164">Redistributable</span></span><br/>       | <span data-ttu-id="2ae04-165">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ae04-165">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2ae04-166">DLL</span><span class="sxs-lookup"><span data-stu-id="2ae04-166">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2ae04-167"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ae04-167"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ae04-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ae04-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae04-169">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="2ae04-169">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
