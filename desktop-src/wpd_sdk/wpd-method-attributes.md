---
description: 'Per Windows 7, i dispositivi portatili Windows supportano gli attributi seguenti per i metodi di un servizio del dispositivo. Questi attributi vengono restituiti dal metodo IPortableDeviceServiceCapabilities:: GetMethodAttributes.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Attributi di metodo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326955"
---
# <a name="method-attributes"></a>Attributi del metodo

Per Windows 7, i dispositivi portatili Windows supportano gli attributi seguenti per i metodi di un servizio del dispositivo. Questi attributi vengono restituiti dal metodo [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .




| Attributo                                      | VarType         | Descrizione                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ accesso all'attributo del metodo WPD \_**             | **\_CLSID VT**   | Accesso al metodo obbligatorio.                                                                                               |
| **\_ \_ \_ formato associato all'attributo del metodo WPD \_** | **\_CLSID VT**   | Formato associato al metodo o **GUID \_ null** se non è associato alcun formato.                                |
| **\_ \_ nome attributo metodo \_ WPD**               | **\_LPWSTR VT**  | Stringa che specifica il nome descrittivo per lo script del metodo. I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '. |
| **\_parametri dell' \_ attributo del metodo WPD \_**         | **VT \_ sconosciuto** | Interfaccia [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che contiene i parametri del metodo.    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 




