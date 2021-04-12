---
description: Converte una data nel formato della stringa FILETIME nel formato DateTime CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Metodo SWbemDateTime. SetFileTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130994"
---
# <a name="swbemdatetimesetfiletime-method"></a><span data-ttu-id="e87ad-103">SWbemDateTime. SetFileTime, metodo</span><span class="sxs-lookup"><span data-stu-id="e87ad-103">SWbemDateTime.SetFileTime method</span></span>

<span data-ttu-id="e87ad-104">Il metodo **SetFileTime** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte una data nel formato della stringa **FILETIME** nel formato [DateTime CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="e87ad-104">The **SetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the string **FILETIME** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="e87ad-105">Il formato **FILETIME** è una struttura datetime a 64 bit che rappresenta il numero di unità 100-nanosecondi a partire dall'inizio del 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="e87ad-105">The **FILETIME** format is a 64-bit datetime structure that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="e87ad-106">Strumentazione gestione Windows (WMI) considera i valori **FILETIME** come rappresentazioni di stringa di numeri senza segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e87ad-106">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="e87ad-107">Per la spiegazione della sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e87ad-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e87ad-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e87ad-108">Syntax</span></span>


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e87ad-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e87ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e87ad-110">*strFileTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e87ad-110">*strFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e87ad-111">Valore **FILETIME** utilizzato per impostare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e87ad-111">**FILETIME** value used to set the object.</span></span>

</dd> <dt>

<span data-ttu-id="e87ad-112">*bIsLocal* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e87ad-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e87ad-113">Se è **true**, *strFileTime* viene interpretato come ora locale.</span><span class="sxs-lookup"><span data-stu-id="e87ad-113">If **TRUE**, *strFileTime* is interpreted as a local time.</span></span> <span data-ttu-id="e87ad-114">La proprietà UTC (Coordinated Universal Time) contiene l'ora locale convertita nell'offset UTC corretto.</span><span class="sxs-lookup"><span data-stu-id="e87ad-114">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="e87ad-115">Quando *bIsLocal* è **false**, *strFileTime* viene convertito direttamente in un valore UTC con un offset di 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e87ad-115">When *bIsLocal* is **FALSE**, then *strFileTime* is converted directly into a UTC value with an offset of 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e87ad-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e87ad-116">Return value</span></span>

<span data-ttu-id="e87ad-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e87ad-117">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e87ad-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e87ad-118">Error codes</span></span>

<span data-ttu-id="e87ad-119">Dopo aver completato il metodo **SetFileTime** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="e87ad-119">After completing the **SetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e87ad-120">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="e87ad-120">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="e87ad-121">Il formato di *strFileTime* non è valido.</span><span class="sxs-lookup"><span data-stu-id="e87ad-121">The format of *strFileTime* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e87ad-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e87ad-122">Remarks</span></span>

<span data-ttu-id="e87ad-123">Al termine di una chiamata a **SetFileTime**, il valore [**DateTime**](datetime.md) viene sempre interpretato come valore assoluto (**DateTime**) e l' [**intervallo**](swbemdatetime-isinterval.md) è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="e87ad-123">After a successful call to **SetFileTime**, the [**datetime**](datetime.md) value is always interpreted as an absolute (**datetime**) value, and [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="e87ad-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="e87ad-124">Examples</span></span>

<span data-ttu-id="e87ad-125">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="e87ad-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="e87ad-126">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="e87ad-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e87ad-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e87ad-127">Requirements</span></span>



| <span data-ttu-id="e87ad-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e87ad-128">Requirement</span></span> | <span data-ttu-id="e87ad-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e87ad-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ad-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e87ad-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e87ad-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e87ad-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e87ad-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e87ad-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e87ad-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e87ad-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e87ad-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e87ad-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e87ad-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e87ad-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e87ad-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e87ad-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="e87ad-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e87ad-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e87ad-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e87ad-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e87ad-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e87ad-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e87ad-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="e87ad-140">CLSID</span></span><br/>                    | <span data-ttu-id="e87ad-141">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="e87ad-141">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="e87ad-142">IID</span><span class="sxs-lookup"><span data-stu-id="e87ad-142">IID</span></span><br/>                      | <span data-ttu-id="e87ad-143">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="e87ad-143">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="e87ad-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e87ad-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e87ad-145">**SWbemDateTime. SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="e87ad-145">**SWbemDateTime.SetVarDate**</span></span>](swbemdatetime-setvardate.md)
</dt> <dt>

[<span data-ttu-id="e87ad-146">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="e87ad-146">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="e87ad-147">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="e87ad-147">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

