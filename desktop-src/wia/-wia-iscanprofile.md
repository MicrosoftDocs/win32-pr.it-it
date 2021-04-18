---
description: L'interfaccia IScanProfile rappresenta un singolo profilo di analisi e consente alle applicazioni di impostare e ottenere le proprietà del profilo.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Interfaccia IScanProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312432"
---
# <a name="iscanprofile-interface"></a><span data-ttu-id="09873-103">Interfaccia IScanProfile</span><span class="sxs-lookup"><span data-stu-id="09873-103">IScanProfile interface</span></span>

<span data-ttu-id="09873-104">L'interfaccia **IScanProfile** rappresenta un singolo profilo di analisi e consente alle applicazioni di impostare e ottenere le proprietà del profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-104">The **IScanProfile** interface represents a single scan profile and enables applications to set and get the properties of the profile.</span></span>

## <a name="members"></a><span data-ttu-id="09873-105">Membri</span><span class="sxs-lookup"><span data-stu-id="09873-105">Members</span></span>

<span data-ttu-id="09873-106">L'interfaccia **IScanProfile** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="09873-106">The **IScanProfile** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="09873-107">**IScanProfile** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="09873-107">**IScanProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="09873-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="09873-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="09873-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="09873-109">Methods</span></span>

<span data-ttu-id="09873-110">L'interfaccia **IScanProfile** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="09873-110">The **IScanProfile** interface has these methods.</span></span>



| <span data-ttu-id="09873-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="09873-111">Method</span></span>                                                     | <span data-ttu-id="09873-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09873-112">Description</span></span>                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09873-113">**GetAllPropIDs**</span><span class="sxs-lookup"><span data-stu-id="09873-113">**GetAllPropIDs**</span></span>](-wia-iscanprofile-getallpropids.md)   | <span data-ttu-id="09873-114">Ottiene tutti gli ID di proprietà disponibili in un profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-114">Gets all available property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="09873-115">**GetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="09873-115">**GetDeviceID**</span></span>](-wia-iscanprofile-getdeviceid.md)       | <span data-ttu-id="09873-116">Restituisce l'ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09873-116">Returns the ID of the device.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="09873-117">**GetGUID**</span><span class="sxs-lookup"><span data-stu-id="09873-117">**GetGUID**</span></span>](-wia-iscanprofile-getguid.md)               | <span data-ttu-id="09873-118">Restituisce il GUID del profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-118">Returns the GUID of the profile.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="09873-119">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="09873-119">**GetItem**</span></span>](-wia-iscanprofile-getitem.md)               | <span data-ttu-id="09873-120">Ottiene il GUID della categoria dell'elemento WIA 2,0 a cui è associato il profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-120">Gets the GUID of the category of the WIA 2.0 item that the profile is associated with.</span></span><br/>                                                   |
| [<span data-ttu-id="09873-121">**GetName**</span><span class="sxs-lookup"><span data-stu-id="09873-121">**GetName**</span></span>](-wia-iscanprofile-getname.md)               | <span data-ttu-id="09873-122">Ottiene il nome descrittivo del profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-122">Gets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="09873-123">**GetNumPropIDS**</span><span class="sxs-lookup"><span data-stu-id="09873-123">**GetNumPropIDS**</span></span>](-wia-iscanprofile-getnumpropids.md)   | <span data-ttu-id="09873-124">Ottiene il numero di ID di proprietà in un profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-124">Gets the number of property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="09873-125">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="09873-125">**GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)       | <span data-ttu-id="09873-126">Ottiene il valore delle proprietà figlio specificate nell' `<Properties>` elemento di un profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="09873-126">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="09873-127">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="09873-127">**IsDefault**</span></span>](-wia-iscanprofile-isdefault.md)           | <span data-ttu-id="09873-128">Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) associato.</span><span class="sxs-lookup"><span data-stu-id="09873-128">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span><br/> |
| [<span data-ttu-id="09873-129">**RemoveProperty**</span><span class="sxs-lookup"><span data-stu-id="09873-129">**RemoveProperty**</span></span>](-wia-iscanprofile-removeproperty.md) | <span data-ttu-id="09873-130">Rimuove un elenco specificato di proprietà figlio nell' `<Properties>` elemento di un profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="09873-130">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="09873-131">**Salva**</span><span class="sxs-lookup"><span data-stu-id="09873-131">**Save**</span></span>](-wia-iscanprofile-save.md)                     | <span data-ttu-id="09873-132">Salva le modifiche apportate a un profilo su disco.</span><span class="sxs-lookup"><span data-stu-id="09873-132">Saves changes to a profile to disk.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="09873-133">**SetItem**</span><span class="sxs-lookup"><span data-stu-id="09873-133">**SetItem**</span></span>](-wia-iscanprofile-setitem.md)               | <span data-ttu-id="09873-134">Imposta il GUID della categoria dell'elemento WIA 2,0 a cui è associato il profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-134">Sets the GUID of the category of WIA 2.0 item that the profile is associated with.</span></span><br/>                                                       |
| [<span data-ttu-id="09873-135">**SetName**</span><span class="sxs-lookup"><span data-stu-id="09873-135">**SetName**</span></span>](-wia-iscanprofile-setname.md)               | <span data-ttu-id="09873-136">Imposta il nome descrittivo del profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-136">Sets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="09873-137">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="09873-137">**SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)       | <span data-ttu-id="09873-138">Imposta il valore delle proprietà figlio specificate nell' `<Properties>` elemento di un profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="09873-138">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="09873-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="09873-139">Remarks</span></span>

<span data-ttu-id="09873-140">Qualsiasi dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) può avere un profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="09873-140">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="09873-141">Tuttavia, gli elementi di **IWiaItem2** di tipo WIA \_ Category \_ finished \_ file e WIA \_ Category \_ root non possono avere profili.</span><span class="sxs-lookup"><span data-stu-id="09873-141">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="09873-142">Se un profilo di analisi viene salvato utilizzando il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , viene archiviato come file XML in% UserProfile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="09873-142">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="09873-143">Per creare un'istanza di un oggetto **IScanProfile** , usare il metodo [**IScanProfileMgr:: CreateProfile**](-wia-iscanprofilemgr-createprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="09873-143">To create an instance of an **IScanProfile** object, use the [**IScanProfileMgr::CreateProfile**](-wia-iscanprofilemgr-createprofile.md) method.</span></span> <span data-ttu-id="09873-144">Per ottenere un riferimento a un profilo di analisi che è già stato salvato su disco, usare il metodo [**IScanProfileMgr:: OpenProfile**](-wia-iscanprofilemgr-openprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="09873-144">To get a reference to a scan profile that has already been saved to disk, use the [**IScanProfileMgr::OpenProfile**](-wia-iscanprofilemgr-openprofile.md) method.</span></span>

<span data-ttu-id="09873-145">Tutti i profili di analisi hanno gli elementi seguenti: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , e `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="09873-145">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="09873-146">Il profilo predefinito di un dispositivo contiene anche un `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="09873-146">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="09873-147">Gli `<ProfileGUID>` `<DeviceID>` elementi e non possono essere modificati dopo la creazione del profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-147">The `<ProfileGUID>` and `<DeviceID>` elements cannot be changed after the profile is created.</span></span> <span data-ttu-id="09873-148">I valori dell' `<ProfileName>` elemento e dell' `<WiaItem>` elemento possono essere modificati dopo la creazione del profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-148">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed after the profile is created.</span></span> <span data-ttu-id="09873-149">L' `<Default>` elemento può essere aggiunto o eliminato.</span><span class="sxs-lookup"><span data-stu-id="09873-149">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="09873-150">Questa operazione può essere eseguita a livello con i metodi [**IScanProfile:: Sename**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr:: sedefault**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="09873-150">This can be done programatically with the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="09873-151">Queste proprietà possono anche essere modificate dagli utenti tramite il metodo [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="09873-151">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="09873-152">L' `<Properties>` elemento contiene `<Property>` elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="09873-152">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="09873-153">Usare questi elementi per aggiungere qualsiasi proprietà dell'elemento o del dispositivo WIA 2,0 al profilo.</span><span class="sxs-lookup"><span data-stu-id="09873-153">Use these to add any WIA 2.0 item or device property to the profile.</span></span> <span data-ttu-id="09873-154">È anche possibile sviluppare una propria immagine acquisizione `<Property>` Children.</span><span class="sxs-lookup"><span data-stu-id="09873-154">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="09873-155">In questo modo lo schema del profilo di analisi diventa estendibile.</span><span class="sxs-lookup"><span data-stu-id="09873-155">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="09873-156">Per ulteriori informazioni sull'estensione dello schema, vedere [definizione di proprietà personalizzate](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="09873-156">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="09873-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09873-157">Requirements</span></span>



| <span data-ttu-id="09873-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="09873-158">Requirement</span></span> | <span data-ttu-id="09873-159">Valore</span><span class="sxs-lookup"><span data-stu-id="09873-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="09873-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09873-160">Minimum supported client</span></span><br/> | <span data-ttu-id="09873-161">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09873-161">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="09873-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09873-162">Minimum supported server</span></span><br/> | <span data-ttu-id="09873-163">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09873-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09873-164">IDL</span><span class="sxs-lookup"><span data-stu-id="09873-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09873-165"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="09873-165"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09873-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09873-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09873-167">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="09873-167">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="09873-168">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="09873-168">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
