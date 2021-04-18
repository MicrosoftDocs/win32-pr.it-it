---
description: L'oggetto SWbemDateTime è un oggetto helper per analizzare e impostare i valori DateTime di Common Information Model (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Oggetto SWbemDateTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313175"
---
# <a name="swbemdatetime-object"></a><span data-ttu-id="8fe0c-103">Oggetto SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="8fe0c-103">SWbemDateTime object</span></span>

<span data-ttu-id="8fe0c-104">L'oggetto **SWbemDateTime** è un oggetto helper per analizzare e impostare i valori [DateTime](datetime.md) di Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="8fe0c-104">The **SWbemDateTime** object is a helper object to parse and set Common Information Model (CIM) [datetime](datetime.md) values.</span></span> <span data-ttu-id="8fe0c-105">Svolge un ruolo simile a [**SWbemObjectPath**](swbemobjectpath.md), che fornisce assistenza per formattare e interpretare i percorsi degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-105">It plays a role similar to [**SWbemObjectPath**](swbemobjectpath.md), which provides assistance to format and interpret object paths.</span></span> <span data-ttu-id="8fe0c-106">Per creare l'oggetto **SWbemDateTime** , è possibile utilizzare la chiamata a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-106">You can use the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call to create the **SWbemDateTime** object.</span></span>

<span data-ttu-id="8fe0c-107">Un oggetto **SWbemDateTime** può essere inizializzato da e formattato in valori di **\_ Data** o **FILETIME** VT utilizzando i metodi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-107">An **SWbemDateTime** object can be initialized from and formatted in either **VT\_DATE** or **FILETIME** values using methods on the object.</span></span> <span data-ttu-id="8fe0c-108">Utilizzando le proprietà dell'oggetto, il valore può essere analizzato in componenti anno, mese, giorno, ora, minuti, secondi o microsecondi.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-108">Using properties of the object, the value can be parsed into component year, month, day, hour, minutes, seconds, or microseconds.</span></span> <span data-ttu-id="8fe0c-109">L'oggetto **SWbemDateTime** può essere formattato in valori sia locali che UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="8fe0c-109">The **SWbemDateTime** object can be formatted into either local or Coordinated Universal Time (UTC) values.</span></span> <span data-ttu-id="8fe0c-110">Per altre informazioni, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="8fe0c-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="8fe0c-111">**SWbemDateTime** è l'unico oggetto di scripting Strumentazione gestione Windows (WMI) contrassegnato come Safe per l'inizializzazione e gli script in esecuzione sulle pagine HTML in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-111">**SWbemDateTime** is the only Windows Management Instrumentation (WMI) scripting object that is marked safe for initialization and scripts running on HTML pages in Internet Explorer.</span></span>

## <a name="members"></a><span data-ttu-id="8fe0c-112">Membri</span><span class="sxs-lookup"><span data-stu-id="8fe0c-112">Members</span></span>

<span data-ttu-id="8fe0c-113">L'oggetto **SWbemDateTime** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8fe0c-113">The **SWbemDateTime** object has these types of members:</span></span>

-   [<span data-ttu-id="8fe0c-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="8fe0c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="8fe0c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8fe0c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8fe0c-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="8fe0c-116">Methods</span></span>

<span data-ttu-id="8fe0c-117">L'oggetto **SWbemDateTime** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-117">The **SWbemDateTime** object has these methods.</span></span>



| <span data-ttu-id="8fe0c-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="8fe0c-118">Method</span></span>                                           | <span data-ttu-id="8fe0c-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fe0c-119">Description</span></span>                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fe0c-120">**GetFileTime ha provocato**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-120">**GetFileTime**</span></span>](swbemdatetime-getfiletime.md) | <span data-ttu-id="8fe0c-121">Converte una data e un'ora **FILETIME** , espresse come **BSTR**, in un formato [DateTime](datetime.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-121">Converts a **FILETIME** date and time, expressed as a **BSTR**, to a WMI [DATETIME](datetime.md) format.</span></span><br/> |
| [<span data-ttu-id="8fe0c-122">**GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-122">**GetVarDate**</span></span>](swbemdatetime-getvardate.md)   | <span data-ttu-id="8fe0c-123">Converte un valore di data e ora in formato [DateTime](datetime.md) WMI in una **\_ Data VT**.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-123">Converts a WMI [DATETIME](datetime.md) formatted date and time value to a **VT\_DATE**.</span></span><br/>                  |
| [<span data-ttu-id="8fe0c-124">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-124">**SetFileTime**</span></span>](swbemdatetime-setfiletime.md) | <span data-ttu-id="8fe0c-125">Converte un formato [DateTime](datetime.md) WMI in una data e un'ora **FILETIME** , espresse come **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-125">Converts a WMI [DATETIME](datetime.md) format to a **FILETIME** date and time, expressed as a **BSTR**.</span></span><br/>  |
| [<span data-ttu-id="8fe0c-126">**SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-126">**SetVarDate**</span></span>](swbemdatetime-setvardate.md)   | <span data-ttu-id="8fe0c-127">Converte una data e un'ora in formato **\_ Data VT** in un valore [DateTime](datetime.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-127">Converts a **VT\_DATE** formatted date and time to a WMI [DATETIME](datetime.md).</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="8fe0c-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8fe0c-128">Properties</span></span>

<span data-ttu-id="8fe0c-129">L'oggetto **SWbemDateTime** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-129">The **SWbemDateTime** object has these properties.</span></span>



| <span data-ttu-id="8fe0c-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8fe0c-130">Property</span></span>                                                                        | <span data-ttu-id="8fe0c-131">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="8fe0c-131">Access type</span></span>           | <span data-ttu-id="8fe0c-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fe0c-132">Description</span></span>                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fe0c-133">**Giorno**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-133">**Day**</span></span>](swbemdatetime-day.md)<br/>                                     | <span data-ttu-id="8fe0c-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-134">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-135">Componente relativo al giorno di un valore [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-135">The day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="8fe0c-136">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-136">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)<br/>                   | <span data-ttu-id="8fe0c-137">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-137">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-138">Indica se il giorno viene specificato o lasciato come carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-138">Indicates whether the day is specified or left as a wildcard.</span></span><br/>                                                        |
| [<span data-ttu-id="8fe0c-139">**Hours**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-139">**Hours**</span></span>](swbemdatetime-hours.md)<br/>                                 | <span data-ttu-id="8fe0c-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-140">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-141">Ore del componente relativo al giorno di un valore [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-141">The hours of the day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                              |
| [<span data-ttu-id="8fe0c-142">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-142">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)<br/>               | <span data-ttu-id="8fe0c-143">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-143">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-144">Indica se l'ora è specificata o lasciata come carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-144">Indicates whether the hour is specified or left as a wildcard.</span></span><br/>                                                       |
| [<span data-ttu-id="8fe0c-145">**Intervallo**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-145">**IsInterval**</span></span>](swbemdatetime-isinterval.md)<br/>                       | <span data-ttu-id="8fe0c-146">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-146">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-147">Indica che almeno un componente del valore [DateTime](datetime.md) CIM rappresenta un intervallo anziché una data.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-147">Indicates that at least one component of the CIM [datetime](datetime.md) represents an interval rather than a date.</span></span><br/> |
| [<span data-ttu-id="8fe0c-148">**Microsecondi**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-148">**Microseconds**</span></span>](swbemdatetime-microseconds.md)<br/>                   | <span data-ttu-id="8fe0c-149">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-149">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-150">Componente di microsecondi di un valore [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-150">The microseconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                  |
| [<span data-ttu-id="8fe0c-151">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-151">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)<br/> | <span data-ttu-id="8fe0c-152">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-152">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-153">Indica se il componente di microsecondi viene specificato o lasciato come carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-153">Indicates whether the microseconds component is specified or left as a wildcard.</span></span><br/>                                     |
| [<span data-ttu-id="8fe0c-154">**Minuti**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-154">**Minutes**</span></span>](swbemdatetime-minutes.md)<br/>                             | <span data-ttu-id="8fe0c-155">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-155">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-156">Componente relativo ai minuti di un valore [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-156">The minutes component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="8fe0c-157">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-157">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)<br/>           | <span data-ttu-id="8fe0c-158">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-158">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-159">Indica se il componente minuti è specificato o lasciato come carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-159">Indicates whether the minutes component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="8fe0c-160">**Mese**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-160">**Month**</span></span>](swbemdatetime-month.md)<br/>                                 | <span data-ttu-id="8fe0c-161">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-161">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-162">Componente relativo al mese di un valore [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-162">The month component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                         |
| [<span data-ttu-id="8fe0c-163">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-163">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)<br/>               | <span data-ttu-id="8fe0c-164">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-164">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-165">Indica se il mese è specificato o lasciato come carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-165">Indicates whether the month is specified or left as a wildcard.</span></span><br/>                                                      |
| [<span data-ttu-id="8fe0c-166">**Secondi**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-166">**Seconds**</span></span>](swbemdatetime-seconds.md)<br/>                             | <span data-ttu-id="8fe0c-167">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-167">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-168">Componente relativo ai secondi di un valore [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-168">The seconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="8fe0c-169">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-169">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)<br/>           | <span data-ttu-id="8fe0c-170">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-170">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-171">Indica se il componente secondi viene specificato o lasciato come carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-171">Indicates whether the seconds component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="8fe0c-172">**UTC**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-172">**UTC**</span></span>](swbemdatetime-utc.md)<br/>                                     | <span data-ttu-id="8fe0c-173">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-173">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-174">Componente UTC di un valore [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-174">The UTC component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="8fe0c-175">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-175">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)<br/>                   | <span data-ttu-id="8fe0c-176">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-176">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-177">Indica se il componente UTC è specificato o lasciato come carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-177">Indicates whether the UTC component is specified or left as a wildcard.</span></span><br/>                                              |
| [<span data-ttu-id="8fe0c-178">**Valore**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-178">**Value**</span></span>](swbemdatetime-value.md)<br/>                                 | <span data-ttu-id="8fe0c-179">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-179">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-180">Valore [DateTime](datetime.md) CIM completo.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-180">The full CIM [datetime](datetime.md) value.</span></span><br/>                                                                         |
| [<span data-ttu-id="8fe0c-181">**Anno**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-181">**Year**</span></span>](swbemdatetime-year.md)<br/>                                   | <span data-ttu-id="8fe0c-182">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-182">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-183">Componente relativo all'anno di un valore [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-183">The year component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                          |
| [<span data-ttu-id="8fe0c-184">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="8fe0c-184">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)<br/>                 | <span data-ttu-id="8fe0c-185">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8fe0c-185">Read/write</span></span><br/> | <span data-ttu-id="8fe0c-186">Indica se l'anno viene specificato o lasciato come carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-186">Indicates whether or not the year is specified or left as a wildcard.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="8fe0c-187">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fe0c-187">Remarks</span></span>

<span data-ttu-id="8fe0c-188">I timestamp del record WMI sono nel formato UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="8fe0c-188">WMI records timestamps in universal time coordinate (UTC) format.</span></span> <span data-ttu-id="8fe0c-189">L'ora UTC non è il formato usato dalla maggior parte degli sviluppatori e dagli amministratori IT.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-189">UTC is not the format that most developers and IT administrators use.</span></span> <span data-ttu-id="8fe0c-190">Pertanto, un problema comune è determinare come tradurre l'ora UTC in un elemento più leggibile.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-190">Therefore, a common issue is determining how to translate UTC into something more readable.</span></span> <span data-ttu-id="8fe0c-191">Per ulteriori informazioni sull'utilizzo dell'ora UTC, vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md) e [utilizzo di date e ore con WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="8fe0c-191">For more information on how to work with UTC, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md) and [Working with Dates and Times using WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span></span> <span data-ttu-id="8fe0c-192">È anche possibile leggere le informazioni sul [tempo (Oh e sulle date)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) e [come è possibile sottrarre un numero specificato di giorni da un valore UTC?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) post di Blog per altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-192">You can also read the [It s About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) and [How Can I Subtract a Specified Number of Days from a UTC Value?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog posts for additional information.</span></span>

<span data-ttu-id="8fe0c-193">Eventuali campi numerici possono avere un valore jolly se la proprietà di [**intervallo**](swbemdatetime-isinterval.md) è impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-193">Any numeric field can have a wildcard value if the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span> <span data-ttu-id="8fe0c-194">I campi con valori jolly contengono asterischi nell'intero campo.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-194">Fields with wildcard values contain asterisks in the entire field.</span></span>

<span data-ttu-id="8fe0c-195">Ogni proprietà, ad esempio [**Day**](swbemdatetime-day.md), ha un valore booleano specificato corrispondente, ad esempio [**DaySpecified**](swbemdatetime-dayspecified.md).</span><span class="sxs-lookup"><span data-stu-id="8fe0c-195">Each property, for example [**Day**](swbemdatetime-day.md), has a corresponding specified Boolean value, such as [**DaySpecified**](swbemdatetime-dayspecified.md).</span></span> <span data-ttu-id="8fe0c-196">Quando **DaySpecified** è **false**, il valore viene interpretato come un intervallo anziché come numero compreso tra 01 e 31.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-196">When **DaySpecified** is **FALSE**, then the value is interpreted as an interval rather than a number between 01 and 31.</span></span> <span data-ttu-id="8fe0c-197">Se un intervallo viene usato in qualsiasi punto del valore [DateTime](datetime.md) CIM, anche l' [**intervallo**](swbemdatetime-isinterval.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-197">If an interval is used anywhere in the CIM [datetime](datetime.md) value, then [**IsInterval**](swbemdatetime-isinterval.md) is also set to **TRUE**.</span></span> <span data-ttu-id="8fe0c-198">Per impostazione predefinita, un valore DateTime CIM deve contenere una data anziché uno o più intervalli.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-198">The default is for a CIM datetime value to contain a date rather than one or more intervals.</span></span>

<span data-ttu-id="8fe0c-199">Se, ad esempio, [**SWbemDateTime. DaySpecified**](swbemdatetime-dayspecified.md) è **true**, [**SWbemDateTime. Value**](swbemdatetime-value.md) include il valore corrente di [**SWbemDateTime. Day**](swbemdatetime-day.md), in caso contrario è un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-199">For example, if [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) is **TRUE**, then [**SWbemDateTime.Value**](swbemdatetime-value.md) includes the current value of [**SWbemDateTime.Day**](swbemdatetime-day.md), otherwise it is a wildcard value.</span></span> <span data-ttu-id="8fe0c-200">La proprietà di [**intervallo**](swbemdatetime-isinterval.md) è **false** in entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-200">The [**IsInterval**](swbemdatetime-isinterval.md) property is **FALSE** in either case.</span></span>

## <a name="examples"></a><span data-ttu-id="8fe0c-201">Esempio</span><span class="sxs-lookup"><span data-stu-id="8fe0c-201">Examples</span></span>

<span data-ttu-id="8fe0c-202">Nell'esempio di codice di script seguente viene illustrato come utilizzare un oggetto **SWbemDateTime** per analizzare un valore della proprietà DateTime letto dal repository WMI, la proprietà **InstallDate** in [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="8fe0c-202">The following script code example shows how to use an **SWbemDateTime** object to parse a datetime property value read from the WMI repository, the **InstallDate** property in [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



<span data-ttu-id="8fe0c-203">Nell'esempio seguente viene illustrato come creare un oggetto **SWbemDateTime** , archiviare un valore di data nell'oggetto, visualizzare la data come ora locale e Coordinated Universal Time (UTC) e archiviare il valore in una classe e una proprietà appena create.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-203">The following example shows how to create an **SWbemDateTime** object, store a date value in the object, display the date as local and Coordinated Universal Time (UTC), and store the value in a newly created class and property.</span></span> <span data-ttu-id="8fe0c-204">Per ulteriori informazioni sulla costante **wbemCimtypeDatetime**, vedere [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="8fe0c-204">For more information about the constant **wbemCimtypeDatetime**, see [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



<span data-ttu-id="8fe0c-205">Nell'esempio di codice di script seguente viene illustrato come utilizzare un oggetto **SWbemDateTime** per modificare un valore di intervallo in una proprietà che viene letta dal repository WMI.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-205">The following script code example shows how to use an **SWbemDateTime** object to modify an interval value on a property that is read from the WMI repository.</span></span>


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



<span data-ttu-id="8fe0c-206">Nell'esempio di codice di script seguente viene illustrato come utilizzare un oggetto **SWbemDate** per leggere un valore **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="8fe0c-206">The following script code example shows how to use an **SWbemDate** object to read a **FILETIME** value.</span></span>


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



<span data-ttu-id="8fe0c-207">Il codice di PowerShell seguente crea un'istanza di un oggetto SWbemDateTime, recupera la data di installazione del sistema operativo e converte la data in un formato diverso</span><span class="sxs-lookup"><span data-stu-id="8fe0c-207">The following PowerShell code creates an instance of a SWbemDateTime object, retrieves the OS install date, and converts the date to a different format</span></span>


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



<span data-ttu-id="8fe0c-208">Il codice di PowerShell seguente converte il codice in un formato pronto per essere utilizzato da un provider CIM.</span><span class="sxs-lookup"><span data-stu-id="8fe0c-208">The following Powershell code translates the code into a format ready to be consumed by a CIM provider.</span></span>


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a><span data-ttu-id="8fe0c-209">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fe0c-209">Requirements</span></span>



| <span data-ttu-id="8fe0c-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fe0c-210">Requirement</span></span> | <span data-ttu-id="8fe0c-211">Valore</span><span class="sxs-lookup"><span data-stu-id="8fe0c-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe0c-212">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fe0c-212">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe0c-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fe0c-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fe0c-214">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fe0c-214">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe0c-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fe0c-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fe0c-216">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fe0c-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe0c-217"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe0c-217"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fe0c-218">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8fe0c-218">Type library</span></span><br/>             | <dl> <span data-ttu-id="8fe0c-219"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8fe0c-219"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8fe0c-220">DLL</span><span class="sxs-lookup"><span data-stu-id="8fe0c-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fe0c-221"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe0c-221"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8fe0c-222">CLSID</span><span class="sxs-lookup"><span data-stu-id="8fe0c-222">CLSID</span></span><br/>                    | <span data-ttu-id="8fe0c-223">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="8fe0c-223">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="8fe0c-224">IID</span><span class="sxs-lookup"><span data-stu-id="8fe0c-224">IID</span></span><br/>                      | <span data-ttu-id="8fe0c-225">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="8fe0c-225">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="8fe0c-226">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fe0c-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe0c-227">WbemCimtypeEnum</span><span class="sxs-lookup"><span data-stu-id="8fe0c-227">WbemCimtypeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[<span data-ttu-id="8fe0c-228">DATETIME</span><span class="sxs-lookup"><span data-stu-id="8fe0c-228">DATETIME</span></span>](datetime.md)
</dt> <dt>

[<span data-ttu-id="8fe0c-229">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="8fe0c-229">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

