---
description: Per Windows 7, Windows dispositivi portatili supporta gli attributi seguenti per gli eventi di un servizio dispositivo. Questi attributi vengono restituiti dal metodo IPortableDeviceServiceCapabilities::GetEventAttributes.
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Attributi dell'evento (PortableDevice.h)
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
ms.openlocfilehash: 9ee6fe335d5e3906a923dfe5c470142cdf36fb1e521c3498963e478369a9b251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193292"
---
# <a name="event-attributes-portabledeviceh"></a>Attributi dell'evento (PortableDevice.h)

Per Windows 7, Windows dispositivi portatili supporta gli attributi seguenti per gli eventi di un servizio dispositivo. Questi attributi vengono restituiti dal [**metodo IPortableDeviceServiceCapabilities::GetEventAttributes.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes)




| Attributo                             | VarType         | Descrizione                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **NOME \_ DELL'ATTRIBUTO \_ DELL'EVENTO \_ WPD**       | **VT \_ LPWSTR**  | Stringa che specifica il nome descrittivo dell'evento. I caratteri validi sono alfanumerici \[ a-zA-Z0-9 \] e ' \_ '. |
| **OPZIONI DEGLI ATTRIBUTI DEGLI EVENTI WPD \_ \_ \_**    | **VT \_ UNKNOWN** | Oggetto [**IPortableDeviceValues**](iportabledevicevalues.md) che contiene le opzioni dell'evento.                               |
| **PARAMETRI \_ DELL'ATTRIBUTO \_ DELL'EVENTO WPD \_** | **VT \_ UNKNOWN** | Oggetto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che contiene i parametri dell'evento.              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 




