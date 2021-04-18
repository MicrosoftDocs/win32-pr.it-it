---
description: Raccolta di oggetti PolicyInformation.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Oggetto CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327996"
---
# <a name="certificatepolicies-object"></a><span data-ttu-id="b7039-103">Oggetto CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="b7039-103">CertificatePolicies object</span></span>

<span data-ttu-id="b7039-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7039-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b7039-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per recuperare i criteri del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="b7039-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="b7039-106">L'oggetto **CertificatePolicies** rappresenta una raccolta di oggetti [**PolicyInformation**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="b7039-106">The **CertificatePolicies** object represents a collection of [**PolicyInformation**](policyinformation.md) objects.</span></span> <span data-ttu-id="b7039-107">Ogni oggetto [**PolicyInformation**](policyinformation.md) rappresenta un singolo criterio di certificato.</span><span class="sxs-lookup"><span data-stu-id="b7039-107">Each [**PolicyInformation**](policyinformation.md) object represents a single certificate policy.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b7039-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b7039-108">When to use</span></span>

<span data-ttu-id="b7039-109">L'oggetto **CertificatePolicies** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7039-109">The **CertificatePolicies** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b7039-110">Recuperare il numero di criteri certificati nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7039-110">Retrieve the number of certificate policies in the collection.</span></span>
-   <span data-ttu-id="b7039-111">Recuperare un oggetto [**PolicyInformation**](policyinformation.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7039-111">Retrieve a specific [**PolicyInformation**](policyinformation.md) object from the collection.</span></span>
-   <span data-ttu-id="b7039-112">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7039-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="b7039-113">Membri</span><span class="sxs-lookup"><span data-stu-id="b7039-113">Members</span></span>

<span data-ttu-id="b7039-114">L'oggetto **CertificatePolicies** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b7039-114">The **CertificatePolicies** object has these types of members:</span></span>

-   [<span data-ttu-id="b7039-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7039-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7039-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7039-116">Properties</span></span>

<span data-ttu-id="b7039-117">L'oggetto **CertificatePolicies** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b7039-117">The **CertificatePolicies** object has these properties.</span></span>



| <span data-ttu-id="b7039-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7039-118">Property</span></span>                                                    | <span data-ttu-id="b7039-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="b7039-119">Access type</span></span>          | <span data-ttu-id="b7039-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7039-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7039-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="b7039-121">**\_NewEnum**</span></span>](certificatepolicies-newenum.md)<br/> | <span data-ttu-id="b7039-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7039-122">Read-only</span></span><br/> | <span data-ttu-id="b7039-123">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7039-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="b7039-124">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="b7039-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="b7039-125">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="b7039-125">**Count**</span></span>](certificatepolicies-count.md)<br/>       | <span data-ttu-id="b7039-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7039-126">Read-only</span></span><br/> | <span data-ttu-id="b7039-127">Recupera il numero di oggetti [**PolicyInformation**](policyinformation.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="b7039-127">Retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="b7039-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b7039-128">**Item**</span></span>](certificatepolicies-item.md)<br/>         | <span data-ttu-id="b7039-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7039-129">Read-only</span></span><br/> | <span data-ttu-id="b7039-130">Recupera un oggetto [**PolicyInformation**](policyinformation.md) che rappresenta i criteri di certificato indicizzati della raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7039-130">Retrieves a [**PolicyInformation**](policyinformation.md) object that represents the indexed certificate policy of the collection.</span></span> <span data-ttu-id="b7039-131">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="b7039-131">This is the default property.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="b7039-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7039-132">Remarks</span></span>

<span data-ttu-id="b7039-133">Impossibile creare l'oggetto **CertificatePolicies** .</span><span class="sxs-lookup"><span data-stu-id="b7039-133">The **CertificatePolicies** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7039-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7039-134">Requirements</span></span>



| <span data-ttu-id="b7039-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7039-135">Requirement</span></span> | <span data-ttu-id="b7039-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b7039-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7039-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b7039-137">End of client support</span></span><br/> | <span data-ttu-id="b7039-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7039-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b7039-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b7039-139">End of server support</span></span><br/> | <span data-ttu-id="b7039-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7039-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b7039-141">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b7039-141">Redistributable</span></span><br/>       | <span data-ttu-id="b7039-142">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7039-142">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b7039-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b7039-143">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b7039-144"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7039-144"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
