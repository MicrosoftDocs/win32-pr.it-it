---
description: Rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Oggetto Qualifier
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328595"
---
# <a name="qualifier-object"></a><span data-ttu-id="79506-103">Oggetto Qualifier</span><span class="sxs-lookup"><span data-stu-id="79506-103">Qualifier object</span></span>

<span data-ttu-id="79506-104">\[L'oggetto **qualificatore** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="79506-104">\[The **Qualifier** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="79506-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="79506-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="79506-106">L'oggetto **qualificatore** rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.</span><span class="sxs-lookup"><span data-stu-id="79506-106">The **Qualifier** object represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="79506-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="79506-107">When to use</span></span>

<span data-ttu-id="79506-108">L'oggetto **qualificatore** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="79506-108">The **Qualifier** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="79506-109">Recuperare l'identificatore di oggetto del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="79506-109">Retrieve the object identifier of the qualifier.</span></span>
-   <span data-ttu-id="79506-110">Recuperare il Uniform Resource Identifier (URI) che punta a un CPS pubblicato dall' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="79506-110">Retrieve the Uniform Resource Identifier (URI) that points to a CPS published by the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="79506-111">Recuperare il nome dell'organizzazione associata al qualificatore.</span><span class="sxs-lookup"><span data-stu-id="79506-111">Retrieve the name of the organization associated with the qualifier.</span></span>
-   <span data-ttu-id="79506-112">Recuperare il nome e il contenuto di un avviso utente.</span><span class="sxs-lookup"><span data-stu-id="79506-112">Retrieve the name and content of a user notice.</span></span>

## <a name="members"></a><span data-ttu-id="79506-113">Membri</span><span class="sxs-lookup"><span data-stu-id="79506-113">Members</span></span>

<span data-ttu-id="79506-114">L'oggetto **qualificatore** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="79506-114">The **Qualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="79506-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="79506-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79506-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="79506-116">Properties</span></span>

<span data-ttu-id="79506-117">L'oggetto **qualificatore** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="79506-117">The **Qualifier** object has these properties.</span></span>



| <span data-ttu-id="79506-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="79506-118">Property</span></span>                                                          | <span data-ttu-id="79506-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="79506-119">Access type</span></span>          | <span data-ttu-id="79506-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79506-120">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79506-121">**CPSPointer**</span><span class="sxs-lookup"><span data-stu-id="79506-121">**CPSPointer**</span></span>](qualifier-cpspointer.md)<br/>             | <span data-ttu-id="79506-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="79506-122">Read-only</span></span><br/> | <span data-ttu-id="79506-123">Recupera una stringa che contiene l'URI che punta a un CPS pubblicato dalla CA.</span><span class="sxs-lookup"><span data-stu-id="79506-123">Retrieves a string that contains the URI that points to a CPS published by the CA.</span></span><br/>                                       |
| [<span data-ttu-id="79506-124">**ExplicitText**</span><span class="sxs-lookup"><span data-stu-id="79506-124">**ExplicitText**</span></span>](qualifier-explicittext.md)<br/>         | <span data-ttu-id="79506-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="79506-125">Read-only</span></span><br/> | <span data-ttu-id="79506-126">Recupera una stringa che contiene il contenuto della comunicazione utente.</span><span class="sxs-lookup"><span data-stu-id="79506-126">Retrieves a string that contains the content of the user notice.</span></span> <span data-ttu-id="79506-127">Questa proprietà può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="79506-127">This property may be empty.</span></span><br/>                             |
| [<span data-ttu-id="79506-128">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="79506-128">**NoticeNumbers**</span></span>](qualifier-noticenumbers.md)<br/>       | <span data-ttu-id="79506-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="79506-129">Read-only</span></span><br/> | <span data-ttu-id="79506-130">Recupera un oggetto **NoticeNumbers** che contiene la raccolta di numeri di nota utente.</span><span class="sxs-lookup"><span data-stu-id="79506-130">Retrieves a **NoticeNumbers** object that contains the collection of user notice numbers.</span></span> <span data-ttu-id="79506-131">Questa proprietà può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="79506-131">This property may be empty.</span></span><br/>    |
| [<span data-ttu-id="79506-132">**OID**</span><span class="sxs-lookup"><span data-stu-id="79506-132">**OID**</span></span>](qualifier-oid.md)<br/>                           | <span data-ttu-id="79506-133">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="79506-133">Read-only</span></span><br/> | <span data-ttu-id="79506-134">Recupera un oggetto [**OID**](oid.md) che identifica il qualificatore.</span><span class="sxs-lookup"><span data-stu-id="79506-134">Retrieves an [**OID**](oid.md) object that identifies the qualifier.</span></span> <span data-ttu-id="79506-135">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="79506-135">This is the default property.</span></span><br/>                      |
| [<span data-ttu-id="79506-136">**OrganizationName**</span><span class="sxs-lookup"><span data-stu-id="79506-136">**OrganizationName**</span></span>](qualifier-organizationname.md)<br/> | <span data-ttu-id="79506-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="79506-137">Read-only</span></span><br/> | <span data-ttu-id="79506-138">Recupera una stringa che contiene il nome dell'organizzazione associata al qualificatore.</span><span class="sxs-lookup"><span data-stu-id="79506-138">Retrieves a string that contains the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="79506-139">Questa proprietà può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="79506-139">This property may be empty.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="79506-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="79506-140">Remarks</span></span>

<span data-ttu-id="79506-141">Impossibile creare l'oggetto **qualificatore** .</span><span class="sxs-lookup"><span data-stu-id="79506-141">The **Qualifier** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="79506-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79506-142">Requirements</span></span>



| <span data-ttu-id="79506-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="79506-143">Requirement</span></span> | <span data-ttu-id="79506-144">Valore</span><span class="sxs-lookup"><span data-stu-id="79506-144">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79506-145">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="79506-145">Redistributable</span></span><br/> | <span data-ttu-id="79506-146">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="79506-146">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="79506-147">DLL</span><span class="sxs-lookup"><span data-stu-id="79506-147">DLL</span></span><br/>             | <dl> <span data-ttu-id="79506-148"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79506-148"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
