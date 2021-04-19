---
description: 'Per Windows 7, i dispositivi portatili Windows supportano gli attributi seguenti per gli eventi di un servizio del dispositivo. Questi attributi vengono restituiti dal metodo IPortableDeviceServiceCapabilities:: GetEventAttributes.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Attributi evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324204"
---
# <a name="event-attributes-portabledeviceh"></a>Attributi evento (PortableDevice. h)

Per Windows 7, i dispositivi portatili Windows supportano gli attributi seguenti per gli eventi di un servizio del dispositivo. Questi attributi vengono restituiti dal metodo [**IPortableDeviceServiceCapabilities:: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .




| Attributo                             | VarType         | Descrizione                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **\_nome dell' \_ attributo dell'evento WPD \_**       | **\_LPWSTR VT**  | Stringa che specifica il nome descrittivo per lo script dell'evento. I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '. |
| **\_Opzioni degli \_ attributi \_ evento WPD**    | **VT \_ sconosciuto** | Oggetto [**IPortableDeviceValues**](iportabledevicevalues.md) che contiene le opzioni dell'evento.                               |
| **\_parametri dell' \_ attributo dell'evento WPD \_** | **VT \_ sconosciuto** | Oggetto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che contiene i parametri dell'evento.              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 




