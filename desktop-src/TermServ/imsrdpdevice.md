---
title: Interfaccia IMsRdpDevice
description: Contiene informazioni su un oggetto dispositivo.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDevice Servizi Desktop remoto
- Interfaccia IMsRdpDevice Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301214"
---
# <a name="imsrdpdevice-interface"></a><span data-ttu-id="bbd80-105">Interfaccia IMsRdpDevice</span><span class="sxs-lookup"><span data-stu-id="bbd80-105">IMsRdpDevice interface</span></span>

<span data-ttu-id="bbd80-106">Contiene informazioni su un oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbd80-106">Contains information about a device object.</span></span>

## <a name="members"></a><span data-ttu-id="bbd80-107">Membri</span><span class="sxs-lookup"><span data-stu-id="bbd80-107">Members</span></span>

<span data-ttu-id="bbd80-108">L'interfaccia **IMsRdpDevice** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bbd80-108">The **IMsRdpDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bbd80-109">**IMsRdpDevice** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bbd80-109">**IMsRdpDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="bbd80-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbd80-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbd80-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbd80-111">Properties</span></span>

<span data-ttu-id="bbd80-112">L'interfaccia **IMsRdpDevice** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bbd80-112">The **IMsRdpDevice** interface has these properties.</span></span>



| <span data-ttu-id="bbd80-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbd80-113">Property</span></span>                                                               | <span data-ttu-id="bbd80-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="bbd80-114">Access type</span></span>           | <span data-ttu-id="bbd80-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbd80-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbd80-116">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="bbd80-116">**DeviceDescription**</span></span>](imsrdpdevice-devicedescription.md)<br/> | <span data-ttu-id="bbd80-117">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="bbd80-117">Read-only</span></span><br/>  | <span data-ttu-id="bbd80-118">Recupera la descrizione del dispositivo da visualizzare all'utente se il nome visualizzato non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bbd80-118">Retrieves the device description to be displayed to the user if the display name is not available.</span></span><br/> |
| [<span data-ttu-id="bbd80-119">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="bbd80-119">**DeviceInstanceId**</span></span>](imsrdpdevice-deviceinstanceid.md)<br/>   | <span data-ttu-id="bbd80-120">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="bbd80-120">Read-only</span></span><br/>  | <span data-ttu-id="bbd80-121">Recupera l'identificatore dell'istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbd80-121">Retrieves the device instance identifier of the device.</span></span><br/>                                            |
| [<span data-ttu-id="bbd80-122">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="bbd80-122">**FriendlyName**</span></span>](imsrdpdevice-friendlyname.md)<br/>           | <span data-ttu-id="bbd80-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="bbd80-123">Read-only</span></span><br/>  | <span data-ttu-id="bbd80-124">Recupera il nome visualizzato per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbd80-124">Retrieves the display name for the device.</span></span><br/>                                                         |
| [<span data-ttu-id="bbd80-125">**RedirectionState**</span><span class="sxs-lookup"><span data-stu-id="bbd80-125">**RedirectionState**</span></span>](imsrdpdevice-redirectionstate.md)<br/>   | <span data-ttu-id="bbd80-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="bbd80-126">Read/write</span></span><br/> | <span data-ttu-id="bbd80-127">Indica lo stato del reindirizzamento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbd80-127">Indicates the redirection state of the device.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="bbd80-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbd80-128">Requirements</span></span>



| <span data-ttu-id="bbd80-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbd80-129">Requirement</span></span> | <span data-ttu-id="bbd80-130">Valore</span><span class="sxs-lookup"><span data-stu-id="bbd80-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd80-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbd80-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd80-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbd80-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bbd80-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbd80-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd80-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbd80-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bbd80-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bbd80-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="bbd80-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbd80-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbd80-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bbd80-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbd80-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbd80-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbd80-139">IID</span><span class="sxs-lookup"><span data-stu-id="bbd80-139">IID</span></span><br/>                      | <span data-ttu-id="bbd80-140">IID \_ IMsRdpDevice è definito come 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="bbd80-140">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="bbd80-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbd80-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd80-142">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="bbd80-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="bbd80-143">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="bbd80-143">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

