---
description: L'interfaccia del dispositivo può essere descritta da un valore GUID. I dispositivi portatili Windows definiscono la seguente interfaccia del dispositivo.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: GUID dell'interfaccia del dispositivo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328978"
---
# <a name="device-interface-guids"></a><span data-ttu-id="065ff-104">GUID dell'interfaccia del dispositivo</span><span class="sxs-lookup"><span data-stu-id="065ff-104">Device Interface GUIDs</span></span>

<span data-ttu-id="065ff-105">L'interfaccia del dispositivo può essere descritta da un valore **GUID** .</span><span class="sxs-lookup"><span data-stu-id="065ff-105">The device interface can be described by a **GUID** value.</span></span> <span data-ttu-id="065ff-106">I dispositivi portatili Windows definiscono la seguente interfaccia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="065ff-106">Windows Portable Devices defines the following device interface.</span></span>



| <span data-ttu-id="065ff-107">Costante</span><span class="sxs-lookup"><span data-stu-id="065ff-107">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="065ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="065ff-108">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <span data-ttu-id="065ff-109"><dt>**GUID \_ DEVINTERFACE \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="065ff-109"><dt>**GUID\_DEVINTERFACE\_WPD**</dt></span></span> </dl>                          | <span data-ttu-id="065ff-110">Identifica i dispositivi che vengono visualizzati in un'enumerazione WPD normale.</span><span class="sxs-lookup"><span data-stu-id="065ff-110">Identifies devices that appear in a normal WPD enumeration.</span></span> <span data-ttu-id="065ff-111">Qualsiasi dispositivo che registra questo GUID dell'interfaccia verrà enumerato quando un'applicazione chiama il metodo [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .</span><span class="sxs-lookup"><span data-stu-id="065ff-111">Any device that registers this interface GUID will be enumerated when an application calls the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.</span></span><br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <span data-ttu-id="065ff-112"><dt>**GUID \_ DEVINTERFACE \_ WPD \_ privato**</dt></span><span class="sxs-lookup"><span data-stu-id="065ff-112"><dt>**GUID\_DEVINTERFACE\_WPD\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="065ff-113">Identifica i dispositivi che non verranno visualizzati durante una normale enumerazione WPD.</span><span class="sxs-lookup"><span data-stu-id="065ff-113">Identifies devices that will not appear during a normal WPD enumeration.</span></span> <span data-ttu-id="065ff-114">Qualsiasi dispositivo che registra questo GUID dell'interfaccia verrà enumerato solo quando un'applicazione chiama il metodo [**IPortableDeviceManager:: GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .</span><span class="sxs-lookup"><span data-stu-id="065ff-114">Any device that registers this interface GUID will be enumerated only when an application calls the [**IPortableDeviceManager::GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) method.</span></span><br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <span data-ttu-id="065ff-115"><dt>**GUID \_ DEVINTERFACE \_ WPD \_ servizio**</dt></span><span class="sxs-lookup"><span data-stu-id="065ff-115"><dt>**GUID\_DEVINTERFACE\_WPD\_SERVICE**</dt></span></span> </dl> | <span data-ttu-id="065ff-116">In Windows 7, le applicazioni possono enumerare tutti i servizi dispositivo WPD chiamando [**IPortableDeviceServiceManager:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) e utilizzando questa classe di interfaccia come GUID del tipo di servizio.</span><span class="sxs-lookup"><span data-stu-id="065ff-116">In Windows 7, applications can enumerate all WPD device services by calling [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) and using this interface class as the service-type GUID.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="065ff-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="065ff-117">Requirements</span></span>



| <span data-ttu-id="065ff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="065ff-118">Requirement</span></span> | <span data-ttu-id="065ff-119">Valore</span><span class="sxs-lookup"><span data-stu-id="065ff-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="065ff-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="065ff-120">Header</span></span><br/> | <dl> <span data-ttu-id="065ff-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="065ff-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="065ff-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="065ff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="065ff-123">Guida di riferimento alla programmazione</span><span class="sxs-lookup"><span data-stu-id="065ff-123">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




