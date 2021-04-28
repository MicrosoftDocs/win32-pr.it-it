---
description: 'Oggetto Certificates: rappresenta una raccolta di oggetti Certificate.'
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
ms.openlocfilehash: 8efb9221f39b8544eabe8f6c00d21f6cfdf20c14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098389"
---
# <a name="certificates-object"></a><span data-ttu-id="4edda-103">Oggetto Certificates</span><span class="sxs-lookup"><span data-stu-id="4edda-103">Certificates object</span></span>

<span data-ttu-id="4edda-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4edda-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4edda-105">Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]</span><span class="sxs-lookup"><span data-stu-id="4edda-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4edda-106">**L'oggetto Certificates** rappresenta una raccolta di [**oggetti**](certificate.md) Certificate.</span><span class="sxs-lookup"><span data-stu-id="4edda-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="4edda-107">Ogni [**oggetto Certificate**](certificate.md) rappresenta un singolo certificato [*digitale.*](../secgloss/d-gly.md)</span><span class="sxs-lookup"><span data-stu-id="4edda-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="4edda-108">**L'oggetto Certificates** espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="4edda-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="4edda-109">**ICertificates2:** introdotto in CAPICOM 2.0.</span><span class="sxs-lookup"><span data-stu-id="4edda-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="4edda-110">**ICertificates:** introdotto in CAPICOM 1.0.</span><span class="sxs-lookup"><span data-stu-id="4edda-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4edda-111">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4edda-111">When to use</span></span>

<span data-ttu-id="4edda-112">**L'oggetto** Certificates viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="4edda-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4edda-113">Aggiungere o rimuovere un [**oggetto Certificate**](certificate.md) da o verso la raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="4edda-114">Generare un subset della raccolta trovando un set di certificati o visualizzando una finestra di dialogo per selezionare i certificati.</span><span class="sxs-lookup"><span data-stu-id="4edda-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="4edda-115">Cancellare tutti gli [**oggetti Certificate**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="4edda-116">Recuperare il numero di certificati nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="4edda-117">Recuperare un [**oggetto Certificate**](certificate.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="4edda-118">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="4edda-119">Membri</span><span class="sxs-lookup"><span data-stu-id="4edda-119">Members</span></span>

<span data-ttu-id="4edda-120">**L'oggetto Certificates** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4edda-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="4edda-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="4edda-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="4edda-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4edda-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4edda-123">Metodi</span><span class="sxs-lookup"><span data-stu-id="4edda-123">Methods</span></span>

<span data-ttu-id="4edda-124">**L'oggetto Certificates** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4edda-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="4edda-125">Metodo</span><span class="sxs-lookup"><span data-stu-id="4edda-125">Method</span></span>                                | <span data-ttu-id="4edda-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4edda-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4edda-127">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="4edda-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="4edda-128">Aggiunge un [**oggetto Certificate**](certificate.md) all'insieme.</span><span class="sxs-lookup"><span data-stu-id="4edda-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="4edda-129">Ereditato da **CertificatesICertificates2**</span><span class="sxs-lookup"><span data-stu-id="4edda-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="4edda-130">**Chiaro**</span><span class="sxs-lookup"><span data-stu-id="4edda-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="4edda-131">Rimuove tutti [**gli oggetti**](certificate.md) Certificate dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="4edda-132">Ereditato da **CertificatesICertificates2**</span><span class="sxs-lookup"><span data-stu-id="4edda-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="4edda-133">**Find**</span><span class="sxs-lookup"><span data-stu-id="4edda-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="4edda-134">Restituisce un **oggetto Certificates** che contiene tutti i certificati che corrispondono ai criteri di ricerca specificati.</span><span class="sxs-lookup"><span data-stu-id="4edda-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="4edda-135">Ereditato da **CertificatesICertificates2**</span><span class="sxs-lookup"><span data-stu-id="4edda-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="4edda-136">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="4edda-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="4edda-137">Rimuove un singolo [**oggetto Certificate**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="4edda-138">Ereditato da **CertificatesICertificates2**</span><span class="sxs-lookup"><span data-stu-id="4edda-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="4edda-139">**Salva**</span><span class="sxs-lookup"><span data-stu-id="4edda-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="4edda-140">Salva i certificati in un file specificato.</span><span class="sxs-lookup"><span data-stu-id="4edda-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="4edda-141">Ereditato da **CertificatesICertificates2**</span><span class="sxs-lookup"><span data-stu-id="4edda-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="4edda-142">**Selezionare**</span><span class="sxs-lookup"><span data-stu-id="4edda-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="4edda-143">Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati.</span><span class="sxs-lookup"><span data-stu-id="4edda-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="4edda-144">Ereditato da **CertificatesICertificates2**</span><span class="sxs-lookup"><span data-stu-id="4edda-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="4edda-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4edda-145">Properties</span></span>

<span data-ttu-id="4edda-146">Queste **proprietà sono** disponibili nell'oggetto Certificates.</span><span class="sxs-lookup"><span data-stu-id="4edda-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="4edda-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4edda-147">Property</span></span>                                             | <span data-ttu-id="4edda-148">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="4edda-148">Access type</span></span>          | <span data-ttu-id="4edda-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4edda-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4edda-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="4edda-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="4edda-151">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4edda-151">Read-only</span></span><br/> | <span data-ttu-id="4edda-152">Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="4edda-153">Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="4edda-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="4edda-154">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="4edda-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="4edda-155">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4edda-155">Read-only</span></span><br/> | <span data-ttu-id="4edda-156">Recupera il numero di [**oggetti Certificate**](certificate.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="4edda-157">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4edda-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="4edda-158">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4edda-158">Read-only</span></span><br/> | <span data-ttu-id="4edda-159">Recupera un [**oggetto Certificate**](certificate.md) che rappresenta il certificato indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="4edda-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="4edda-160">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="4edda-160">This is the default property.</span></span><br/> <span data-ttu-id="4edda-161">Ereditato da **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="4edda-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="4edda-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="4edda-162">Remarks</span></span>

<span data-ttu-id="4edda-163">**L'oggetto Certificates** può essere creato ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="4edda-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="4edda-164">Il ProgID per **l'oggetto Certificates** è "CAPICOM. Certificates.2".</span><span class="sxs-lookup"><span data-stu-id="4edda-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="4edda-165">**CAPICOM 1. *x*:** ProgID per l'oggetto **Certificates** è "CAPICOM. Certificates.1".</span><span class="sxs-lookup"><span data-stu-id="4edda-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="4edda-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4edda-166">Requirements</span></span>



| <span data-ttu-id="4edda-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="4edda-167">Requirement</span></span> | <span data-ttu-id="4edda-168">Valore</span><span class="sxs-lookup"><span data-stu-id="4edda-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4edda-169">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4edda-169">End of client support</span></span><br/> | <span data-ttu-id="4edda-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4edda-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4edda-171">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4edda-171">End of server support</span></span><br/> | <span data-ttu-id="4edda-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4edda-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4edda-173">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4edda-173">Redistributable</span></span><br/>       | <span data-ttu-id="4edda-174">CAPICOM 2.0 o versione successiva in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4edda-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4edda-175">DLL</span><span class="sxs-lookup"><span data-stu-id="4edda-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4edda-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4edda-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4edda-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4edda-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edda-178">**Oggetti di crittografia**</span><span class="sxs-lookup"><span data-stu-id="4edda-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
