---
description: L'interfaccia del dispositivo può essere descritta da un valore GUID. Windows Dispositivi portatili definisce l'interfaccia del dispositivo seguente.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: GUID dell'interfaccia del dispositivo (PortableDevice.h)
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
ms.openlocfilehash: 6f4bd170aeae46f738f5ce4a5a98bc694583a19fe3e7fa6eccc21c86fdc871d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657921"
---
# <a name="device-interface-guids"></a>GUID dell'interfaccia del dispositivo

L'interfaccia del dispositivo può essere descritta da un **valore GUID.** Windows Dispositivi portatili definisce l'interfaccia del dispositivo seguente.



| Costante                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD**</dt> </dl>                          | Identifica i dispositivi visualizzati in una normale enumerazione WPD. Qualsiasi dispositivo che registra questo GUID di interfaccia verrà enumerato quando un'applicazione chiama il [**metodo IPortableDeviceManager::GetDevices.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ PRIVATE**</dt> </dl> | Identifica i dispositivi che non verranno visualizzati durante una normale enumerazione WPD. Qualsiasi dispositivo che registra questo GUID di interfaccia verrà enumerato solo quando un'applicazione chiama il [**metodo IPortableDeviceManager::GetPrivateDevices.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices)<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ SERVICE**</dt> </dl> | In Windows 7, le applicazioni possono enumerare tutti i servizi dei dispositivi WPD chiamando [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) e usando questa classe di interfaccia come GUID del tipo di servizio.<br/>                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

 




