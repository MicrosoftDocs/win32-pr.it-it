---
description: La funzione PdhVbGetDoubleCounterValue restituisce il valore corrente del contatore specificato come valore a virgola mobile a precisione doppia.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: PdhVbGetDoubleCounterValue (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345511"
---
# <a name="pdhvbgetdoublecountervalue-function"></a><span data-ttu-id="5b882-103">PdhVbGetDoubleCounterValue (funzione)</span><span class="sxs-lookup"><span data-stu-id="5b882-103">PdhVbGetDoubleCounterValue function</span></span>

<span data-ttu-id="5b882-104">La funzione **PdhVbGetDoubleCounterValue** restituisce il valore corrente del contatore specificato come valore a virgola mobile a precisione doppia.</span><span class="sxs-lookup"><span data-stu-id="5b882-104">The **PdhVbGetDoubleCounterValue** function returns the current value of the specified counter as a double-precision floating point value.</span></span> <span data-ttu-id="5b882-105">È necessario controllare *CounterStatus* prima di utilizzare il numero restituito, perché il contatore potrebbe non essere valido durante la lettura.</span><span class="sxs-lookup"><span data-stu-id="5b882-105">You should check *CounterStatus* before using the returned number, because the counter may not be valid when it is read.</span></span> <span data-ttu-id="5b882-106">Per controllare lo stato del contatore, chiamare la funzione [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="5b882-106">To check the counter status, call the [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b882-107">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="5b882-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="5b882-108">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5b882-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="5b882-109">Funzione PdhVbGetDoubleCounterValue ( \_ ByVal CounterHandle Long, \_ ByVal CounterStatus Long \_ ) As Double</span><span class="sxs-lookup"><span data-stu-id="5b882-109">Function PdhVbGetDoubleCounterValue( \_ ByVal CounterHandle As Long, \_ ByVal CounterStatus As Long \_ ) As Double</span></span>

## <a name="parameters"></a><span data-ttu-id="5b882-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b882-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b882-111">*CounterHandle*</span><span class="sxs-lookup"><span data-stu-id="5b882-111">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="5b882-112">ID del contatore il cui valore corrente deve essere letto.</span><span class="sxs-lookup"><span data-stu-id="5b882-112">ID of the counter whose current value is to be read.</span></span>

</dd> <dt>

<span data-ttu-id="5b882-113">*CounterStatus*</span><span class="sxs-lookup"><span data-stu-id="5b882-113">*CounterStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="5b882-114">Variabile in cui lo stato corrente del valore del contatore viene restituito al chiamante.</span><span class="sxs-lookup"><span data-stu-id="5b882-114">Variable in which the current status of the counter value is returned to the caller.</span></span> <span data-ttu-id="5b882-115">Il valore dei dati restituiti è valido solo se il valore restituito in CounterStatus è PDH \_ CSTATUS \_ dati validi \_ o PDH \_ CSTATUS \_ nuovi \_ dati (vedere codici di errore PDH).</span><span class="sxs-lookup"><span data-stu-id="5b882-115">The returned data value is valid if and only if the value returned in CounterStatus is PDH\_CSTATUS\_VALID\_DATA or PDH\_CSTATUS\_NEW\_DATA (see PDH error codes).</span></span> <span data-ttu-id="5b882-116">Se il valore restituito in CounterStatus è qualsiasi altro valore, non usare i dati.</span><span class="sxs-lookup"><span data-stu-id="5b882-116">If the value returned in CounterStatus is any other value, do not use the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b882-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b882-117">Return value</span></span>

<span data-ttu-id="5b882-118">La funzione restituisce il valore in virgola mobile e precisione doppia del contatore corrente, calcolato e formattato in base a quanto definito dal tipo di contatore.</span><span class="sxs-lookup"><span data-stu-id="5b882-118">The function returns the double-precision floating point value of the current counter, computed and formatted as defined by the counter type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b882-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b882-119">Requirements</span></span>



| <span data-ttu-id="5b882-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b882-120">Requirement</span></span> | <span data-ttu-id="5b882-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5b882-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b882-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b882-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b882-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5b882-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b882-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b882-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b882-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b882-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b882-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b882-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b882-127"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b882-127"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="5b882-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5b882-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b882-129"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b882-129"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b882-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b882-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b882-131">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="5b882-131">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




