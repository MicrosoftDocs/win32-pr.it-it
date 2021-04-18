---
description: Ottiene o imposta un valore che rappresenta il componente mese del valore DateTime.
ms.assetid: 05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. month (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Month
- ISWbemDateTime.Month
- ISWbemDateTime.get_Month
- ISWbemDateTime.put_Month
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73769d73cffc5b9731cfd55785e2fa087182b33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318864"
---
# <a name="swbemdatetimemonth-property"></a><span data-ttu-id="25e38-103">Proprietà SWbemDateTime. month</span><span class="sxs-lookup"><span data-stu-id="25e38-103">SWbemDateTime.Month property</span></span>

<span data-ttu-id="25e38-104">La proprietà **Month** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta un valore che rappresenta il componente month del valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="25e38-104">The **Month** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the month component of the datetime value.</span></span> <span data-ttu-id="25e38-105">Il numero deve essere compreso tra 01 e 12 o viene restituito l'errore **wbemValueOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="25e38-105">The number must be in the range of 01 through 12 or the error **wbemValueOutOfRange** is returned.</span></span>

<span data-ttu-id="25e38-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="25e38-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="25e38-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="25e38-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="25e38-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25e38-108">Syntax</span></span>


```VB
SWbemDateTime.Month As Long
```



## <a name="property-value"></a><span data-ttu-id="25e38-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="25e38-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="25e38-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="25e38-110">Examples</span></span>

<span data-ttu-id="25e38-111">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="25e38-111">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="25e38-112">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="25e38-112">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25e38-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25e38-113">Requirements</span></span>



| <span data-ttu-id="25e38-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="25e38-114">Requirement</span></span> | <span data-ttu-id="25e38-115">Valore</span><span class="sxs-lookup"><span data-stu-id="25e38-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25e38-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25e38-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25e38-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25e38-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25e38-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25e38-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25e38-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25e38-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25e38-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25e38-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25e38-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="25e38-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="25e38-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="25e38-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="25e38-124">DLL</span><span class="sxs-lookup"><span data-stu-id="25e38-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25e38-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="25e38-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="25e38-126">CLSID</span></span><br/>                    | <span data-ttu-id="25e38-127">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="25e38-127">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="25e38-128">IID</span><span class="sxs-lookup"><span data-stu-id="25e38-128">IID</span></span><br/>                      | <span data-ttu-id="25e38-129">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="25e38-129">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="25e38-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25e38-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e38-131">**SWbemDateTime. MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="25e38-131">**SWbemDateTime.MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
</dt> <dt>

[<span data-ttu-id="25e38-132">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="25e38-132">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="25e38-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="25e38-133">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




