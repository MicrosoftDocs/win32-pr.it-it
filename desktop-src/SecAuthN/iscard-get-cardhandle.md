---
description: Recupera l'handle per una smart card connessa. Questo metodo restituisce ( \* pHandle) = = null se non è connesso.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'Metodo IsValid:: get_CardHandle (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966455"
---
# <a name="iscardget_cardhandle-method"></a><span data-ttu-id="133ce-104">Metodo IsValid:: Get \_ CardHandle</span><span class="sxs-lookup"><span data-stu-id="133ce-104">ISCard::get\_CardHandle method</span></span>

<span data-ttu-id="133ce-105">\[Il metodo **get \_ CardHandle** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="133ce-105">\[The **get\_CardHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="133ce-106">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="133ce-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="133ce-107">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="133ce-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="133ce-108">Il metodo **get \_ CardHandle** recupera l'handle per una [*Smart Card*](../secgloss/s-gly.md)connessa.</span><span class="sxs-lookup"><span data-stu-id="133ce-108">The **get\_CardHandle** method retrieves the handle for a connected [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="133ce-109">Questo metodo restituisce ( \* pHandle) = = **null** se non è connesso.</span><span class="sxs-lookup"><span data-stu-id="133ce-109">This method returns (\*pHandle) == **NULL** if not connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="133ce-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="133ce-110">Syntax</span></span>


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a><span data-ttu-id="133ce-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="133ce-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="133ce-112">*pHandle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="133ce-112">*pHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="133ce-113">Puntatore all'handle della scheda al ritorno.</span><span class="sxs-lookup"><span data-stu-id="133ce-113">Pointer to the card handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="133ce-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="133ce-114">Return value</span></span>

<span data-ttu-id="133ce-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="133ce-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="133ce-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="133ce-116">Return code</span></span>                                                                                  | <span data-ttu-id="133ce-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="133ce-117">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="133ce-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="133ce-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="133ce-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="133ce-119">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="133ce-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="133ce-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="133ce-121">Il parametro *pHandle* non è valido.</span><span class="sxs-lookup"><span data-stu-id="133ce-121">The *pHandle* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="133ce-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="133ce-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="133ce-123">Un puntatore errato è stato passato in *pHandle*.</span><span class="sxs-lookup"><span data-stu-id="133ce-123">A bad pointer was passed in *pHandle*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="133ce-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="133ce-124">Remarks</span></span>

<span data-ttu-id="133ce-125">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="133ce-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="133ce-126">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="133ce-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="133ce-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="133ce-127">Examples</span></span>

<span data-ttu-id="133ce-128">Nell'esempio seguente viene illustrato come recuperare l'handle della smart card.</span><span class="sxs-lookup"><span data-stu-id="133ce-128">The following example shows retrieving the smart card handle.</span></span>


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a><span data-ttu-id="133ce-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="133ce-129">Requirements</span></span>



| <span data-ttu-id="133ce-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="133ce-130">Requirement</span></span> | <span data-ttu-id="133ce-131">Valore</span><span class="sxs-lookup"><span data-stu-id="133ce-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="133ce-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="133ce-132">Minimum supported client</span></span><br/> | <span data-ttu-id="133ce-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="133ce-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="133ce-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="133ce-134">Minimum supported server</span></span><br/> | <span data-ttu-id="133ce-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="133ce-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="133ce-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="133ce-136">End of client support</span></span><br/>    | <span data-ttu-id="133ce-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="133ce-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="133ce-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="133ce-138">End of server support</span></span><br/>    | <span data-ttu-id="133ce-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="133ce-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="133ce-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="133ce-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="133ce-141"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="133ce-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="133ce-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="133ce-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="133ce-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="133ce-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="133ce-144">DLL</span><span class="sxs-lookup"><span data-stu-id="133ce-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="133ce-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="133ce-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="133ce-146">IID</span><span class="sxs-lookup"><span data-stu-id="133ce-146">IID</span></span><br/>                      | <span data-ttu-id="133ce-147">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="133ce-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="133ce-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="133ce-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="133ce-149">**Ottieni \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="133ce-149">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="133ce-150">**ottenere il \_ contesto**</span><span class="sxs-lookup"><span data-stu-id="133ce-150">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="133ce-151">**ottenere il \_ protocollo**</span><span class="sxs-lookup"><span data-stu-id="133ce-151">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="133ce-152">**ottenere \_ lo stato**</span><span class="sxs-lookup"><span data-stu-id="133ce-152">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="133ce-153">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="133ce-153">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
