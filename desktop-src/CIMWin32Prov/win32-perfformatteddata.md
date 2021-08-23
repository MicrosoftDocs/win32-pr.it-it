---
description: Classe di base astratta per le classi di dati calcolate preinstallate.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Win32_PerfFormattedData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 55a765102d5fcc40caff41a7fa68184afea114838152dd84157d506a62c15da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020139"
---
# <a name="win32_perfformatteddata-class"></a>Classe \_ PerfFormattedData Win32

Classe di base astratta per le classi di dati calcolate preinstallate. Un esempio di tale classe è [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md). Queste classi contengono valori calcolati forniti dal servizio prestazioni formattate a [prestazioni elevate provider di dati](../wmisdk/formatted-performance-data-provider.md).

La sintassi seguente è semplificata dal codice MOF e mostra tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
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

La **classe \_ PerfFormattedData Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ PerfFormattedData Win32** ha queste proprietà.

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

Questa proprietà viene ereditata da [**Win32 \_ Perf.**](win32-perf.md)

</dd> <dt>

**Frequency \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in tick al secondo della **proprietà Frequency \_ PerfTime.** È possibile ottenere un valore chiamando la Windows [**queryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

Questa proprietà viene ereditata da [**Win32 \_ Perf.**](win32-perf.md)

</dd> <dt>

**Frequenza \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in tick al secondo della **proprietà \_ Timestamp Sys100NS** (10000000).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

Questa proprietà viene ereditata da [**Win32 \_ Perf.**](win32-perf.md)

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

Questa proprietà viene ereditata da [**Win32 \_ Perf.**](win32-perf.md)

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp del contatore prestazioni elevate. È possibile ottenere un valore chiamando la Windows [**queryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

Questa proprietà viene ereditata da [**Win32 \_ Perf.**](win32-perf.md)

</dd> <dt>

**Timestamp \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di timestamp in unità di 100 nanosecondi.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

Questa proprietà viene ereditata da [**Win32 \_ Perf.**](win32-perf.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Win32 PerfFormattedData** è derivata da [**Win32 \_ Perf,**](win32-perf.md)derivato da [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md) La classe si trova nello spazio dei **\\ nomi radice cimv2.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                             |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Perf**](win32-perf.md)
</dt> <dt>

[Classi dei contatori delle prestazioni](performance-counter-classes.md)
</dt> <dt>

[Accesso alle classi di prestazioni preinstallate WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Attività WMI: Monitoraggio delle prestazioni](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Accesso ai dati sulle prestazioni nello script](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
