---
description: Fornisce le proprietà e i metodi che è possibile usare per scegliere, gestire e usare gli archivi certificati e i certificati in tali archivi.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Oggetto Store
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330019"
---
# <a name="store-object"></a><span data-ttu-id="16eae-103">Oggetto Store</span><span class="sxs-lookup"><span data-stu-id="16eae-103">Store object</span></span>

<span data-ttu-id="16eae-104">\[L'oggetto **Store** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="16eae-104">\[The **Store** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="16eae-105">Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="16eae-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="16eae-106">L'oggetto **Store** fornisce le proprietà e i metodi che è possibile usare per scegliere, gestire e usare gli [*archivi certificati*](../secgloss/c-gly.md) e i certificati in tali archivi.</span><span class="sxs-lookup"><span data-stu-id="16eae-106">The **Store** object provides properties and methods that you can use to choose, manage, and use [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="16eae-107">CAPICOM può usare gli archivi utente corrente, computer locale, memoria e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="16eae-107">CAPICOM can use Current-User, Local-Machine, memory, and Active Directory stores.</span></span> <span data-ttu-id="16eae-108">Inoltre, gli archivi supportano gli archivi certificati basati su smart card.</span><span class="sxs-lookup"><span data-stu-id="16eae-108">Also, stores support smart card–based certificate stores.</span></span> <span data-ttu-id="16eae-109">Gli sviluppatori devono tenere presente che alcuni metodi potrebbero avere esito negativo con alcuni archivi se si tenta di eseguire operazioni per le quali l'utente non dispone di diritti.</span><span class="sxs-lookup"><span data-stu-id="16eae-109">Developers should be aware that some methods may fail with some stores if operations are attempted for which the user does not have rights.</span></span>

## <a name="members"></a><span data-ttu-id="16eae-110">Membri</span><span class="sxs-lookup"><span data-stu-id="16eae-110">Members</span></span>

<span data-ttu-id="16eae-111">L'oggetto **Store** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="16eae-111">The **Store** object has these types of members:</span></span>

-   [<span data-ttu-id="16eae-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="16eae-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="16eae-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16eae-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="16eae-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="16eae-114">Methods</span></span>

<span data-ttu-id="16eae-115">L'oggetto **Store** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="16eae-115">The **Store** object has these methods.</span></span>



| <span data-ttu-id="16eae-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="16eae-116">Method</span></span>                         | <span data-ttu-id="16eae-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16eae-117">Description</span></span>                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16eae-118">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="16eae-118">**Add**</span></span>](store-add.md)       | <span data-ttu-id="16eae-119">Aggiunge un oggetto [**certificato**](certificate.md) all'archivio certificati aperto.</span><span class="sxs-lookup"><span data-stu-id="16eae-119">Adds a [**Certificate**](certificate.md) object to the open certificate store.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="16eae-120">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="16eae-120">**Close**</span></span>](store-close.md)   | <span data-ttu-id="16eae-121">Chiude un archivio certificati aperto.</span><span class="sxs-lookup"><span data-stu-id="16eae-121">Closes an open certificate store.</span></span><br/> <span data-ttu-id="16eae-122">**CAPICOM 2.0.0.3 e versioni precedenti:** Il metodo [**Close**](store-close.md) non è supportato.</span><span class="sxs-lookup"><span data-stu-id="16eae-122">**CAPICOM 2.0.0.3 and earlier:** The [**Close**](store-close.md) method is not supported.</span></span><br/>                                                               |
| [<span data-ttu-id="16eae-123">**Delete**</span><span class="sxs-lookup"><span data-stu-id="16eae-123">**Delete**</span></span>](store-delete.md) | <span data-ttu-id="16eae-124">Elimina l'archivio certificati rappresentato dall'oggetto [**Archivio**](certificate.md) corrente.</span><span class="sxs-lookup"><span data-stu-id="16eae-124">Deletes the certificate store represented by the current [**Store**](certificate.md) object.</span></span><br/> <span data-ttu-id="16eae-125">**CAPICOM 2.0.0.3 e versioni precedenti:** Il metodo [**Delete**](store-delete.md) non è supportato.</span><span class="sxs-lookup"><span data-stu-id="16eae-125">**CAPICOM 2.0.0.3 and earlier:** The [**Delete**](store-delete.md) method is not supported.</span></span><br/> |
| [<span data-ttu-id="16eae-126">**Esportazione**</span><span class="sxs-lookup"><span data-stu-id="16eae-126">**Export**</span></span>](store-export.md) | <span data-ttu-id="16eae-127">Esporta l'archivio di un [*BLOB*](../secgloss/b-gly.md)codificato.</span><span class="sxs-lookup"><span data-stu-id="16eae-127">Exports the store of an encoded [*BLOB*](../secgloss/b-gly.md).</span></span><br/>                                                                                                       |
| [<span data-ttu-id="16eae-128">**Importa**</span><span class="sxs-lookup"><span data-stu-id="16eae-128">**Import**</span></span>](store-import.md) | <span data-ttu-id="16eae-129">Importa un archivio precedentemente esportato.</span><span class="sxs-lookup"><span data-stu-id="16eae-129">Imports a previously exported store.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="16eae-130">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="16eae-130">**Load**</span></span>](store-load.md)     | <span data-ttu-id="16eae-131">Importa oggetti [**certificato**](certificate.md) da un file nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="16eae-131">Imports [**Certificate**](certificate.md) objects from a file into the store.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="16eae-132">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="16eae-132">**Open**</span></span>](store-open.md)     | <span data-ttu-id="16eae-133">Apre un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="16eae-133">Opens a certificate store.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="16eae-134">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="16eae-134">**Remove**</span></span>](store-remove.md) | <span data-ttu-id="16eae-135">Rimuove un oggetto [**certificato**](certificate.md) da un archivio aperto.</span><span class="sxs-lookup"><span data-stu-id="16eae-135">Removes a [**Certificate**](certificate.md) object from an open store.</span></span><br/>                                                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="16eae-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16eae-136">Properties</span></span>

<span data-ttu-id="16eae-137">L'oggetto **Store** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="16eae-137">The **Store** object has these properties.</span></span>



| <span data-ttu-id="16eae-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16eae-138">Property</span></span>                                              | <span data-ttu-id="16eae-139">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="16eae-139">Access type</span></span>          | <span data-ttu-id="16eae-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16eae-140">Description</span></span>                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16eae-141">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="16eae-141">**Certificates**</span></span>](store-certificates.md)<br/> | <span data-ttu-id="16eae-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="16eae-142">Read-only</span></span><br/> | <span data-ttu-id="16eae-143">Recupera la raccolta di [**certificati**](certificates.md) dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="16eae-143">Retrieves the [**Certificates**](certificates.md) collection of the store.</span></span> <span data-ttu-id="16eae-144">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="16eae-144">This is the default property.</span></span><br/>                                                                                  |
| [<span data-ttu-id="16eae-145">**Location**</span><span class="sxs-lookup"><span data-stu-id="16eae-145">**Location**</span></span>](store-location.md)<br/>         | <span data-ttu-id="16eae-146">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="16eae-146">Read-only</span></span><br/> | <span data-ttu-id="16eae-147">Recupera il percorso dell'archivio certificati rappresentato da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="16eae-147">Retrieves the location of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="16eae-148">**CAPICOM 2.0.0.3 e versioni precedenti:** La proprietà [**location**](store-location.md) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="16eae-148">**CAPICOM 2.0.0.3 and earlier:** The [**Location**](store-location.md) property is not supported.</span></span><br/> |
| [<span data-ttu-id="16eae-149">**Nome**</span><span class="sxs-lookup"><span data-stu-id="16eae-149">**Name**</span></span>](store-name.md)<br/>                 | <span data-ttu-id="16eae-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="16eae-150">Read-only</span></span><br/> | <span data-ttu-id="16eae-151">Recupera il nome dell'archivio certificati rappresentato da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="16eae-151">Retrieves the name of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="16eae-152">**CAPICOM 2.0.0.3 e versioni precedenti:** La proprietà [**Name**](store-name.md) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="16eae-152">**CAPICOM 2.0.0.3 and earlier:** The [**Name**](store-name.md) property is not supported.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="16eae-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="16eae-153">Remarks</span></span>

<span data-ttu-id="16eae-154">È possibile creare l'oggetto **Store** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="16eae-154">The **Store** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="16eae-155">Il ProgID per l'oggetto **Store** è capicom. Archivio. 2.</span><span class="sxs-lookup"><span data-stu-id="16eae-155">The ProgID for the **Store** object is CAPICOM.Store.2.</span></span>

<span data-ttu-id="16eae-156">**CAPICOM 1. *x*:** il ProgID per l'oggetto **Store** è capicom. Archivio. 1.</span><span class="sxs-lookup"><span data-stu-id="16eae-156">**CAPICOM 1.*x*:** The ProgID for the **Store** object is CAPICOM.Store.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="16eae-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16eae-157">Requirements</span></span>



| <span data-ttu-id="16eae-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="16eae-158">Requirement</span></span> | <span data-ttu-id="16eae-159">Valore</span><span class="sxs-lookup"><span data-stu-id="16eae-159">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16eae-160">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="16eae-160">Redistributable</span></span><br/> | <span data-ttu-id="16eae-161">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="16eae-161">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="16eae-162">DLL</span><span class="sxs-lookup"><span data-stu-id="16eae-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="16eae-163"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16eae-163"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16eae-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16eae-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16eae-165">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="16eae-165">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
