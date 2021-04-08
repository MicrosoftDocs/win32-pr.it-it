---
description: Classe di base astratta per le classi di dati calcolate preinstallate.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Classe Win32_PerfFormattedData
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
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966290"
---
# <a name="win32_perfformatteddata-class"></a>Win32 \_ PerfFormattedData (classe)

Classe di base astratta per le classi di dati calcolate preinstallate. Un esempio di tale classe è [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](../wmisdk/retrieving-raw-and-formatted-performance-data.md). Queste classi contengono i valori calcolati forniti dalle [prestazioni provider di dati formattate](../wmisdk/formatted-performance-data-provider.md)ad alte prestazioni.

La sintassi seguente è semplificata dal codice MOF e Mostra tutte le proprietà ereditate.

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

La classe **Win32 \_ PerfFormattedData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PerfFormattedData** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale per la statistica o la metrica.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale della statistica o della metrica.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

</dd> <dt>

**Frequency ( \_ oggetto)**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in cicli al secondo della proprietà dell' **\_ oggetto timestamp** . Se sottoclassato, il provider definisce questa proprietà.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).

</dd> <dt>

**Frequenza \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in cicli al secondo della proprietà **Frequency \_ PerfTime** . È possibile ottenere un valore chiamando la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)di Windows.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).

</dd> <dt>

**Frequenza \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in cicli al secondo della proprietà **timestamp \_ Sys100NS** (10 milioni).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Etichetta con la quale è nota la statistica o la metrica. Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

</dd> <dt>

**Timestamp ( \_ oggetto)**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp definito dall'oggetto. Il provider definisce la proprietà.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp elevato del contatore delle prestazioni. È possibile ottenere un valore chiamando la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)di Windows.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).

</dd> <dt>

**Timestamp \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore timestamp in unità di 100 nanosecondi.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PerfFormattedData** è derivata da [**\_ Perf Win32**](win32-perf.md), derivata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md). La classe si trova nello spazio dei nomi **\\ CIMV2 radice** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                             |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Prestazioni Win32**](win32-perf.md)
</dt> <dt>

[Classi del contatore delle prestazioni](performance-counter-classes.md)
</dt> <dt>

[Accesso alle classi di prestazioni preinstallate WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Attività WMI: monitoraggio delle prestazioni](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Accesso ai dati sulle prestazioni nello script](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
