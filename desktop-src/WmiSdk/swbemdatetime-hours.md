---
description: Ottiene o imposta un valore che rappresenta il componente relativo alle ore del valore DateTime.
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. hours (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 27edb3c209e2e95ae7aff20930d260f8f6d44427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233455"
---
# <a name="swbemdatetimehours-property"></a><span data-ttu-id="87310-103">Proprietà SWbemDateTime. hours</span><span class="sxs-lookup"><span data-stu-id="87310-103">SWbemDateTime.Hours property</span></span>

<span data-ttu-id="87310-104">La proprietà **hours** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta un valore che rappresenta il componente hours del valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="87310-104">The **Hours** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the hours component of the datetime value.</span></span>

<span data-ttu-id="87310-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="87310-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="87310-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="87310-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="87310-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87310-107">Syntax</span></span>


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a><span data-ttu-id="87310-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="87310-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="87310-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="87310-109">Error codes</span></span>

<span data-ttu-id="87310-110">Dopo avere ottenuto o impostato la proprietà **hours** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="87310-110">After you get or set the **Hours** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="87310-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="87310-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="87310-112">Il valore non è compreso nell'intervallo tra 0 e 23.</span><span class="sxs-lookup"><span data-stu-id="87310-112">The value was not in the range of 0 through 23.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="87310-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="87310-113">Examples</span></span>

<span data-ttu-id="87310-114">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="87310-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="87310-115">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="87310-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87310-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87310-116">Requirements</span></span>



| <span data-ttu-id="87310-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="87310-117">Requirement</span></span> | <span data-ttu-id="87310-118">Valore</span><span class="sxs-lookup"><span data-stu-id="87310-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87310-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87310-119">Minimum supported client</span></span><br/> | <span data-ttu-id="87310-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87310-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87310-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87310-121">Minimum supported server</span></span><br/> | <span data-ttu-id="87310-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87310-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87310-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87310-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="87310-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="87310-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="87310-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="87310-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="87310-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="87310-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="87310-127">DLL</span><span class="sxs-lookup"><span data-stu-id="87310-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87310-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87310-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="87310-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="87310-129">CLSID</span></span><br/>                    | <span data-ttu-id="87310-130">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="87310-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="87310-131">IID</span><span class="sxs-lookup"><span data-stu-id="87310-131">IID</span></span><br/>                      | <span data-ttu-id="87310-132">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="87310-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="87310-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87310-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87310-134">**SWbemDateTime. HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="87310-134">**SWbemDateTime.HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
</dt> <dt>

[<span data-ttu-id="87310-135">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="87310-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="87310-136">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="87310-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

