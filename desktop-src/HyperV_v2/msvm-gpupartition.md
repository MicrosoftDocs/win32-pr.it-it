---
description: Rappresenta lo stato della partizione GPU.
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Classe Msvm_GpuPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307913"
---
# <a name="msvm_gpupartition-class"></a>\_Classe MSVM GpuPartition

Rappresenta lo stato della partizione GPU.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a>Members

La **classe \_ GpuPartition di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ GpuPartition di MSVM** dispone di queste proprietà.

<dl> <dt>

**DeviceInstancePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che contiene il percorso dell'istanza del dispositivo che identifica il dispositivo di partizione GPU.

</dd> <dt>

**PartitionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID partizione del dispositivo di partizione GPU.

</dd> <dt>

**PartitionVfLuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzione virtuale LUID, che rappresenta una partizione GPU.

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

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




