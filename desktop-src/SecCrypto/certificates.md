---
description: Rappresenta una raccolta di oggetti certificate.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Oggetto Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323979"
---
# <a name="certificates-object"></a><span data-ttu-id="a3f8e-103">Oggetto Certificates</span><span class="sxs-lookup"><span data-stu-id="a3f8e-103">Certificates object</span></span>

<span data-ttu-id="a3f8e-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a3f8e-105">Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a3f8e-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a3f8e-106">L'oggetto **Certificates** rappresenta una raccolta di oggetti [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="a3f8e-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="a3f8e-107">Ogni oggetto [**certificato**](certificate.md) rappresenta un singolo [*certificato digitale*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a3f8e-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="a3f8e-108">L'oggetto **Certificates** espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3f8e-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="a3f8e-109">**ICertificates2**: introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="a3f8e-110">**ICertificates**: introdotta in capicol 1,0.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a3f8e-111">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a3f8e-111">When to use</span></span>

<span data-ttu-id="a3f8e-112">L'oggetto **certificati** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3f8e-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="a3f8e-113">Aggiungere o rimuovere un oggetto [**certificato**](certificate.md) da o verso la raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="a3f8e-114">Generare un subset della raccolta cercando un set di certificati o visualizzando una finestra di dialogo per selezionare i certificati.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="a3f8e-115">Cancellare tutti gli oggetti [**certificato**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="a3f8e-116">Recuperare il numero di certificati nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="a3f8e-117">Recuperare un oggetto [**certificato**](certificate.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="a3f8e-118">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="a3f8e-119">Membri</span><span class="sxs-lookup"><span data-stu-id="a3f8e-119">Members</span></span>

<span data-ttu-id="a3f8e-120">L'oggetto **certificati** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a3f8e-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="a3f8e-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="a3f8e-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="a3f8e-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a3f8e-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a3f8e-123">Metodi</span><span class="sxs-lookup"><span data-stu-id="a3f8e-123">Methods</span></span>

<span data-ttu-id="a3f8e-124">Questi metodi sono disponibili nell'oggetto **Certificates** .</span><span class="sxs-lookup"><span data-stu-id="a3f8e-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="a3f8e-125">Metodo</span><span class="sxs-lookup"><span data-stu-id="a3f8e-125">Method</span></span>                                | <span data-ttu-id="a3f8e-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3f8e-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3f8e-127">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="a3f8e-128">Aggiunge un oggetto [**certificato**](certificate.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="a3f8e-129">(Ereditato da **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a3f8e-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="a3f8e-130">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="a3f8e-131">Rimuove tutti gli oggetti [**certificato**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="a3f8e-132">(Ereditato da **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a3f8e-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="a3f8e-133">**Find**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="a3f8e-134">Restituisce un oggetto **Certificates** che contiene tutti i certificati che corrispondono ai criteri di ricerca specificati.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="a3f8e-135">(Ereditato da **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a3f8e-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="a3f8e-136">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="a3f8e-137">Rimuove un singolo oggetto [**certificato**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="a3f8e-138">(Ereditato da **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a3f8e-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="a3f8e-139">**Salva**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="a3f8e-140">Salva i certificati in un file specificato.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="a3f8e-141">(Ereditato da **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a3f8e-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="a3f8e-142">**Select**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="a3f8e-143">Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="a3f8e-144">(Ereditato da **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a3f8e-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="a3f8e-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a3f8e-145">Properties</span></span>

<span data-ttu-id="a3f8e-146">L'oggetto **Certificates** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="a3f8e-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a3f8e-147">Property</span></span>                                             | <span data-ttu-id="a3f8e-148">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a3f8e-148">Access type</span></span>          | <span data-ttu-id="a3f8e-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3f8e-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3f8e-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="a3f8e-151">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a3f8e-151">Read-only</span></span><br/> | <span data-ttu-id="a3f8e-152">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="a3f8e-153">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="a3f8e-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="a3f8e-154">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="a3f8e-155">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a3f8e-155">Read-only</span></span><br/> | <span data-ttu-id="a3f8e-156">Recupera il numero di oggetti [**certificato**](certificate.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="a3f8e-157">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="a3f8e-158">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a3f8e-158">Read-only</span></span><br/> | <span data-ttu-id="a3f8e-159">Recupera un oggetto [**certificato**](certificate.md) che rappresenta il certificato indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="a3f8e-160">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-160">This is the default property.</span></span><br/> <span data-ttu-id="a3f8e-161">(Ereditato da **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="a3f8e-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="a3f8e-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3f8e-162">Remarks</span></span>

<span data-ttu-id="a3f8e-163">È possibile creare l'oggetto **certificati** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="a3f8e-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="a3f8e-164">Il ProgID per l'oggetto **certificati** è "CAPICOM. Certificati. 2 ".</span><span class="sxs-lookup"><span data-stu-id="a3f8e-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="a3f8e-165">**CAPICOM 1. *x*:** il ProgID per l'oggetto **certificati** è "CAPICOM. Certificates. 1 ".</span><span class="sxs-lookup"><span data-stu-id="a3f8e-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f8e-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3f8e-166">Requirements</span></span>



| <span data-ttu-id="a3f8e-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f8e-167">Requirement</span></span> | <span data-ttu-id="a3f8e-168">Valore</span><span class="sxs-lookup"><span data-stu-id="a3f8e-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f8e-169">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a3f8e-169">End of client support</span></span><br/> | <span data-ttu-id="a3f8e-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3f8e-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a3f8e-171">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a3f8e-171">End of server support</span></span><br/> | <span data-ttu-id="a3f8e-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3f8e-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a3f8e-173">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a3f8e-173">Redistributable</span></span><br/>       | <span data-ttu-id="a3f8e-174">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3f8e-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a3f8e-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a3f8e-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a3f8e-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3f8e-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f8e-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3f8e-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f8e-178">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="a3f8e-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
