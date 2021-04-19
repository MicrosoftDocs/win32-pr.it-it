---
description: L'oggetto Product rappresenta un'istanza univoca di un prodotto annunciato, installato o sconosciuto. È possibile creare un'istanza dell'oggetto con la proprietà Product come &\# 0034; WindowsInstaller. Installer. Product (ProductCode, UserSid, context) &\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Oggetto Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326540"
---
# <a name="product-object"></a><span data-ttu-id="3ca36-103">Oggetto Product</span><span class="sxs-lookup"><span data-stu-id="3ca36-103">Product object</span></span>

<span data-ttu-id="3ca36-104">L'oggetto **Product** rappresenta un'istanza univoca di un prodotto annunciato, installato o sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="3ca36-104">The **Product** object represents a unique instance of a product that is either advertised, installed or unknown.</span></span>

<span data-ttu-id="3ca36-105">È possibile creare un'istanza dell'oggetto con la proprietà **Product** come "WindowsInstaller. Installer. Product (*ProductCode*, *UserSID*, *context*)".</span><span class="sxs-lookup"><span data-stu-id="3ca36-105">The object can be instantiated with the **Product** property as "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="3ca36-106">*UserSID* deve essere null per il contesto per computer.</span><span class="sxs-lookup"><span data-stu-id="3ca36-106">*UserSid* must be NULL for per-machine context.</span></span> <span data-ttu-id="3ca36-107">*UserSID* può essere null per l'utente corrente specificato, quando il contesto non è per computer.</span><span class="sxs-lookup"><span data-stu-id="3ca36-107">*UserSid* can be null to specified current user, when context is not per-machine.</span></span> <span data-ttu-id="3ca36-108">*ProductCode* e i parametri di *contesto* sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="3ca36-108">*ProductCode* and *Context* parameters are required.</span></span>

## <a name="members"></a><span data-ttu-id="3ca36-109">Membri</span><span class="sxs-lookup"><span data-stu-id="3ca36-109">Members</span></span>

<span data-ttu-id="3ca36-110">L'oggetto **prodotto** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3ca36-110">The **Product** object has these types of members:</span></span>

-   [<span data-ttu-id="3ca36-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3ca36-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3ca36-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ca36-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3ca36-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="3ca36-113">Methods</span></span>

<span data-ttu-id="3ca36-114">L'oggetto **prodotto** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3ca36-114">The **Product** object has these methods.</span></span>



| <span data-ttu-id="3ca36-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="3ca36-115">Method</span></span>                                                                 | <span data-ttu-id="3ca36-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ca36-116">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca36-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="3ca36-117">**SourceListAddMediaDisk**</span></span>](product-sourcelistaddmediadisk.md)       | <span data-ttu-id="3ca36-118">Aggiungere un disco al set di dischi registrati.</span><span class="sxs-lookup"><span data-stu-id="3ca36-118">Add a disk to the set of registered disks.</span></span><br/>                                                              |
| [<span data-ttu-id="3ca36-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="3ca36-119">**SourceListAddSource**</span></span>](product-sourcelistaddsource.md)             | <span data-ttu-id="3ca36-120">Aggiungere un'origine di rete o URL all'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="3ca36-120">Add a network or URL source to the source list.</span></span><br/>                                                         |
| [<span data-ttu-id="3ca36-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="3ca36-121">**SourceListClearAll**</span></span>](product-sourcelistclearall.md)               | <span data-ttu-id="3ca36-122">Cancella l'elenco di origine completo del tipo di origine specificato.</span><span class="sxs-lookup"><span data-stu-id="3ca36-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                       |
| [<span data-ttu-id="3ca36-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="3ca36-123">**SourceListClearMediaDisk**</span></span>](product-sourcelistclearmediadisk.md)   | <span data-ttu-id="3ca36-124">Rimuovere un disco dal set di dischi registrati dall'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="3ca36-124">Remove a disk from the set of registered disks from the source list.</span></span><br/>                                    |
| [<span data-ttu-id="3ca36-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="3ca36-125">**SourceListClearSource**</span></span>](product-sourcelistclearsource.md)         | <span data-ttu-id="3ca36-126">Rimuovere un'origine di rete o URL dall'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="3ca36-126">Remove a network or URL source from the source list.</span></span><br/>                                                    |
| [<span data-ttu-id="3ca36-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="3ca36-127">**SourceListForceResolution**</span></span>](product-sourcelistforceresolution.md) | <span data-ttu-id="3ca36-128">Cancella l'ultima origine usata.</span><span class="sxs-lookup"><span data-stu-id="3ca36-128">Clears the last used source.</span></span> <span data-ttu-id="3ca36-129">Questa operazione impone la risoluzione dell'elenco di origine la volta successiva che l'origine è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="3ca36-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3ca36-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ca36-130">Properties</span></span>

<span data-ttu-id="3ca36-131">L'oggetto **Product** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3ca36-131">The **Product** object has these properties.</span></span>



| <span data-ttu-id="3ca36-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ca36-132">Property</span></span>                                                      | <span data-ttu-id="3ca36-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ca36-133">Description</span></span>                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca36-134">**ComponentState**</span><span class="sxs-lookup"><span data-stu-id="3ca36-134">**ComponentState**</span></span>](product-componentstate.md)<br/>   | <span data-ttu-id="3ca36-135">Stato di un componente specificato per questa istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3ca36-135">The state of a specified component for this product instance.</span></span> <br/>                   |
| [<span data-ttu-id="3ca36-136">**Context**</span><span class="sxs-lookup"><span data-stu-id="3ca36-136">**Context**</span></span>](product-context.md)<br/>                 | <span data-ttu-id="3ca36-137">Contesto di questa istanza del prodotto come valore MSIINSTALLCONTEXT.</span><span class="sxs-lookup"><span data-stu-id="3ca36-137">Context of this product instance as an MSIINSTALLCONTEXT value.</span></span> <br/>                 |
| [<span data-ttu-id="3ca36-138">**FeatureState**</span><span class="sxs-lookup"><span data-stu-id="3ca36-138">**FeatureState**</span></span>](product-featurestate.md)<br/>       | <span data-ttu-id="3ca36-139">Stato di una funzionalità specificata per questa istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3ca36-139">The state of a specified feature for this product instance.</span></span> <br/>                     |
| [<span data-ttu-id="3ca36-140">**InstallProperty**</span><span class="sxs-lookup"><span data-stu-id="3ca36-140">**InstallProperty**</span></span>](product-installproperty.md)<br/> | <span data-ttu-id="3ca36-141">Valore di una proprietà specificata.</span><span class="sxs-lookup"><span data-stu-id="3ca36-141">The value of a specified property.</span></span> <br/>                                              |
| [<span data-ttu-id="3ca36-142">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="3ca36-142">**MediaDisks**</span></span>](product-mediadisks.md)<br/>           | <span data-ttu-id="3ca36-143">Enumera tutti i dischi multimediali per questa istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3ca36-143">Enumerates all the media disks for this product instance.</span></span><br/>                        |
| [<span data-ttu-id="3ca36-144">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="3ca36-144">**ProductCode**</span></span>](product-productcode.md)<br/>         | <span data-ttu-id="3ca36-145">Restituisce il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3ca36-145">Returns the product code.</span></span> <br/>                                                       |
| [<span data-ttu-id="3ca36-146">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="3ca36-146">**SourceListInfo**</span></span>](product-sourcelistinfo.md)<br/>   | <span data-ttu-id="3ca36-147">Ottenere e impostare le proprietà delle informazioni sull'origine.</span><span class="sxs-lookup"><span data-stu-id="3ca36-147">Get and set the source information properties.</span></span> <span data-ttu-id="3ca36-148">Si tratta di una proprietà di lettura o scrittura.</span><span class="sxs-lookup"><span data-stu-id="3ca36-148">This is a read or write property.</span></span><br/> |
| [<span data-ttu-id="3ca36-149">**Fonti**</span><span class="sxs-lookup"><span data-stu-id="3ca36-149">**Sources**</span></span>](product-sources.md)<br/>                 | <span data-ttu-id="3ca36-150">Enumera tutte le origini per questa istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3ca36-150">Enumerates all the sources for this product instance.</span></span><br/>                            |
| [<span data-ttu-id="3ca36-151">**State**</span><span class="sxs-lookup"><span data-stu-id="3ca36-151">**State**</span></span>](product-state.md)<br/>                     | <span data-ttu-id="3ca36-152">Stato di installazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3ca36-152">Installation state of the product.</span></span><br/>                                               |
| [<span data-ttu-id="3ca36-153">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="3ca36-153">**UserSid**</span></span>](product-usersid.md)<br/>                 | <span data-ttu-id="3ca36-154">Restituisce il SID dell'utente, in base al quale account è disponibile questa istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3ca36-154">Returns the User SID, under which account this product instance is available.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="3ca36-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ca36-155">Requirements</span></span>



| <span data-ttu-id="3ca36-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ca36-156">Requirement</span></span> | <span data-ttu-id="3ca36-157">Valore</span><span class="sxs-lookup"><span data-stu-id="3ca36-157">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca36-158">Versione</span><span class="sxs-lookup"><span data-stu-id="3ca36-158">Version</span></span><br/> | <span data-ttu-id="3ca36-159">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3ca36-159">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3ca36-160">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3ca36-160">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3ca36-161">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ca36-161">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="3ca36-162">DLL</span><span class="sxs-lookup"><span data-stu-id="3ca36-162">DLL</span></span><br/>     | <dl> <span data-ttu-id="3ca36-163"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ca36-163"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="3ca36-164">IID</span><span class="sxs-lookup"><span data-stu-id="3ca36-164">IID</span></span><br/>     | <span data-ttu-id="3ca36-165">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3ca36-165">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="3ca36-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ca36-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca36-167">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3ca36-167">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




