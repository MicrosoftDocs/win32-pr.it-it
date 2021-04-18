---
description: Valore booleano che indica se il componente Year nel valore DateTime CIM contiene un intervallo o un valore jolly.
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. YearSpecified (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.YearSpecified
- ISWbemDateTime.YearSpecified
- ISWbemDateTime.get_YearSpecified
- ISWbemDateTime.put_YearSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3ad6ae5b120c2b38d7b6170951ef30b3b19f5295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309856"
---
# <a name="swbemdatetimeyearspecified-property"></a><span data-ttu-id="95182-103">Proprietà SWbemDateTime. YearSpecified</span><span class="sxs-lookup"><span data-stu-id="95182-103">SWbemDateTime.YearSpecified property</span></span>

<span data-ttu-id="95182-104">La proprietà **YearSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente Year nel valore DateTime CIM contiene un intervallo o un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="95182-104">The **YearSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the year component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="95182-105">Se **YearSpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. Year**](swbemdatetime-year.md) contiene un valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="95182-105">If **YearSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Year**](swbemdatetime-year.md) contains a datetime value.</span></span> <span data-ttu-id="95182-106">Un valore DateTime che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="95182-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="95182-107">Se **YearSpecified** è **false** e l' **intervallo** è **true**, **SWbemDateTime. Year** contiene un intervallo.</span><span class="sxs-lookup"><span data-stu-id="95182-107">If **YearSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Year** contains an interval.</span></span>

<span data-ttu-id="95182-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="95182-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="95182-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="95182-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="95182-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95182-110">Syntax</span></span>


```VB
SWbemDateTime.YearSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="95182-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="95182-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="95182-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="95182-112">Examples</span></span>

<span data-ttu-id="95182-113">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="95182-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="95182-114">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="95182-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95182-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95182-115">Requirements</span></span>



| <span data-ttu-id="95182-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="95182-116">Requirement</span></span> | <span data-ttu-id="95182-117">Valore</span><span class="sxs-lookup"><span data-stu-id="95182-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95182-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95182-118">Minimum supported client</span></span><br/> | <span data-ttu-id="95182-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95182-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95182-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95182-120">Minimum supported server</span></span><br/> | <span data-ttu-id="95182-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95182-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95182-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95182-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="95182-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95182-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="95182-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="95182-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="95182-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="95182-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="95182-126">DLL</span><span class="sxs-lookup"><span data-stu-id="95182-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95182-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95182-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="95182-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="95182-128">CLSID</span></span><br/>                    | <span data-ttu-id="95182-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="95182-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="95182-130">IID</span><span class="sxs-lookup"><span data-stu-id="95182-130">IID</span></span><br/>                      | <span data-ttu-id="95182-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="95182-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="95182-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95182-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95182-133">**SWbemDateTime. Year**</span><span class="sxs-lookup"><span data-stu-id="95182-133">**SWbemDateTime.Year**</span></span>](swbemdatetime-year.md)
</dt> <dt>

[<span data-ttu-id="95182-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="95182-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="95182-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="95182-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




