---
description: Ottiene o imposta un valore che rappresenta il componente Year del valore DATETIME.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. Year (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315990"
---
# <a name="swbemdatetimeyear-property"></a><span data-ttu-id="6978e-103">Proprietà SWbemDateTime. Year</span><span class="sxs-lookup"><span data-stu-id="6978e-103">SWbemDateTime.Year property</span></span>

<span data-ttu-id="6978e-104">La proprietà **year** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta un valore che rappresenta il componente Year del valore [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="6978e-104">The **Year** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the year component of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="6978e-105">Il valore deve essere compreso nell'intervallo 0000-9999 o viene restituito l'errore wbemErrValueOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="6978e-105">The value must be in the range of 0000 - 9999 or the error wbemErrValueOutOfRange is returned.</span></span>

<span data-ttu-id="6978e-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6978e-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6978e-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6978e-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6978e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6978e-108">Syntax</span></span>


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a><span data-ttu-id="6978e-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6978e-109">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="6978e-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6978e-110">Error codes</span></span>

<span data-ttu-id="6978e-111">Dopo avere ottenuto o impostato la proprietà **year** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6978e-111">After you get or set the **Year** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="6978e-112">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="6978e-112">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="6978e-113">Il valore non è compreso nell'intervallo tra 0000 e 9999.</span><span class="sxs-lookup"><span data-stu-id="6978e-113">The value was not in the range of 0000 through 9999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="6978e-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="6978e-114">Examples</span></span>

<span data-ttu-id="6978e-115">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="6978e-115">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="6978e-116">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="6978e-116">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6978e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6978e-117">Requirements</span></span>



| <span data-ttu-id="6978e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6978e-118">Requirement</span></span> | <span data-ttu-id="6978e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6978e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6978e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6978e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6978e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6978e-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6978e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6978e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6978e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6978e-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6978e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6978e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6978e-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6978e-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6978e-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6978e-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6978e-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6978e-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6978e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6978e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6978e-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6978e-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6978e-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="6978e-130">CLSID</span></span><br/>                    | <span data-ttu-id="6978e-131">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="6978e-131">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="6978e-132">IID</span><span class="sxs-lookup"><span data-stu-id="6978e-132">IID</span></span><br/>                      | <span data-ttu-id="6978e-133">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="6978e-133">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6978e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6978e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6978e-135">**SWbemDateTime. YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="6978e-135">**SWbemDateTime.YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
</dt> <dt>

[<span data-ttu-id="6978e-136">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="6978e-136">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="6978e-137">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="6978e-137">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

