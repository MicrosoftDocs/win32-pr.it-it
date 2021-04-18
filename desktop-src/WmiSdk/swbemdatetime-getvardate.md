---
description: Converte un valore di data e ora nel formato DATETIME CIM nel formato di \_ Data VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Metodo SWbemDateTime. GetVarDate (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309869"
---
# <a name="swbemdatetimegetvardate-method"></a><span data-ttu-id="00a55-103">SWbemDateTime. GetVarDate, metodo</span><span class="sxs-lookup"><span data-stu-id="00a55-103">SWbemDateTime.GetVarDate method</span></span>

<span data-ttu-id="00a55-104">Il metodo **getVarDate** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte un valore di data e ora nel formato [**DateTime**](datetime.md) CIM nel formato **\_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="00a55-104">The **GetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [**DATETIME**](datetime.md) format to the **VT\_DATE** format.</span></span>

<span data-ttu-id="00a55-105">Il formato della **\_ Data VT** è un valore [**DateTime**](datetime.md) della variante di automazione che Visual Basic e ActiveX usano.</span><span class="sxs-lookup"><span data-stu-id="00a55-105">The **VT\_DATE** format is an automation variant [**DATETIME**](datetime.md) value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="00a55-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="00a55-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="00a55-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00a55-107">Syntax</span></span>


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="00a55-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="00a55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a55-109">*bIsLocal* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="00a55-109">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="00a55-110">Indica se il valore restituito viene interpretato come ora locale.</span><span class="sxs-lookup"><span data-stu-id="00a55-110">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="00a55-111">La proprietà UTC (Coordinated Universal Time) contiene l'ora locale convertita nell'offset UTC corretto.</span><span class="sxs-lookup"><span data-stu-id="00a55-111">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="00a55-112">Se il valore è **false**, il valore viene interpretato come UTC con un offset zero (0).</span><span class="sxs-lookup"><span data-stu-id="00a55-112">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a55-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00a55-113">Return value</span></span>

<span data-ttu-id="00a55-114">Valore di data e ora nel formato **di \_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="00a55-114">The date and time value in the **VT\_DATE** format.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a55-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="00a55-115">Remarks</span></span>

<span data-ttu-id="00a55-116">**VT \_** I valori di data e **FILETIME** non possono contenere campi con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="00a55-116">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="00a55-117">Il metodo **getVarDate** ha esito negativo (**wbemErrFailed**) se una delle proprietà seguenti è **false**:</span><span class="sxs-lookup"><span data-stu-id="00a55-117">The **GetVarDate** method fails (**wbemErrFailed**) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="00a55-118">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="00a55-118">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="00a55-119">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="00a55-119">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="00a55-120">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="00a55-120">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="00a55-121">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="00a55-121">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="00a55-122">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="00a55-122">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="00a55-123">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="00a55-123">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="00a55-124">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="00a55-124">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="00a55-125">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="00a55-125">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="00a55-126">In seguito all'esito positivo della restituzione da [**SetVarDate**](swbemdatetime-setvardate.md), tutte queste proprietà vengono impostate su **true**.</span><span class="sxs-lookup"><span data-stu-id="00a55-126">On successful return from [**SetVarDate**](swbemdatetime-setvardate.md), all of these properties are set to **TRUE**.</span></span>

<span data-ttu-id="00a55-127">Al termine di una chiamata a [**SetVarDate**](swbemdatetime-setvardate.md), il valore [**DateTime**](datetime.md) viene sempre interpretato come valore **DateTime** assoluto anziché come intervallo e l' [**intervallo**](swbemdatetime-isinterval.md) è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="00a55-127">After a successful call to [**SetVarDate**](swbemdatetime-setvardate.md), the [**DATETIME**](datetime.md) value is always interpreted as an absolute **DATETIME** value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

<span data-ttu-id="00a55-128">Se l' [**intervallo**](swbemdatetime-isinterval.md) è impostato su **true**, una chiamata a **getVarDate** genera l'errore **wbemErrFailed** .</span><span class="sxs-lookup"><span data-stu-id="00a55-128">If [**IsInterval**](swbemdatetime-isinterval.md) is set to **TRUE**, then a call to **GetVarDate** results in the **wbemErrFailed** error.</span></span>

<span data-ttu-id="00a55-129">Quando si chiama **getVarDate**, si verifica una perdita di precisione, perché i valori [DateTime](datetime.md) hanno una risoluzione di un microsecondo (s) e i valori di **\_ data VT** hanno una risoluzione di 500 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="00a55-129">Some loss of precision occurs when you call **GetVarDate**, because [datetime](datetime.md) values have a one microsecond ( s) resolution, and **VT\_DATE** values have a 500 millisecond resolution.</span></span>

## <a name="examples"></a><span data-ttu-id="00a55-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="00a55-130">Examples</span></span>

<span data-ttu-id="00a55-131">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e da **FILETIME** o dal formato **di \_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="00a55-131">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="00a55-132">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="00a55-132">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00a55-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00a55-133">Requirements</span></span>



| <span data-ttu-id="00a55-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a55-134">Requirement</span></span> | <span data-ttu-id="00a55-135">Valore</span><span class="sxs-lookup"><span data-stu-id="00a55-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00a55-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a55-136">Minimum supported client</span></span><br/> | <span data-ttu-id="00a55-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00a55-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00a55-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a55-138">Minimum supported server</span></span><br/> | <span data-ttu-id="00a55-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00a55-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00a55-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00a55-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a55-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a55-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="00a55-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="00a55-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="00a55-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="00a55-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="00a55-144">DLL</span><span class="sxs-lookup"><span data-stu-id="00a55-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00a55-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00a55-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="00a55-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="00a55-146">CLSID</span></span><br/>                    | <span data-ttu-id="00a55-147">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="00a55-147">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="00a55-148">IID</span><span class="sxs-lookup"><span data-stu-id="00a55-148">IID</span></span><br/>                      | <span data-ttu-id="00a55-149">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="00a55-149">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="00a55-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00a55-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a55-151">**SWbemDateTime. GetFileTime ha provocato**</span><span class="sxs-lookup"><span data-stu-id="00a55-151">**SWbemDateTime.GetFileTime**</span></span>](swbemdatetime-getfiletime.md)
</dt> <dt>

[<span data-ttu-id="00a55-152">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="00a55-152">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="00a55-153">DATETIME</span><span class="sxs-lookup"><span data-stu-id="00a55-153">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




