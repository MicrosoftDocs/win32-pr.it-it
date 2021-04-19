---
description: Rappresenta la chiave privata associata a un certificato.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Oggetto PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324887"
---
# <a name="privatekey-object"></a><span data-ttu-id="d832c-103">Oggetto PrivateKey</span><span class="sxs-lookup"><span data-stu-id="d832c-103">PrivateKey object</span></span>

<span data-ttu-id="d832c-104">\[L'oggetto **PrivateKey** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d832c-104">\[The **PrivateKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d832c-105">Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d832c-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d832c-106">L'oggetto **PrivateKey** rappresenta la [*chiave privata*](../secgloss/p-gly.md) associata a un certificato.</span><span class="sxs-lookup"><span data-stu-id="d832c-106">The **PrivateKey** object represents the [*private key*](../secgloss/p-gly.md) associated with a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d832c-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d832c-107">When to use</span></span>

<span data-ttu-id="d832c-108">L'oggetto **PrivateKey** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="d832c-108">The **PrivateKey** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d832c-109">Recuperare le informazioni sulla chiave privata.</span><span class="sxs-lookup"><span data-stu-id="d832c-109">Retrieve information about the private key.</span></span>
-   <span data-ttu-id="d832c-110">Aprire il contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="d832c-110">Open the private key container.</span></span>
-   <span data-ttu-id="d832c-111">Eliminare la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="d832c-111">Delete the private key.</span></span>

## <a name="members"></a><span data-ttu-id="d832c-112">Membri</span><span class="sxs-lookup"><span data-stu-id="d832c-112">Members</span></span>

<span data-ttu-id="d832c-113">L'oggetto **PrivateKey** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d832c-113">The **PrivateKey** object has these types of members:</span></span>

-   [<span data-ttu-id="d832c-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="d832c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d832c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d832c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d832c-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="d832c-116">Methods</span></span>

<span data-ttu-id="d832c-117">L'oggetto **PrivateKey** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d832c-117">The **PrivateKey** object has these methods.</span></span>



| <span data-ttu-id="d832c-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="d832c-118">Method</span></span>                                                  | <span data-ttu-id="d832c-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d832c-119">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d832c-120">**Eliminare**</span><span class="sxs-lookup"><span data-stu-id="d832c-120">**Delete**</span></span>](privatekey-delete.md)                     | <span data-ttu-id="d832c-121">Elimina il contenitore di chiavi private a cui fa riferimento l'oggetto **PrivateKey** .</span><span class="sxs-lookup"><span data-stu-id="d832c-121">Deletes the private key container referenced by the **PrivateKey** object.</span></span><br/>                                                                                |
| [<span data-ttu-id="d832c-122">**IsAccessible**</span><span class="sxs-lookup"><span data-stu-id="d832c-122">**IsAccessible**</span></span>](privatekey-isaccessible.md)         | <span data-ttu-id="d832c-123">Recupera un valore booleano che indica se la chiave privata è accessibile dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d832c-123">Retrieves a Boolean value that indicates whether the private key is accessible by the user.</span></span> <span data-ttu-id="d832c-124">Se true, l'utente può accedere alla chiave privata.</span><span class="sxs-lookup"><span data-stu-id="d832c-124">If true, the user can access the private key.</span></span><br/>                 |
| [<span data-ttu-id="d832c-125">**IsExportable**</span><span class="sxs-lookup"><span data-stu-id="d832c-125">**IsExportable**</span></span>](privatekey-isexportable.md)         | <span data-ttu-id="d832c-126">Recupera un valore booleano che indica se la chiave privata può essere esportata.</span><span class="sxs-lookup"><span data-stu-id="d832c-126">Retrieves a Boolean value that indicates whether the private key can be exported.</span></span> <span data-ttu-id="d832c-127">Se true, la chiave privata può essere esportata.</span><span class="sxs-lookup"><span data-stu-id="d832c-127">If true, the private key can be exported.</span></span><br/>                               |
| [<span data-ttu-id="d832c-128">**IsHardwareDevice**</span><span class="sxs-lookup"><span data-stu-id="d832c-128">**IsHardwareDevice**</span></span>](privatekey-ishardwaredevice.md) | <span data-ttu-id="d832c-129">Recupera un valore booleano che indica se la chiave privata è archiviata in un dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="d832c-129">Retrieves a Boolean value that indicates whether the private key is stored on a hardware device.</span></span> <span data-ttu-id="d832c-130">Se true, la chiave privata viene archiviata in un dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="d832c-130">If true, the private key is stored on a hardware device.</span></span><br/> |
| [<span data-ttu-id="d832c-131">**IsMachineKeyset**</span><span class="sxs-lookup"><span data-stu-id="d832c-131">**IsMachineKeyset**</span></span>](privatekey-ismachinekeyset.md)   | <span data-ttu-id="d832c-132">Recupera un valore booleano che indica se la chiave privata è una chiave del computer.</span><span class="sxs-lookup"><span data-stu-id="d832c-132">Retrieves a Boolean value that indicates whether the private key is a machine key.</span></span> <span data-ttu-id="d832c-133">Se true, la chiave privata è una chiave del computer.</span><span class="sxs-lookup"><span data-stu-id="d832c-133">If true, the private key is a machine key.</span></span><br/>                             |
| [<span data-ttu-id="d832c-134">**IsProtected**</span><span class="sxs-lookup"><span data-stu-id="d832c-134">**IsProtected**</span></span>](privatekey-isprotected.md)           | <span data-ttu-id="d832c-135">Recupera un valore booleano che indica se la chiave privata è protetta.</span><span class="sxs-lookup"><span data-stu-id="d832c-135">Retrieves a Boolean value that indicates whether the private key is protected.</span></span> <span data-ttu-id="d832c-136">Se true, la chiave privata è protetta.</span><span class="sxs-lookup"><span data-stu-id="d832c-136">If true, the private key is protected.</span></span><br/>                                     |
| [<span data-ttu-id="d832c-137">**IsRemovable**</span><span class="sxs-lookup"><span data-stu-id="d832c-137">**IsRemovable**</span></span>](privatekey-isremovable.md)           | <span data-ttu-id="d832c-138">Recupera un valore booleano che indica se la chiave privata si trova in un dispositivo rimovibile.</span><span class="sxs-lookup"><span data-stu-id="d832c-138">Retrieves a Boolean value that indicates whether the private key is on a removable device.</span></span> <span data-ttu-id="d832c-139">Se true, la chiave privata si trova in un dispositivo rimovibile.</span><span class="sxs-lookup"><span data-stu-id="d832c-139">If true, the private key is on a removable device.</span></span><br/>             |
| [<span data-ttu-id="d832c-140">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="d832c-140">**Open**</span></span>](privatekey-open.md)                         | <span data-ttu-id="d832c-141">Accede a un contenitore di chiavi esistente.</span><span class="sxs-lookup"><span data-stu-id="d832c-141">Accesses an existing key container.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="d832c-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d832c-142">Properties</span></span>

<span data-ttu-id="d832c-143">L'oggetto **PrivateKey** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d832c-143">The **PrivateKey** object has these properties.</span></span>



| <span data-ttu-id="d832c-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d832c-144">Property</span></span>                                                                 | <span data-ttu-id="d832c-145">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d832c-145">Access type</span></span>          | <span data-ttu-id="d832c-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d832c-146">Description</span></span>                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d832c-147">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="d832c-147">**ContainerName**</span></span>](privatekey-containername.md)<br/>             | <span data-ttu-id="d832c-148">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d832c-148">Read-only</span></span><br/> | <span data-ttu-id="d832c-149">Recupera una stringa che contiene il nome del contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="d832c-149">Retrieves a string that contains the private key container name.</span></span> <span data-ttu-id="d832c-150">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="d832c-150">This is the default property.</span></span><br/> |
| [<span data-ttu-id="d832c-151">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="d832c-151">**KeySpec**</span></span>](privatekey-keyspec.md)<br/>                         | <span data-ttu-id="d832c-152">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d832c-152">Read-only</span></span><br/> | <span data-ttu-id="d832c-153">Recupera la specifica della chiave.</span><span class="sxs-lookup"><span data-stu-id="d832c-153">Retrieves the key specification.</span></span><br/>                                                               |
| [<span data-ttu-id="d832c-154">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="d832c-154">**ProviderName**</span></span>](privatekey-providername.md)<br/>               | <span data-ttu-id="d832c-155">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d832c-155">Read-only</span></span><br/> | <span data-ttu-id="d832c-156">Recupera una stringa che contiene il nome del CSP.</span><span class="sxs-lookup"><span data-stu-id="d832c-156">Retrieves a string that contains the name of the CSP.</span></span><br/>                                          |
| [<span data-ttu-id="d832c-157">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="d832c-157">**ProviderType**</span></span>](privatekey-providertype.md)<br/>               | <span data-ttu-id="d832c-158">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d832c-158">Read-only</span></span><br/> | <span data-ttu-id="d832c-159">Recupera un valore di enumerazione che specifica il tipo di provider.</span><span class="sxs-lookup"><span data-stu-id="d832c-159">Retrieves an enumeration value that specifies the type of provider.</span></span><br/>                            |
| [<span data-ttu-id="d832c-160">**UniqueContainerName**</span><span class="sxs-lookup"><span data-stu-id="d832c-160">**UniqueContainerName**</span></span>](privatekey-uniquecontainername.md)<br/> | <span data-ttu-id="d832c-161">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d832c-161">Read-only</span></span><br/> | <span data-ttu-id="d832c-162">Recupera una stringa che contiene il nome univoco del contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="d832c-162">Retrieves a string that contains the unique private key container name.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d832c-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="d832c-163">Remarks</span></span>

<span data-ttu-id="d832c-164">È possibile creare l'oggetto **PrivateKey** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="d832c-164">The **PrivateKey** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="d832c-165">Il ProgID per l'oggetto **PrivateKey** è capicom. PrivateKey. 1.</span><span class="sxs-lookup"><span data-stu-id="d832c-165">The ProgID for the **PrivateKey** object is CAPICOM.PrivateKey.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="d832c-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d832c-166">Requirements</span></span>



| <span data-ttu-id="d832c-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="d832c-167">Requirement</span></span> | <span data-ttu-id="d832c-168">Valore</span><span class="sxs-lookup"><span data-stu-id="d832c-168">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d832c-169">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d832c-169">Redistributable</span></span><br/> | <span data-ttu-id="d832c-170">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d832c-170">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d832c-171">DLL</span><span class="sxs-lookup"><span data-stu-id="d832c-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="d832c-172"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d832c-172"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
