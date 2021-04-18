---
description: Rappresenta una raccolta di oggetti EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Oggetto EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331425"
---
# <a name="ekus-object"></a><span data-ttu-id="4d730-103">Oggetto EKU</span><span class="sxs-lookup"><span data-stu-id="4d730-103">EKUs object</span></span>

<span data-ttu-id="4d730-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4d730-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4d730-105">Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4d730-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4d730-106">L'oggetto **EKU** rappresenta una raccolta di oggetti [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="4d730-106">The **EKUs** object represents a collection of [**EKU**](eku.md) objects.</span></span> <span data-ttu-id="4d730-107">Ogni oggetto [**EKU**](eku.md) rappresenta una singola proprietà di utilizzo chiavi avanzato (EKU) di un certificato.</span><span class="sxs-lookup"><span data-stu-id="4d730-107">Each [**EKU**](eku.md) object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4d730-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4d730-108">When to use</span></span>

<span data-ttu-id="4d730-109">La raccolta **EKU** viene utilizzata per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d730-109">The **EKUs** collection is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4d730-110">Recuperare il numero di proprietà EKU nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="4d730-110">Retrieve the number of EKU properties in the collection.</span></span>
-   <span data-ttu-id="4d730-111">Recuperare un oggetto [**EKU**](eku.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4d730-111">Retrieve a specific [**EKU**](eku.md) object from the collection.</span></span>
-   <span data-ttu-id="4d730-112">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="4d730-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="4d730-113">Membri</span><span class="sxs-lookup"><span data-stu-id="4d730-113">Members</span></span>

<span data-ttu-id="4d730-114">L'oggetto **EKU** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4d730-114">The **EKUs** object has these types of members:</span></span>

-   [<span data-ttu-id="4d730-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d730-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d730-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d730-116">Properties</span></span>

<span data-ttu-id="4d730-117">L'oggetto **EKU** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d730-117">The **EKUs** object has these properties.</span></span>



| <span data-ttu-id="4d730-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d730-118">Property</span></span>                                     | <span data-ttu-id="4d730-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="4d730-119">Access type</span></span>          | <span data-ttu-id="4d730-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d730-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d730-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="4d730-121">**\_NewEnum**</span></span>](ekus-newenum.md)<br/> | <span data-ttu-id="4d730-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d730-122">Read-only</span></span><br/> | <span data-ttu-id="4d730-123">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="4d730-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="4d730-124">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="4d730-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="4d730-125">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="4d730-125">**Count**</span></span>](ekus-count.md)<br/>       | <span data-ttu-id="4d730-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d730-126">Read-only</span></span><br/> | <span data-ttu-id="4d730-127">Recupera il numero di oggetti [**EKU**](eku.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="4d730-127">Retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="4d730-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4d730-128">**Item**</span></span>](ekus-item.md)<br/>         | <span data-ttu-id="4d730-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d730-129">Read-only</span></span><br/> | <span data-ttu-id="4d730-130">Recupera l'oggetto [**EKU**](eku.md) che rappresenta la proprietà EKU indicizzata.</span><span class="sxs-lookup"><span data-stu-id="4d730-130">Retrieves the [**EKU**](eku.md) object that represents the indexed EKU property.</span></span> <span data-ttu-id="4d730-131">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="4d730-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="4d730-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d730-132">Remarks</span></span>

<span data-ttu-id="4d730-133">Questa raccolta viene recuperata dalla proprietà [**ExtendedKeyUsage. EKU**](extendedkeyusage-ekus.md) .</span><span class="sxs-lookup"><span data-stu-id="4d730-133">This collection is retrieved by the [**ExtendedKeyUsage.EKUs**](extendedkeyusage-ekus.md) property.</span></span>

<span data-ttu-id="4d730-134">Impossibile creare l'oggetto **EKU** .</span><span class="sxs-lookup"><span data-stu-id="4d730-134">The **EKUs** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d730-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d730-135">Requirements</span></span>



| <span data-ttu-id="4d730-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d730-136">Requirement</span></span> | <span data-ttu-id="4d730-137">Valore</span><span class="sxs-lookup"><span data-stu-id="4d730-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d730-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4d730-138">End of client support</span></span><br/> | <span data-ttu-id="4d730-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d730-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4d730-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4d730-140">End of server support</span></span><br/> | <span data-ttu-id="4d730-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d730-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4d730-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4d730-142">Redistributable</span></span><br/>       | <span data-ttu-id="4d730-143">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d730-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4d730-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4d730-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4d730-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d730-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
