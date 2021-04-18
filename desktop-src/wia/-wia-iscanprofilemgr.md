---
description: L'interfaccia IScanProfileMgr fornisce metodi per la creazione, l'apertura, l'eliminazione e la gestione dei profili di analisi.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Interfaccia IScanProfileMgr (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308249"
---
# <a name="iscanprofilemgr-interface"></a><span data-ttu-id="7310d-103">Interfaccia IScanProfileMgr</span><span class="sxs-lookup"><span data-stu-id="7310d-103">IScanProfileMgr interface</span></span>

<span data-ttu-id="7310d-104">L'interfaccia **IScanProfileMgr** fornisce metodi per la creazione, l'apertura, l'eliminazione e la gestione dei profili di analisi.</span><span class="sxs-lookup"><span data-stu-id="7310d-104">The **IScanProfileMgr** interface provides methods for creating, opening, deleting, and managing scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="7310d-105">Membri</span><span class="sxs-lookup"><span data-stu-id="7310d-105">Members</span></span>

<span data-ttu-id="7310d-106">L'interfaccia **IScanProfileMgr** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7310d-106">The **IScanProfileMgr** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7310d-107">**IScanProfileMgr** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7310d-107">**IScanProfileMgr** also has these types of members:</span></span>

-   [<span data-ttu-id="7310d-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="7310d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7310d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="7310d-109">Methods</span></span>

<span data-ttu-id="7310d-110">L'interfaccia **IScanProfileMgr** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7310d-110">The **IScanProfileMgr** interface has these methods.</span></span>



| <span data-ttu-id="7310d-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="7310d-111">Method</span></span>                                                                              | <span data-ttu-id="7310d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7310d-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7310d-113">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="7310d-113">**CreateProfile**</span></span>](-wia-iscanprofilemgr-createprofile.md)                         | <span data-ttu-id="7310d-114">Crea un profilo di analisi vuoto e lo associa a uno scanner o a un altro elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="7310d-114">Creates an empty scan profile and associates it with a scanner or other WIA 2.0 item.</span></span><br/>                       |
| [<span data-ttu-id="7310d-115">**DeleteAllProfiles**</span><span class="sxs-lookup"><span data-stu-id="7310d-115">**DeleteAllProfiles**</span></span>](-wia-iscanprofilemgr-deleteallprofiles.md)                 | <span data-ttu-id="7310d-116">Elimina tutti i profili di analisi associati al dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="7310d-116">Deletes all the scan profiles associated with the specified device.</span></span><br/>                                         |
| [<span data-ttu-id="7310d-117">**DeleteAllProfilesForUser**</span><span class="sxs-lookup"><span data-stu-id="7310d-117">**DeleteAllProfilesForUser**</span></span>](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | <span data-ttu-id="7310d-118">Elimina tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7310d-118">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span> <br/> |
| [<span data-ttu-id="7310d-119">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="7310d-119">**DeleteProfile**</span></span>](-wia-iscanprofilemgr-deleteprofile.md)                         | <span data-ttu-id="7310d-120">Elimina il profilo di analisi specificato.</span><span class="sxs-lookup"><span data-stu-id="7310d-120">Deletes the specified scan profile.</span></span><br/>                                                                         |
| [<span data-ttu-id="7310d-121">**GetDefaultProfile**</span><span class="sxs-lookup"><span data-stu-id="7310d-121">**GetDefaultProfile**</span></span>](-wia-iscanprofilemgr-getdefaultprofile.md)                 | <span data-ttu-id="7310d-122">Ottiene il profilo di analisi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7310d-122">Gets the default scan profile.</span></span><br/>                                                                              |
| [<span data-ttu-id="7310d-123">**GetNumProfiles**</span><span class="sxs-lookup"><span data-stu-id="7310d-123">**GetNumProfiles**</span></span>](-wia-iscanprofilemgr-getnumprofiles.md)                       | <span data-ttu-id="7310d-124">Ottiene il numero di profili di analisi creati per l'utente nel sistema in cui viene eseguita l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7310d-124">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span><br/> |
| [<span data-ttu-id="7310d-125">**GetNumProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7310d-125">**GetNumProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | <span data-ttu-id="7310d-126">Ottiene il numero di profili di analisi per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7310d-126">Gets the number of scan profiles for the device.</span></span><br/>                                                            |
| [<span data-ttu-id="7310d-127">**GetProfiles**</span><span class="sxs-lookup"><span data-stu-id="7310d-127">**GetProfiles**</span></span>](-wia-iscanprofilemgr-getprofiles.md)                             | <span data-ttu-id="7310d-128">Ottiene tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7310d-128">Gets all the scan profiles available for the user in the system that your application is running under.</span></span><br/>     |
| [<span data-ttu-id="7310d-129">**GetProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7310d-129">**GetProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | <span data-ttu-id="7310d-130">Ottiene tutti i profili di analisi associati a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7310d-130">Gets all the scan profiles associated with a device.</span></span><br/>                                                        |
| [<span data-ttu-id="7310d-131">**OpenProfile**</span><span class="sxs-lookup"><span data-stu-id="7310d-131">**OpenProfile**</span></span>](-wia-iscanprofilemgr-openprofile.md)                             | <span data-ttu-id="7310d-132">Apre un profilo di analisi salvato su disco come file XML.</span><span class="sxs-lookup"><span data-stu-id="7310d-132">Opens a scan profile that has been saved to disk as an XML file.</span></span><br/>                                            |
| [<span data-ttu-id="7310d-133">**Aggiorna**</span><span class="sxs-lookup"><span data-stu-id="7310d-133">**Refresh**</span></span>](-wia-iscanprofilemgr-refresh.md)                                     | <span data-ttu-id="7310d-134">Enumera nuovamente tutti i profili di analisi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="7310d-134">Re-enumerates all the scan profiles in the system.</span></span><br/>                                                          |
| [<span data-ttu-id="7310d-135">**SetDefault**</span><span class="sxs-lookup"><span data-stu-id="7310d-135">**SetDefault**</span></span>](-wia-iscanprofilemgr-setdefault.md)                               | <span data-ttu-id="7310d-136">Imposta il profilo di analisi specificato come profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="7310d-136">Sets the specified scan profile as the default profile.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="7310d-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="7310d-137">Remarks</span></span>

<span data-ttu-id="7310d-138">Per creare un oggetto **IScanProfileMgr** , usare il metodo [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="7310d-138">To create an **IScanProfileMgr** object, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method with the following parameters:</span></span>

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

<span data-ttu-id="7310d-139">Se un profilo di analisi viene salvato utilizzando il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , viene archiviato come file XML in% UserProfile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="7310d-139">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="7310d-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7310d-140">Requirements</span></span>



| <span data-ttu-id="7310d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7310d-141">Requirement</span></span> | <span data-ttu-id="7310d-142">Valore</span><span class="sxs-lookup"><span data-stu-id="7310d-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7310d-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7310d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7310d-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7310d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7310d-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7310d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7310d-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7310d-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7310d-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7310d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7310d-148"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7310d-148"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="7310d-149">IDL</span><span class="sxs-lookup"><span data-stu-id="7310d-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7310d-150"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7310d-150"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7310d-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7310d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7310d-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="7310d-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="7310d-153">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="7310d-153">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
