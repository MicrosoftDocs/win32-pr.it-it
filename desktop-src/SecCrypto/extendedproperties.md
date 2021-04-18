---
description: Rappresenta una raccolta di oggetti ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Oggetto ExtendedProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329226"
---
# <a name="extendedproperties-object"></a><span data-ttu-id="fd3c0-103">Oggetto ExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="fd3c0-103">ExtendedProperties object</span></span>

<span data-ttu-id="fd3c0-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fd3c0-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="fd3c0-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd3c0-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="fd3c0-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="fd3c0-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="fd3c0-108">L'oggetto **ExtendedProperties** rappresenta una raccolta di oggetti [**ExtendedProperty**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3c0-108">The **ExtendedProperties** object represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span> <span data-ttu-id="fd3c0-109">Ogni oggetto rappresenta una singola proprietà estesa.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-109">Each object represents a single extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="fd3c0-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="fd3c0-110">When to use</span></span>

<span data-ttu-id="fd3c0-111">L'oggetto **ExtendedProperties** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd3c0-111">The **ExtendedProperties** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="fd3c0-112">Aggiungere o rimuovere un oggetto [**ExtendedProperty**](extendedproperty.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-112">Add or remove an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="fd3c0-113">Recuperare il numero di proprietà estese nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-113">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="fd3c0-114">Recuperare un oggetto [**ExtendedProperty**](extendedproperty.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-114">Retrieve a specific [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="fd3c0-115">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="fd3c0-116">Membri</span><span class="sxs-lookup"><span data-stu-id="fd3c0-116">Members</span></span>

<span data-ttu-id="fd3c0-117">L'oggetto **ExtendedProperties** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fd3c0-117">The **ExtendedProperties** object has these types of members:</span></span>

-   [<span data-ttu-id="fd3c0-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="fd3c0-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="fd3c0-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd3c0-119">Properties</span></span>](#extendedproperties-object)

### <a name="methods"></a><span data-ttu-id="fd3c0-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="fd3c0-120">Methods</span></span>

<span data-ttu-id="fd3c0-121">L'oggetto **ExtendedProperties** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-121">The **ExtendedProperties** object has these methods.</span></span>



| <span data-ttu-id="fd3c0-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="fd3c0-122">Method</span></span>                                      | <span data-ttu-id="fd3c0-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd3c0-123">Description</span></span>                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd3c0-124">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="fd3c0-124">**Add**</span></span>](extendedproperties-add.md)       | <span data-ttu-id="fd3c0-125">Aggiunge un oggetto [**ExtendedProperty**](extendedproperty.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-125">Adds an [**ExtendedProperty**](extendedproperty.md) object to the collection.</span></span><br/>      |
| [<span data-ttu-id="fd3c0-126">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="fd3c0-126">**Remove**</span></span>](extendedproperties-remove.md) | <span data-ttu-id="fd3c0-127">Rimuove un oggetto [**ExtendedProperty**](extendedproperty.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-127">Removes an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fd3c0-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd3c0-128">Properties</span></span>

<span data-ttu-id="fd3c0-129">L'oggetto **ExtendedProperties** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-129">The **ExtendedProperties** object has these properties.</span></span>



| <span data-ttu-id="fd3c0-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd3c0-130">Property</span></span>                                                   | <span data-ttu-id="fd3c0-131">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="fd3c0-131">Access type</span></span>          | <span data-ttu-id="fd3c0-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd3c0-132">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd3c0-133">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="fd3c0-133">**\_NewEnum**</span></span>](extendedproperties-newenum.md)<br/> | <span data-ttu-id="fd3c0-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd3c0-134">Read-only</span></span><br/> | <span data-ttu-id="fd3c0-135">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-135">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="fd3c0-136">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fd3c0-136">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="fd3c0-137">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="fd3c0-137">**Count**</span></span>](extendedproperties-count.md)<br/>       | <span data-ttu-id="fd3c0-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd3c0-138">Read-only</span></span><br/> | <span data-ttu-id="fd3c0-139">Recupera il numero di oggetti [**ExtendedProperty**](extendedproperty.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-139">Retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="fd3c0-140">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fd3c0-140">**Item**</span></span>](extendedproperties-item.md)<br/>         | <span data-ttu-id="fd3c0-141">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd3c0-141">Read-only</span></span><br/> | <span data-ttu-id="fd3c0-142">Recupera un oggetto [**ExtendedProperty**](extendedproperty.md) che rappresenta la proprietà estesa indicizzata della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-142">Retrieves an [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span> <span data-ttu-id="fd3c0-143">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="fd3c0-143">This is the default property.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="fd3c0-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd3c0-144">Remarks</span></span>

<span data-ttu-id="fd3c0-145">Impossibile creare l'oggetto **ExtendedProperty** .</span><span class="sxs-lookup"><span data-stu-id="fd3c0-145">The **ExtendedProperties** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3c0-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd3c0-146">Requirements</span></span>



| <span data-ttu-id="fd3c0-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd3c0-147">Requirement</span></span> | <span data-ttu-id="fd3c0-148">Valore</span><span class="sxs-lookup"><span data-stu-id="fd3c0-148">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3c0-149">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fd3c0-149">End of client support</span></span><br/> | <span data-ttu-id="fd3c0-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd3c0-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fd3c0-151">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fd3c0-151">End of server support</span></span><br/> | <span data-ttu-id="fd3c0-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd3c0-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fd3c0-153">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fd3c0-153">Redistributable</span></span><br/>       | <span data-ttu-id="fd3c0-154">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fd3c0-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fd3c0-155">DLL</span><span class="sxs-lookup"><span data-stu-id="fd3c0-155">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fd3c0-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd3c0-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
