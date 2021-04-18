---
description: Rappresenta una raccolta di oggetti OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Oggetto Oid
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325152"
---
# <a name="oids-object"></a><span data-ttu-id="d12f2-103">Oggetto Oid</span><span class="sxs-lookup"><span data-stu-id="d12f2-103">OIDs object</span></span>

<span data-ttu-id="d12f2-104">\[L'oggetto **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d12f2-104">\[The **OIDs** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d12f2-105">Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d12f2-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d12f2-106">L'oggetto **OID** rappresenta una raccolta di oggetti [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="d12f2-106">The **OIDs** object represents a collection of [**OID**](oid.md) objects.</span></span> <span data-ttu-id="d12f2-107">Ogni oggetto [**OID**](oid.md) rappresenta un identificatore di oggetto singolo.</span><span class="sxs-lookup"><span data-stu-id="d12f2-107">Each [**OID**](oid.md) object represents a single object identifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d12f2-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d12f2-108">When to use</span></span>

<span data-ttu-id="d12f2-109">L'oggetto **OID** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="d12f2-109">The **OIDs** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d12f2-110">Aggiungere o rimuovere un oggetto [**OID**](oid.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-110">Add or remove an [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="d12f2-111">Cancellare tutti gli oggetti [**OID**](oid.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-111">Clear all the [**OID**](oid.md) objects from the collection.</span></span>
-   <span data-ttu-id="d12f2-112">Recuperare il numero di identificatori di oggetto nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-112">Retrieve the number of object identifiers in the collection.</span></span>
-   <span data-ttu-id="d12f2-113">Recuperare un oggetto [**OID**](oid.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-113">Retrieve a specific [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="d12f2-114">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="d12f2-115">Membri</span><span class="sxs-lookup"><span data-stu-id="d12f2-115">Members</span></span>

<span data-ttu-id="d12f2-116">L'oggetto **OID** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d12f2-116">The **OIDs** object has these types of members:</span></span>

-   [<span data-ttu-id="d12f2-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="d12f2-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="d12f2-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d12f2-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d12f2-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="d12f2-119">Methods</span></span>

<span data-ttu-id="d12f2-120">L'oggetto **OID** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d12f2-120">The **OIDs** object has these methods.</span></span>



| <span data-ttu-id="d12f2-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="d12f2-121">Method</span></span>                        | <span data-ttu-id="d12f2-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d12f2-122">Description</span></span>                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="d12f2-123">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="d12f2-123">**Add**</span></span>](oids-add.md)       | <span data-ttu-id="d12f2-124">Aggiunge un oggetto [**OID**](oid.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-124">Adds an [**OID**](oid.md) object to the collection.</span></span><br/>              |
| [<span data-ttu-id="d12f2-125">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="d12f2-125">**Clear**</span></span>](oids-clear.md)   | <span data-ttu-id="d12f2-126">Cancella tutti gli oggetti [**OID**](oid.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-126">Clears all [**OID**](oid.md) objects from the collection.</span></span><br/>        |
| [<span data-ttu-id="d12f2-127">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="d12f2-127">**Remove**</span></span>](oids-remove.md) | <span data-ttu-id="d12f2-128">Rimuove un oggetto [**OID**](oid.md) indicizzato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-128">Removes an indexed [**OID**](oid.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d12f2-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d12f2-129">Properties</span></span>

<span data-ttu-id="d12f2-130">L'oggetto **OID** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d12f2-130">The **OIDs** object has these properties.</span></span>



| <span data-ttu-id="d12f2-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d12f2-131">Property</span></span>                                     | <span data-ttu-id="d12f2-132">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d12f2-132">Access type</span></span>          | <span data-ttu-id="d12f2-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d12f2-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d12f2-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="d12f2-134">**\_NewEnum**</span></span>](oids-newenum.md)<br/> | <span data-ttu-id="d12f2-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d12f2-135">Read-only</span></span><br/> | <span data-ttu-id="d12f2-136">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="d12f2-137">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="d12f2-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="d12f2-138">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="d12f2-138">**Count**</span></span>](oids-count.md)<br/>       | <span data-ttu-id="d12f2-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d12f2-139">Read-only</span></span><br/> | <span data-ttu-id="d12f2-140">Recupera il numero di oggetti [**OID**](oid.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-140">Retrieves the number of [**OID**](oid.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="d12f2-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d12f2-141">**Item**</span></span>](oids-item.md)<br/>         | <span data-ttu-id="d12f2-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d12f2-142">Read-only</span></span><br/> | <span data-ttu-id="d12f2-143">Recupera un oggetto [**OID**](oid.md) indicizzato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d12f2-143">Retrieves an indexed [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="d12f2-144">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="d12f2-144">This is the default property.</span></span><br/>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="d12f2-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="d12f2-145">Remarks</span></span>

<span data-ttu-id="d12f2-146">Impossibile creare l'oggetto **OID** .</span><span class="sxs-lookup"><span data-stu-id="d12f2-146">The **OIDs** object cannot be created.</span></span>

<span data-ttu-id="d12f2-147">L'oggetto **OID** viene usato dalle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="d12f2-147">The **OIDs** object is used by the following properties:</span></span>

-   [<span data-ttu-id="d12f2-148">**CertificateStatus. ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="d12f2-148">**CertificateStatus.ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md)
-   [<span data-ttu-id="d12f2-149">**CertificateStatus. CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="d12f2-149">**CertificateStatus.CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a><span data-ttu-id="d12f2-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d12f2-150">Requirements</span></span>



| <span data-ttu-id="d12f2-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="d12f2-151">Requirement</span></span> | <span data-ttu-id="d12f2-152">Valore</span><span class="sxs-lookup"><span data-stu-id="d12f2-152">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d12f2-153">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d12f2-153">Redistributable</span></span><br/> | <span data-ttu-id="d12f2-154">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d12f2-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d12f2-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d12f2-155">DLL</span></span><br/>             | <dl> <span data-ttu-id="d12f2-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d12f2-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
