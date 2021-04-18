---
description: Rappresenta una raccolta di oggetti firmatari.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Oggetto signers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325287"
---
# <a name="signers-object"></a><span data-ttu-id="17890-103">Oggetto signers</span><span class="sxs-lookup"><span data-stu-id="17890-103">Signers object</span></span>

<span data-ttu-id="17890-104">\[L'oggetto **signers** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="17890-104">\[The **Signers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="17890-105">Usare invece una raccolta di oggetti CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="17890-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="17890-106">Per ulteriori informazioni, vedere la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="17890-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="17890-107">L'oggetto **signers** rappresenta una raccolta di oggetti [**firmatari**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="17890-107">The **Signers** object represents a collection of [**Signer**](signer.md) objects.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="17890-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="17890-108">When to use</span></span>

<span data-ttu-id="17890-109">L'oggetto **signers** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="17890-109">The **Signers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="17890-110">Recuperare il numero di certificati nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="17890-110">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="17890-111">Recuperare un oggetto **firmatari** specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="17890-111">Retrieve a specific **Signers** object from the collection.</span></span>
-   <span data-ttu-id="17890-112">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="17890-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="17890-113">Membri</span><span class="sxs-lookup"><span data-stu-id="17890-113">Members</span></span>

<span data-ttu-id="17890-114">L'oggetto **signers** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="17890-114">The **Signers** object has these types of members:</span></span>

-   [<span data-ttu-id="17890-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17890-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17890-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17890-116">Properties</span></span>

<span data-ttu-id="17890-117">L'oggetto **signers** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="17890-117">The **Signers** object has these properties.</span></span>



| <span data-ttu-id="17890-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17890-118">Property</span></span>                                        | <span data-ttu-id="17890-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="17890-119">Access type</span></span>          | <span data-ttu-id="17890-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17890-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17890-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="17890-121">**\_NewEnum**</span></span>](signers-newenum.md)<br/> | <span data-ttu-id="17890-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="17890-122">Read-only</span></span><br/> | <span data-ttu-id="17890-123">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="17890-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="17890-124">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="17890-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="17890-125">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="17890-125">**Count**</span></span>](signers-count.md)<br/>       | <span data-ttu-id="17890-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="17890-126">Read-only</span></span><br/> | <span data-ttu-id="17890-127">Numero di oggetti [**firmatari**](signer.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="17890-127">Number of [**Signer**](signer.md) objects in the collection.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="17890-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="17890-128">**Item**</span></span>](signers-item.md)<br/>         | <span data-ttu-id="17890-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="17890-129">Read-only</span></span><br/> | <span data-ttu-id="17890-130">Recupera l'oggetto [**firmatario**](signer.md) che rappresenta il firmatario indicizzato.</span><span class="sxs-lookup"><span data-stu-id="17890-130">Retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="17890-131">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="17890-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="17890-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="17890-132">Remarks</span></span>

<span data-ttu-id="17890-133">Impossibile creare l'oggetto **firmatari** .</span><span class="sxs-lookup"><span data-stu-id="17890-133">The **Signers** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="17890-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17890-134">Requirements</span></span>



| <span data-ttu-id="17890-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="17890-135">Requirement</span></span> | <span data-ttu-id="17890-136">Valore</span><span class="sxs-lookup"><span data-stu-id="17890-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17890-137">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="17890-137">Redistributable</span></span><br/> | <span data-ttu-id="17890-138">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="17890-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="17890-139">DLL</span><span class="sxs-lookup"><span data-stu-id="17890-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="17890-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17890-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17890-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17890-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17890-142">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="17890-142">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
