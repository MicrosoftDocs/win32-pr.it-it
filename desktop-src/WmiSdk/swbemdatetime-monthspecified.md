---
description: Valore booleano che indica se il componente month nel valore DateTime CIM contiene un intervallo o un valore jolly.
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. MonthSpecified (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MonthSpecified
- ISWbemDateTime.MonthSpecified
- ISWbemDateTime.get_MonthSpecified
- ISWbemDateTime.put_MonthSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 52b44444a5810577289353778c2c00b1ebfb80fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309860"
---
# <a name="swbemdatetimemonthspecified-property"></a><span data-ttu-id="d692a-103">Proprietà SWbemDateTime. MonthSpecified</span><span class="sxs-lookup"><span data-stu-id="d692a-103">SWbemDateTime.MonthSpecified property</span></span>

<span data-ttu-id="d692a-104">La proprietà **MonthSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente month nel valore DateTime CIM contiene un intervallo o un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="d692a-104">The **MonthSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the month component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="d692a-105">Se **MonthSpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. month**](swbemdatetime-month.md) contiene un valore date.</span><span class="sxs-lookup"><span data-stu-id="d692a-105">If **MonthSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Month**](swbemdatetime-month.md) contains a date value.</span></span> <span data-ttu-id="d692a-106">Un valore DateTime che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="d692a-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="d692a-107">Se **MonthSpecified** è **false** e l' **intervallo** è **true**, **SWbemDateTime. month** contiene un intervallo.</span><span class="sxs-lookup"><span data-stu-id="d692a-107">If **MonthSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Month** contains an interval.</span></span>

<span data-ttu-id="d692a-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d692a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d692a-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d692a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d692a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d692a-110">Syntax</span></span>


```VB
SWbemDateTime.MonthSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d692a-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d692a-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="d692a-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="d692a-112">Examples</span></span>

<span data-ttu-id="d692a-113">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="d692a-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="d692a-114">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="d692a-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d692a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d692a-115">Requirements</span></span>



| <span data-ttu-id="d692a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d692a-116">Requirement</span></span> | <span data-ttu-id="d692a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d692a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d692a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d692a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d692a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d692a-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d692a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d692a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d692a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d692a-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d692a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d692a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d692a-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d692a-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d692a-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d692a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="d692a-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d692a-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d692a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d692a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d692a-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d692a-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d692a-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="d692a-128">CLSID</span></span><br/>                    | <span data-ttu-id="d692a-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="d692a-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="d692a-130">IID</span><span class="sxs-lookup"><span data-stu-id="d692a-130">IID</span></span><br/>                      | <span data-ttu-id="d692a-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="d692a-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d692a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d692a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d692a-133">**SWbemDateTime. month**</span><span class="sxs-lookup"><span data-stu-id="d692a-133">**SWbemDateTime.Month**</span></span>](swbemdatetime-month.md)
</dt> <dt>

[<span data-ttu-id="d692a-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="d692a-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="d692a-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="d692a-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




