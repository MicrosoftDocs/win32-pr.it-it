---
description: Fornisce accesso in sola lettura alle proprietà dell'utilizzo chiavi avanzato (EKU) di un certificato.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Oggetto ExtendedKeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330133"
---
# <a name="extendedkeyusage-object"></a><span data-ttu-id="951a5-103">Oggetto ExtendedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="951a5-103">ExtendedKeyUsage object</span></span>

<span data-ttu-id="951a5-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="951a5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="951a5-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="951a5-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="951a5-106">L'oggetto **ExtendedKeyUsage** fornisce accesso in sola lettura alle proprietà di utilizzo chiavi avanzato (EKU) di un certificato.</span><span class="sxs-lookup"><span data-stu-id="951a5-106">The **ExtendedKeyUsage** object provides read-only access to the extended key usage (EKU) properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="951a5-107">Membri</span><span class="sxs-lookup"><span data-stu-id="951a5-107">Members</span></span>

<span data-ttu-id="951a5-108">L'oggetto **ExtendedKeyUsage** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="951a5-108">The **ExtendedKeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="951a5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="951a5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="951a5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="951a5-110">Properties</span></span>

<span data-ttu-id="951a5-111">L'oggetto **ExtendedKeyUsage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="951a5-111">The **ExtendedKeyUsage** object has these properties.</span></span>



| <span data-ttu-id="951a5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="951a5-112">Property</span></span>                                                     | <span data-ttu-id="951a5-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="951a5-113">Access type</span></span>          | <span data-ttu-id="951a5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="951a5-114">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="951a5-115">**EKU**</span><span class="sxs-lookup"><span data-stu-id="951a5-115">**EKUs**</span></span>](extendedkeyusage-ekus.md)<br/>             | <span data-ttu-id="951a5-116">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="951a5-116">Read-only</span></span><br/> | <span data-ttu-id="951a5-117">Raccolta [**EKU**](ekus.md) che contiene gli oggetti [**EKU**](eku.md) per il certificato.</span><span class="sxs-lookup"><span data-stu-id="951a5-117">[**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span><br/>                            |
| [<span data-ttu-id="951a5-118">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="951a5-118">**IsCritical**</span></span>](extendedkeyusage-iscritical.md)<br/> | <span data-ttu-id="951a5-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="951a5-119">Read-only</span></span><br/> | <span data-ttu-id="951a5-120">Recupera un valore **booleano** che indica se l'estensione EKU è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="951a5-120">Retrieves a **Boolean** value that indicates whether the EKU extension is marked critical.</span></span><br/>                                   |
| [<span data-ttu-id="951a5-121">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="951a5-121">**IsPresent**</span></span>](extendedkeyusage-ispresent.md)<br/>   | <span data-ttu-id="951a5-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="951a5-122">Read-only</span></span><br/> | <span data-ttu-id="951a5-123">Recupera un valore **booleano** che indica se l'estensione EKU è presente.</span><span class="sxs-lookup"><span data-stu-id="951a5-123">Retrieves a **Boolean** value that indicates whether the EKU extension is present.</span></span><br/> <span data-ttu-id="951a5-124">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="951a5-124">This is the default property.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="951a5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="951a5-125">Remarks</span></span>

<span data-ttu-id="951a5-126">Impossibile creare l'oggetto **ExtendedKeyUsage** .</span><span class="sxs-lookup"><span data-stu-id="951a5-126">The **ExtendedKeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="951a5-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="951a5-127">Requirements</span></span>



| <span data-ttu-id="951a5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="951a5-128">Requirement</span></span> | <span data-ttu-id="951a5-129">Valore</span><span class="sxs-lookup"><span data-stu-id="951a5-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="951a5-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="951a5-130">End of client support</span></span><br/> | <span data-ttu-id="951a5-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="951a5-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="951a5-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="951a5-132">End of server support</span></span><br/> | <span data-ttu-id="951a5-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="951a5-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="951a5-134">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="951a5-134">Redistributable</span></span><br/>       | <span data-ttu-id="951a5-135">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="951a5-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="951a5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="951a5-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="951a5-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="951a5-137"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="951a5-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="951a5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951a5-139">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="951a5-139">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
