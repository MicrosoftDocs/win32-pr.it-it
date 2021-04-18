---
description: L'oggetto patch rappresenta un'istanza univoca di una patch che è stata registrata o applicata. È possibile creare un'istanza dell'oggetto con la proprietà patch come &\# 0034; WindowsInstaller. Installer. patch (PatchCode, ProductCode, UserSid, context) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Patch (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325025"
---
# <a name="patch-object"></a><span data-ttu-id="c0a8f-103">Patch (oggetto)</span><span class="sxs-lookup"><span data-stu-id="c0a8f-103">Patch object</span></span>

<span data-ttu-id="c0a8f-104">L'oggetto **patch** rappresenta un'istanza univoca di una patch che è stata registrata o applicata.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-104">The **Patch** object represents a unique instance of a patch that has been registered or applied.</span></span>

<span data-ttu-id="c0a8f-105">È possibile creare un'istanza dell'oggetto con la proprietà **patch** come "WindowsInstaller. Installer. patch (*PatchCode*, *ProductCode*, *UserSID*, *context*)".</span><span class="sxs-lookup"><span data-stu-id="c0a8f-105">The object can be instantiated with the **Patch** property as "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="c0a8f-106">Per un contesto macchina, il parametro *UserSID* deve essere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-106">For a machine context, the *UserSid* parameter must be an empty string.</span></span> <span data-ttu-id="c0a8f-107">*ProductCode* può essere impostato su una stringa vuota per le patch registrate solo e non ancora applicate a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-107">The *ProductCode* can be set to an empty string for patches that are registered only and not yet applied to any product.</span></span> <span data-ttu-id="c0a8f-108">*ProductCode* può essere impostato su una stringa vuota solo leggendo o aggiornando le informazioni dell'elenco di origine di una patch.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-108">The *ProductCode* can be set to an empty string when only reading or updating a patch's source list information.</span></span>

## <a name="members"></a><span data-ttu-id="c0a8f-109">Membri</span><span class="sxs-lookup"><span data-stu-id="c0a8f-109">Members</span></span>

<span data-ttu-id="c0a8f-110">L'oggetto **patch** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0a8f-110">The **Patch** object has these types of members:</span></span>

-   [<span data-ttu-id="c0a8f-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0a8f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0a8f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0a8f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0a8f-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0a8f-113">Methods</span></span>

<span data-ttu-id="c0a8f-114">L'oggetto **patch** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-114">The **Patch** object has these methods.</span></span>



| <span data-ttu-id="c0a8f-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="c0a8f-115">Method</span></span>                                                               | <span data-ttu-id="c0a8f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0a8f-116">Description</span></span>                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0a8f-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-117">**SourceListAddMediaDisk**</span></span>](patch-sourcelistaddmediadisk.md)       | <span data-ttu-id="c0a8f-118">Aggiungere un disco al set di dischi registrati.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-118">Add a disk to the set of registered disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c0a8f-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-119">**SourceListAddSource**</span></span>](patch-sourcelistaddsource.md)             | <span data-ttu-id="c0a8f-120">Aggiungere un'origine di rete o URL all'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-120">Add a network or URL source to the source list.</span></span> <br/>                                                                             |
| [<span data-ttu-id="c0a8f-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-121">**SourceListClearAll**</span></span>](patch-sourcelistclearall.md)               | <span data-ttu-id="c0a8f-122">Cancella l'elenco di origine completo del tipo di origine specificato.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                                            |
| [<span data-ttu-id="c0a8f-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-123">**SourceListClearMediaDisk**</span></span>](patch-sourcelistclearmediadisk.md)   | <span data-ttu-id="c0a8f-124">Rimuovere un disco dal set di dischi registrati dall'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-124">Remove a disk from the set of registered disks from the source list.</span></span> <br/>                                                        |
| [<span data-ttu-id="c0a8f-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-125">**SourceListClearSource**</span></span>](patch-sourcelistclearsource.md)         | <span data-ttu-id="c0a8f-126">Rimuovere un'origine di rete o URL dall'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-126">Remove a network or URL source from the source list.</span></span><br/>                                                                         |
| [<span data-ttu-id="c0a8f-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-127">**SourceListForceResolution**</span></span>](patch-sourcelistforceresolution.md) | <span data-ttu-id="c0a8f-128">Cancella l'ultima origine utilizzata dall'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-128">Clears the last used source from the source list.</span></span> <span data-ttu-id="c0a8f-129">Questa operazione impone la risoluzione dell'elenco di origine la volta successiva che l'origine è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c0a8f-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0a8f-130">Properties</span></span>

<span data-ttu-id="c0a8f-131">L'oggetto **patch** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-131">The **Patch** object has these properties.</span></span>



| <span data-ttu-id="c0a8f-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0a8f-132">Property</span></span>                                                  | <span data-ttu-id="c0a8f-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0a8f-133">Description</span></span>                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0a8f-134">**Context**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-134">**Context**</span></span>](patch-context.md)<br/>               | <span data-ttu-id="c0a8f-135">Il contesto di questa istanza di patch è un valore MSIINSTALLCONTEXT.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-135">Context of this patch instance is an MSIINSTALLCONTEXT value.</span></span><br/>                                   |
| [<span data-ttu-id="c0a8f-136">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-136">**MediaDisks**</span></span>](patch-mediadisks.md)<br/>         | <span data-ttu-id="c0a8f-137">Enumera tutti i dischi multimediali per questa istanza della patch.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-137">Enumerates all the media disks for this patch instance.</span></span><br/>                                         |
| [<span data-ttu-id="c0a8f-138">**PatchCode**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-138">**PatchCode**</span></span>](patch-patchcode.md)<br/>           | <span data-ttu-id="c0a8f-139">Restituisce il codice della patch.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-139">Returns the patch code.</span></span><br/>                                                                         |
| [<span data-ttu-id="c0a8f-140">**PatchProperty**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-140">**PatchProperty**</span></span>](patch-patchproperty.md)<br/>   | <span data-ttu-id="c0a8f-141">Ottiene le informazioni sulle proprietà di una patch specifica applicata a un'istanza specifica del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-141">Gets property information about a specific patch applied to a specific instance of the product.</span></span><br/> |
| [<span data-ttu-id="c0a8f-142">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-142">**ProductCode**</span></span>](patch-productcode.md)<br/>       | <span data-ttu-id="c0a8f-143">Restituisce il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-143">Returns the product code.</span></span><br/>                                                                       |
| [<span data-ttu-id="c0a8f-144">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-144">**SourceListInfo**</span></span>](patch-sourcelistinfo.md)<br/> | <span data-ttu-id="c0a8f-145">Ottiene e imposta le proprietà delle informazioni sull'origine.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-145">Gets and sets the source information properties.</span></span> <span data-ttu-id="c0a8f-146">Si tratta di una proprietà di lettura o scrittura.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-146">This is a read or write property.</span></span><br/>              |
| [<span data-ttu-id="c0a8f-147">**Fonti**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-147">**Sources**</span></span>](patch-sources.md)<br/>               | <span data-ttu-id="c0a8f-148">Enumera tutte le origini per questa istanza della patch.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-148">Enumerates all the sources for this patch instance.</span></span><br/>                                             |
| [<span data-ttu-id="c0a8f-149">**State**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-149">**State**</span></span>](patch-state.md)<br/>                   | <span data-ttu-id="c0a8f-150">Stato di installazione della patch.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-150">Installation state of the patch.</span></span><br/>                                                                |
| [<span data-ttu-id="c0a8f-151">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="c0a8f-151">**UserSid**</span></span>](patch-usersid.md)<br/>               | <span data-ttu-id="c0a8f-152">Restituisce il SID dell'utente, nell'account in cui è disponibile questa istanza di patch.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-152">Returns the User SID, under the account this patch instance is available.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="c0a8f-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0a8f-153">Requirements</span></span>



| <span data-ttu-id="c0a8f-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a8f-154">Requirement</span></span> | <span data-ttu-id="c0a8f-155">Valore</span><span class="sxs-lookup"><span data-stu-id="c0a8f-155">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a8f-156">Versione</span><span class="sxs-lookup"><span data-stu-id="c0a8f-156">Version</span></span><br/> | <span data-ttu-id="c0a8f-157">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-157">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c0a8f-158">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-158">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c0a8f-159">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c0a8f-159">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="c0a8f-160">DLL</span><span class="sxs-lookup"><span data-stu-id="c0a8f-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0a8f-161"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0a8f-161"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="c0a8f-162">IID</span><span class="sxs-lookup"><span data-stu-id="c0a8f-162">IID</span></span><br/>     | <span data-ttu-id="c0a8f-163">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c0a8f-163">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="c0a8f-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0a8f-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a8f-165">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c0a8f-165">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




