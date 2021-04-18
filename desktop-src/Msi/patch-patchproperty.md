---
description: La proprietà PatchProperty ottiene informazioni su una patch specifica applicata a un'istanza specifica del prodotto. Questa proprietà chiama MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Patch. PatchProperty, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329469"
---
# <a name="patchpatchproperty-method"></a><span data-ttu-id="3325b-104">Patch. PatchProperty, metodo</span><span class="sxs-lookup"><span data-stu-id="3325b-104">Patch.PatchProperty method</span></span>

<span data-ttu-id="3325b-105">La proprietà **PatchProperty** ottiene informazioni su una patch specifica applicata a un'istanza specifica del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3325b-105">The **PatchProperty** property gets information about a specific patch applied to a specific instance of the product.</span></span> <span data-ttu-id="3325b-106">Questa proprietà chiama [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="3325b-106">This property calls [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="3325b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3325b-107">Syntax</span></span>


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a><span data-ttu-id="3325b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3325b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3325b-109">*szProperty*</span><span class="sxs-lookup"><span data-stu-id="3325b-109">*szProperty*</span></span> 
</dt> <dd>

<span data-ttu-id="3325b-110">Il parametro *szProperty* può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3325b-110">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="3325b-111">Nome</span><span class="sxs-lookup"><span data-stu-id="3325b-111">Name</span></span>          | <span data-ttu-id="3325b-112">Significato</span><span class="sxs-lookup"><span data-stu-id="3325b-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3325b-113">LocalPackage</span><span class="sxs-lookup"><span data-stu-id="3325b-113">LocalPackage</span></span>  | <span data-ttu-id="3325b-114">Ottiene il file di patch memorizzato nella cache utilizzato dal prodotto.</span><span class="sxs-lookup"><span data-stu-id="3325b-114">Get the cached patch file used by the product.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3325b-115">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="3325b-115">Transforms</span></span>    | <span data-ttu-id="3325b-116">Ottenere il set di trasformazioni di patch applicato al prodotto dall'ultima installazione della patch.</span><span class="sxs-lookup"><span data-stu-id="3325b-116">Get the set of patch transforms applied to the product by the last patch installation.</span></span> <span data-ttu-id="3325b-117">Questo valore potrebbe non essere disponibile per le applicazioni non gestite per utente se l'utente non è connesso al computer.</span><span class="sxs-lookup"><span data-stu-id="3325b-117">This value may not be available for per-user-unmanaged applications if the user is not logged in to the computer.</span></span>                                                                                                                     |
| <span data-ttu-id="3325b-118">InstallDate</span><span class="sxs-lookup"><span data-stu-id="3325b-118">InstallDate</span></span>   | <span data-ttu-id="3325b-119">Ottenere la data in cui è stata applicata la patch al prodotto.</span><span class="sxs-lookup"><span data-stu-id="3325b-119">Get the date when the patch was applied to the product.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3325b-120">Disinstallabili</span><span class="sxs-lookup"><span data-stu-id="3325b-120">Uninstallable</span></span> | <span data-ttu-id="3325b-121">Restituisce "1" se la patch è contrassegnata come possibile per la disinstallazione dal prodotto.</span><span class="sxs-lookup"><span data-stu-id="3325b-121">Returns "1" if the patch is marked as possible to uninstall from the product.</span></span> <span data-ttu-id="3325b-122">In questo caso, il programma di installazione può comunque bloccare la disinstallazione se questa patch è richiesta da un'altra patch che non può essere disinstallata.</span><span class="sxs-lookup"><span data-stu-id="3325b-122">In this case, the installer can still block the uninstallation if this patch is required by another patch that cannot be uninstalled.</span></span>                                                                                                          |
| <span data-ttu-id="3325b-123">State</span><span class="sxs-lookup"><span data-stu-id="3325b-123">State</span></span>         | <span data-ttu-id="3325b-124">Restituisce "1" Se questa patch è attualmente applicata al prodotto.</span><span class="sxs-lookup"><span data-stu-id="3325b-124">Returns "1" if this patch is currently applied to the product.</span></span> <span data-ttu-id="3325b-125">Restituisce "2" Se questa patch è stata sostituita da un'altra patch.</span><span class="sxs-lookup"><span data-stu-id="3325b-125">Returns "2" if this patch has been superseded by another patch.</span></span> <span data-ttu-id="3325b-126">Restituisce "4" Se questa patch è stata resa obsoleta da un'altra patch.</span><span class="sxs-lookup"><span data-stu-id="3325b-126">Returns "4" if this patch has been made obsolete by another patch.</span></span> <span data-ttu-id="3325b-127">Questi valori corrispondono alle costanti usate dal parametro *dwFilter* di [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="3325b-127">These values correspond to the constants used by the *dwFilter* parameter of [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span> |
| <span data-ttu-id="3325b-128">DisplayName</span><span class="sxs-lookup"><span data-stu-id="3325b-128">DisplayName</span></span>   | <span data-ttu-id="3325b-129">Ottenere il nome visualizzato registrato per la patch.</span><span class="sxs-lookup"><span data-stu-id="3325b-129">Get the registered display name for the patch.</span></span> <span data-ttu-id="3325b-130">Per le patch che non includono la proprietà DisplayName nella tabella [MsiPatchMetadata](msipatchmetadata-table.md) , il nome visualizzato restituito è una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="3325b-130">For patches that do not include the DisplayName property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned display name is an empty string ("").</span></span>                                                                                                      |
| <span data-ttu-id="3325b-131">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="3325b-131">MoreInfoURL</span></span>   | <span data-ttu-id="3325b-132">Ottenere l'URL delle informazioni di supporto registrato per la patch.</span><span class="sxs-lookup"><span data-stu-id="3325b-132">Get the registered support information URL for the patch.</span></span> <span data-ttu-id="3325b-133">Per le patch che non includono la proprietà MoreInfoURL nella tabella [MsiPatchMetadata](msipatchmetadata-table.md) , l'URL delle informazioni di supporto restituito è una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="3325b-133">For patches that do not include the MoreInfoURL property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned support information URL is an empty string ("").</span></span>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3325b-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3325b-134">Return value</span></span>

<span data-ttu-id="3325b-135">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3325b-135">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3325b-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="3325b-136">Remarks</span></span>

<span data-ttu-id="3325b-137">Questo metodo può restituire \_ l'errore Unknown \_ patch, se l'oggetto [**patch**](patch-object.md) viene inizializzato con una stringa vuota per *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="3325b-137">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3325b-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3325b-138">Requirements</span></span>



| <span data-ttu-id="3325b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="3325b-139">Requirement</span></span> | <span data-ttu-id="3325b-140">Valore</span><span class="sxs-lookup"><span data-stu-id="3325b-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3325b-141">Versione</span><span class="sxs-lookup"><span data-stu-id="3325b-141">Version</span></span><br/> | <span data-ttu-id="3325b-142">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3325b-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3325b-143">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3325b-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3325b-144">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3325b-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="3325b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3325b-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="3325b-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3325b-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="3325b-147">IID</span><span class="sxs-lookup"><span data-stu-id="3325b-147">IID</span></span><br/>     | <span data-ttu-id="3325b-148">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3325b-148">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="3325b-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3325b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3325b-150">**Patch**</span><span class="sxs-lookup"><span data-stu-id="3325b-150">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="3325b-151">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="3325b-151">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="3325b-152">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="3325b-152">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="3325b-153">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="3325b-153">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




