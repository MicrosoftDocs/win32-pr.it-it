---
description: Rappresenta una raccolta di qualificatori.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Oggetto Qualifiers (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326891"
---
# <a name="qualifiers-object"></a><span data-ttu-id="97d1f-103">Oggetto qualificatori</span><span class="sxs-lookup"><span data-stu-id="97d1f-103">Qualifiers object</span></span>

<span data-ttu-id="97d1f-104">\[L'oggetto **qualificatori** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="97d1f-104">\[The **Qualifiers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97d1f-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="97d1f-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="97d1f-106">L'oggetto **Qualifiers** rappresenta una raccolta di qualificatori.</span><span class="sxs-lookup"><span data-stu-id="97d1f-106">The **Qualifiers** object represents a collection of qualifiers.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="97d1f-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="97d1f-107">When to use</span></span>

<span data-ttu-id="97d1f-108">L'oggetto **qualificatori** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="97d1f-108">The **Qualifiers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="97d1f-109">Recuperare una proprietà estesa specifica dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="97d1f-109">Retrieve a specific extended property from the collection.</span></span>
-   <span data-ttu-id="97d1f-110">Recuperare il numero di proprietà estese nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="97d1f-110">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="97d1f-111">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="97d1f-111">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="97d1f-112">Membri</span><span class="sxs-lookup"><span data-stu-id="97d1f-112">Members</span></span>

<span data-ttu-id="97d1f-113">L'oggetto **qualificatori** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="97d1f-113">The **Qualifiers** object has these types of members:</span></span>

-   [<span data-ttu-id="97d1f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97d1f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97d1f-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97d1f-115">Properties</span></span>

<span data-ttu-id="97d1f-116">L'oggetto **qualificatori** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="97d1f-116">The **Qualifiers** object has these properties.</span></span>



| <span data-ttu-id="97d1f-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97d1f-117">Property</span></span>                                           | <span data-ttu-id="97d1f-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="97d1f-118">Access type</span></span>          | <span data-ttu-id="97d1f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97d1f-119">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97d1f-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="97d1f-120">**\_NewEnum**</span></span>](qualifiers-newenum.md)<br/> | <span data-ttu-id="97d1f-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97d1f-121">Read-only</span></span><br/> | <span data-ttu-id="97d1f-122">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="97d1f-122">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="97d1f-123">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="97d1f-123">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="97d1f-124">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="97d1f-124">**Count**</span></span>](qualifiers-count.md)<br/>       | <span data-ttu-id="97d1f-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97d1f-125">Read-only</span></span><br/> | <span data-ttu-id="97d1f-126">Recupera il numero di qualificatori nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="97d1f-126">Retrieves the number of qualifiers in the collection.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="97d1f-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="97d1f-127">**Item**</span></span>](qualifiers-item.md)<br/>         | <span data-ttu-id="97d1f-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97d1f-128">Read-only</span></span><br/> | <span data-ttu-id="97d1f-129">Recupera un oggetto [**qualificatore**](qualifier.md) che rappresenta il qualificatore indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="97d1f-129">Retrieves a [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span> <span data-ttu-id="97d1f-130">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="97d1f-130">This is the default property.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="97d1f-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="97d1f-131">Remarks</span></span>

<span data-ttu-id="97d1f-132">Impossibile creare l'oggetto **qualificatori** .</span><span class="sxs-lookup"><span data-stu-id="97d1f-132">The **Qualifiers** object cannot be created.</span></span>

<span data-ttu-id="97d1f-133">La proprietà dell'oggetto [**PolicyInformation. Qualifiers**](policyinformation-qualifiers.md) CAPICOM restituisce un oggetto **qualificatori** .</span><span class="sxs-lookup"><span data-stu-id="97d1f-133">The [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) CAPICOM object property returns a **Qualifiers** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d1f-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97d1f-134">Requirements</span></span>



| <span data-ttu-id="97d1f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="97d1f-135">Requirement</span></span> | <span data-ttu-id="97d1f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="97d1f-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97d1f-137">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="97d1f-137">Redistributable</span></span><br/> | <span data-ttu-id="97d1f-138">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="97d1f-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="97d1f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97d1f-139">Header</span></span><br/>          | <dl> <span data-ttu-id="97d1f-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="97d1f-140"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="97d1f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="97d1f-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="97d1f-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d1f-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
