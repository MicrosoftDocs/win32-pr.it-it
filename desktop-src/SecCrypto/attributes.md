---
description: Rappresenta una raccolta di oggetti attributo.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Oggetto Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326530"
---
# <a name="attributes-object"></a><span data-ttu-id="e35be-103">Oggetto Attributes</span><span class="sxs-lookup"><span data-stu-id="e35be-103">Attributes object</span></span>

<span data-ttu-id="e35be-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e35be-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="e35be-105">Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e35be-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e35be-106">L'oggetto **Attributes** rappresenta una raccolta di oggetti [**attribute**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e35be-106">The **Attributes** object represents a collection of [**Attribute**](attribute.md) objects.</span></span> <span data-ttu-id="e35be-107">Ogni oggetto [**attributo**](attribute.md) rappresenta un singolo attributo di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="e35be-107">Each [**Attribute**](attribute.md) object represents a single attribute of a message.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e35be-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e35be-108">When to use</span></span>

<span data-ttu-id="e35be-109">L'oggetto **Attributes** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="e35be-109">The **Attributes** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e35be-110">Aggiungere o rimuovere un oggetto [**attributo**](attribute.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-110">Add or remove a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="e35be-111">Cancellare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-111">Clear the collection.</span></span>
-   <span data-ttu-id="e35be-112">Recuperare il numero di attributi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-112">Retrieve the number of attributes in the collection.</span></span>
-   <span data-ttu-id="e35be-113">Recuperare un oggetto [**attributo**](attribute.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-113">Retrieve a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="e35be-114">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="e35be-115">Membri</span><span class="sxs-lookup"><span data-stu-id="e35be-115">Members</span></span>

<span data-ttu-id="e35be-116">L'oggetto **Attributes** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e35be-116">The **Attributes** object has these types of members:</span></span>

-   [<span data-ttu-id="e35be-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="e35be-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="e35be-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e35be-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e35be-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="e35be-119">Methods</span></span>

<span data-ttu-id="e35be-120">L'oggetto **Attributes** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e35be-120">The **Attributes** object has these methods.</span></span>



| <span data-ttu-id="e35be-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="e35be-121">Method</span></span>                              | <span data-ttu-id="e35be-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e35be-122">Description</span></span>                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="e35be-123">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="e35be-123">**Add**</span></span>](attributes-add.md)       | <span data-ttu-id="e35be-124">Aggiunge un oggetto [**attributo**](attribute.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-124">Adds an [**Attribute**](attribute.md) object to the collection.</span></span><br/>       |
| [<span data-ttu-id="e35be-125">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="e35be-125">**Clear**</span></span>](attributes-clear.md)   | <span data-ttu-id="e35be-126">Cancella tutti gli oggetti [**attributo**](attribute.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-126">Clears all [**Attribute**](attribute.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="e35be-127">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="e35be-127">**Remove**</span></span>](attributes-remove.md) | <span data-ttu-id="e35be-128">Rimuove un oggetto [**attributo**](attribute.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-128">Removes an [**Attribute**](attribute.md) object from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="e35be-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e35be-129">Properties</span></span>

<span data-ttu-id="e35be-130">L'oggetto **Attributes** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e35be-130">The **Attributes** object has these properties.</span></span>



| <span data-ttu-id="e35be-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e35be-131">Property</span></span>                                           | <span data-ttu-id="e35be-132">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e35be-132">Access type</span></span>          | <span data-ttu-id="e35be-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e35be-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e35be-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e35be-134">**\_NewEnum**</span></span>](attributes-newenum.md)<br/> | <span data-ttu-id="e35be-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e35be-135">Read-only</span></span><br/> | <span data-ttu-id="e35be-136">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="e35be-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e35be-137">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e35be-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="e35be-138">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="e35be-138">**Count**</span></span>](attributes-count.md)<br/>       | <span data-ttu-id="e35be-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e35be-139">Read-only</span></span><br/> | <span data-ttu-id="e35be-140">Recupera il numero di oggetti [**attributo**](attribute.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="e35be-140">Retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="e35be-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e35be-141">**Item**</span></span>](attributes-item.md)<br/>         | <span data-ttu-id="e35be-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e35be-142">Read-only</span></span><br/> | <span data-ttu-id="e35be-143">Recupera l'oggetto [**attributo**](attribute.md) che rappresenta l'attributo indicizzato.</span><span class="sxs-lookup"><span data-stu-id="e35be-143">Retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="e35be-144">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="e35be-144">This is the default property.</span></span><br/>                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="e35be-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="e35be-145">Remarks</span></span>

<span data-ttu-id="e35be-146">Impossibile creare l'oggetto **Attributes** .</span><span class="sxs-lookup"><span data-stu-id="e35be-146">The **Attributes** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="e35be-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e35be-147">Requirements</span></span>



| <span data-ttu-id="e35be-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="e35be-148">Requirement</span></span> | <span data-ttu-id="e35be-149">Valore</span><span class="sxs-lookup"><span data-stu-id="e35be-149">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e35be-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e35be-150">End of client support</span></span><br/> | <span data-ttu-id="e35be-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e35be-151">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e35be-152">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e35be-152">End of server support</span></span><br/> | <span data-ttu-id="e35be-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e35be-153">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e35be-154">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e35be-154">Redistributable</span></span><br/>       | <span data-ttu-id="e35be-155">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e35be-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e35be-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e35be-156">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e35be-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e35be-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e35be-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e35be-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e35be-159">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="e35be-159">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
