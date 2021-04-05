---
description: Valore booleano che indica se il componente secondi nel valore DATETIME CIM contiene un intervallo o un valore jolly.
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. SecondsSpecified (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SecondsSpecified
- ISWbemDateTime.SecondsSpecified
- ISWbemDateTime.get_SecondsSpecified
- ISWbemDateTime.put_SecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0cf97eff544d6e244890014108506f39b1934b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885033"
---
# <a name="swbemdatetimesecondsspecified-property"></a><span data-ttu-id="fcd82-103">Proprietà SWbemDateTime. SecondsSpecified</span><span class="sxs-lookup"><span data-stu-id="fcd82-103">SWbemDateTime.SecondsSpecified property</span></span>

<span data-ttu-id="fcd82-104">La proprietà **SecondsSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente secondi nel valore [**DateTime**](datetime.md) CIM contiene un intervallo o un valore jolly.</span><span class="sxs-lookup"><span data-stu-id="fcd82-104">The **SecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the seconds component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="fcd82-105">Se **SecondsSpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. seconds**](swbemdatetime-seconds.md) contiene un valore di data.</span><span class="sxs-lookup"><span data-stu-id="fcd82-105">If **SecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contains a date value.</span></span> <span data-ttu-id="fcd82-106">Un valore DateTime che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="fcd82-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="fcd82-107">Se **SecondsSpecified** è **false** e l' **intervallo** è **true**, **SWbemDateTime. seconds** contiene un intervallo.</span><span class="sxs-lookup"><span data-stu-id="fcd82-107">If **SecondsSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Seconds** contains an interval.</span></span>

<span data-ttu-id="fcd82-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fcd82-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="fcd82-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fcd82-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd82-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fcd82-110">Syntax</span></span>


```VB
SWbemDateTime.SecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="fcd82-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fcd82-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="fcd82-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="fcd82-112">Examples</span></span>

<span data-ttu-id="fcd82-113">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="fcd82-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="fcd82-114">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="fcd82-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd82-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcd82-115">Requirements</span></span>



| <span data-ttu-id="fcd82-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcd82-116">Requirement</span></span> | <span data-ttu-id="fcd82-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fcd82-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd82-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcd82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd82-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fcd82-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fcd82-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcd82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd82-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcd82-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fcd82-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fcd82-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcd82-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcd82-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcd82-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fcd82-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="fcd82-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fcd82-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fcd82-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fcd82-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcd82-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcd82-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fcd82-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="fcd82-128">CLSID</span></span><br/>                    | <span data-ttu-id="fcd82-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="fcd82-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="fcd82-130">IID</span><span class="sxs-lookup"><span data-stu-id="fcd82-130">IID</span></span><br/>                      | <span data-ttu-id="fcd82-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="fcd82-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="fcd82-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcd82-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd82-133">**SWbemDateTime. secondi**</span><span class="sxs-lookup"><span data-stu-id="fcd82-133">**SWbemDateTime.Seconds**</span></span>](swbemdatetime-seconds.md)
</dt> <dt>

[<span data-ttu-id="fcd82-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="fcd82-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="fcd82-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="fcd82-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




