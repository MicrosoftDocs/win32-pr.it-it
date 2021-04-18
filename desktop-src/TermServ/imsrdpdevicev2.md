---
title: Interfaccia IMsRdpDeviceV2
description: Contiene informazioni su un oggetto dispositivo. Si tratta di un miglioramento dell'interfaccia IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300988"
---
# <a name="imsrdpdevicev2-interface"></a><span data-ttu-id="f9e12-106">Interfaccia IMsRdpDeviceV2</span><span class="sxs-lookup"><span data-stu-id="f9e12-106">IMsRdpDeviceV2 interface</span></span>

<span data-ttu-id="f9e12-107">Contiene informazioni su un oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9e12-107">Contains information about a device object.</span></span> <span data-ttu-id="f9e12-108">Si tratta di un miglioramento dell'interfaccia [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="f9e12-108">This is an enhancement of the [**IMsRdpDevice**](imsrdpdevice.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="f9e12-109">Membri</span><span class="sxs-lookup"><span data-stu-id="f9e12-109">Members</span></span>

<span data-ttu-id="f9e12-110">L'interfaccia **IMsRdpDeviceV2** eredita da [**IMsRdpDevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f9e12-110">The **IMsRdpDeviceV2** interface inherits from [**IMsRdpDevice**](imsrdpdevice.md).</span></span> <span data-ttu-id="f9e12-111">**IMsRdpDeviceV2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f9e12-111">**IMsRdpDeviceV2** also has these types of members:</span></span>

-   [<span data-ttu-id="f9e12-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9e12-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9e12-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9e12-113">Properties</span></span>

<span data-ttu-id="f9e12-114">L'interfaccia **IMsRdpDeviceV2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f9e12-114">The **IMsRdpDeviceV2** interface has these properties.</span></span>



| <span data-ttu-id="f9e12-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9e12-115">Property</span></span>                                                                 | <span data-ttu-id="f9e12-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="f9e12-116">Access type</span></span>          | <span data-ttu-id="f9e12-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9e12-117">Description</span></span>                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9e12-118">**CmClassGuid**</span><span class="sxs-lookup"><span data-stu-id="f9e12-118">**CmClassGuid**</span></span>](imsrdpdevicev2-cmclassguid.md)<br/>             | <span data-ttu-id="f9e12-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e12-119">Read-only</span></span><br/> | <span data-ttu-id="f9e12-120">Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9e12-120">Contains the configuration manager setup class GUID for the device.</span></span><br/>                     |
| [<span data-ttu-id="f9e12-121">**CmDeviceInstance**</span><span class="sxs-lookup"><span data-stu-id="f9e12-121">**CmDeviceInstance**</span></span>](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | <span data-ttu-id="f9e12-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e12-122">Read-only</span></span><br/> | <span data-ttu-id="f9e12-123">Contiene l'istanza del dispositivo di Configuration Manager del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9e12-123">Contains the configuration manager device instance of the device.</span></span><br/>                       |
| [<span data-ttu-id="f9e12-124">**DeviceText**</span><span class="sxs-lookup"><span data-stu-id="f9e12-124">**DeviceText**</span></span>](imsrdpdevicev2-devicetext.md)<br/>               | <span data-ttu-id="f9e12-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e12-125">Read-only</span></span><br/> | <span data-ttu-id="f9e12-126">Contiene il testo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9e12-126">Contains the device text.</span></span><br/>                                                               |
| [<span data-ttu-id="f9e12-127">**DriveLetterBitmap**</span><span class="sxs-lookup"><span data-stu-id="f9e12-127">**DriveLetterBitmap**</span></span>](imsrdpdevicev2-driveletterbitmap.md)<br/> | <span data-ttu-id="f9e12-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e12-128">Read-only</span></span><br/> | <span data-ttu-id="f9e12-129">Contiene un bit che rappresenta una mappa delle lettere di unità contenute all'interno del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9e12-129">Contains a bitfield that represents a map of drive letters contained within the device.</span></span><br/> |
| [<span data-ttu-id="f9e12-130">**IsCompositeDevice**</span><span class="sxs-lookup"><span data-stu-id="f9e12-130">**IsCompositeDevice**</span></span>](imsrdpdevicev2-iscompositedevice.md)<br/> | <span data-ttu-id="f9e12-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e12-131">Read-only</span></span><br/> | <span data-ttu-id="f9e12-132">Specifica se il dispositivo è un dispositivo composito.</span><span class="sxs-lookup"><span data-stu-id="f9e12-132">Specifies if the device is a composite device.</span></span><br/>                                          |
| [<span data-ttu-id="f9e12-133">**IsOptionalDevice**</span><span class="sxs-lookup"><span data-stu-id="f9e12-133">**IsOptionalDevice**</span></span>](imsrdpdevicev2-isoptionaldevice.md)<br/>   | <span data-ttu-id="f9e12-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e12-134">Read-only</span></span><br/> | <span data-ttu-id="f9e12-135">Specifica se il dispositivo è facoltativo per il reindirizzamento USB.</span><span class="sxs-lookup"><span data-stu-id="f9e12-135">Specifies if the device is optional for USB redirection.</span></span><br/>                                |
| [<span data-ttu-id="f9e12-136">**IsUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="f9e12-136">**IsUSBDevice**</span></span>](imsrdpdevicev2-isusbdevice.md)<br/>             | <span data-ttu-id="f9e12-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e12-137">Read-only</span></span><br/> | <span data-ttu-id="f9e12-138">Specifica se il dispositivo è per il reindirizzamento USB.</span><span class="sxs-lookup"><span data-stu-id="f9e12-138">Specifies if the device is for USB redirection.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="f9e12-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9e12-139">Requirements</span></span>



| <span data-ttu-id="f9e12-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9e12-140">Requirement</span></span> | <span data-ttu-id="f9e12-141">Valore</span><span class="sxs-lookup"><span data-stu-id="f9e12-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e12-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9e12-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e12-143">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="f9e12-143">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="f9e12-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9e12-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e12-145">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="f9e12-145">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="f9e12-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f9e12-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9e12-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9e12-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9e12-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f9e12-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9e12-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9e12-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9e12-150">IID</span><span class="sxs-lookup"><span data-stu-id="f9e12-150">IID</span></span><br/>                      | <span data-ttu-id="f9e12-151">IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="f9e12-151">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



 

 





