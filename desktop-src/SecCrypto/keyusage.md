---
description: Fornisce accesso in sola lettura alle proprietà di utilizzo delle chiavi di un certificato.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: DataUsage (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323944"
---
# <a name="keyusage-object"></a><span data-ttu-id="43e86-103">DataUsage (oggetto)</span><span class="sxs-lookup"><span data-stu-id="43e86-103">KeyUsage object</span></span>

<span data-ttu-id="43e86-104">\[L'oggetto **DataUsage** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="43e86-104">\[The **KeyUsage** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="43e86-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="43e86-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="43e86-106">L'oggetto **DataUsage** fornisce accesso in sola lettura alle proprietà di utilizzo delle chiavi di un certificato.</span><span class="sxs-lookup"><span data-stu-id="43e86-106">The **KeyUsage** object provides read-only access to key usage properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="43e86-107">Membri</span><span class="sxs-lookup"><span data-stu-id="43e86-107">Members</span></span>

<span data-ttu-id="43e86-108">L'oggetto **DataUsage** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="43e86-108">The **KeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="43e86-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43e86-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43e86-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43e86-110">Properties</span></span>

<span data-ttu-id="43e86-111">L'oggetto **DataUsage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="43e86-111">The **KeyUsage** object has these properties.</span></span>



| <span data-ttu-id="43e86-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43e86-112">Property</span></span>                                                                           | <span data-ttu-id="43e86-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="43e86-113">Access type</span></span>          | <span data-ttu-id="43e86-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43e86-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43e86-115">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="43e86-115">**IsCritical**</span></span>](keyusage-iscritical.md)<br/>                               | <span data-ttu-id="43e86-116">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-116">Read-only</span></span><br/> | <span data-ttu-id="43e86-117">Recupera un valore booleano che indica se l'estensione per l' **utilizzo dei dati** è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="43e86-117">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is marked critical.</span></span><br/>                                  |
| [<span data-ttu-id="43e86-118">**IsCRLSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-118">**IsCRLSignEnabled**</span></span>](keyusage-iscrlsignenabled.md)<br/>                   | <span data-ttu-id="43e86-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-119">Read-only</span></span><br/> | <span data-ttu-id="43e86-120">Recupera un valore booleano che indica se il bit bit crlsign è impostato.</span><span class="sxs-lookup"><span data-stu-id="43e86-120">Retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span><br/>                                                         |
| [<span data-ttu-id="43e86-121">**IsDataEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-121">**IsDataEnciphermentEnabled**</span></span>](keyusage-isdataenciphermentenabled.md)<br/> | <span data-ttu-id="43e86-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-122">Read-only</span></span><br/> | <span data-ttu-id="43e86-123">Recupera un valore booleano che indica se il bit dataEncipherment è impostato.</span><span class="sxs-lookup"><span data-stu-id="43e86-123">Retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="43e86-124">**IsDecipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-124">**IsDecipherOnlyEnabled**</span></span>](keyusage-isdecipheronlyenabled.md)<br/>         | <span data-ttu-id="43e86-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-125">Read-only</span></span><br/> | <span data-ttu-id="43e86-126">Recupera un valore booleano che indica se il bit decipherOnly è impostato.</span><span class="sxs-lookup"><span data-stu-id="43e86-126">Retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="43e86-127">**IsDigitalSignatureEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-127">**IsDigitalSignatureEnabled**</span></span>](keyusage-isdigitalsignatureenabled.md)<br/> | <span data-ttu-id="43e86-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-128">Read-only</span></span><br/> | <span data-ttu-id="43e86-129">Recupera un valore booleano che indica se il bit digitalSignature è impostato.</span><span class="sxs-lookup"><span data-stu-id="43e86-129">Retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="43e86-130">**IsEncipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-130">**IsEncipherOnlyEnabled**</span></span>](keyusage-isencipheronlyenabled.md)<br/>         | <span data-ttu-id="43e86-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-131">Read-only</span></span><br/> | <span data-ttu-id="43e86-132">Recupera un valore booleano che indica se il bit encipherOnly è impostato.</span><span class="sxs-lookup"><span data-stu-id="43e86-132">Retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="43e86-133">**IsKeyAgreementEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-133">**IsKeyAgreementEnabled**</span></span>](keyusage-iskeyagreementenabled.md)<br/>         | <span data-ttu-id="43e86-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-134">Read-only</span></span><br/> | <span data-ttu-id="43e86-135">Recupera un valore booleano che indica se è stato impostato il bit di un contratto.</span><span class="sxs-lookup"><span data-stu-id="43e86-135">Retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="43e86-136">**IsKeyCertSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-136">**IsKeyCertSignEnabled**</span></span>](keyusage-iskeycertsignenabled.md)<br/>           | <span data-ttu-id="43e86-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-137">Read-only</span></span><br/> | <span data-ttu-id="43e86-138">Recupera un valore booleano che indica se il bit bit keycertsign è impostato.</span><span class="sxs-lookup"><span data-stu-id="43e86-138">Retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span><br/>                                                     |
| [<span data-ttu-id="43e86-139">**IsKeyEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-139">**IsKeyEnciphermentEnabled**</span></span>](keyusage-iskeyenciphermentenabled.md)<br/>   | <span data-ttu-id="43e86-140">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-140">Read-only</span></span><br/> | <span data-ttu-id="43e86-141">Recupera un valore booleano che indica se il bit keyEncipherment è impostato.</span><span class="sxs-lookup"><span data-stu-id="43e86-141">Retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span><br/>                                                 |
| [<span data-ttu-id="43e86-142">**IsNonRepudiationEnabled**</span><span class="sxs-lookup"><span data-stu-id="43e86-142">**IsNonRepudiationEnabled**</span></span>](keyusage-isnonrepudiationenabled.md)<br/>     | <span data-ttu-id="43e86-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-143">Read-only</span></span><br/> | <span data-ttu-id="43e86-144">Recupera un valore booleano che indica se il bit nonRepudiationEnabled è impostato.</span><span class="sxs-lookup"><span data-stu-id="43e86-144">Retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span><br/>                                           |
| [<span data-ttu-id="43e86-145">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="43e86-145">**IsPresent**</span></span>](keyusage-ispresent.md)<br/>                                 | <span data-ttu-id="43e86-146">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e86-146">Read-only</span></span><br/> | <span data-ttu-id="43e86-147">Recupera un valore booleano che indica se l'estensione per l' **utilizzo di dati** è presente.</span><span class="sxs-lookup"><span data-stu-id="43e86-147">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is present.</span></span><br/> <span data-ttu-id="43e86-148">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="43e86-148">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43e86-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="43e86-149">Remarks</span></span>

<span data-ttu-id="43e86-150">Impossibile creare l'oggetto **DataUsage** .</span><span class="sxs-lookup"><span data-stu-id="43e86-150">The **KeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e86-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43e86-151">Requirements</span></span>



| <span data-ttu-id="43e86-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e86-152">Requirement</span></span> | <span data-ttu-id="43e86-153">Valore</span><span class="sxs-lookup"><span data-stu-id="43e86-153">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43e86-154">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="43e86-154">Redistributable</span></span><br/> | <span data-ttu-id="43e86-155">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="43e86-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="43e86-156">DLL</span><span class="sxs-lookup"><span data-stu-id="43e86-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="43e86-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43e86-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e86-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43e86-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e86-159">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="43e86-159">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
