---
description: Valore booleano che indica se un campo di un valore DateTime CIM deve essere interpretato come un intervallo.
ms.assetid: ba5fcf17-7c26-4960-9da9-e380d90e5f3e
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. Interval (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.IsInterval
- ISWbemDateTime.IsInterval
- ISWbemDateTime.get_IsInterval
- ISWbemDateTime.put_IsInterval
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 468ea16de4f1206a9a15c58c2c7891df8afd4c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233990"
---
# <a name="swbemdatetimeisinterval-property"></a><span data-ttu-id="9ff0f-103">Proprietà SWbemDateTime. Interval</span><span class="sxs-lookup"><span data-stu-id="9ff0f-103">SWbemDateTime.IsInterval property</span></span>

<span data-ttu-id="9ff0f-104">La proprietà di **intervallo** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se un campo di un valore DateTime CIM deve essere interpretato come un intervallo.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-104">The **IsInterval** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether any field in a CIM datetime value should be interpreted as an interval.</span></span>

<span data-ttu-id="9ff0f-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9ff0f-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="9ff0f-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff0f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ff0f-107">Syntax</span></span>


```VB
SWbemDateTime.IsInterval As boolean
```



## <a name="property-value"></a><span data-ttu-id="9ff0f-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9ff0f-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="9ff0f-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="9ff0f-109">Examples</span></span>

<span data-ttu-id="9ff0f-110">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori DateTime CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="9ff0f-110">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM datetime values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="9ff0f-111">Per una descrizione del formato DateTime CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="9ff0f-111">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff0f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ff0f-112">Requirements</span></span>



| <span data-ttu-id="9ff0f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ff0f-113">Requirement</span></span> | <span data-ttu-id="9ff0f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9ff0f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff0f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ff0f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff0f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ff0f-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ff0f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ff0f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff0f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ff0f-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ff0f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ff0f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff0f-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff0f-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ff0f-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9ff0f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ff0f-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ff0f-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ff0f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff0f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff0f-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff0f-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ff0f-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="9ff0f-125">CLSID</span></span><br/>                    | <span data-ttu-id="9ff0f-126">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="9ff0f-126">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="9ff0f-127">IID</span><span class="sxs-lookup"><span data-stu-id="9ff0f-127">IID</span></span><br/>                      | <span data-ttu-id="9ff0f-128">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="9ff0f-128">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9ff0f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ff0f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff0f-130">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="9ff0f-130">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="9ff0f-131">Formato di data e ora</span><span class="sxs-lookup"><span data-stu-id="9ff0f-131">Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 




