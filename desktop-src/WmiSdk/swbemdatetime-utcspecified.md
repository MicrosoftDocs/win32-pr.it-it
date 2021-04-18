---
description: Valore booleano che indica se il componente UTC (Universal Coordinated Time) nel valore DateTime CIM contiene un intervallo o un valore jolly.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. UTCSpecified (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314571"
---
# <a name="swbemdatetimeutcspecified-property"></a><span data-ttu-id="8b62e-103">Proprietà SWbemDateTime. UTCSpecified</span><span class="sxs-lookup"><span data-stu-id="8b62e-103">SWbemDateTime.UTCSpecified property</span></span>

<span data-ttu-id="8b62e-104">La proprietà **UTCSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente UTC (Universal Coordinated Time) nel valore DateTime CIM contiene un intervallo o un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="8b62e-104">The **UTCSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="8b62e-105">Se **UTCSpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. UTC**](swbemdatetime-utc.md) contiene un valore [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="8b62e-105">If **UTCSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contains a [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="8b62e-106">Un valore **DateTime** che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="8b62e-106">A **DATETIME** value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="8b62e-107">Se **UTCSpecified** è **false** e l' **intervallo** è **true**, **SWbemDateTime. UTC** contiene un intervallo.</span><span class="sxs-lookup"><span data-stu-id="8b62e-107">If **UTCSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.UTC** contains an interval.</span></span>

<span data-ttu-id="8b62e-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8b62e-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="8b62e-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8b62e-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b62e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b62e-110">Syntax</span></span>


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8b62e-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8b62e-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="8b62e-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="8b62e-112">Examples</span></span>

<span data-ttu-id="8b62e-113">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="8b62e-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="8b62e-114">Per una descrizione del formato DateTime CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="8b62e-114">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b62e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b62e-115">Requirements</span></span>



| <span data-ttu-id="8b62e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b62e-116">Requirement</span></span> | <span data-ttu-id="8b62e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8b62e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b62e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b62e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8b62e-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b62e-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b62e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b62e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8b62e-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b62e-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b62e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b62e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b62e-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b62e-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b62e-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8b62e-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b62e-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b62e-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b62e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8b62e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b62e-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b62e-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b62e-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="8b62e-128">CLSID</span></span><br/>                    | <span data-ttu-id="8b62e-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="8b62e-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="8b62e-130">IID</span><span class="sxs-lookup"><span data-stu-id="8b62e-130">IID</span></span><br/>                      | <span data-ttu-id="8b62e-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="8b62e-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="8b62e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b62e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b62e-133">**SWbemDateTime. UTC**</span><span class="sxs-lookup"><span data-stu-id="8b62e-133">**SWbemDateTime.UTC**</span></span>](swbemdatetime-utc.md)
</dt> <dt>

[<span data-ttu-id="8b62e-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="8b62e-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="8b62e-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="8b62e-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




