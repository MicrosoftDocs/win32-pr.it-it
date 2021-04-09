---
description: Definisce un singolo metodo di callback.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interfaccia IConnectionRequestCallback (Devpkey. h)
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
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968600"
---
# <a name="iconnectionrequestcallback-interface"></a>Interfaccia IConnectionRequestCallback

L'interfaccia **IConnectionRequestCallback** definisce un solo metodo di callback. Un'applicazione Windows Portable Devices (WPD) implementa questa interfaccia facoltativa Component Object Model (COM) per ricevere notifiche sulle richieste completate e per annullare le richieste in sospeso. Le richieste vengono inviate usando i metodi [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D di connessione**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="members"></a>Membri

L'interfaccia **IConnectionRequestCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionRequestCallback** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IConnectionRequestCallback** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**OnComplete**](iconnectionrequestcallback-oncomplete.md) | Notifica a un'applicazione che una richiesta pianificata in precedenza è stata completata.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

