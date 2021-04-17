---
description: Converte un valore di data e ora nel formato DATETIME CIM nel formato FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Metodo SWbemDateTime. GetFileTime ha provocato (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485732"
---
# <a name="swbemdatetimegetfiletime-method"></a><span data-ttu-id="f37f2-103">SWbemDateTime. GetFileTime ha provocato, metodo</span><span class="sxs-lookup"><span data-stu-id="f37f2-103">SWbemDateTime.GetFileTime method</span></span>

<span data-ttu-id="f37f2-104">Il metodo **GetFileTime ha provocato** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte un valore di data e ora nel formato [DateTime](datetime.md) CIM nel formato FILETIME.</span><span class="sxs-lookup"><span data-stu-id="f37f2-104">The **GetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [DATETIME](datetime.md) format to the FILETIME format.</span></span>

<span data-ttu-id="f37f2-105">Se il parametro è impostato su **true**, il valore restituito rappresenta un'ora locale per il client.</span><span class="sxs-lookup"><span data-stu-id="f37f2-105">If the parameter is set to **TRUE**, then the return value represents a local time for the client.</span></span> <span data-ttu-id="f37f2-106">In caso contrario, il valore restituito è un'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="f37f2-106">Otherwise, the return value is a Coordinated Universal Time (UTC) time.</span></span> <span data-ttu-id="f37f2-107">Una struttura [DateTime](datetime.md) **FILETIME** è un valore a 64 bit che rappresenta il numero di unità 100-nanosecondi a partire dall'inizio del 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="f37f2-107">A **FILETIME** [DATETIME](datetime.md) structure is a 64-bit value that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="f37f2-108">Strumentazione gestione Windows (WMI) considera i valori **FILETIME** come rappresentazioni di stringa di numeri senza segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f37f2-108">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="f37f2-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f37f2-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f37f2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f37f2-110">Syntax</span></span>


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f37f2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f37f2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f37f2-112">*bIsLocaL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f37f2-112">*bIsLocaL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f2-113">Indica se il valore restituito viene interpretato come ora locale.</span><span class="sxs-lookup"><span data-stu-id="f37f2-113">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="f37f2-114">La proprietà UTC contiene quindi l'ora locale convertita nell'offset UTC (Coordinated Universal Time) corretto.</span><span class="sxs-lookup"><span data-stu-id="f37f2-114">The UTC property then contains the local time converted to the correct Coordinated Universal Times (UTC) offset.</span></span> <span data-ttu-id="f37f2-115">Se il valore è **false**, il valore viene interpretato come UTC con un offset zero (0).</span><span class="sxs-lookup"><span data-stu-id="f37f2-115">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f37f2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f37f2-116">Return value</span></span>

<span data-ttu-id="f37f2-117">Data e ora nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="f37f2-117">The date and time in the **FILETIME** format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f37f2-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f37f2-118">Error codes</span></span>

<span data-ttu-id="f37f2-119">Dopo aver completato il metodo **GetFileTime ha provocato** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="f37f2-119">After completing the **GetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f37f2-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f37f2-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f37f2-121">La chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f37f2-121">The call failed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f37f2-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f37f2-122">Remarks</span></span>

<span data-ttu-id="f37f2-123">**VT \_** I valori di data e **FILETIME** non possono contenere campi con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="f37f2-123">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="f37f2-124">Il metodo **GetFileTime ha provocato** ha esito negativo (wbemErrFailed) se una delle proprietà seguenti è **false**:</span><span class="sxs-lookup"><span data-stu-id="f37f2-124">The **GetFileTime** method fails (wbemErrFailed) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="f37f2-125">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="f37f2-125">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="f37f2-126">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="f37f2-126">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="f37f2-127">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="f37f2-127">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="f37f2-128">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="f37f2-128">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="f37f2-129">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="f37f2-129">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="f37f2-130">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="f37f2-130">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="f37f2-131">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="f37f2-131">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="f37f2-132">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="f37f2-132">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="f37f2-133">In seguito al corretto ritorno da [**SetFileTime**](swbemdatetime-setfiletime.md), tutte queste proprietà sono impostate su **true**.</span><span class="sxs-lookup"><span data-stu-id="f37f2-133">On a successful return from [**SetFileTime**](swbemdatetime-setfiletime.md), all of these properties are set to **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="f37f2-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="f37f2-134">Examples</span></span>

<span data-ttu-id="f37f2-135">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="f37f2-135">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="f37f2-136">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="f37f2-136">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f37f2-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f37f2-137">Requirements</span></span>



| <span data-ttu-id="f37f2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f37f2-138">Requirement</span></span> | <span data-ttu-id="f37f2-139">Valore</span><span class="sxs-lookup"><span data-stu-id="f37f2-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f37f2-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f37f2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f37f2-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f37f2-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f37f2-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f37f2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f37f2-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f37f2-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f37f2-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f37f2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f37f2-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f37f2-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f37f2-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f37f2-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="f37f2-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f37f2-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f37f2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f37f2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f37f2-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f37f2-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f37f2-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="f37f2-150">CLSID</span></span><br/>                    | <span data-ttu-id="f37f2-151">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="f37f2-151">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="f37f2-152">IID</span><span class="sxs-lookup"><span data-stu-id="f37f2-152">IID</span></span><br/>                      | <span data-ttu-id="f37f2-153">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="f37f2-153">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f37f2-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f37f2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f37f2-155">**SWbemDateTime. GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="f37f2-155">**SWbemDateTime.GetVarDate**</span></span>](swbemdatetime-getvardate.md)
</dt> <dt>

[<span data-ttu-id="f37f2-156">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="f37f2-156">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="f37f2-157">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="f37f2-157">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

