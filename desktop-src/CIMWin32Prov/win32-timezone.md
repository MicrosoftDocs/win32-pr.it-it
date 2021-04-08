---
description: Il \_ fuso orario Win32&\# 8194; Classe WMI rappresenta le informazioni sul fuso orario per un computer che esegue Windows, che include le modifiche necessarie per la transizione alla transizione dell'ora legale.
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Classe Win32_TimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877661"
---
# <a name="win32_timezone-class"></a>\_Classe TimeZone di Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) del **\_ fuso orario Win32** rappresenta le informazioni sul fuso orario per un computer che esegue Windows, che include le modifiche necessarie per la transizione alla transizione dell'ora legale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a>Members

La classe del **\_ fuso orario Win32** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe del **\_ fuso orario Win32** dispone di queste proprietà.

<dl> <dt>

**Bias**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| Debias [**\_ \_ Information fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")
</dt> </dl>

Distorsione corrente per la conversione dell'ora locale. La distorsione è la differenza tra l'ora UTC (Coordinated Universal Time) e l'ora locale. Tutte le traduzioni tra l'ora UTC e l'ora locale sono basate sulla formula seguente: UTC = tempo locale-bias. Questa proprietà è obbligatoria.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**DaylightBias**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")
</dt> </dl>

Valore di distorsione da utilizzare durante le conversioni dell'ora locale che si verificano durante l'ora legale. Questa proprietà viene ignorata se non viene fornito un valore per la proprietà **DaylightDay** . Il valore di questa proprietà viene aggiunto alla proprietà **Bias** per formare la distorsione utilizzata durante l'ora legale. Nella maggior parte dei fusi orari, il valore di questa proprietà è-60.

</dd> <dt>

**DaylightDay**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDay")
</dt> </dl>

**DaylightDayOfWeek** di **DaylightMonth** quando si verifica la transizione dall'ora solare all'ora legale in questo sistema operativo.

Esempio: se il giorno di transizione (**DaylightDayOfWeek**) si verifica a domenica, il valore "1" indica la prima domenica di **DaylightMonth**, "2" indica la seconda domenica e così via. Il valore "5" indica l'ultimo **DaylightDayOfWeek** del mese.

</dd> <dt>

**DaylightDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDayOfWeek")
</dt> </dl>

Giorno della settimana in cui si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domenica** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunedì** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martedì** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercoledì** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Giovedi** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Venerdì** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sabato** (6)


</dt> <dd></dd> </dl>

Esempio: 1

</dd> <dt>

**DaylightHour**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wHour")
</dt> </dl>

Ora del giorno in cui si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

Esempio: 2

</dd> <dt>

**DaylightMillisecond**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMilliseconds")
</dt> </dl>

Millisecondi di **DaylightSecond** quando si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

</dd> <dt>

**DaylightMinute**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMinute")
</dt> </dl>

Minuto del **DaylightHour** quando si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

Esempio: 59

</dd> <dt>

**DaylightMonth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMonth")
</dt> </dl>

Mese in cui si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Gennaio** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Febbraio** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Marzo** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Aprile** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Maggio** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Giugno** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Luglio** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Settembre** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Ottobre** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembre** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dicembre** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**DaylightName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")
</dt> </dl>

Fuso orario rappresentato quando è attiva l'ora legale.

Esempio: "EDT" (ora legale orientale)

</dd> <dt>

**DaylightSecond**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wSecond")
</dt> </dl>

Secondo **DaylightMinute** quando la transizione dall'ora solare all'ora legale si verifica in un sistema operativo.

Esempio: 59

</dd> <dt>

**DaylightYear**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")
</dt> </dl>

Anno in cui è attiva l'ora legale. Questa proprietà non è obbligatoria.

Esempio: 1997

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**StandardBias**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")
</dt> </dl>

Valore di distorsione da utilizzare quando l'ora legale non è attiva. Questa proprietà viene ignorata se non viene specificato un valore per **StandardDay** . Il valore di questa proprietà viene aggiunto alla proprietà **Bias** per formare la distorsione durante l'ora solare.

Esempio: 0

</dd> <dt>

**StandardDay**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDay")
</dt> </dl>

**StandardDayofWeek** di **StandardMonth** quando si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

Se il giorno di transizione (**StandardDayofWeek**) si verifica a domenica, il valore "1" indica la prima domenica del **StandardMonth**, "2" indica la seconda domenica e così via. Il valore "5" indica l'ultimo **StandardDayofWeek** del mese.

</dd> <dt>

**StandardDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")
</dt> </dl>

Giorno della settimana in cui si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domenica** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunedì** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martedì** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercoledì** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Giovedi** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Venerdì** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sabato** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardHour**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")
</dt> </dl>

Ora del giorno in cui si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

Esempio: 11

</dd> <dt>

**StandardMillisecond**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")
</dt> </dl>

Millisecondi di **StandardSecond** quando la transizione dall'ora legale all'ora solare si verifica in un sistema operativo.

</dd> <dt>

**StandardMinute**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")
</dt> </dl>

Minuto del **StandardDay** quando la transizione dall'ora legale all'ora solare si verifica in un sistema operativo.

Esempio: 59

</dd> <dt>

**StandardMonth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")
</dt> </dl>

Mese in cui la transizione dall'ora legale all'ora solare si verifica in un sistema operativo.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Gennaio** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Febbraio** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Marzo** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Aprile** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Maggio** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Giugno** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Luglio** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Settembre** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Ottobre** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembre** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dicembre** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")
</dt> </dl>

Nome del fuso orario rappresentato quando è attiva l'ora solare.

Esempio: "EST" (ora solare fuso orientale)

</dd> <dt>

**StandardSecond**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")
</dt> </dl>

Secondo **StandardMinute** quando la transizione dall'ora legale all'ora solare si verifica in un sistema operativo.

Esempio: 59

</dd> <dt>

**StandardYear**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")
</dt> </dl>

Anno in cui è attiva l'ora solare. Questa proprietà non è obbligatoria.

Esempio: 1997

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe del **\_ fuso orario Win32** deriva [**dall' \_ impostazione CIM**](cim-setting.md).

Non è possibile usare formati di data e ora standard, ad esempio 10/18/2002, durante la scrittura di query WMI. Al contrario, è necessario convertire le date utilizzate nelle query nel formato UTC. Questa operazione richiede due passaggi: 1) è necessario determinare l'offset (differenza in minuti) tra il fuso orario e l'ora di Greenwich e 2) è necessario convertire 10/18/2002 in un valore UTC.

Determinazione dell'offset rispetto all'ora di Greenwich

Di fatto, WMI rende difficile l'utilizzo di date e ore; Fortunatamente, WMI rende almeno più semplice determinare l'offset tra il fuso orario e l'ora di Greenwich. Il fuso orario Win32 della classe WMI \_ include una proprietà-bias, che restituisce l'offset GMT.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



Conversione di una data in un valore UTC

Dopo aver determinato l'offset GMT, è necessario convertire una data standard, ad esempio 10/18/2002, in una data UTC. Per convertire una data standard in una data UTC, è possibile utilizzare le funzioni di data VBScript, ad esempio anno, mese e giorno, per isolare i singoli componenti che costituiscono una data UTC. Quando si dispone di singoli valori per questi componenti, è possibile concatenarli nello stesso modo in cui si otterrebbe qualsiasi altro valore stringa. Le date UTC vengono considerate come stringhe perché l'offset GMT deve essere aggiunto alla fine. Se la data è stata considerata come numero, questo valore:

`20011018113047.000000-480`

Verrebbe erroneamente trattato come equazione matematica (le parentesi aggiunte per maggiore chiarezza):

`(20011018113047.000000) - (480)`

Ad esempio, nella data 10/18/2002, i singoli componenti sono:

-   Anno: 2002
-   Mese: 10
-   Giorno: 18

Lo script deve combinare questi tre valori, la stringa "113047,000000" (che rappresenta l'ora, inclusi i millisecondi) e l'offset GMT per derivare una data UTC. Ad esempio, (le parentesi aggiunte per maggiore chiarezza):

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> È possibile utilizzare le funzioni VBScript hour, minute e Second per convertire la parte relativa all'ora di una data UTC. Quindi, un'ora, ad esempio 11:30:47 A.M. verrebbe convertito in 113047.

 

Esiste un fattore di complicazione. Il mese deve occupare le posizioni 5 e 6 nella stringa; il giorno deve occupare le posizioni 7 e 8. Non si tratta di un problema con il mese 10 e il giorno 18. Ma come si ottiene il 5 luglio (mese 7, giorno 5) per riempire le posizioni richieste? La risposta consiste nell'aggiungere uno zero principale a ogni valore, impostando in questo modo il valore da 7 a 07 e da 5 a 05.

A tale scopo, utilizzare la funzione VBScript Len per verificare la lunghezza (numero di caratteri) del mese e del giorno. Se la lunghezza è 1 (ovvero è presente un solo carattere), aggiungere uno zero iniziali. Così


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente la data corrente viene convertita in una data UTC.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



Il codice VBScript seguente sampledetermines l'offset GMT, quindi converte una data corrente specificata (in questo caso, 10/18/2002) in formato di data e ora UTC. Dopo la conversione della data, questo valore viene usato per la ricerca in un computer e restituisce un elenco di tutte le cartelle create dopo 10/18/2002.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



Nell'esempio di codice VBScript seguente vengono visualizzate le impostazioni per le \_ istanze del fuso orario Win32.


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**SWbemDateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[Formato di data e ora](../wmisdk/date-and-time-format.md)
</dt> <dt>

[Attività WMI: date e ore](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
