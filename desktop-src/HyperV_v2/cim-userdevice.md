---
description: Rappresenta un dispositivo logico che consente a un utente di immettere, visualizzare o ascoltare i dati nel computer.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: Classe CIM_UserDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880754"
---
# <a name="cim_userdevice-class-hyper-v-management"></a>Classe CIM_UserDevice (gestione Hyper-V)

Rappresenta un dispositivo logico che consente a un utente di immettere, visualizzare o ascoltare i dati nel computer.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a>Members

La classe **CIM \_ UserDevice** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ UserDevice** dispone di queste proprietà.

<dl> <dt>

**IsLocked**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se il dispositivo è bloccato, impedendo l'input o l'output dell'utente; in caso contrario, **false**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




