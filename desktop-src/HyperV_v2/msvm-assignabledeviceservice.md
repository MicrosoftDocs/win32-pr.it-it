---
description: Gestisce i dispositivi assegnabili in un sistema di computer host.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Msvm_AssignableDeviceService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55ed0dc2cfdaa3f351537e18994a0b45c8490097f93c2cfaddbdf575d07e03c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790301"
---
# <a name="msvm_assignabledeviceservice-class"></a>Classe Msvm \_ AssignableDeviceService

Gestisce i dispositivi assegnabili in un sistema di computer host.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a>Members

La **classe Msvm \_ AssignableDeviceService** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe Msvm \_ AssignableDeviceService** include questi metodi.



| Metodo                                                                                    | Descrizione                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**DismountAssignableDevice**](msvm-assignabledeviceservice-dismountassignabledevice.md) | Smonta il dispositivo PCI specificato in modo che possa essere assegnato.<br/>                      |
| [**MountAssignableDevice**](msvm-assignabledeviceservice-mountassignabledevice.md)       | Monta il dispositivo PCI specificato in modo che possa essere usato dal sistema del computer host.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




