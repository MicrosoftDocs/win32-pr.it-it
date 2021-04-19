---
description: La proprietà HoursSpecified dell'oggetto SWbemDateTime è un valore booleano che indica se il componente hours nel valore DateTime CIM contiene un intervallo o un valore jolly.
ms.assetid: 55211da6-cbd5-4e61-ab7d-ee20363e9d81
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. HoursSpecified (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.HoursSpecified
- ISWbemDateTime.HoursSpecified
- ISWbemDateTime.get_HoursSpecified
- ISWbemDateTime.put_HoursSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e092747768035b7948ddef66f4c4d542bfa2c38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309868"
---
# <a name="swbemdatetimehoursspecified-property"></a><span data-ttu-id="9b69f-103">Proprietà SWbemDateTime. HoursSpecified</span><span class="sxs-lookup"><span data-stu-id="9b69f-103">SWbemDateTime.HoursSpecified property</span></span>

<span data-ttu-id="9b69f-104">La proprietà **HoursSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente hours nel valore DateTime CIM contiene un intervallo o un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="9b69f-104">The **HoursSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the hours component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="9b69f-105">Se **HoursSpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. hours**](swbemdatetime-hours.md) contiene un valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="9b69f-105">If **HoursSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Hours**](swbemdatetime-hours.md) contains a datetime value.</span></span> <span data-ttu-id="9b69f-106">Un valore DateTime che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="9b69f-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="9b69f-107">Se **HoursSpecified** è **false** e l' **intervallo** è **true**, **SWbemDateTime. hours** contiene un intervallo.</span><span class="sxs-lookup"><span data-stu-id="9b69f-107">If **HoursSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Hours** contains an interval.</span></span>

<span data-ttu-id="9b69f-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9b69f-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="9b69f-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9b69f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b69f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b69f-110">Syntax</span></span>


```VB
SWbemDateTime.HoursSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9b69f-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9b69f-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="9b69f-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="9b69f-112">Examples</span></span>

<span data-ttu-id="9b69f-113">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="9b69f-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="9b69f-114">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="9b69f-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b69f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b69f-115">Requirements</span></span>



| <span data-ttu-id="9b69f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b69f-116">Requirement</span></span> | <span data-ttu-id="9b69f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9b69f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b69f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b69f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9b69f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b69f-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b69f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b69f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9b69f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b69f-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b69f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b69f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b69f-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b69f-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b69f-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9b69f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b69f-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b69f-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b69f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9b69f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b69f-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b69f-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b69f-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="9b69f-128">CLSID</span></span><br/>                    | <span data-ttu-id="9b69f-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="9b69f-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="9b69f-130">IID</span><span class="sxs-lookup"><span data-stu-id="9b69f-130">IID</span></span><br/>                      | <span data-ttu-id="9b69f-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="9b69f-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9b69f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b69f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b69f-133">**SWbemDateTime. hours**</span><span class="sxs-lookup"><span data-stu-id="9b69f-133">**SWbemDateTime.Hours**</span></span>](swbemdatetime-hours.md)
</dt> <dt>

[<span data-ttu-id="9b69f-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="9b69f-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="9b69f-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="9b69f-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




