---
description: Classe di base astratta per tutte le classi del contatore delle prestazioni raw concrete.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Classe Win32_PerfRawData
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
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524273"
---
# <a name="win32_perfrawdata-class"></a>Win32 \_ PerfRawData (classe)

Classe di base astratta per tutte le classi del contatore delle prestazioni raw concrete.

Per essere visualizzati in monitoraggio di sistema, le classi del contatore delle prestazioni devono essere aggiunte allo \\ spazio dei nomi CIMV2 radice e derivate da **Win32 \_ PerfRawData**. I dati in queste classi sono forniti dal [provider del contatore delle prestazioni](../wmisdk/performance-counter-provider.md)a prestazioni elevate.

Le proprietà seguenti vengono ereditate quando una classe viene derivata da **Win32 \_ PerfRawData**:

-   **Timestamp \_ PerfTime**
-   **Timestamp \_ Sys100NS**
-   **Timestamp ( \_ oggetto)**
-   **Frequenza \_ PerfTime**
-   **Frequenza \_ Sys100NS**
-   **Frequency ( \_ oggetto)**

In ogni caso, le proprietà devono essere compilate dal provider o la classe non può essere visualizzata in Monitor di sistema. Queste proprietà vengono utilizzate per calcolare le formule del tipo di contatore in base ai consumer dei dati sulle prestazioni.

La sintassi seguente è semplificata dal codice MOF e Mostra tutte le proprietà ereditate.

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

La classe **Win32 \_ PerfRawData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PerfRawData** dispone di queste proprietà.

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

La classe **Win32 \_ PerfRawData** è derivata da [**\_ Perf Win32**](win32-perf.md), derivata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

Tutte le classi derivate da [**\_ Perf Win32**](win32-perf.md) sono progettate per essere utilizzate con un oggetto di [*aggiornamento*](../wmisdk/gloss-r.md) . Per ulteriori informazioni su come creare e utilizzare un oggetto di aggiornamento nel linguaggio di programmazione C++, vedere [accesso ai dati sulle prestazioni in c++](../wmisdk/accessing-performance-data-in-c--.md). Per ulteriori informazioni su come creare e utilizzare un oggetto di aggiornamento in un linguaggio di programmazione script, vedere [aggiornamento di dati WMI negli script](../wmisdk/refreshing-wmi-data-in-scripts.md).

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

 

 
