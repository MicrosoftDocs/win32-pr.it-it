---
description: Consente di accedere alle informazioni sui criteri di un'estensione.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Oggetto PolicyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324839"
---
# <a name="policyinformation-object"></a><span data-ttu-id="e799b-103">Oggetto PolicyInformation</span><span class="sxs-lookup"><span data-stu-id="e799b-103">PolicyInformation object</span></span>

<span data-ttu-id="e799b-104">\[L'oggetto **PolicyInformation** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e799b-104">\[The **PolicyInformation** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e799b-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per elaborare le informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="e799b-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="e799b-106">L'oggetto **PolicyInformation** fornisce l'accesso alle informazioni sui criteri di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="e799b-106">The **PolicyInformation** object provides access to the policy information of an extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e799b-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e799b-107">When to use</span></span>

<span data-ttu-id="e799b-108">L'oggetto **PolicyInformation** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="e799b-108">The **PolicyInformation** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e799b-109">Recuperare l'OID del criterio.</span><span class="sxs-lookup"><span data-stu-id="e799b-109">Retrieve the policy OID.</span></span>
-   <span data-ttu-id="e799b-110">Recuperare una raccolta dei qualificatori del criterio.</span><span class="sxs-lookup"><span data-stu-id="e799b-110">Retrieve a collection of the policy's qualifiers.</span></span>

## <a name="members"></a><span data-ttu-id="e799b-111">Membri</span><span class="sxs-lookup"><span data-stu-id="e799b-111">Members</span></span>

<span data-ttu-id="e799b-112">L'oggetto **PolicyInformation** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e799b-112">The **PolicyInformation** object has these types of members:</span></span>

-   [<span data-ttu-id="e799b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e799b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e799b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e799b-114">Properties</span></span>

<span data-ttu-id="e799b-115">L'oggetto **PolicyInformation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e799b-115">The **PolicyInformation** object has these properties.</span></span>



| <span data-ttu-id="e799b-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e799b-116">Property</span></span>                                                      | <span data-ttu-id="e799b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e799b-117">Description</span></span>                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e799b-118">**OID**</span><span class="sxs-lookup"><span data-stu-id="e799b-118">**OID**</span></span>](policyinformation-oid.md)<br/>               | <span data-ttu-id="e799b-119">Recupera l'OID del criterio come oggetto [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="e799b-119">Retrieves the policy's OID, as an [**OID**](oid.md) object.</span></span> <span data-ttu-id="e799b-120">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="e799b-120">This is the default property.</span></span><br/>       |
| [<span data-ttu-id="e799b-121">**Qualificatori**</span><span class="sxs-lookup"><span data-stu-id="e799b-121">**Qualifiers**</span></span>](policyinformation-qualifiers.md)<br/> | <span data-ttu-id="e799b-122">Recupera una raccolta dei qualificatori del criterio come oggetto [**qualificatori**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="e799b-122">Retrieves a collection of the policy's qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e799b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e799b-123">Remarks</span></span>

<span data-ttu-id="e799b-124">Impossibile creare l'oggetto **PolicyInformation** .</span><span class="sxs-lookup"><span data-stu-id="e799b-124">The **PolicyInformation** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="e799b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e799b-125">Requirements</span></span>



| <span data-ttu-id="e799b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e799b-126">Requirement</span></span> | <span data-ttu-id="e799b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e799b-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e799b-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e799b-128">Redistributable</span></span><br/> | <span data-ttu-id="e799b-129">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e799b-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e799b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e799b-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="e799b-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e799b-131"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
