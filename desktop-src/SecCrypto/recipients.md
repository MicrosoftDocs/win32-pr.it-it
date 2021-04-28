---
description: 'Oggetto Recipients: rappresenta una raccolta di oggetti Certificate.'
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
ms.openlocfilehash: e0f0f6474c6ed8883eb591591eff387fe387f7d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103739"
---
# <a name="recipients-object"></a><span data-ttu-id="bd59a-103">Oggetto Recipients</span><span class="sxs-lookup"><span data-stu-id="bd59a-103">Recipients object</span></span>

<span data-ttu-id="bd59a-104">\[**L'oggetto** Recipients è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.</span><span class="sxs-lookup"><span data-stu-id="bd59a-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bd59a-105">Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="bd59a-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="bd59a-106">**L'oggetto Recipients** rappresenta una raccolta di [**oggetti**](certificate.md) Certificate.</span><span class="sxs-lookup"><span data-stu-id="bd59a-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="bd59a-107">Ogni oggetto rappresenta un destinatario previsto del messaggio in busta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="bd59a-108">I dati in un oggetto [**EnvelopedData**](envelopeddata.md) vengono crittografati con una chiave di sessione simmetrica e tale chiave di sessione simmetrica viene quindi crittografata per ogni destinatario usando la chiave pubblica del certificato del destinatario. [](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="bd59a-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="bd59a-109">Un destinatario con accesso alla chiave privata [](../secgloss/p-gly.md) associata alla [](../secgloss/s-gly.md) chiave pubblica di un certificato può decrittografare la chiave di sessione e usare la chiave di sessione decrittografata per decrittografare i dati effettivi. [](../secgloss/p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="bd59a-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="bd59a-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="bd59a-110">When to use</span></span>

<span data-ttu-id="bd59a-111">**L'oggetto Recipients** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd59a-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="bd59a-112">Aggiungere o rimuovere un [**oggetto Certificate**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="bd59a-113">Recuperare il numero di certificati nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="bd59a-114">Recuperare un oggetto **Destinatari** specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="bd59a-115">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="bd59a-116">Membri</span><span class="sxs-lookup"><span data-stu-id="bd59a-116">Members</span></span>

<span data-ttu-id="bd59a-117">**L'oggetto Recipients** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bd59a-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="bd59a-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="bd59a-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="bd59a-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd59a-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bd59a-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="bd59a-120">Methods</span></span>

<span data-ttu-id="bd59a-121">**L'oggetto Recipients** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bd59a-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="bd59a-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="bd59a-122">Method</span></span>                              | <span data-ttu-id="bd59a-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd59a-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd59a-124">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="bd59a-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="bd59a-125">Aggiunge un [**oggetto Certificate**](certificate.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="bd59a-126">**Chiaro**</span><span class="sxs-lookup"><span data-stu-id="bd59a-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="bd59a-127">Rimuove tutti [**gli oggetti Certificate**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="bd59a-128">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="bd59a-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="bd59a-129">Rimuove un [**oggetto Certificate**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="bd59a-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd59a-130">Properties</span></span>

<span data-ttu-id="bd59a-131">**L'oggetto Recipients** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bd59a-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="bd59a-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd59a-132">Property</span></span>                                           | <span data-ttu-id="bd59a-133">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="bd59a-133">Access type</span></span>          | <span data-ttu-id="bd59a-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd59a-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd59a-135">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="bd59a-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="bd59a-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="bd59a-136">Read-only</span></span><br/> | <span data-ttu-id="bd59a-137">Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="bd59a-138">Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="bd59a-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="bd59a-139">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="bd59a-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="bd59a-140">Numero di oggetti nella **raccolta Recipients.**</span><span class="sxs-lookup"><span data-stu-id="bd59a-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="bd59a-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bd59a-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="bd59a-142">Oggetto indicizzato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd59a-142">An indexed object in the collection.</span></span> <span data-ttu-id="bd59a-143">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="bd59a-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="bd59a-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd59a-144">Remarks</span></span>

<span data-ttu-id="bd59a-145">Impossibile **creare l'oggetto** Recipients.</span><span class="sxs-lookup"><span data-stu-id="bd59a-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd59a-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd59a-146">Requirements</span></span>



| <span data-ttu-id="bd59a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd59a-147">Requirement</span></span> | <span data-ttu-id="bd59a-148">Valore</span><span class="sxs-lookup"><span data-stu-id="bd59a-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd59a-149">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bd59a-149">Redistributable</span></span><br/> | <span data-ttu-id="bd59a-150">CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bd59a-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bd59a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bd59a-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="bd59a-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd59a-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd59a-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd59a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd59a-154">**Oggetti di crittografia**</span><span class="sxs-lookup"><span data-stu-id="bd59a-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
