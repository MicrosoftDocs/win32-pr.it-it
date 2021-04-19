---
description: L'oggetto PublicKey rappresenta una chiave pubblica in un oggetto Certificate.
title: PublicKey (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333285"
---
# <a name="publickey-object"></a><span data-ttu-id="20aaf-103">PublicKey (oggetto)</span><span class="sxs-lookup"><span data-stu-id="20aaf-103">PublicKey object</span></span>

<span data-ttu-id="20aaf-104">\[L'oggetto **publicKey** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="20aaf-104">\[The **PublicKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="20aaf-105">Usare invece la [**Proprietà X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="20aaf-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="20aaf-106">L'oggetto **publicKey** rappresenta una chiave pubblica in un oggetto [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="20aaf-106">The **PublicKey** object represents a public key in a [**Certificate**](certificate.md) object.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="20aaf-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="20aaf-107">When to use</span></span>

<span data-ttu-id="20aaf-108">L'oggetto **publicKey** viene utilizzato per recuperare i dati relativi alla chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="20aaf-108">The **PublicKey** object is used to retrieve data about the public key.</span></span>

## <a name="members"></a><span data-ttu-id="20aaf-109">Membri</span><span class="sxs-lookup"><span data-stu-id="20aaf-109">Members</span></span>

<span data-ttu-id="20aaf-110">L'oggetto **publicKey** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="20aaf-110">The **PublicKey** object has these types of members:</span></span>

-   [<span data-ttu-id="20aaf-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20aaf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20aaf-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20aaf-112">Properties</span></span>

<span data-ttu-id="20aaf-113">L'oggetto **publicKey** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="20aaf-113">The **PublicKey** object has these properties.</span></span>



| <span data-ttu-id="20aaf-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20aaf-114">Property</span></span>                                                            | <span data-ttu-id="20aaf-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="20aaf-115">Access type</span></span>          | <span data-ttu-id="20aaf-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aaf-116">Description</span></span>                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aaf-117">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="20aaf-117">**Algorithm**</span></span>](publickey-algorithm.md)<br/>                 | <span data-ttu-id="20aaf-118">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20aaf-118">Read-only</span></span><br/> | <span data-ttu-id="20aaf-119">Recupera l'oggetto [**OID**](oid.md) che identifica l'algoritmo utilizzato dalla chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="20aaf-119">Retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="20aaf-120">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="20aaf-120">This is the default property.</span></span><br/> |
| [<span data-ttu-id="20aaf-121">**EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="20aaf-121">**EncodedKey**</span></span>](publickey-encodedkey.md)<br/>               | <span data-ttu-id="20aaf-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20aaf-122">Read-only</span></span><br/> | <span data-ttu-id="20aaf-123">Recupera un oggetto [**EncodedData**](encodeddata.md) che fornisce l'accesso al valore della chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="20aaf-123">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span><br/>                 |
| [<span data-ttu-id="20aaf-124">**EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="20aaf-124">**EncodedParameters**</span></span>](publickey-encodedparameters.md)<br/> | <span data-ttu-id="20aaf-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20aaf-125">Read-only</span></span><br/> | <span data-ttu-id="20aaf-126">Recupera un oggetto [**EncodedData**](encodeddata.md) che fornisce l'accesso ai parametri dell'algoritmo a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="20aaf-126">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span><br/>  |
| [<span data-ttu-id="20aaf-127">**Lunghezza**</span><span class="sxs-lookup"><span data-stu-id="20aaf-127">**Length**</span></span>](publickey-length.md)<br/>                       | <span data-ttu-id="20aaf-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20aaf-128">Read-only</span></span><br/> | <span data-ttu-id="20aaf-129">Recupera la lunghezza della chiave pubblica in bit.</span><span class="sxs-lookup"><span data-stu-id="20aaf-129">Retrieves the length of the public key in bits.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="20aaf-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="20aaf-130">Remarks</span></span>

<span data-ttu-id="20aaf-131">Impossibile creare l'oggetto **publicKey** .</span><span class="sxs-lookup"><span data-stu-id="20aaf-131">The **PublicKey** object cannot be created.</span></span>

<span data-ttu-id="20aaf-132">L'oggetto **publicKey** viene utilizzato dal metodo [**Certificate. PublicKey**](certificate-publickey.md) .</span><span class="sxs-lookup"><span data-stu-id="20aaf-132">The **PublicKey** object is used by the [**Certificate.PublicKey**](certificate-publickey.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="20aaf-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20aaf-133">Requirements</span></span>



| <span data-ttu-id="20aaf-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="20aaf-134">Requirement</span></span> | <span data-ttu-id="20aaf-135">Valore</span><span class="sxs-lookup"><span data-stu-id="20aaf-135">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20aaf-136">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="20aaf-136">Redistributable</span></span><br/> | <span data-ttu-id="20aaf-137">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="20aaf-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="20aaf-138">DLL</span><span class="sxs-lookup"><span data-stu-id="20aaf-138">DLL</span></span><br/>             | <dl> <span data-ttu-id="20aaf-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20aaf-139"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
