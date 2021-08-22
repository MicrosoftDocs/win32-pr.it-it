---
description: Definisce un singolo metodo di callback.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interfaccia IConnectionRequestCallback (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 53e1549767c8577507b3126b3a293dfe4e523612809c144ff24c04dce4ab1ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697419"
---
# <a name="iconnectionrequestcallback-interface"></a>Interfaccia IConnectionRequestCallback

**L'interfaccia IConnectionRequestCallback** definisce un singolo metodo di callback. Un Windows di dispositivi portatili (WPD) implementa questa interfaccia COM (Optional Component Object Model) per ricevere notifiche sulle richieste completate e annullare le richieste in sospeso. Le richieste vengono inviate usando i metodi [**IPortableDeviceConnector::Connessione**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) [**e IPortableDeviceConnector::D isconnect.**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect)

## <a name="members"></a>Membri

**L'interfaccia IConnectionRequestCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionRequestCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IConnectionRequestCallback** include questi metodi.



| Metodo                                                      | Descrizione                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**OnComplete**](iconnectionrequestcallback-oncomplete.md) | Notifica a un'applicazione che una richiesta pianificata in precedenza è stata completata.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



 

