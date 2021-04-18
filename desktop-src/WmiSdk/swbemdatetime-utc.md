---
description: Ottiene o imposta la rappresentazione UTC (Coordinated Universal Time) del valore DateTime.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. UTC (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309858"
---
# <a name="swbemdatetimeutc-property"></a><span data-ttu-id="4c1d8-103">Proprietà SWbemDateTime. UTC</span><span class="sxs-lookup"><span data-stu-id="4c1d8-103">SWbemDateTime.UTC property</span></span>

<span data-ttu-id="4c1d8-104">La proprietà **UTC** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta la rappresentazione UTC (Coordinated Universal Time) del valore **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="4c1d8-104">The **UTC** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the Coordinated Universal Times (UTC) representation of the **datetime** value.</span></span> <span data-ttu-id="4c1d8-105">L'ora UTC è l'ora impostata in base allo standard temporale.</span><span class="sxs-lookup"><span data-stu-id="4c1d8-105">UTC is the time as set by the World Time Standard.</span></span> <span data-ttu-id="4c1d8-106">UTC ha sostituito l'ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="4c1d8-106">UTC has replaced Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="4c1d8-107">Un valore UTC con un offset pari a zero corrisponde a GMT con un offset pari a zero.</span><span class="sxs-lookup"><span data-stu-id="4c1d8-107">A UTC value with a zero offset is the same as GMT with a zero offset.</span></span> <span data-ttu-id="4c1d8-108">Il numero con segno deve essere compreso tra-720 e 720 o viene restituito l'errore **wbemErrValueOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="4c1d8-108">The signed number must be in the range of -720 through 720 or the error **wbemErrValueOutOfRange** is returned.</span></span>

<span data-ttu-id="4c1d8-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4c1d8-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="4c1d8-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4c1d8-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c1d8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c1d8-111">Syntax</span></span>


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a><span data-ttu-id="4c1d8-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4c1d8-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="4c1d8-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4c1d8-113">Error codes</span></span>

<span data-ttu-id="4c1d8-114">Dopo avere ottenuto o impostato la proprietà **UTC** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4c1d8-114">After you get or set the **UTC** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="4c1d8-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="4c1d8-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="4c1d8-116">Il valore non è compreso nell'intervallo tra-720 e 720.</span><span class="sxs-lookup"><span data-stu-id="4c1d8-116">The value was not in the range of -720 through 720.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4c1d8-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="4c1d8-117">Examples</span></span>

<span data-ttu-id="4c1d8-118">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="4c1d8-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="4c1d8-119">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="4c1d8-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c1d8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c1d8-120">Requirements</span></span>



| <span data-ttu-id="4c1d8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c1d8-121">Requirement</span></span> | <span data-ttu-id="4c1d8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4c1d8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c1d8-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c1d8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4c1d8-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c1d8-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c1d8-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c1d8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4c1d8-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c1d8-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c1d8-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c1d8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c1d8-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c1d8-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c1d8-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4c1d8-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c1d8-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c1d8-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c1d8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4c1d8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c1d8-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c1d8-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c1d8-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="4c1d8-133">CLSID</span></span><br/>                    | <span data-ttu-id="4c1d8-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="4c1d8-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="4c1d8-135">IID</span><span class="sxs-lookup"><span data-stu-id="4c1d8-135">IID</span></span><br/>                      | <span data-ttu-id="4c1d8-136">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="4c1d8-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="4c1d8-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c1d8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c1d8-138">**SWbemDateTime. UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="4c1d8-138">**SWbemDateTime.UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)
</dt> <dt>

[<span data-ttu-id="4c1d8-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="4c1d8-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="4c1d8-140">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="4c1d8-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

