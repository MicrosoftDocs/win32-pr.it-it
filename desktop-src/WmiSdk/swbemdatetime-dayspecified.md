---
description: Valore booleano che indica se il componente relativo al giorno nel valore DATETIME CIM contiene un intervallo o un valore jolly.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. DaySpecified (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309871"
---
# <a name="swbemdatetimedayspecified-property"></a><span data-ttu-id="1859d-103">Proprietà SWbemDateTime. DaySpecified</span><span class="sxs-lookup"><span data-stu-id="1859d-103">SWbemDateTime.DaySpecified property</span></span>

<span data-ttu-id="1859d-104">La proprietà **DaySpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente relativo al giorno nel valore [**DateTime**](datetime.md) CIM contiene un intervallo o un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="1859d-104">The **DaySpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the day component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="1859d-105">Se **DaySpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. Day**](swbemdatetime-day.md) contiene un valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="1859d-105">If **DaySpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Day**](swbemdatetime-day.md) contains a datetime value.</span></span> <span data-ttu-id="1859d-106">Un valore [**DateTime**](datetime.md) che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="1859d-106">A [**DATETIME**](datetime.md) value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="1859d-107">Se **DaySpecified** è **false** e l' **intervallo** è **true**, **SWbemDateTime. Day** contiene un intervallo.</span><span class="sxs-lookup"><span data-stu-id="1859d-107">If **DaySpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Day** contains an interval.</span></span>

<span data-ttu-id="1859d-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1859d-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="1859d-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1859d-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1859d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1859d-110">Syntax</span></span>


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="1859d-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1859d-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="1859d-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="1859d-112">Examples</span></span>

<span data-ttu-id="1859d-113">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="1859d-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="1859d-114">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="1859d-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1859d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1859d-115">Requirements</span></span>



| <span data-ttu-id="1859d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1859d-116">Requirement</span></span> | <span data-ttu-id="1859d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1859d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1859d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1859d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1859d-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1859d-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1859d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1859d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1859d-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1859d-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1859d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1859d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1859d-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1859d-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1859d-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1859d-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="1859d-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1859d-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1859d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1859d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1859d-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1859d-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1859d-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="1859d-128">CLSID</span></span><br/>                    | <span data-ttu-id="1859d-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="1859d-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="1859d-130">IID</span><span class="sxs-lookup"><span data-stu-id="1859d-130">IID</span></span><br/>                      | <span data-ttu-id="1859d-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="1859d-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="1859d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1859d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1859d-133">**SWbemDateTime. giorno**</span><span class="sxs-lookup"><span data-stu-id="1859d-133">**SWbemDateTime.Day**</span></span>](swbemdatetime-day.md)
</dt> <dt>

[<span data-ttu-id="1859d-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="1859d-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="1859d-135">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="1859d-135">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




