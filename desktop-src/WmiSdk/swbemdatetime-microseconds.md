---
description: Ottiene o imposta un valore che rappresenta il componente microsecondi del valore DateTime.
ms.assetid: b810b781-86a3-4730-8114-44d10454f7c3
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. microsecondi (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Microseconds
- ISWbemDateTime.Microseconds
- ISWbemDateTime.get_Microseconds
- ISWbemDateTime.put_Microseconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 94213eb70a98be1af8f8404ddece8bf2f07ca807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349621"
---
# <a name="swbemdatetimemicroseconds-property"></a><span data-ttu-id="2c045-103">Proprietà SWbemDateTime. microsecondi</span><span class="sxs-lookup"><span data-stu-id="2c045-103">SWbemDateTime.Microseconds property</span></span>

<span data-ttu-id="2c045-104">La proprietà **microsecondi** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta un valore che rappresenta il componente microsecondi del valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="2c045-104">The **Microseconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the microseconds component of the datetime value.</span></span>

<span data-ttu-id="2c045-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2c045-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="2c045-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2c045-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c045-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c045-107">Syntax</span></span>


```VB
SWbemDateTime.Microseconds As Long
```



## <a name="property-value"></a><span data-ttu-id="2c045-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2c045-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c045-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2c045-109">Error codes</span></span>

<span data-ttu-id="2c045-110">Dopo avere ottenuto o impostato la proprietà **microsecondi** , l'oggetto **Err** può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2c045-110">After you get or set the **Microseconds** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="2c045-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="2c045-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="2c045-112">Il valore non è compreso nell'intervallo tra 0 e 999999.</span><span class="sxs-lookup"><span data-stu-id="2c045-112">The value was not in the range of 0 through 999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2c045-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="2c045-113">Examples</span></span>

<span data-ttu-id="2c045-114">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="2c045-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="2c045-115">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="2c045-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c045-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c045-116">Requirements</span></span>



| <span data-ttu-id="2c045-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c045-117">Requirement</span></span> | <span data-ttu-id="2c045-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2c045-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c045-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c045-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c045-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c045-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c045-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c045-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c045-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c045-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c045-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c045-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c045-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c045-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c045-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2c045-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c045-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c045-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c045-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2c045-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c045-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c045-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c045-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="2c045-129">CLSID</span></span><br/>                    | <span data-ttu-id="2c045-130">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="2c045-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="2c045-131">IID</span><span class="sxs-lookup"><span data-stu-id="2c045-131">IID</span></span><br/>                      | <span data-ttu-id="2c045-132">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="2c045-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="2c045-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c045-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c045-134">**SWbemDateTime. MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="2c045-134">**SWbemDateTime.MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
</dt> <dt>

[<span data-ttu-id="2c045-135">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="2c045-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="2c045-136">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="2c045-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




