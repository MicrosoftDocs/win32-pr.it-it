---
description: Classe di base astratta per tutte le classi di contatori delle prestazioni non elaborati concrete.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Win32_PerfRawData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: f6500706b7e2298ad98aa894e33436b0306e406e003562fcb6533265abd0b2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020129"
---
# <a name="win32_perfrawdata-class"></a>Classe \_ Win32 PerfRawData

Classe di base astratta per tutte le classi di contatori delle prestazioni non elaborati concrete.

Per essere visualizzate in Monitoraggio di sistema, le classi dei contatori delle prestazioni devono essere aggiunte allo spazio dei nomi cimv2 radice e derivate \\ da **Win32 \_ PerfRawData**. I dati in queste classi vengono forniti dal provider di contatori delle prestazioni [ad alte prestazioni.](../wmisdk/performance-counter-provider.md)

Le proprietà seguenti vengono ereditate quando una classe viene derivata da **Win32 \_ PerfRawData:**

-   **Timestamp \_ PerfTime**
-   **Timestamp \_ Sys100NS**
-   **Oggetto \_ Timestamp**
-   **Frequenza \_ perfTime**
-   **Frequenza \_ Sys100NS**
-   **Oggetto \_ Frequency**

In ogni caso, le proprietà devono essere compilate dal provider o la classe non può essere visualizzata in Monitoraggio di sistema. Queste proprietà vengono usate per calcolare le formule del tipo di contatore da parte dei consumer dei dati sulle prestazioni.

La sintassi seguente è semplificata dal codice MOF e mostra tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

La **classe \_ Win32 PerfRawData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Win32 PerfRawData** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
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

Tipo di dati: **stringa**
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

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Frequenza \_ perfTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in tick al secondo della **proprietà Frequency \_ PerfTime.** È possibile ottenere un valore chiamando la funzione Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Frequenza \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza in tick al secondo della **proprietà \_ Timestamp Sys100NS** (100000000).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Etichetta con cui è nota la statistica o la metrica. Quando è sottoclassata, questa proprietà può essere sottoposta a override per essere una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md)

</dd> <dt>

**Oggetto \_ Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp definito dall'oggetto. Il provider definisce la proprietà .

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp del contatore ad alte prestazioni. È possibile ottenere un valore chiamando la funzione Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Timestamp \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore del timestamp in unità da 100 nanosecondi.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**Win32 \_ Perf**](win32-perf.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe Win32 \_ PerfRawData** deriva da [**Win32 \_ Perf**](win32-perf.md), derivata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

Tutte le classi derivate [**da Win32 \_ Perf**](win32-perf.md) sono progettate per essere usate con un [*oggetto di aggiornamento.*](../wmisdk/gloss-r.md) Per altre informazioni su come creare e usare un oggetto di aggiornamento nel linguaggio di programmazione C++, vedere Accesso ai dati sulle [prestazioni in C++.](../wmisdk/accessing-performance-data-in-c--.md) Per altre informazioni su come creare e usare un oggetto di aggiornamento in un linguaggio di programmazione script, vedere [Aggiornamento di dati WMI negli script](../wmisdk/refreshing-wmi-data-in-scripts.md).

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

 

 
