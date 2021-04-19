---
description: Rappresenta una singola estensione del certificato.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Oggetto Extension (Mmcobj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326518"
---
# <a name="extension-object"></a><span data-ttu-id="0d4d6-103">Oggetto di estensione</span><span class="sxs-lookup"><span data-stu-id="0d4d6-103">Extension object</span></span>

<span data-ttu-id="0d4d6-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0d4d6-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0d4d6-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0d4d6-106">L'oggetto di **estensione** rappresenta una singola estensione del certificato.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-106">The **Extension** object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0d4d6-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0d4d6-107">When to use</span></span>

<span data-ttu-id="0d4d6-108">L'oggetto **estensione** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d4d6-108">The **Extension** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="0d4d6-109">Recuperare l'OID dell'estensione del certificato.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-109">Retrieve the OID of the certificate extension.</span></span>
-   <span data-ttu-id="0d4d6-110">Recuperare i dati dell'estensione del certificato rappresentati da un oggetto [**EncodedData**](encodeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="0d4d6-110">Retrieve the certificate extension data represented by an [**EncodedData**](encodeddata.md) object.</span></span>
-   <span data-ttu-id="0d4d6-111">Determinare se l'estensione del certificato è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-111">Determine whether the certificate extension is marked as critical.</span></span>

## <a name="members"></a><span data-ttu-id="0d4d6-112">Membri</span><span class="sxs-lookup"><span data-stu-id="0d4d6-112">Members</span></span>

<span data-ttu-id="0d4d6-113">L'oggetto di **estensione** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0d4d6-113">The **Extension** object has these types of members:</span></span>

-   [<span data-ttu-id="0d4d6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d4d6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d4d6-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d4d6-115">Properties</span></span>

<span data-ttu-id="0d4d6-116">L'oggetto **estensione** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-116">The **Extension** object has these properties.</span></span>



| <span data-ttu-id="0d4d6-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d4d6-117">Property</span></span>                                                | <span data-ttu-id="0d4d6-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="0d4d6-118">Access type</span></span>          | <span data-ttu-id="0d4d6-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d4d6-119">Description</span></span>                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d4d6-120">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="0d4d6-120">**EncodedData**</span></span>](extension-encodeddata.md)<br/> | <span data-ttu-id="0d4d6-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d4d6-121">Read-only</span></span><br/> | <span data-ttu-id="0d4d6-122">Recupera i dati codificati per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-122">Retrieves the encoded data for the extension.</span></span><br/>                                      |
| [<span data-ttu-id="0d4d6-123">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="0d4d6-123">**IsCritical**</span></span>](extension-iscritical.md)<br/>   | <span data-ttu-id="0d4d6-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d4d6-124">Read-only</span></span><br/> | <span data-ttu-id="0d4d6-125">Recupera un valore booleano che indica se l'estensione è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-125">Retrieves a Boolean value that indicates whether the extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="0d4d6-126">**OID**</span><span class="sxs-lookup"><span data-stu-id="0d4d6-126">**OID**</span></span>](extension-oid.md)<br/>                 | <span data-ttu-id="0d4d6-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d4d6-127">Read-only</span></span><br/> | <span data-ttu-id="0d4d6-128">Recupera l'identificatore di oggetto per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-128">Retrieves the object identifier for the extension.</span></span> <span data-ttu-id="0d4d6-129">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="0d4d6-129">This is the default property.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="0d4d6-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d4d6-130">Remarks</span></span>

<span data-ttu-id="0d4d6-131">Impossibile creare l'oggetto di **estensione** .</span><span class="sxs-lookup"><span data-stu-id="0d4d6-131">The **Extension** object cannot be created.</span></span>

<span data-ttu-id="0d4d6-132">L'oggetto di **estensione** viene utilizzato dall'oggetto della raccolta [**Extensions**](extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="0d4d6-132">The **Extension** object is used by the [**Extensions**](extensions.md) collection object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4d6-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d4d6-133">Requirements</span></span>



| <span data-ttu-id="0d4d6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4d6-134">Requirement</span></span> | <span data-ttu-id="0d4d6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0d4d6-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4d6-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0d4d6-136">End of client support</span></span><br/> | <span data-ttu-id="0d4d6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d4d6-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0d4d6-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0d4d6-138">End of server support</span></span><br/> | <span data-ttu-id="0d4d6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d4d6-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0d4d6-140">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0d4d6-140">Redistributable</span></span><br/>       | <span data-ttu-id="0d4d6-141">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d4d6-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0d4d6-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d4d6-142">Header</span></span><br/>                | <dl> <span data-ttu-id="0d4d6-143"><dt>Mmcobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4d6-143"><dt>Mmcobj.h</dt></span></span> </dl>    |
| <span data-ttu-id="0d4d6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0d4d6-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0d4d6-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d4d6-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
