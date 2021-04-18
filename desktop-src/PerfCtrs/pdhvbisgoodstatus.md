---
description: La funzione PdhVbIsGoodStatus verifica un valore di stato per determinare se si tratta di un codice di esito positivo o negativo. Se il valore di stato è quello corretto, il valore restituito sarà diverso da zero. Se si tratta di un codice di stato di errore, il valore restituito sarà zero.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312146"
---
# <a name="pdhvbisgoodstatus-function"></a><span data-ttu-id="52a3f-105">PdhVbIsGoodStatus (funzione)</span><span class="sxs-lookup"><span data-stu-id="52a3f-105">PdhVbIsGoodStatus function</span></span>

<span data-ttu-id="52a3f-106">La funzione **PdhVbIsGoodStatus** verifica un valore di stato per determinare se si tratta di un codice di esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="52a3f-106">The **PdhVbIsGoodStatus** function tests a status value to determine if it is a success or failure code.</span></span> <span data-ttu-id="52a3f-107">Se il valore di stato è quello corretto, il valore restituito sarà diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="52a3f-107">If the status value is a successful one, then the return value will be nonzero.</span></span> <span data-ttu-id="52a3f-108">Se si tratta di un codice di stato di errore, il valore restituito sarà zero.</span><span class="sxs-lookup"><span data-stu-id="52a3f-108">If it is a failure status code, the return value will be zero.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52a3f-109">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="52a3f-109">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="52a3f-110">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="52a3f-110">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="52a3f-111">Funzione PdhVbIsGoodStatus ( \_ ByVal StatusValue Long \_ ) Long</span><span class="sxs-lookup"><span data-stu-id="52a3f-111">Function PdhVbIsGoodStatus( \_ ByVal StatusValue As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="52a3f-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="52a3f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a3f-113">*StatusValue*</span><span class="sxs-lookup"><span data-stu-id="52a3f-113">*StatusValue*</span></span> 
</dt> <dd>

<span data-ttu-id="52a3f-114">Valore di stato restituito da un'altra funzione PDH che deve essere testata.</span><span class="sxs-lookup"><span data-stu-id="52a3f-114">Status value returned by another PDH function that is to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a3f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52a3f-115">Return value</span></span>

<span data-ttu-id="52a3f-116">La funzione restituisce zero se il codice di stato è un codice di stato di errore.</span><span class="sxs-lookup"><span data-stu-id="52a3f-116">The function returns zero if the status code is a failure status code.</span></span> <span data-ttu-id="52a3f-117">Restituisce un valore diverso da zero se il codice di stato è un codice di stato di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="52a3f-117">It returns nonzero if the status code is a success status code.</span></span>

## <a name="requirements"></a><span data-ttu-id="52a3f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52a3f-118">Requirements</span></span>



| <span data-ttu-id="52a3f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a3f-119">Requirement</span></span> | <span data-ttu-id="52a3f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="52a3f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52a3f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52a3f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52a3f-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="52a3f-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52a3f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52a3f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52a3f-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52a3f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="52a3f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="52a3f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="52a3f-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52a3f-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="52a3f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="52a3f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52a3f-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52a3f-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a3f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52a3f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a3f-130">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="52a3f-130">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




