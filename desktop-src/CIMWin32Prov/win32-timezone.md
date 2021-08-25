---
description: TimeZone Win32 \_&\# 8194; La classe WMI rappresenta le informazioni sul fuso orario per un computer che esegue Windows, incluse le modifiche necessarie per la transizione alla transizione all'ora legale.
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Win32_TimeZone classe
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
ms.openlocfilehash: 02b6d9d5c6100a652cf50096f5ef513fc164cfcfd2d8036e8444adc702459d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827661"
---
# <a name="win32_timezone-class"></a>Classe TimeZone Win32 \_

La classe  [WMI](../wmisdk/retrieving-a-class.md) **\_ TimeZone Win32** rappresenta le informazioni sul fuso orario per un computer che esegue Windows, incluse le modifiche necessarie per la transizione alla transizione all'ora legale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

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

La **classe \_ TimeZone Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TimeZone Win32** ha queste proprietà.

<dl> <dt>

**Bias**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Distorsione corrente per la traduzione dell'ora locale. La distorsione è la differenza tra Coordinated Universal Time (UTC) e l'ora locale. Tutte le traduzioni tra l'ora UTC e l'ora locale si basano sulla formula seguente: UTC = ora locale - distorsione. Questa proprietà è obbligatoria.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**DaylightBias**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporiche Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")
</dt> </dl>

Valore di distorsione da usare durante le traduzioni dell'ora locale che si verificano durante l'ora legale. Questa proprietà viene ignorata se non viene fornito un valore per la proprietà **DaylightDay.** Il valore di questa proprietà viene aggiunto alla proprietà **Bias** per formare la distorsione usata durante l'ora legale. Nella maggior parte dei fusi orari il valore di questa proprietà è -60.

</dd> <dt>

**Giorno legale**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDay")
</dt> </dl>

**DaylightDayOfWeek di** **DaylightMonth** quando si verifica la transizione dall'ora solare all'ora legale in questo sistema operativo.

Esempio: se il giorno di transizione (**DaylightDayOfWeek**) si verifica una domenica, il valore "1" indica la prima domenica del **daylightmonth**, "2" indica la seconda domenica e così via. Il valore "5" indica l'ultimo **DaylightDayOfWeek** del mese.

</dd> <dt>

**DaylightDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture dell'ora Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDayOfWeek")
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

**Giovedì** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Venerdì** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sabato** (6)


</dt> <dd></dd> </dl>

Esempio: 1

</dd> <dt>

**Ora legale**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wHour")
</dt> </dl>

Ora del giorno in cui si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

Esempio: 2

</dd> <dt>

**DaylightMillisecond**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture dell'ora Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMilliseconds")
</dt> </dl>

Millisecondo di **DaylightSecond quando** si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

</dd> <dt>

**Ora legaleMinute**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMinute")
</dt> </dl>

Minuti dell'ora **legale quando** si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

Esempio: 59

</dd> <dt>

**DaylightMonth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMonth")
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

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")
</dt> </dl>

Fuso orario rappresentato quando è in vigore l'ora legale.

Esempio: "EDT" (ora legale fuso orientale)

</dd> <dt>

**DaylightSecond**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture dell'ora Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wSecond")
</dt> </dl>

Secondo di **DaylightMinute quando** si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.

Esempio: 59

</dd> <dt>

**DaylightYear**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di tempo Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")
</dt> </dl>

Anno in cui è in vigore l'ora legale. Questa proprietà non è obbligatoria.

Esempio: 1997

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**StandardBias**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporiche Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Unità**](../wmisdk/standard-qualifiers.md) ("minuti")
</dt> </dl>

Valore di distorsione da usare quando l'ora legale non è in vigore. Questa proprietà viene ignorata se non viene specificato un valore per **StandardDay.** Il valore di questa proprietà viene aggiunto alla proprietà **Bias** per formare la distorsione durante l'ora solare.

Esempio: 0

</dd> <dt>

**StandardDay**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDay")
</dt> </dl>

**StandardDayOfWeek** di **StandardMonth** quando si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

Se il giorno di transizione (**StandardDayOfWeek**) si verifica di domenica, il valore "1" indica la prima domenica di **StandardMonth**, "2" indica la seconda domenica e così via. Il valore "5" indica l'ultimo **StandardDayOfWeek** del mese.

</dd> <dt>

**StandardDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")
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

**Giovedì** (4)


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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")
</dt> </dl>

Ora del giorno in cui si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

Esempio: 11

</dd> <dt>

**StandardMillisecond**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")
</dt> </dl>

Millisecondo di **StandardSecond** quando si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

</dd> <dt>

**StandardMinute**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")
</dt> </dl>

Minuto del giorno **standard quando** si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

Esempio: 59

</dd> <dt>

**StandardMonth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")
</dt> </dl>

Mese in cui si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

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

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")
</dt> </dl>

Nome del fuso orario rappresentato quando è in vigore l'ora solare.

Esempio: "EST" (ora solare fuso orientale)

</dd> <dt>

**StandardSecond**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")
</dt> </dl>

Secondo di **StandardMinute quando** si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.

Esempio: 59

</dd> <dt>

**StandardYear**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture temporizzazione Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")
</dt> </dl>

Anno in cui è in vigore l'ora solare. Questa proprietà non è obbligatoria.

Esempio: 1997

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ TimeZone Win32** deriva dall'impostazione [**CIM \_**](cim-setting.md).

Non è possibile usare formati di data e ora standard, ad esempio il 18/10/2002, quando si scrivono query WMI. È invece necessario convertire tutte le date usate nelle query nel formato UTC. Questa operazione richiede due passaggi: 1) È necessario determinare l'offset (differenza in minuti) tra il fuso orario e l'ora di Greenwich e 2) è necessario convertire il 18/10/2002 in un valore UTC.

Determinazione dell'offset dall'ora media di Greenwich

In effetti, WMI rende difficile l'utilizzo di date e ore; Fortunatamente, WMI almeno semplifica la determinazione dell'offset tra il fuso orario e l'ora di Greenwich. La classe WMI Win32 \_ TimeZone include una proprietà, Bias, che restituisce l'offset GMT.


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

Dopo aver determinato l'offset GMT, è necessario convertire una data standard, ad esempio il 18/10/2002, in una data UTC. Per convertire una data standard in una data UTC, è possibile usare funzioni data VBScript, ad esempio Anno, Mese e Giorno, per isolare i singoli componenti che costituiscono una data UTC. Dopo aver creato singoli valori per questi componenti, è possibile concatenarli nello stesso modo in cui si farebbe con qualsiasi altro valore stringa. Le date UTC vengono considerate stringhe perché l'offset GMT deve essere aggiunto alla fine. Se la data è stata considerata come un numero, questo valore:

`20011018113047.000000-480`

Verrebbe erroneamente trattato come un'equazione matematica (parentesi aggiunte per maggiore chiarezza):

`(20011018113047.000000) - (480)`

Ad esempio, nella data 18/10/2002, i singoli componenti sono:

-   Anno: 2002
-   Mese: 10
-   Giorno: 18

Lo script deve combinare questi tre valori, la stringa "113047.000000" (che rappresenta l'ora, inclusi i millisecondi) e l'offset GMT per derivare una data UTC. Ad esempio, (parentesi aggiunte di nuovo per maggiore chiarezza):

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> È possibile usare le funzioni VBScript Hour, Minute e Second per convertire la parte relativa all'ora di una data UTC. Di conseguenza, un orario come 11:30:47 verrebbe convertito in 113047.

 

Esiste un fattore di complicazione. Il mese deve assumere le posizioni 5 e 6 nella stringa. il giorno deve assumere le posizioni 7 e 8. Questo non è un problema con il mese 10 e il giorno 18. Ma come si ottiene il 5 luglio (mese 7, giorno 5) per riempire le posizioni richieste? La risposta è aggiungere uno zero iniziale a ogni valore, modificando quindi 7 in 07 e 5 a 05.

A tale scopo, usare la funzione VBScript Len per controllare la lunghezza (numero di caratteri) nel mese e nel giorno. Se la lunghezza è 1 (vale a dire che è presente un solo carattere), aggiungere uno zero iniziale. Così:


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a>Esempio

Nell'esempio di VBScript seguente la data corrente viene convertita in una data UTC.


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



L'esempio VBScript seguente determina l'offset GMT e quindi converte una data corrente specificata (in questo caso, 18/10/2002) nel formato data-ora UTC. Dopo la conversione della data, tale valore viene usato per cercare un computer e restituisce un elenco di tutte le cartelle create dopo il 18/10/2002.


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



Nell'esempio di codice VBScript seguente vengono visualizzate le impostazioni per le istanze \_ di TimeZone Win32.


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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**SWbemDateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[Formato di data e ora](../wmisdk/date-and-time-format.md)
</dt> <dt>

[Attività WMI: date e ore](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
