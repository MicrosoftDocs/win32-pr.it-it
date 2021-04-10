---
description: Indica se il componente minuti nel valore DateTime CIM contiene un intervallo o un valore jolly.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. MinutesSpecified (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130995"
---
# <a name="swbemdatetimeminutesspecified-property"></a><span data-ttu-id="16dda-103">Proprietà SWbemDateTime. MinutesSpecified</span><span class="sxs-lookup"><span data-stu-id="16dda-103">SWbemDateTime.MinutesSpecified property</span></span>

<span data-ttu-id="16dda-104">La proprietà **MinutesSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente minuti nel valore DateTime CIM contiene un intervallo o un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="16dda-104">The **MinutesSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the minutes component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="16dda-105">Se **MinutesSpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false** (che indica che il valore DateTime CIM non ha caratteri jolly), [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) contiene un valore date.</span><span class="sxs-lookup"><span data-stu-id="16dda-105">If **MinutesSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE** (indicating that the CIM datetime value has no wildcards), then [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) contains a date value.</span></span> <span data-ttu-id="16dda-106">Un valore DateTime che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="16dda-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="16dda-107">Se [**HoursSpecified**](swbemdatetime-hoursspecified.md) è **false** e l' **intervallo** è **true**, **SWbemDateTime. minutes** contiene un intervallo.</span><span class="sxs-lookup"><span data-stu-id="16dda-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Minutes** contains an interval.</span></span>

<span data-ttu-id="16dda-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="16dda-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="16dda-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="16dda-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="16dda-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16dda-110">Syntax</span></span>


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a><span data-ttu-id="16dda-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="16dda-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="16dda-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="16dda-112">Examples</span></span>

<span data-ttu-id="16dda-113">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="16dda-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="16dda-114">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="16dda-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16dda-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16dda-115">Requirements</span></span>



| <span data-ttu-id="16dda-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="16dda-116">Requirement</span></span> | <span data-ttu-id="16dda-117">Valore</span><span class="sxs-lookup"><span data-stu-id="16dda-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16dda-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16dda-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16dda-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16dda-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16dda-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16dda-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16dda-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16dda-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16dda-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16dda-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="16dda-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="16dda-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="16dda-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="16dda-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="16dda-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="16dda-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="16dda-126">DLL</span><span class="sxs-lookup"><span data-stu-id="16dda-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16dda-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16dda-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="16dda-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="16dda-128">CLSID</span></span><br/>                    | <span data-ttu-id="16dda-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="16dda-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="16dda-130">IID</span><span class="sxs-lookup"><span data-stu-id="16dda-130">IID</span></span><br/>                      | <span data-ttu-id="16dda-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="16dda-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="16dda-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16dda-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16dda-133">**SWbemDateTime. minuti**</span><span class="sxs-lookup"><span data-stu-id="16dda-133">**SWbemDateTime.Minutes**</span></span>](swbemdatetime-minutes.md)
</dt> <dt>

[<span data-ttu-id="16dda-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="16dda-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="16dda-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="16dda-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




