---
description: Ottiene o imposta un valore che rappresenta il componente minuti del valore DateTime.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. minutes (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318865"
---
# <a name="swbemdatetimeminutes-property"></a><span data-ttu-id="55d8a-103">Proprietà SWbemDateTime. minutes</span><span class="sxs-lookup"><span data-stu-id="55d8a-103">SWbemDateTime.Minutes property</span></span>

<span data-ttu-id="55d8a-104">La proprietà **minutes** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta un valore che rappresenta il componente minuti del valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="55d8a-104">The **Minutes** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the minutes component of the datetime value.</span></span>

<span data-ttu-id="55d8a-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="55d8a-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="55d8a-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="55d8a-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d8a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55d8a-107">Syntax</span></span>


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a><span data-ttu-id="55d8a-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="55d8a-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="55d8a-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="55d8a-109">Error codes</span></span>

<span data-ttu-id="55d8a-110">Dopo avere ottenuto o impostato la proprietà **minutes** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="55d8a-110">After you get or set the **Minutes** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="55d8a-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="55d8a-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="55d8a-112">Il valore non è compreso nell'intervallo tra 0 e 59.</span><span class="sxs-lookup"><span data-stu-id="55d8a-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55d8a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="55d8a-113">Remarks</span></span>

<span data-ttu-id="55d8a-114">Se la proprietà **SWbemDateTime. minutes** è impostata su 1, la proprietà [**SWbemDateTime. seconds**](swbemdatetime-seconds.md) contiene un valore offset di un secondo un errore di arrotondamento che si verifica quando un valore **DateTime** CIM viene convertito in un valore di **\_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="55d8a-114">If the **SWbemDateTime.Minutes** property is set to 1, then the [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) property contains a value that is offset by one second a rounding error that occurs when a CIM **datetime** value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="55d8a-115">Se invece la proprietà **minutes** è impostata su 0, la proprietà **seconds** restituisce il valore corretto.</span><span class="sxs-lookup"><span data-stu-id="55d8a-115">If the **Minutes** property is set to 0 instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="55d8a-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="55d8a-116">Examples</span></span>

<span data-ttu-id="55d8a-117">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="55d8a-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="55d8a-118">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="55d8a-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55d8a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55d8a-119">Requirements</span></span>



| <span data-ttu-id="55d8a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d8a-120">Requirement</span></span> | <span data-ttu-id="55d8a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="55d8a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55d8a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d8a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="55d8a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55d8a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55d8a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d8a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="55d8a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55d8a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55d8a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55d8a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d8a-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="55d8a-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="55d8a-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="55d8a-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="55d8a-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55d8a-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55d8a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="55d8a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55d8a-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55d8a-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="55d8a-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="55d8a-132">CLSID</span></span><br/>                    | <span data-ttu-id="55d8a-133">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="55d8a-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="55d8a-134">IID</span><span class="sxs-lookup"><span data-stu-id="55d8a-134">IID</span></span><br/>                      | <span data-ttu-id="55d8a-135">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="55d8a-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="55d8a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55d8a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d8a-137">**SWbemDateTime. MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="55d8a-137">**SWbemDateTime.MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
</dt> <dt>

[<span data-ttu-id="55d8a-138">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="55d8a-138">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="55d8a-139">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="55d8a-139">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

