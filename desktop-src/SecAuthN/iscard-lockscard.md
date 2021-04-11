---
description: Il metodo LockSCard rivendica l'accesso esclusivo alla smart card.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: 'Metodo IsValid:: LockSCard (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d5b834afec339aa4c3a4eee42f9817409fabb917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233267"
---
# <a name="iscardlockscard-method"></a><span data-ttu-id="2ffe3-103">Metodo IsValid:: LockSCard</span><span class="sxs-lookup"><span data-stu-id="2ffe3-103">ISCard::LockSCard method</span></span>

<span data-ttu-id="2ffe3-104">\[Il metodo **LockSCard** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2ffe3-104">\[The **LockSCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2ffe3-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2ffe3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ffe3-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2ffe3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2ffe3-107">Il metodo **LockSCard** rivendica l'accesso esclusivo alla [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2ffe3-107">The **LockSCard** method claims exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ffe3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ffe3-108">Syntax</span></span>


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a><span data-ttu-id="2ffe3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ffe3-109">Parameters</span></span>

<span data-ttu-id="2ffe3-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2ffe3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ffe3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ffe3-111">Return value</span></span>

<span data-ttu-id="2ffe3-112">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="2ffe3-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2ffe3-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2ffe3-113">Return code</span></span>                                                                          | <span data-ttu-id="2ffe3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ffe3-114">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2ffe3-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe3-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2ffe3-116">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="2ffe3-116">Operation completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ffe3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ffe3-117">Remarks</span></span>

<span data-ttu-id="2ffe3-118">Oltre al codice di errore COM elencato sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2ffe3-118">In addition to the COM error code listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2ffe3-119">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2ffe3-119">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="2ffe3-120">Per sbloccare la smart card, chiamare il metodo IsValid [**:: UnlockSCard**](iscard-unlockscard.md) .</span><span class="sxs-lookup"><span data-stu-id="2ffe3-120">To unlock the smart card, call the [**ISCard::UnlockSCard**](iscard-unlockscard.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2ffe3-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="2ffe3-121">Examples</span></span>

<span data-ttu-id="2ffe3-122">Nell'esempio seguente viene illustrato come acquisire l'accesso esclusivo alla smart card.</span><span class="sxs-lookup"><span data-stu-id="2ffe3-122">The following example shows acquiring exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
```



## <a name="requirements"></a><span data-ttu-id="2ffe3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ffe3-123">Requirements</span></span>



| <span data-ttu-id="2ffe3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ffe3-124">Requirement</span></span> | <span data-ttu-id="2ffe3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2ffe3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ffe3-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ffe3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2ffe3-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2ffe3-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2ffe3-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ffe3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2ffe3-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ffe3-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ffe3-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2ffe3-130">End of client support</span></span><br/>    | <span data-ttu-id="2ffe3-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ffe3-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2ffe3-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2ffe3-132">End of server support</span></span><br/>    | <span data-ttu-id="2ffe3-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ffe3-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2ffe3-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ffe3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ffe3-135"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe3-135"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ffe3-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2ffe3-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ffe3-137"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe3-137"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2ffe3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2ffe3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ffe3-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe3-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2ffe3-140">IID</span><span class="sxs-lookup"><span data-stu-id="2ffe3-140">IID</span></span><br/>                      | <span data-ttu-id="2ffe3-141">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2ffe3-141">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2ffe3-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ffe3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ffe3-143">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="2ffe3-143">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="2ffe3-144">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="2ffe3-144">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
