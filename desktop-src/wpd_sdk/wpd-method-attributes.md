---
description: Per Windows 7, Windows dispositivi portatili supporta gli attributi seguenti per i metodi di un servizio dispositivo. Questi attributi vengono restituiti dal metodo IPortableDeviceServiceCapabilities::GetMethodAttributes.
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Attributi dei metodi (PortableDevice.h)
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
ms.openlocfilehash: ac41b4e9c7273c953a9689ce8c3d9f44d32925aded5b36291c45895b872fa9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026338"
---
# <a name="method-attributes"></a>Attributi del metodo

Per Windows 7, Windows dispositivi portatili supporta gli attributi seguenti per i metodi di un servizio dispositivo. Questi attributi vengono restituiti dal [**metodo IPortableDeviceServiceCapabilities::GetMethodAttributes.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes)




| Attributo                                      | VarType         | Descrizione                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **ACCESSO AGLI ATTRIBUTI DEL METODO WPD \_ \_ \_**             | **VT \_ CLSID**   | Accesso al metodo richiesto.                                                                                               |
| **FORMATO ASSOCIATO \_ \_ ALL'ATTRIBUTO DEL \_ METODO \_ WPD** | **VT \_ CLSID**   | Formato associato al metodo o **GUID \_ NULL** se non è presente alcun formato associato.                                |
| **NOME DELL'ATTRIBUTO DEL METODO WPD \_ \_ \_**               | **VT \_ LPWSTR**  | Stringa che specifica il nome descrittivo per lo script del metodo. I caratteri validi sono alfanumerici \[ a-zA-Z0-9 \] e ' \_ '. |
| **PARAMETRI DEGLI ATTRIBUTI DEL METODO WPD \_ \_ \_**         | **VT \_ UNKNOWN** | Interfaccia [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che contiene i parametri del metodo.    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 




