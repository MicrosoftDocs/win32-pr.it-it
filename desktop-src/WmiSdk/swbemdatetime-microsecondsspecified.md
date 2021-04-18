---
description: Valore booleano che indica se il componente microsecondi nel valore DateTime CIM contiene un intervallo o un valore jolly.
ms.assetid: 65244ece-2326-4edc-b982-57e2046ec33e
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. MicrosecondsSpecified (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.get_MicrosecondsSpecified
- ISWbemDateTime.put_MicrosecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d4fa9d99cf323e19ccd298786896f789bbb08be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309863"
---
# <a name="swbemdatetimemicrosecondsspecified-property"></a><span data-ttu-id="c1f89-103">Proprietà SWbemDateTime. MicrosecondsSpecified</span><span class="sxs-lookup"><span data-stu-id="c1f89-103">SWbemDateTime.MicrosecondsSpecified property</span></span>

<span data-ttu-id="c1f89-104">La proprietà **MicrosecondsSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente microsecondi nel valore DateTime CIM contiene un intervallo o un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="c1f89-104">The **MicrosecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the microseconds component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="c1f89-105">Se **MicrosecondsSpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. microsecondi**](swbemdatetime-microseconds.md) contiene un valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="c1f89-105">If **MicrosecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Microseconds**](swbemdatetime-microseconds.md) contains a datetime value.</span></span> <span data-ttu-id="c1f89-106">Un valore DateTime che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="c1f89-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="c1f89-107">Se [**HoursSpecified**](swbemdatetime-hoursspecified.md) è **false** e l' **intervallo** è **true**, **SWbemDateTime. microsecondi** contiene un intervallo.</span><span class="sxs-lookup"><span data-stu-id="c1f89-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Microseconds** contains an interval.</span></span>

<span data-ttu-id="c1f89-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c1f89-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c1f89-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c1f89-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1f89-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1f89-110">Syntax</span></span>


```VB
SWbemDateTime.MicrosecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c1f89-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c1f89-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="c1f89-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1f89-112">Examples</span></span>

<span data-ttu-id="c1f89-113">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="c1f89-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="c1f89-114">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="c1f89-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1f89-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1f89-115">Requirements</span></span>



| <span data-ttu-id="c1f89-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1f89-116">Requirement</span></span> | <span data-ttu-id="c1f89-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c1f89-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f89-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1f89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c1f89-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1f89-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1f89-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1f89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c1f89-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1f89-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1f89-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1f89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1f89-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1f89-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1f89-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c1f89-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1f89-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1f89-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1f89-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c1f89-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1f89-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1f89-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1f89-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="c1f89-128">CLSID</span></span><br/>                    | <span data-ttu-id="c1f89-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="c1f89-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="c1f89-130">IID</span><span class="sxs-lookup"><span data-stu-id="c1f89-130">IID</span></span><br/>                      | <span data-ttu-id="c1f89-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="c1f89-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c1f89-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1f89-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f89-133">**SWbemDateTime. microsecondi**</span><span class="sxs-lookup"><span data-stu-id="c1f89-133">**SWbemDateTime.Microseconds**</span></span>](swbemdatetime-microseconds.md)
</dt> <dt>

[<span data-ttu-id="c1f89-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="c1f89-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="c1f89-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="c1f89-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




