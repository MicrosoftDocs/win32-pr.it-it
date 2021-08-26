---
description: Classe di base per le classi dei contatori delle prestazioni Win32 \_ PerfRawData e Win32 \_ PerfFormattedData.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Win32_Perf classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 356fdba0e2ebb7fb202f4996daa6b1929cd61fc67b028f67e8b041748306c0ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972241"
---
# <a name="win32_perf-class"></a>Classe \_ Win32 Perf

Classe di base per le classi dei contatori delle [**prestazioni Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData.**](win32-perfformatteddata.md)

**Win32 \_ Perf** definisce le proprietà obbligatorie di timestamp e frequenza usate negli algoritmi [**CounterType**](../wmisdk/countertype-qualifier.md) per le classi dei contatori delle prestazioni.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 Perf** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Win32 Perf** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale per la statistica o la metrica.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale della statistica o della metrica.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md)

</dd> <dt>

**Oggetto \_ Frequency**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in tick al secondo della **proprietà Timestamp \_ Object.** In caso di sottoclasse, il provider definisce questa proprietà.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Frequency \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in tick al secondo della **proprietà Frequency \_ PerfTime.** È possibile ottenere un valore chiamando la funzione Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Frequenza \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in tick al secondo della **proprietà \_ Timestamp Sys100NS** (10000000).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Etichetta con cui è nota la statistica o la metrica. Quando è sottoclassata, questa proprietà può essere sottoposta a override come proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md)

</dd> <dt>

**Oggetto \_ Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp definito dall'oggetto. Il provider definisce la proprietà .

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp del contatore prestazioni elevate. È possibile ottenere un valore chiamando la funzione Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Timestamp \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di timestamp in unità di 100 nanosecondi.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Win32 Perf** deriva da [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                             |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                     |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)
</dt> <dt>

[Classi dei contatori delle prestazioni](performance-counter-classes.md)
</dt> <dt>

[Accesso alle classi di prestazioni preinstallate WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Attività WMI: Monitoraggio delle prestazioni](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Accesso ai dati sulle prestazioni nello script](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
