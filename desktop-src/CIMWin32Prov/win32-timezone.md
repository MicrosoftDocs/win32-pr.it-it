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
# <a name="win32_timezone-class"></a><span data-ttu-id="607b4-103">\_Classe TimeZone di Win32</span><span class="sxs-lookup"><span data-stu-id="607b4-103">Win32\_TimeZone class</span></span>

<span data-ttu-id="607b4-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) del **\_ fuso orario Win32** rappresenta le informazioni sul fuso orario per un computer che esegue Windows, che include le modifiche necessarie per la transizione alla transizione dell'ora legale.</span><span class="sxs-lookup"><span data-stu-id="607b4-104">The **Win32\_TimeZone** [WMI class](../wmisdk/retrieving-a-class.md) represents the time zone information for a computer system running Windows, which includes the changes required for transitioning to daylight saving time transition.</span></span>

<span data-ttu-id="607b4-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="607b4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="607b4-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="607b4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="607b4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="607b4-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="607b4-108">Members</span><span class="sxs-lookup"><span data-stu-id="607b4-108">Members</span></span>

<span data-ttu-id="607b4-109">La classe del **\_ fuso orario Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="607b4-109">The **Win32\_TimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="607b4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="607b4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="607b4-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="607b4-111">Properties</span></span>

<span data-ttu-id="607b4-112">La classe del **\_ fuso orario Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="607b4-112">The **Win32\_TimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="607b4-113">**Bias**</span><span class="sxs-lookup"><span data-stu-id="607b4-113">**Bias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-114">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="607b4-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-116">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| Debias [**\_ \_ Information fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="607b4-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-117">Distorsione corrente per la conversione dell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="607b4-117">Current bias for local time translation.</span></span> <span data-ttu-id="607b4-118">La distorsione è la differenza tra l'ora UTC (Coordinated Universal Time) e l'ora locale.</span><span class="sxs-lookup"><span data-stu-id="607b4-118">The bias is the difference between Coordinated Universal Time (UTC) and local time.</span></span> <span data-ttu-id="607b4-119">Tutte le traduzioni tra l'ora UTC e l'ora locale sono basate sulla formula seguente: UTC = tempo locale-bias.</span><span class="sxs-lookup"><span data-stu-id="607b4-119">All translations between UTC and local time are based on the following formula: UTC = local time - bias.</span></span> <span data-ttu-id="607b4-120">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="607b4-120">This property is required.</span></span>

</dd> <dt>

<span data-ttu-id="607b4-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="607b4-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607b4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-124">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="607b4-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="607b4-125">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="607b4-125">Short textual description of the current object.</span></span>

<span data-ttu-id="607b4-126">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="607b4-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="607b4-127">**DaylightBias**</span><span class="sxs-lookup"><span data-stu-id="607b4-127">**DaylightBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-128">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="607b4-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-130">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="607b4-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-131">Valore di distorsione da utilizzare durante le conversioni dell'ora locale che si verificano durante l'ora legale.</span><span class="sxs-lookup"><span data-stu-id="607b4-131">Bias value to be used during local time translations that occur during daylight saving time.</span></span> <span data-ttu-id="607b4-132">Questa proprietà viene ignorata se non viene fornito un valore per la proprietà **DaylightDay** .</span><span class="sxs-lookup"><span data-stu-id="607b4-132">This property is ignored if a value for the **DaylightDay** property is not supplied.</span></span> <span data-ttu-id="607b4-133">Il valore di questa proprietà viene aggiunto alla proprietà **Bias** per formare la distorsione utilizzata durante l'ora legale.</span><span class="sxs-lookup"><span data-stu-id="607b4-133">The value of this property is added to the **Bias** property to form the bias used during daylight time.</span></span> <span data-ttu-id="607b4-134">Nella maggior parte dei fusi orari, il valore di questa proprietà è-60.</span><span class="sxs-lookup"><span data-stu-id="607b4-134">In most time zones, the value of this property is -60.</span></span>

</dd> <dt>

<span data-ttu-id="607b4-135">**DaylightDay**</span><span class="sxs-lookup"><span data-stu-id="607b4-135">**DaylightDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-136">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-138">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDay")</span><span class="sxs-lookup"><span data-stu-id="607b4-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-139">**DaylightDayOfWeek** di **DaylightMonth** quando si verifica la transizione dall'ora solare all'ora legale in questo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-139">**DaylightDayOfWeek** of the **DaylightMonth** when the transition from standard time to daylight saving time occurs on this operating system.</span></span>

<span data-ttu-id="607b4-140">Esempio: se il giorno di transizione (**DaylightDayOfWeek**) si verifica a domenica, il valore "1" indica la prima domenica di **DaylightMonth**, "2" indica la seconda domenica e così via.</span><span class="sxs-lookup"><span data-stu-id="607b4-140">Example: If the transition day (**DaylightDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **DaylightMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="607b4-141">Il valore "5" indica l'ultimo **DaylightDayOfWeek** del mese.</span><span class="sxs-lookup"><span data-stu-id="607b4-141">The value "5" indicates the last **DaylightDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="607b4-142">**DaylightDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="607b4-142">**DaylightDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-143">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="607b4-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-145">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDayOfWeek")</span><span class="sxs-lookup"><span data-stu-id="607b4-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-146">Giorno della settimana in cui si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-146">Day of the week when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="607b4-147">**Domenica** (0)</span><span class="sxs-lookup"><span data-stu-id="607b4-147">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="607b4-148">**Lunedì** (1)</span><span class="sxs-lookup"><span data-stu-id="607b4-148">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="607b4-149">**Martedì** (2)</span><span class="sxs-lookup"><span data-stu-id="607b4-149">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="607b4-150">**Mercoledì** (3)</span><span class="sxs-lookup"><span data-stu-id="607b4-150">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="607b4-151">**Giovedi** (4)</span><span class="sxs-lookup"><span data-stu-id="607b4-151">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="607b4-152">**Venerdì** (5)</span><span class="sxs-lookup"><span data-stu-id="607b4-152">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="607b4-153">**Sabato** (6)</span><span class="sxs-lookup"><span data-stu-id="607b4-153">**Saturday** (6)</span></span>


<span data-ttu-id="607b4-154"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="607b4-154"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="607b4-155">Esempio: 1</span><span class="sxs-lookup"><span data-stu-id="607b4-155">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="607b4-156">**DaylightHour**</span><span class="sxs-lookup"><span data-stu-id="607b4-156">**DaylightHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-159">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wHour")</span><span class="sxs-lookup"><span data-stu-id="607b4-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-160">Ora del giorno in cui si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-160">Hour of the day when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="607b4-161">Esempio: 2</span><span class="sxs-lookup"><span data-stu-id="607b4-161">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="607b4-162">**DaylightMillisecond**</span><span class="sxs-lookup"><span data-stu-id="607b4-162">**DaylightMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-165">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMilliseconds")</span><span class="sxs-lookup"><span data-stu-id="607b4-165">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-166">Millisecondi di **DaylightSecond** quando si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-166">Millisecond of the **DaylightSecond** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="607b4-167">**DaylightMinute**</span><span class="sxs-lookup"><span data-stu-id="607b4-167">**DaylightMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-170">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMinute")</span><span class="sxs-lookup"><span data-stu-id="607b4-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-171">Minuto del **DaylightHour** quando si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-171">Minute of the **DaylightHour** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="607b4-172">Esempio: 59</span><span class="sxs-lookup"><span data-stu-id="607b4-172">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="607b4-173">**DaylightMonth**</span><span class="sxs-lookup"><span data-stu-id="607b4-173">**DaylightMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-174">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-176">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMonth")</span><span class="sxs-lookup"><span data-stu-id="607b4-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-177">Mese in cui si verifica la transizione dall'ora solare all'ora legale in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-177">Month when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="607b4-178">**Gennaio** (1)</span><span class="sxs-lookup"><span data-stu-id="607b4-178">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="607b4-179">**Febbraio** (2)</span><span class="sxs-lookup"><span data-stu-id="607b4-179">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="607b4-180">**Marzo** (3)</span><span class="sxs-lookup"><span data-stu-id="607b4-180">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="607b4-181">**Aprile** (4)</span><span class="sxs-lookup"><span data-stu-id="607b4-181">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="607b4-182">**Maggio** (5)</span><span class="sxs-lookup"><span data-stu-id="607b4-182">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="607b4-183">**Giugno** (6)</span><span class="sxs-lookup"><span data-stu-id="607b4-183">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="607b4-184">**Luglio** (7)</span><span class="sxs-lookup"><span data-stu-id="607b4-184">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="607b4-185">**Agosto** (8)</span><span class="sxs-lookup"><span data-stu-id="607b4-185">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="607b4-186">**Settembre** (9)</span><span class="sxs-lookup"><span data-stu-id="607b4-186">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="607b4-187">**Ottobre** (10)</span><span class="sxs-lookup"><span data-stu-id="607b4-187">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="607b4-188">**Novembre** (11)</span><span class="sxs-lookup"><span data-stu-id="607b4-188">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="607b4-189">**Dicembre** (12)</span><span class="sxs-lookup"><span data-stu-id="607b4-189">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="607b4-190">**DaylightName**</span><span class="sxs-lookup"><span data-stu-id="607b4-190">**DaylightName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607b4-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-193">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")</span><span class="sxs-lookup"><span data-stu-id="607b4-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightName")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-194">Fuso orario rappresentato quando è attiva l'ora legale.</span><span class="sxs-lookup"><span data-stu-id="607b4-194">Time zone being represented when daylight saving time is in effect.</span></span>

<span data-ttu-id="607b4-195">Esempio: "EDT" (ora legale orientale)</span><span class="sxs-lookup"><span data-stu-id="607b4-195">Example: "EDT" (Eastern Daylight Time)</span></span>

</dd> <dt>

<span data-ttu-id="607b4-196">**DaylightSecond**</span><span class="sxs-lookup"><span data-stu-id="607b4-196">**DaylightSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-197">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-199">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wSecond")</span><span class="sxs-lookup"><span data-stu-id="607b4-199">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-200">Secondo **DaylightMinute** quando la transizione dall'ora solare all'ora legale si verifica in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-200">Second of the **DaylightMinute** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="607b4-201">Esempio: 59</span><span class="sxs-lookup"><span data-stu-id="607b4-201">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="607b4-202">**DaylightYear**</span><span class="sxs-lookup"><span data-stu-id="607b4-202">**DaylightYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-203">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-205">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")</span><span class="sxs-lookup"><span data-stu-id="607b4-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-206">Anno in cui è attiva l'ora legale.</span><span class="sxs-lookup"><span data-stu-id="607b4-206">Year when daylight saving time is in effect.</span></span> <span data-ttu-id="607b4-207">Questa proprietà non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="607b4-207">This property is not required.</span></span>

<span data-ttu-id="607b4-208">Esempio: 1997</span><span class="sxs-lookup"><span data-stu-id="607b4-208">Example: 1997</span></span>

</dd> <dt>

<span data-ttu-id="607b4-209">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="607b4-209">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607b4-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607b4-212">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="607b4-212">Textual description of the current object.</span></span>

<span data-ttu-id="607b4-213">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="607b4-213">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="607b4-214">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="607b4-214">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607b4-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-217">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="607b4-217">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="607b4-218">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="607b4-218">Identifier by which the current object is known.</span></span>

<span data-ttu-id="607b4-219">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="607b4-219">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="607b4-220">**StandardBias**</span><span class="sxs-lookup"><span data-stu-id="607b4-220">**StandardBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-221">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-223">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="607b4-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-224">Valore di distorsione da utilizzare quando l'ora legale non è attiva.</span><span class="sxs-lookup"><span data-stu-id="607b4-224">Bias value to use when daylight saving time is not in effect.</span></span> <span data-ttu-id="607b4-225">Questa proprietà viene ignorata se non viene specificato un valore per **StandardDay** .</span><span class="sxs-lookup"><span data-stu-id="607b4-225">This property is ignored if a value for **StandardDay** is not supplied.</span></span> <span data-ttu-id="607b4-226">Il valore di questa proprietà viene aggiunto alla proprietà **Bias** per formare la distorsione durante l'ora solare.</span><span class="sxs-lookup"><span data-stu-id="607b4-226">The value of this property is added to the **Bias** property to form the bias during standard time.</span></span>

<span data-ttu-id="607b4-227">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="607b4-227">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="607b4-228">**StandardDay**</span><span class="sxs-lookup"><span data-stu-id="607b4-228">**StandardDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-229">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-231">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDay")</span><span class="sxs-lookup"><span data-stu-id="607b4-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-232">**StandardDayofWeek** di **StandardMonth** quando si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-232">**StandardDayOfWeek** of the **StandardMonth** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="607b4-233">Se il giorno di transizione (**StandardDayofWeek**) si verifica a domenica, il valore "1" indica la prima domenica del **StandardMonth**, "2" indica la seconda domenica e così via.</span><span class="sxs-lookup"><span data-stu-id="607b4-233">If the transition day (**StandardDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **StandardMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="607b4-234">Il valore "5" indica l'ultimo **StandardDayofWeek** del mese.</span><span class="sxs-lookup"><span data-stu-id="607b4-234">The value "5" indicates the last **StandardDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="607b4-235">**StandardDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="607b4-235">**StandardDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-236">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="607b4-236">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-238">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")</span><span class="sxs-lookup"><span data-stu-id="607b4-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-239">Giorno della settimana in cui si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-239">Day of the week when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="607b4-240">**Domenica** (0)</span><span class="sxs-lookup"><span data-stu-id="607b4-240">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="607b4-241">**Lunedì** (1)</span><span class="sxs-lookup"><span data-stu-id="607b4-241">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="607b4-242">**Martedì** (2)</span><span class="sxs-lookup"><span data-stu-id="607b4-242">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="607b4-243">**Mercoledì** (3)</span><span class="sxs-lookup"><span data-stu-id="607b4-243">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="607b4-244">**Giovedi** (4)</span><span class="sxs-lookup"><span data-stu-id="607b4-244">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="607b4-245">**Venerdì** (5)</span><span class="sxs-lookup"><span data-stu-id="607b4-245">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="607b4-246">**Sabato** (6)</span><span class="sxs-lookup"><span data-stu-id="607b4-246">**Saturday** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="607b4-247">**StandardHour**</span><span class="sxs-lookup"><span data-stu-id="607b4-247">**StandardHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-248">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-248">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-250">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")</span><span class="sxs-lookup"><span data-stu-id="607b4-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-251">Ora del giorno in cui si verifica la transizione dall'ora legale all'ora solare in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-251">Hour of the day when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="607b4-252">Esempio: 11</span><span class="sxs-lookup"><span data-stu-id="607b4-252">Example: 11</span></span>

</dd> <dt>

<span data-ttu-id="607b4-253">**StandardMillisecond**</span><span class="sxs-lookup"><span data-stu-id="607b4-253">**StandardMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-254">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-256">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")</span><span class="sxs-lookup"><span data-stu-id="607b4-256">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-257">Millisecondi di **StandardSecond** quando la transizione dall'ora legale all'ora solare si verifica in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-257">Millisecond of the **StandardSecond** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="607b4-258">**StandardMinute**</span><span class="sxs-lookup"><span data-stu-id="607b4-258">**StandardMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-259">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-261">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")</span><span class="sxs-lookup"><span data-stu-id="607b4-261">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-262">Minuto del **StandardDay** quando la transizione dall'ora legale all'ora solare si verifica in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-262">Minute of the **StandardDay** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="607b4-263">Esempio: 59</span><span class="sxs-lookup"><span data-stu-id="607b4-263">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="607b4-264">**StandardMonth**</span><span class="sxs-lookup"><span data-stu-id="607b4-264">**StandardMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-265">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-267">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")</span><span class="sxs-lookup"><span data-stu-id="607b4-267">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-268">Mese in cui la transizione dall'ora legale all'ora solare si verifica in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-268">Month when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="607b4-269">**Gennaio** (1)</span><span class="sxs-lookup"><span data-stu-id="607b4-269">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="607b4-270">**Febbraio** (2)</span><span class="sxs-lookup"><span data-stu-id="607b4-270">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="607b4-271">**Marzo** (3)</span><span class="sxs-lookup"><span data-stu-id="607b4-271">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="607b4-272">**Aprile** (4)</span><span class="sxs-lookup"><span data-stu-id="607b4-272">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="607b4-273">**Maggio** (5)</span><span class="sxs-lookup"><span data-stu-id="607b4-273">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="607b4-274">**Giugno** (6)</span><span class="sxs-lookup"><span data-stu-id="607b4-274">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="607b4-275">**Luglio** (7)</span><span class="sxs-lookup"><span data-stu-id="607b4-275">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="607b4-276">**Agosto** (8)</span><span class="sxs-lookup"><span data-stu-id="607b4-276">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="607b4-277">**Settembre** (9)</span><span class="sxs-lookup"><span data-stu-id="607b4-277">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="607b4-278">**Ottobre** (10)</span><span class="sxs-lookup"><span data-stu-id="607b4-278">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="607b4-279">**Novembre** (11)</span><span class="sxs-lookup"><span data-stu-id="607b4-279">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="607b4-280">**Dicembre** (12)</span><span class="sxs-lookup"><span data-stu-id="607b4-280">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="607b4-281">**StandardName**</span><span class="sxs-lookup"><span data-stu-id="607b4-281">**StandardName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607b4-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-284">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")</span><span class="sxs-lookup"><span data-stu-id="607b4-284">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardName")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-285">Nome del fuso orario rappresentato quando è attiva l'ora solare.</span><span class="sxs-lookup"><span data-stu-id="607b4-285">Name of the time zone being represented when standard time is in effect.</span></span>

<span data-ttu-id="607b4-286">Esempio: "EST" (ora solare fuso orientale)</span><span class="sxs-lookup"><span data-stu-id="607b4-286">Example: "EST" (Eastern Standard Time)</span></span>

</dd> <dt>

<span data-ttu-id="607b4-287">**StandardSecond**</span><span class="sxs-lookup"><span data-stu-id="607b4-287">**StandardSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-288">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-290">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")</span><span class="sxs-lookup"><span data-stu-id="607b4-290">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-291">Secondo **StandardMinute** quando la transizione dall'ora legale all'ora solare si verifica in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="607b4-291">Second of the **StandardMinute** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="607b4-292">Esempio: 59</span><span class="sxs-lookup"><span data-stu-id="607b4-292">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="607b4-293">**StandardYear**</span><span class="sxs-lookup"><span data-stu-id="607b4-293">**StandardYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607b4-294">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b4-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607b4-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607b4-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607b4-296">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures \| [**\_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")</span><span class="sxs-lookup"><span data-stu-id="607b4-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="607b4-297">Anno in cui è attiva l'ora solare.</span><span class="sxs-lookup"><span data-stu-id="607b4-297">Year when standard time is in effect.</span></span> <span data-ttu-id="607b4-298">Questa proprietà non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="607b4-298">This property is not required.</span></span>

<span data-ttu-id="607b4-299">Esempio: 1997</span><span class="sxs-lookup"><span data-stu-id="607b4-299">Example: 1997</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="607b4-300">Commenti</span><span class="sxs-lookup"><span data-stu-id="607b4-300">Remarks</span></span>

<span data-ttu-id="607b4-301">La classe del **\_ fuso orario Win32** deriva [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="607b4-301">The **Win32\_TimeZone** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="607b4-302">Non è possibile usare formati di data e ora standard, ad esempio 10/18/2002, durante la scrittura di query WMI.</span><span class="sxs-lookup"><span data-stu-id="607b4-302">You cannot use standard date-time formats - such as 10/18/2002 - when writing WMI queries.</span></span> <span data-ttu-id="607b4-303">Al contrario, è necessario convertire le date utilizzate nelle query nel formato UTC.</span><span class="sxs-lookup"><span data-stu-id="607b4-303">Instead, you need to convert any dates used in your queries to UTC format.</span></span> <span data-ttu-id="607b4-304">Questa operazione richiede due passaggi: 1) è necessario determinare l'offset (differenza in minuti) tra il fuso orario e l'ora di Greenwich e 2) è necessario convertire 10/18/2002 in un valore UTC.</span><span class="sxs-lookup"><span data-stu-id="607b4-304">This requires two steps: 1) You must determine the offset (difference in minutes) between your time zone and Greenwich Mean Time, and 2) you must convert 10/18/2002 to a UTC value.</span></span>

<span data-ttu-id="607b4-305">Determinazione dell'offset rispetto all'ora di Greenwich</span><span class="sxs-lookup"><span data-stu-id="607b4-305">Determining the Offset from Greenwich Mean Time</span></span>

<span data-ttu-id="607b4-306">Di fatto, WMI rende difficile l'utilizzo di date e ore; Fortunatamente, WMI rende almeno più semplice determinare l'offset tra il fuso orario e l'ora di Greenwich.</span><span class="sxs-lookup"><span data-stu-id="607b4-306">Admittedly, WMI makes it difficult to work with dates and times; fortunately, WMI at least makes it easy to determine the offset between your time zone and Greenwich Mean Time.</span></span> <span data-ttu-id="607b4-307">Il fuso orario Win32 della classe WMI \_ include una proprietà-bias, che restituisce l'offset GMT.</span><span class="sxs-lookup"><span data-stu-id="607b4-307">The WMI class Win32\_TimeZone includes a property - Bias - that returns the GMT offset.</span></span>


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



<span data-ttu-id="607b4-308">Conversione di una data in un valore UTC</span><span class="sxs-lookup"><span data-stu-id="607b4-308">Converting a Date to a UTC Value</span></span>

<span data-ttu-id="607b4-309">Dopo aver determinato l'offset GMT, è necessario convertire una data standard, ad esempio 10/18/2002, in una data UTC.</span><span class="sxs-lookup"><span data-stu-id="607b4-309">After you determine the GMT offset, you must then convert a standard date such as 10/18/2002 to a UTC date.</span></span> <span data-ttu-id="607b4-310">Per convertire una data standard in una data UTC, è possibile utilizzare le funzioni di data VBScript, ad esempio anno, mese e giorno, per isolare i singoli componenti che costituiscono una data UTC.</span><span class="sxs-lookup"><span data-stu-id="607b4-310">To convert a standard date to a UTC date, you can use VBScript date functions such as Year, Month, and Day to isolate the individual components that make up a UTC date.</span></span> <span data-ttu-id="607b4-311">Quando si dispone di singoli valori per questi componenti, è possibile concatenarli nello stesso modo in cui si otterrebbe qualsiasi altro valore stringa.</span><span class="sxs-lookup"><span data-stu-id="607b4-311">After you have individual values for these components, you can concatenate them in the same manner as you would any other string value.</span></span> <span data-ttu-id="607b4-312">Le date UTC vengono considerate come stringhe perché l'offset GMT deve essere aggiunto alla fine.</span><span class="sxs-lookup"><span data-stu-id="607b4-312">UTC dates are treated as strings because the GMT offset must be appended to the end.</span></span> <span data-ttu-id="607b4-313">Se la data è stata considerata come numero, questo valore:</span><span class="sxs-lookup"><span data-stu-id="607b4-313">If the date were seen as a number, this value:</span></span>

`20011018113047.000000-480`

<span data-ttu-id="607b4-314">Verrebbe erroneamente trattato come equazione matematica (le parentesi aggiunte per maggiore chiarezza):</span><span class="sxs-lookup"><span data-stu-id="607b4-314">Would be erroneously treated as a mathematical equation (parentheses added for clarity):</span></span>

`(20011018113047.000000) - (480)`

<span data-ttu-id="607b4-315">Ad esempio, nella data 10/18/2002, i singoli componenti sono:</span><span class="sxs-lookup"><span data-stu-id="607b4-315">For example, in the date 10/18/2002, the individual components are:</span></span>

-   <span data-ttu-id="607b4-316">Anno: 2002</span><span class="sxs-lookup"><span data-stu-id="607b4-316">Year: 2002</span></span>
-   <span data-ttu-id="607b4-317">Mese: 10</span><span class="sxs-lookup"><span data-stu-id="607b4-317">Month: 10</span></span>
-   <span data-ttu-id="607b4-318">Giorno: 18</span><span class="sxs-lookup"><span data-stu-id="607b4-318">Day: 18</span></span>

<span data-ttu-id="607b4-319">Lo script deve combinare questi tre valori, la stringa "113047,000000" (che rappresenta l'ora, inclusi i millisecondi) e l'offset GMT per derivare una data UTC.</span><span class="sxs-lookup"><span data-stu-id="607b4-319">The script would need to combine these three values, the string "113047.000000" (representing the time, including milliseconds), and the GMT offset to derive a UTC date.</span></span> <span data-ttu-id="607b4-320">Ad esempio, (le parentesi aggiunte per maggiore chiarezza):</span><span class="sxs-lookup"><span data-stu-id="607b4-320">For example, (parentheses again added for clarity):</span></span>

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> <span data-ttu-id="607b4-321">È possibile utilizzare le funzioni VBScript hour, minute e Second per convertire la parte relativa all'ora di una data UTC.</span><span class="sxs-lookup"><span data-stu-id="607b4-321">You can use the VBScript functions Hour, Minute, and Second to convert the time portion of a UTC date.</span></span> <span data-ttu-id="607b4-322">Quindi, un'ora, ad esempio 11:30:47 A.M.</span><span class="sxs-lookup"><span data-stu-id="607b4-322">Thus, a time such as 11:30:47 A.M.</span></span> <span data-ttu-id="607b4-323">verrebbe convertito in 113047.</span><span class="sxs-lookup"><span data-stu-id="607b4-323">would be converted to 113047.</span></span>

 

<span data-ttu-id="607b4-324">Esiste un fattore di complicazione.</span><span class="sxs-lookup"><span data-stu-id="607b4-324">There is one complicating factor.</span></span> <span data-ttu-id="607b4-325">Il mese deve occupare le posizioni 5 e 6 nella stringa; il giorno deve occupare le posizioni 7 e 8.</span><span class="sxs-lookup"><span data-stu-id="607b4-325">The month must take up positions 5 and 6 in the string; the day must take up positions 7 and 8.</span></span> <span data-ttu-id="607b4-326">Non si tratta di un problema con il mese 10 e il giorno 18.</span><span class="sxs-lookup"><span data-stu-id="607b4-326">This is no problem with month 10 and day 18.</span></span> <span data-ttu-id="607b4-327">Ma come si ottiene il 5 luglio (mese 7, giorno 5) per riempire le posizioni richieste?</span><span class="sxs-lookup"><span data-stu-id="607b4-327">But how do you get July 5 (month 7, day 5) to fill up the requisite positions?</span></span> <span data-ttu-id="607b4-328">La risposta consiste nell'aggiungere uno zero principale a ogni valore, impostando in questo modo il valore da 7 a 07 e da 5 a 05.</span><span class="sxs-lookup"><span data-stu-id="607b4-328">The answer is to add a leading zero to each value, thus changing the 7 to 07 and the 5 to 05.</span></span>

<span data-ttu-id="607b4-329">A tale scopo, utilizzare la funzione VBScript Len per verificare la lunghezza (numero di caratteri) del mese e del giorno.</span><span class="sxs-lookup"><span data-stu-id="607b4-329">To do this, use the VBScript Len function to check the length (number of characters) in the month and the day.</span></span> <span data-ttu-id="607b4-330">Se la lunghezza è 1 (ovvero è presente un solo carattere), aggiungere uno zero iniziali.</span><span class="sxs-lookup"><span data-stu-id="607b4-330">If the length is 1 (meaning that there is just one character), add a leading zero.</span></span> <span data-ttu-id="607b4-331">Così</span><span class="sxs-lookup"><span data-stu-id="607b4-331">Thus:</span></span>


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a><span data-ttu-id="607b4-332">Esempio</span><span class="sxs-lookup"><span data-stu-id="607b4-332">Examples</span></span>

<span data-ttu-id="607b4-333">Nell'esempio VBScript seguente la data corrente viene convertita in una data UTC.</span><span class="sxs-lookup"><span data-stu-id="607b4-333">The following VBScript example converts the current date to a UTC date.</span></span>


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



<span data-ttu-id="607b4-334">Il codice VBScript seguente sampledetermines l'offset GMT, quindi converte una data corrente specificata (in questo caso, 10/18/2002) in formato di data e ora UTC.</span><span class="sxs-lookup"><span data-stu-id="607b4-334">The following VBScript sampledetermines the GMT offset, and then converts a specified current date (in this case, 10/18/2002) to UTC date-time format.</span></span> <span data-ttu-id="607b4-335">Dopo la conversione della data, questo valore viene usato per la ricerca in un computer e restituisce un elenco di tutte le cartelle create dopo 10/18/2002.</span><span class="sxs-lookup"><span data-stu-id="607b4-335">After the date has been converted, that value is used to search a computer and returns a list of all the folders that were created after 10/18/2002.</span></span>


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



<span data-ttu-id="607b4-336">Nell'esempio di codice VBScript seguente vengono visualizzate le impostazioni per le \_ istanze del fuso orario Win32.</span><span class="sxs-lookup"><span data-stu-id="607b4-336">The following VBScript code example displays the settings for Win32\_TimeZone instances.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="607b4-337">Requisiti</span><span class="sxs-lookup"><span data-stu-id="607b4-337">Requirements</span></span>



| <span data-ttu-id="607b4-338">Requisito</span><span class="sxs-lookup"><span data-stu-id="607b4-338">Requirement</span></span> | <span data-ttu-id="607b4-339">Valore</span><span class="sxs-lookup"><span data-stu-id="607b4-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="607b4-340">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="607b4-340">Minimum supported client</span></span><br/> | <span data-ttu-id="607b4-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="607b4-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="607b4-342">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="607b4-342">Minimum supported server</span></span><br/> | <span data-ttu-id="607b4-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="607b4-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="607b4-344">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="607b4-344">Namespace</span></span><br/>                | <span data-ttu-id="607b4-345">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="607b4-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="607b4-346">MOF</span><span class="sxs-lookup"><span data-stu-id="607b4-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="607b4-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="607b4-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="607b4-348">DLL</span><span class="sxs-lookup"><span data-stu-id="607b4-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="607b4-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="607b4-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607b4-350">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="607b4-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607b4-351">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="607b4-351">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="607b4-352">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="607b4-352">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="607b4-353">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="607b4-353">**SWbemDateTime**</span></span>](../wmisdk/swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="607b4-354">Formato di data e ora</span><span class="sxs-lookup"><span data-stu-id="607b4-354">Date and Time Format</span></span>](../wmisdk/date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="607b4-355">Attività WMI: date e ore</span><span class="sxs-lookup"><span data-stu-id="607b4-355">WMI Tasks: Dates and Times</span></span>](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
