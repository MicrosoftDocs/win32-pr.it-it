---
description: Rappresenta lo stato configurato di un dispositivo di partizione GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Msvm_GpuPartitionSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 39fe0f5a794875c25cf844c39df2217fae04d1b791a5a5174358fa0ea70150ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014529"
---
# <a name="msvm_gpupartitionsettingdata-class"></a>Classe Msvm \_ GpuPartitionSettingData

Rappresenta lo stato configurato di un dispositivo di partizione GPU.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ GpuPartitionSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ GpuPartitionSettingData** ha queste proprietà.

<dl> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità massima di motori di calcolo che verranno visualizzati nella partizione GPU.

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità massima di motori di decodifica che verranno visualizzati nella partizione GPU.

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità massima di motori di codifica che verranno visualizzati nella partizione GPU.

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità massima di VRAM che verrà visualizzata nella partizione GPU.

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità minumum di motori di calcolo che verranno visualizzati nella partizione GPU.

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità minima di motori di decodifica che verranno visualizzati nella partizione GPU.

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità minima di motori di codifica che verranno visualizzati nella partizione GPU.

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità minima di VRAM che verrà visualizzata nella partizione GPU.

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità ottimale di motori di calcolo che verranno visualizzati nella partizione GPU.

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità ottimale di motori di decodifica che verranno visualizzati nella partizione GPU.

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità ottimale di motori di codifica che verranno visualizzati nella partizione GPU.

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quantità ottimale di VRAM che verrà visualizzata nella partizione GPU.

</dd> </dl>

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

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




