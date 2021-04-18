---
description: Rappresenta una raccolta di oggetti certificate.
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Oggetto Recipients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324462"
---
# <a name="recipients-object"></a><span data-ttu-id="d4181-103">Oggetto Recipients</span><span class="sxs-lookup"><span data-stu-id="d4181-103">Recipients object</span></span>

<span data-ttu-id="d4181-104">\[L'oggetto **destinatari** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d4181-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d4181-105">Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d4181-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d4181-106">L'oggetto **Recipients** rappresenta una raccolta di oggetti [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="d4181-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="d4181-107">Ogni oggetto rappresenta un destinatario previsto del messaggio in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="d4181-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="d4181-108">I dati in un oggetto [**EnvelopedData**](envelopeddata.md) vengono crittografati con una chiave di sessione [*simmetrica*](../secgloss/s-gly.md) e la chiave della sessione simmetrica viene quindi crittografata per ogni destinatario utilizzando la chiave pubblica del certificato del destinatario desiderato.</span><span class="sxs-lookup"><span data-stu-id="d4181-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="d4181-109">Un destinatario con accesso alla [*chiave privata*](../secgloss/p-gly.md) associata alla [*chiave pubblica*](../secgloss/p-gly.md) di un certificato può decrittografare la [*chiave della sessione*](../secgloss/s-gly.md) e utilizzare la chiave della sessione decrittografata per decrittografare i dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="d4181-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d4181-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d4181-110">When to use</span></span>

<span data-ttu-id="d4181-111">L'oggetto **Recipients** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4181-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d4181-112">Aggiungere o rimuovere un oggetto [**certificato**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="d4181-113">Recuperare il numero di certificati nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="d4181-114">Recuperare un oggetto **destinatari** specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="d4181-115">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="d4181-116">Membri</span><span class="sxs-lookup"><span data-stu-id="d4181-116">Members</span></span>

<span data-ttu-id="d4181-117">L'oggetto **destinatari** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d4181-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="d4181-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="d4181-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="d4181-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d4181-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d4181-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="d4181-120">Methods</span></span>

<span data-ttu-id="d4181-121">L'oggetto **Recipients** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d4181-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="d4181-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="d4181-122">Method</span></span>                              | <span data-ttu-id="d4181-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4181-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4181-124">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="d4181-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="d4181-125">Aggiunge un oggetto [**certificato**](certificate.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="d4181-126">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="d4181-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="d4181-127">Rimuove tutti gli oggetti [**certificato**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="d4181-128">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="d4181-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="d4181-129">Rimuove un oggetto [**certificato**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="d4181-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d4181-130">Properties</span></span>

<span data-ttu-id="d4181-131">L'oggetto **destinatari** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d4181-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="d4181-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d4181-132">Property</span></span>                                           | <span data-ttu-id="d4181-133">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d4181-133">Access type</span></span>          | <span data-ttu-id="d4181-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4181-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4181-135">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="d4181-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="d4181-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d4181-136">Read-only</span></span><br/> | <span data-ttu-id="d4181-137">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="d4181-138">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="d4181-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="d4181-139">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="d4181-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="d4181-140">Numero di oggetti nella raccolta di **destinatari** .</span><span class="sxs-lookup"><span data-stu-id="d4181-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="d4181-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d4181-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="d4181-142">Oggetto indicizzato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4181-142">An indexed object in the collection.</span></span> <span data-ttu-id="d4181-143">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="d4181-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="d4181-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4181-144">Remarks</span></span>

<span data-ttu-id="d4181-145">Impossibile creare l'oggetto **destinatari** .</span><span class="sxs-lookup"><span data-stu-id="d4181-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4181-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4181-146">Requirements</span></span>



| <span data-ttu-id="d4181-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4181-147">Requirement</span></span> | <span data-ttu-id="d4181-148">Valore</span><span class="sxs-lookup"><span data-stu-id="d4181-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4181-149">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d4181-149">Redistributable</span></span><br/> | <span data-ttu-id="d4181-150">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4181-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d4181-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d4181-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="d4181-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4181-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4181-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4181-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4181-154">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="d4181-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
