---
description: Rappresenta una raccolta di oggetti di estensione.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Oggetto Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329018"
---
# <a name="extensions-object"></a><span data-ttu-id="54867-103">Oggetto Extensions</span><span class="sxs-lookup"><span data-stu-id="54867-103">Extensions object</span></span>

<span data-ttu-id="54867-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="54867-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="54867-105">Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="54867-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="54867-106">L'oggetto **Extensions** rappresenta una raccolta di oggetti di [**estensione**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="54867-106">The **Extensions** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="54867-107">Ogni oggetto [**estensione**](extension.md) rappresenta una singola estensione del certificato.</span><span class="sxs-lookup"><span data-stu-id="54867-107">Each [**Extension**](extension.md) object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="54867-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="54867-108">When to use</span></span>

<span data-ttu-id="54867-109">L'oggetto **Extensions** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="54867-109">The **Extensions** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="54867-110">Recuperare il numero di estensioni del certificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="54867-110">Retrieve the number of certificate extensions in the collection.</span></span>
-   <span data-ttu-id="54867-111">Recuperare un oggetto [**estensione**](extension.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="54867-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="54867-112">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="54867-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="54867-113">Membri</span><span class="sxs-lookup"><span data-stu-id="54867-113">Members</span></span>

<span data-ttu-id="54867-114">L'oggetto **Extensions** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="54867-114">The **Extensions** object has these types of members:</span></span>

-   [<span data-ttu-id="54867-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54867-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54867-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54867-116">Properties</span></span>

<span data-ttu-id="54867-117">L'oggetto **Extensions** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="54867-117">The **Extensions** object has these properties.</span></span>



| <span data-ttu-id="54867-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54867-118">Property</span></span>                                           | <span data-ttu-id="54867-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="54867-119">Access type</span></span>          | <span data-ttu-id="54867-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54867-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54867-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="54867-121">**\_NewEnum**</span></span>](extensions-newenum.md)<br/> | <span data-ttu-id="54867-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="54867-122">Read-only</span></span><br/> | <span data-ttu-id="54867-123">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="54867-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="54867-124">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="54867-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="54867-125">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="54867-125">**Count**</span></span>](extensions-count.md)<br/>       | <span data-ttu-id="54867-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="54867-126">Read-only</span></span><br/> | <span data-ttu-id="54867-127">Recupera il numero di oggetti di [**estensione**](extension.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="54867-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="54867-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="54867-128">**Item**</span></span>](extensions-item.md)<br/>         | <span data-ttu-id="54867-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="54867-129">Read-only</span></span><br/> | <span data-ttu-id="54867-130">Recupera l'oggetto di [**estensione**](extension.md) che rappresenta l'estensione del certificato indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="54867-130">Retrieves the [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span> <span data-ttu-id="54867-131">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="54867-131">This is the default property.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="54867-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="54867-132">Remarks</span></span>

<span data-ttu-id="54867-133">L'oggetto **Extensions** viene restituito dal metodo [**Certificate. Extensions**](certificate-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="54867-133">The **Extensions** object is returned by the [**Certificate.Extensions**](certificate-extensions.md) method.</span></span>

<span data-ttu-id="54867-134">Impossibile creare l'oggetto **Extensions** .</span><span class="sxs-lookup"><span data-stu-id="54867-134">The **Extensions** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="54867-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54867-135">Requirements</span></span>



| <span data-ttu-id="54867-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="54867-136">Requirement</span></span> | <span data-ttu-id="54867-137">Valore</span><span class="sxs-lookup"><span data-stu-id="54867-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54867-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="54867-138">End of client support</span></span><br/> | <span data-ttu-id="54867-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54867-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="54867-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="54867-140">End of server support</span></span><br/> | <span data-ttu-id="54867-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54867-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="54867-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="54867-142">Redistributable</span></span><br/>       | <span data-ttu-id="54867-143">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="54867-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="54867-144">DLL</span><span class="sxs-lookup"><span data-stu-id="54867-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="54867-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54867-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
