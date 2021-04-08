---
description: Ottiene o imposta un valore che rappresenta il componente giorno del valore DateTime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. Day (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968363"
---
# <a name="swbemdatetimeday-property"></a><span data-ttu-id="7ba10-103">Proprietà SWbemDateTime. Day</span><span class="sxs-lookup"><span data-stu-id="7ba10-103">SWbemDateTime.Day property</span></span>

<span data-ttu-id="7ba10-104">La proprietà **Day** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta un valore che rappresenta il componente giorno del valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="7ba10-104">The **Day** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the day component of the datetime value.</span></span> <span data-ttu-id="7ba10-105">Se l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, il valore deve essere compreso tra 1 e 31.</span><span class="sxs-lookup"><span data-stu-id="7ba10-105">The value must be in the range of 1 through 31 if [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**.</span></span> <span data-ttu-id="7ba10-106">Tuttavia, il controllo degli errori non è sensibile al valore del mese.</span><span class="sxs-lookup"><span data-stu-id="7ba10-106">However, error checking is not sensitive to the month value.</span></span> <span data-ttu-id="7ba10-107">Pertanto, il valore compreso nell'intervallo 31 non restituirà un errore nei casi in cui il valore [**SWbemDateTime. month**](swbemdatetime-month.md) è per un mese di meno di 31 giorni (febbraio, aprile, giugno, settembre, novembre).</span><span class="sxs-lookup"><span data-stu-id="7ba10-107">Thus, the in-range value of 31 will not return an error in the cases where the [**SWbemDateTime.Month**](swbemdatetime-month.md) value is for a month of fewer than 31 days (February, April, June, September, November).</span></span>

<span data-ttu-id="7ba10-108">Il valore predefinito per **Day** è 01.</span><span class="sxs-lookup"><span data-stu-id="7ba10-108">The default value for **Day** is 01.</span></span>

<span data-ttu-id="7ba10-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7ba10-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="7ba10-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7ba10-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba10-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ba10-111">Syntax</span></span>


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a><span data-ttu-id="7ba10-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7ba10-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="7ba10-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7ba10-113">Error codes</span></span>

<span data-ttu-id="7ba10-114">Dopo avere ottenuto o impostato la proprietà **Day** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="7ba10-114">After you get or set the **Day** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="7ba10-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="7ba10-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="7ba10-116">Se l' [**intervallo**](swbemdatetime-isinterval.md) è **true** e l'intervallo di valori corretti supera 0 e 99999999.</span><span class="sxs-lookup"><span data-stu-id="7ba10-116">If [**IsInterval**](swbemdatetime-isinterval.md) is **TRUE** and the range of correct values exceeds 0 through 99999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7ba10-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="7ba10-117">Examples</span></span>

<span data-ttu-id="7ba10-118">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="7ba10-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="7ba10-119">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="7ba10-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba10-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ba10-120">Requirements</span></span>



| <span data-ttu-id="7ba10-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ba10-121">Requirement</span></span> | <span data-ttu-id="7ba10-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7ba10-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba10-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ba10-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba10-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ba10-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ba10-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ba10-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba10-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ba10-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ba10-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ba10-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ba10-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ba10-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ba10-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7ba10-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ba10-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7ba10-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7ba10-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7ba10-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ba10-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ba10-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ba10-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="7ba10-133">CLSID</span></span><br/>                    | <span data-ttu-id="7ba10-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="7ba10-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="7ba10-135">IID</span><span class="sxs-lookup"><span data-stu-id="7ba10-135">IID</span></span><br/>                      | <span data-ttu-id="7ba10-136">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="7ba10-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7ba10-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ba10-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba10-138">**SWbemDateTime. DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="7ba10-138">**SWbemDateTime.DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
</dt> <dt>

[<span data-ttu-id="7ba10-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="7ba10-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="7ba10-140">DATETIME</span><span class="sxs-lookup"><span data-stu-id="7ba10-140">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

