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
# <a name="device-interface-guids"></a>GUID dell'interfaccia del dispositivo

L'interfaccia del dispositivo può essere descritta da un valore **GUID** . I dispositivi portatili Windows definiscono la seguente interfaccia del dispositivo.



| Costante                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD**</dt> </dl>                          | Identifica i dispositivi che vengono visualizzati in un'enumerazione WPD normale. Qualsiasi dispositivo che registra questo GUID dell'interfaccia verrà enumerato quando un'applicazione chiama il metodo [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ privato**</dt> </dl> | Identifica i dispositivi che non verranno visualizzati durante una normale enumerazione WPD. Qualsiasi dispositivo che registra questo GUID dell'interfaccia verrà enumerato solo quando un'applicazione chiama il metodo [**IPortableDeviceManager:: GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ servizio**</dt> </dl> | In Windows 7, le applicazioni possono enumerare tutti i servizi dispositivo WPD chiamando [**IPortableDeviceServiceManager:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) e utilizzando questa classe di interfaccia come GUID del tipo di servizio.<br/>                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

 




