---
description: Ottiene o imposta un valore che rappresenta il componente secondi del valore DateTime.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. seconds (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ef4ef15f13bf3d8dfc9272b2a3b734c3678f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309861"
---
# <a name="swbemdatetimeseconds-property"></a><span data-ttu-id="e6c4d-103">Proprietà SWbemDateTime. seconds</span><span class="sxs-lookup"><span data-stu-id="e6c4d-103">SWbemDateTime.Seconds property</span></span>

<span data-ttu-id="e6c4d-104">La proprietà **seconds** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta un valore che rappresenta il componente secondi del valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="e6c4d-104">The **Seconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the seconds component of the datetime value.</span></span>

<span data-ttu-id="e6c4d-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e6c4d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e6c4d-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e6c4d-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c4d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6c4d-107">Syntax</span></span>


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a><span data-ttu-id="e6c4d-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e6c4d-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6c4d-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e6c4d-109">Error codes</span></span>

<span data-ttu-id="e6c4d-110">Dopo avere ottenuto o impostato la proprietà **seconds** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="e6c4d-110">After you get or set the **Seconds** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="e6c4d-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="e6c4d-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="e6c4d-112">Il valore non è compreso nell'intervallo tra 0 e 59.</span><span class="sxs-lookup"><span data-stu-id="e6c4d-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6c4d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6c4d-113">Remarks</span></span>

<span data-ttu-id="e6c4d-114">Se la proprietà [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) è stata impostata su 1, la proprietà **SWbemDateTime. seconds** potrebbe contenere un valore non corretto.</span><span class="sxs-lookup"><span data-stu-id="e6c4d-114">The **SWbemDateTime.Seconds** property may contain an incorrect value if the [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) property has been set to 1.</span></span> <span data-ttu-id="e6c4d-115">Contiene un valore che viene sottoposto a offset di un secondo a causa di un errore di arrotondamento che si verifica quando un valore [**DateTime**](datetime.md) CIM viene convertito in un valore di **\_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="e6c4d-115">It contains a value that is offset by one second because of a rounding error that occurs when a CIM [**DATETIME**](datetime.md) value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="e6c4d-116">Se invece la proprietà **minutes** è impostata su 0 (zero), la proprietà **seconds** restituisce il valore corretto.</span><span class="sxs-lookup"><span data-stu-id="e6c4d-116">If the **Minutes** property is set to 0 (zero) instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="e6c4d-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="e6c4d-117">Examples</span></span>

<span data-ttu-id="e6c4d-118">Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="e6c4d-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="e6c4d-119">Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="e6c4d-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c4d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6c4d-120">Requirements</span></span>



| <span data-ttu-id="e6c4d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c4d-121">Requirement</span></span> | <span data-ttu-id="e6c4d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e6c4d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c4d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6c4d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c4d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6c4d-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e6c4d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6c4d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c4d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6c4d-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e6c4d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6c4d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6c4d-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c4d-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6c4d-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e6c4d-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6c4d-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e6c4d-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e6c4d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c4d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6c4d-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c4d-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6c4d-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="e6c4d-133">CLSID</span></span><br/>                    | <span data-ttu-id="e6c4d-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="e6c4d-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="e6c4d-135">IID</span><span class="sxs-lookup"><span data-stu-id="e6c4d-135">IID</span></span><br/>                      | <span data-ttu-id="e6c4d-136">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="e6c4d-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="e6c4d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6c4d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c4d-138">**SWbemDateTime. SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="e6c4d-138">**SWbemDateTime.SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
</dt> <dt>

[<span data-ttu-id="e6c4d-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="e6c4d-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="e6c4d-140">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="e6c4d-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

