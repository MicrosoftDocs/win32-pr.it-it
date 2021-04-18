---
description: Rappresenta le impostazioni di un sistema virtuale da importare. Utilizzato dal metodo smontaggio della \_ classe MSVM AssignableDeviceService.
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Classe Msvm_AssignableDeviceDismountSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314344"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a>\_Classe MSVM AssignableDeviceDismountSettingData

Rappresenta le impostazioni di un sistema virtuale da importare. Utilizzato dal metodo [**smontaggio**](msvm-assignabledeviceservice-dismountassignabledevice.md) della classe [**MSVM \_ AssignableDeviceService**](msvm-assignabledeviceservice.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a>Members

La **classe \_ AssignableDeviceDismountSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ AssignableDeviceDismountSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**DeviceInstancePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

ID istanza del dispositivo PNP.

</dd> <dt>

**DeviceLocationPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Percorso del dispositivo PNP.

</dd> <dt>

**RequireAcsSupport**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il supporto ACS necessario deve essere preposto prima di consentire lo smontaggio.

</dd> <dt>

**RequireDeviceMitigations**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se devono essere applicate le attenuazioni dei dispositivi prima di consentire lo smontaggio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




