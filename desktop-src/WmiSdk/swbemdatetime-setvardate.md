---
description: Converte una data nel \_ formato di data VT nel formato DateTime CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Metodo SWbemDateTime. SetVarDate (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348886"
---
# <a name="swbemdatetimesetvardate-method"></a><span data-ttu-id="a42ba-103">SWbemDateTime. SetVarDate, metodo</span><span class="sxs-lookup"><span data-stu-id="a42ba-103">SWbemDateTime.SetVarDate method</span></span>

<span data-ttu-id="a42ba-104">Il metodo **SetVarDate** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte una data nel formato di **\_ Data VT** nel formato [DateTime CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="a42ba-104">The **SetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the **VT\_DATE** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="a42ba-105">Un valore di **\_ Data VT** è un valore datetime Variant che Visual Basic e ActiveX usano.</span><span class="sxs-lookup"><span data-stu-id="a42ba-105">A **VT\_DATE** value is a variant datetime value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="a42ba-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a42ba-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a42ba-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a42ba-107">Syntax</span></span>


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a42ba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a42ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a42ba-109">*Vdate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a42ba-109">*vdate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a42ba-110">Valore della data Variant per l'impostazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a42ba-110">The variant date value to set the object.</span></span> <span data-ttu-id="a42ba-111">Questo parametro deve essere nel formato **di \_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="a42ba-111">This parameter must be in the **VT\_DATE** format.</span></span>

</dd> <dt>

<span data-ttu-id="a42ba-112">*bIsLocal* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a42ba-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a42ba-113">Se è **true**, *Vdate* viene interpretato come ora locale e la proprietà UTC (Coordinated Universal Time) contiene l'ora locale convertita nell'offset UTC corretto.</span><span class="sxs-lookup"><span data-stu-id="a42ba-113">If **TRUE**, *vdate* is interpreted as a local time, and the Coordinated Universal Time (UTC) property contains the local time that is converted to the correct UTC offset.</span></span> <span data-ttu-id="a42ba-114">Quando *bIsLocal* è **false**, *Vdate* viene convertito direttamente in un valore UTC con un offset pari a zero (0).</span><span class="sxs-lookup"><span data-stu-id="a42ba-114">When *bIsLocal* is **FALSE**, then *vdate* is converted directly into a UTC value with an offset of zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a42ba-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a42ba-115">Return value</span></span>

<span data-ttu-id="a42ba-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a42ba-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a42ba-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a42ba-117">Error codes</span></span>

<span data-ttu-id="a42ba-118">Dopo aver completato il metodo **SetVarDate** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="a42ba-118">After completing the **SetVarDate** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a42ba-119">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="a42ba-119">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="a42ba-120">Il formato di *Vdate* non è valido.</span><span class="sxs-lookup"><span data-stu-id="a42ba-120">The format of *vdate* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a42ba-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a42ba-121">Remarks</span></span>

<span data-ttu-id="a42ba-122">Dopo una chiamata a **SetVarDate**, il valore [**DateTime**](datetime.md) viene interpretato come valore DateTime assoluto anziché come intervallo e la proprietà di [**intervallo**](swbemdatetime-isinterval.md) è impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="a42ba-122">After a successful call to **SetVarDate**, the [**DATETIME**](datetime.md) value is interpreted as an absolute datetime value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span>

<span data-ttu-id="a42ba-123">La funzione intrinseca Visual Basic o VBScript [CDate](/previous-versions//2dt118h2(v=vs.85)) fornisce un valore [**DateTime**](datetime.md) nel formato di **\_ Data VT** per l'input in **SetVarDate**.</span><span class="sxs-lookup"><span data-stu-id="a42ba-123">The intrinsic Visual Basic or VBScript function [CDate](/previous-versions//2dt118h2(v=vs.85)) provides a [**datetime**](datetime.md) value in the **VT\_DATE** format for input to **SetVarDate**.</span></span>

## <a name="examples"></a><span data-ttu-id="a42ba-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="a42ba-124">Examples</span></span>

<span data-ttu-id="a42ba-125">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="a42ba-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="a42ba-126">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="a42ba-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="a42ba-127">L'esempio di codice [Convert date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript della raccolta TechNet USA SetVarDate per convertire un valore di data e ora normale nel formato di data e ora UTC.</span><span class="sxs-lookup"><span data-stu-id="a42ba-127">The [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript code sample in the TechNet Gallery uses SetVarDate to convert a regular date-time value into the UTC date-time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="a42ba-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a42ba-128">Requirements</span></span>



| <span data-ttu-id="a42ba-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a42ba-129">Requirement</span></span> | <span data-ttu-id="a42ba-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a42ba-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a42ba-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a42ba-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a42ba-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a42ba-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a42ba-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a42ba-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a42ba-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a42ba-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a42ba-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a42ba-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a42ba-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a42ba-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a42ba-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a42ba-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a42ba-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a42ba-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a42ba-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a42ba-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a42ba-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a42ba-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a42ba-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="a42ba-141">CLSID</span></span><br/>                    | <span data-ttu-id="a42ba-142">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="a42ba-142">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="a42ba-143">IID</span><span class="sxs-lookup"><span data-stu-id="a42ba-143">IID</span></span><br/>                      | <span data-ttu-id="a42ba-144">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="a42ba-144">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a42ba-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a42ba-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a42ba-146">**SWbemDateTime. SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="a42ba-146">**SWbemDateTime.SetFileTime**</span></span>](swbemdatetime-setfiletime.md)
</dt> <dt>

[<span data-ttu-id="a42ba-147">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="a42ba-147">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="a42ba-148">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="a42ba-148">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

