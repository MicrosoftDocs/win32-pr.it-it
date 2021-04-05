---
description: Ottiene o imposta la data CIM non elaborata nel formato DMTF (Distributed Management Task Force).
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. Value (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130991"
---
# <a name="swbemdatetimevalue-property"></a><span data-ttu-id="c23b3-103">Proprietà SWbemDateTime. Value</span><span class="sxs-lookup"><span data-stu-id="c23b3-103">SWbemDateTime.Value property</span></span>

<span data-ttu-id="c23b3-104">La proprietà **value** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta la data CIM non elaborata nel formato DMTF (Distributed Management Task Force).</span><span class="sxs-lookup"><span data-stu-id="c23b3-104">The **Value** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the raw CIM date in the DMTF (Distributed Management Task Force) format.</span></span> <span data-ttu-id="c23b3-105">Il formato DMTF è una rappresentazione di stringa del valore [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="c23b3-105">The DMTF format is a string representation of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="c23b3-106">Questa proprietà è la proprietà predefinita per gli oggetti **SWbemDateTime** .</span><span class="sxs-lookup"><span data-stu-id="c23b3-106">This property is the default property for **SWbemDateTime** objects.</span></span> <span data-ttu-id="c23b3-107">Il valore predefinito della proprietà **value** è 00000101000000.000000 + 000.</span><span class="sxs-lookup"><span data-stu-id="c23b3-107">The **Value** property has a default value of 00000101000000.000000+000.</span></span>

<span data-ttu-id="c23b3-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c23b3-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c23b3-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c23b3-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c23b3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c23b3-110">Syntax</span></span>


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a><span data-ttu-id="c23b3-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c23b3-111">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="c23b3-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c23b3-112">Error codes</span></span>

<span data-ttu-id="c23b3-113">Quando si ottiene o si imposta la proprietà **value** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c23b3-113">After you get or set the **Value** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="c23b3-114">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="c23b3-114">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="c23b3-115">Il formato di *strValue* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c23b3-115">The format of *strValue* is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c23b3-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="c23b3-116">Examples</span></span>

<span data-ttu-id="c23b3-117">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="c23b3-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="c23b3-118">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="c23b3-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c23b3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c23b3-119">Requirements</span></span>



| <span data-ttu-id="c23b3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c23b3-120">Requirement</span></span> | <span data-ttu-id="c23b3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c23b3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c23b3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c23b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c23b3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c23b3-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c23b3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c23b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c23b3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c23b3-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c23b3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c23b3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c23b3-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c23b3-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c23b3-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c23b3-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="c23b3-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c23b3-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c23b3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c23b3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c23b3-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c23b3-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c23b3-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="c23b3-132">CLSID</span></span><br/>                    | <span data-ttu-id="c23b3-133">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="c23b3-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="c23b3-134">IID</span><span class="sxs-lookup"><span data-stu-id="c23b3-134">IID</span></span><br/>                      | <span data-ttu-id="c23b3-135">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="c23b3-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c23b3-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c23b3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c23b3-137">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="c23b3-137">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="c23b3-138">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="c23b3-138">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

