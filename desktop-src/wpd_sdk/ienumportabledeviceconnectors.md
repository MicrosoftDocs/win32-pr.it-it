---
description: Supporta l'enumerazione delle interfacce IPortableDeviceConnector, che rappresentano i dispositivi MTP/Bluetooth associati al PC.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interfaccia IEnumPortableDeviceConnectors (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231575"
---
# <a name="ienumportabledeviceconnectors-interface"></a>Interfaccia IEnumPortableDeviceConnectors

L'interfaccia **IEnumPortableDeviceConnectors** supporta l'enumerazione delle interfacce [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , che rappresentano i dispositivi MTP/Bluetooth associati al PC. Si noti che questa operazione recupererà tutti i dispositivi precedentemente associati, inclusi i dispositivi abbinati ma disconnessi. Per determinare se un dispositivo è ancora connesso, eseguire una query sulla proprietà **DEVPKEY \_ MTPBTH \_ disconnected** per tale dispositivo.

## <a name="members"></a>Membri

L'interfaccia **IEnumPortableDeviceConnectors** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumPortableDeviceConnectors** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumPortableDeviceConnectors** dispone di questi metodi.



| Metodo                                               | Descrizione                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](ienumportabledeviceconnectors-clone.md) | Crea una copia dell'interfaccia **IEnumPortableDeviceConnectors** corrente.<br/>                                                       |
| [**Avanti**](ienumportabledeviceconnectors-next.md)   | Recupera uno o più oggetti [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) successivi nella sequenza di enumerazione.<br/> |
| [**Reset**](ienumportabledeviceconnectors-reset.md) | Riporta all'inizio la sequenza di enumerazione.<br/>                                                                                |
| [**Ignora**](ienumportabledeviceconnectors-skip.md)   | Ignora il numero specificato di dispositivi nella sequenza di enumerazione.<br/>                                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

