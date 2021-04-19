---
description: Esegue un'operazione di scrittura e lettura sull'oggetto comando della smart card (unità dati del protocollo dell'applicazione).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'Metodo IsValid:: Transaction (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309436"
---
# <a name="iscardtransaction-method"></a><span data-ttu-id="54dcd-103">Metodo IsValid:: Transaction</span><span class="sxs-lookup"><span data-stu-id="54dcd-103">ISCard::Transaction method</span></span>

<span data-ttu-id="54dcd-104">\[Il metodo di **transazione** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="54dcd-104">\[The **Transaction** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="54dcd-105">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="54dcd-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="54dcd-106">Il metodo di **transazione** esegue un'operazione di scrittura e lettura nell'oggetto comando della [*Smart Card*](../secgloss/s-gly.md) ([*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="54dcd-106">The **Transaction** method executes a write and read operation on the [*smart card*](../secgloss/s-gly.md) command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span> <span data-ttu-id="54dcd-107">La stringa di risposta dalla smart card per la stringa di comando definita nella scheda inviata alla smart card sarà accessibile dopo la restituzione di questa funzione.</span><span class="sxs-lookup"><span data-stu-id="54dcd-107">The reply string from the smart card for the command string defined in the card that was sent to the smart card will be accessible after this function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="54dcd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54dcd-108">Syntax</span></span>


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="54dcd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="54dcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54dcd-110">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="54dcd-110">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54dcd-111">Puntatore all'oggetto comando della smart card.</span><span class="sxs-lookup"><span data-stu-id="54dcd-111">A pointer to the smart card command object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54dcd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54dcd-112">Return value</span></span>

<span data-ttu-id="54dcd-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="54dcd-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="54dcd-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="54dcd-114">Return code</span></span>                                                                                   | <span data-ttu-id="54dcd-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54dcd-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="54dcd-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="54dcd-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="54dcd-117">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="54dcd-117">The operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="54dcd-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="54dcd-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="54dcd-119">Il parametro *ppCmd* non è valido.</span><span class="sxs-lookup"><span data-stu-id="54dcd-119">The *ppCmd* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="54dcd-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="54dcd-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="54dcd-121">Un puntatore errato è stato passato in *ppCmd*.</span><span class="sxs-lookup"><span data-stu-id="54dcd-121">A bad pointer was passed in *ppCmd*.</span></span><br/>          |
| <dl> <span data-ttu-id="54dcd-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="54dcd-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="54dcd-123">La memoria per soddisfare la richiesta non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="54dcd-123">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54dcd-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="54dcd-124">Remarks</span></span>

<span data-ttu-id="54dcd-125">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="54dcd-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="54dcd-126">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="54dcd-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="54dcd-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="54dcd-127">Examples</span></span>

<span data-ttu-id="54dcd-128">Nell'esempio seguente viene illustrata l'esecuzione di un'operazione di scrittura e lettura sull'oggetto comando della smart card.</span><span class="sxs-lookup"><span data-stu-id="54dcd-128">The following example shows executing a write and read operation on the smart card command object.</span></span>


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="54dcd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54dcd-129">Requirements</span></span>



| <span data-ttu-id="54dcd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="54dcd-130">Requirement</span></span> | <span data-ttu-id="54dcd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="54dcd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54dcd-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54dcd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="54dcd-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="54dcd-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="54dcd-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54dcd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="54dcd-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54dcd-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54dcd-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="54dcd-136">End of client support</span></span><br/>    | <span data-ttu-id="54dcd-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="54dcd-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="54dcd-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="54dcd-138">End of server support</span></span><br/>    | <span data-ttu-id="54dcd-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="54dcd-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="54dcd-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54dcd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="54dcd-141"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="54dcd-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="54dcd-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="54dcd-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="54dcd-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54dcd-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54dcd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="54dcd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54dcd-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54dcd-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="54dcd-146">IID</span><span class="sxs-lookup"><span data-stu-id="54dcd-146">IID</span></span><br/>                      | <span data-ttu-id="54dcd-147">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="54dcd-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="54dcd-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54dcd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54dcd-149">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="54dcd-149">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="54dcd-150">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="54dcd-150">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="54dcd-151">**Scollegare**</span><span class="sxs-lookup"><span data-stu-id="54dcd-151">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="54dcd-152">**Ottieni \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="54dcd-152">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="54dcd-153">**ottenere \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="54dcd-153">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="54dcd-154">**ottenere il \_ contesto**</span><span class="sxs-lookup"><span data-stu-id="54dcd-154">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="54dcd-155">**ottenere il \_ protocollo**</span><span class="sxs-lookup"><span data-stu-id="54dcd-155">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="54dcd-156">**ottenere \_ lo stato**</span><span class="sxs-lookup"><span data-stu-id="54dcd-156">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="54dcd-157">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="54dcd-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="54dcd-158">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="54dcd-158">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> <dt>

[<span data-ttu-id="54dcd-159">**Ricollegare**</span><span class="sxs-lookup"><span data-stu-id="54dcd-159">**ReAttach**</span></span>](iscard-reattach.md)
</dt> <dt>

[<span data-ttu-id="54dcd-160">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="54dcd-160">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
