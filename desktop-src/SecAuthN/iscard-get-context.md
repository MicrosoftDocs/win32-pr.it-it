---
description: Recupera l'handle di contesto corrente di Resource Manager. Questo metodo restituisce ( \* pContext) = = null se non è stato stabilito alcun contesto.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'Metodo IsValid:: get_Context (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884494"
---
# <a name="iscardget_context-method"></a><span data-ttu-id="fe718-104">Metodo di contesto IsValid:: Get \_</span><span class="sxs-lookup"><span data-stu-id="fe718-104">ISCard::get\_Context method</span></span>

<span data-ttu-id="fe718-105">\[Il metodo **get \_ context** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requirements.</span><span class="sxs-lookup"><span data-stu-id="fe718-105">\[The **get\_Context** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fe718-106">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fe718-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe718-107">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="fe718-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fe718-108">Il metodo **get \_ context** recupera l'handle di contesto corrente di [*Resource Manager*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fe718-108">The **get\_Context** method retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span> <span data-ttu-id="fe718-109">Questo metodo restituisce ( \* *pContext*) = = **null** se non è stato stabilito alcun contesto.</span><span class="sxs-lookup"><span data-stu-id="fe718-109">This method returns (\**pContext*) == **NULL** if no context has been established.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe718-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe718-110">Syntax</span></span>


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="fe718-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe718-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe718-112">*pContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe718-112">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe718-113">Puntatore all'handle di contesto alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="fe718-113">Pointer to the context handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe718-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe718-114">Return value</span></span>

<span data-ttu-id="fe718-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="fe718-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fe718-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fe718-116">Return code</span></span>                                                                                  | <span data-ttu-id="fe718-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe718-117">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="fe718-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe718-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fe718-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="fe718-119">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="fe718-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fe718-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fe718-121">Il parametro *pContext* non è valido.</span><span class="sxs-lookup"><span data-stu-id="fe718-121">The *pContext* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="fe718-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="fe718-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="fe718-123">Un puntatore errato è stato passato in *pContext*.</span><span class="sxs-lookup"><span data-stu-id="fe718-123">A bad pointer was passed in *pContext*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe718-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe718-124">Remarks</span></span>

<span data-ttu-id="fe718-125">Il contesto di Resource Manager viene impostato chiamando la funzione [*Smart Card*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span><span class="sxs-lookup"><span data-stu-id="fe718-125">The resource manager context is set by calling the [*smart card*](../secgloss/s-gly.md) function [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span></span>

<span data-ttu-id="fe718-126">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fe718-126">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fe718-127">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fe718-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fe718-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="fe718-128">Examples</span></span>

<span data-ttu-id="fe718-129">L'esempio seguente mostra come recuperare l'handle di contesto corrente di [*Resource Manager*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fe718-129">The following example shows retrieving the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span>


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a><span data-ttu-id="fe718-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe718-130">Requirements</span></span>



| <span data-ttu-id="fe718-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe718-131">Requirement</span></span> | <span data-ttu-id="fe718-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fe718-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe718-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe718-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fe718-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fe718-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fe718-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe718-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fe718-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe718-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fe718-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fe718-137">End of client support</span></span><br/>    | <span data-ttu-id="fe718-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe718-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fe718-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fe718-139">End of server support</span></span><br/>    | <span data-ttu-id="fe718-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe718-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fe718-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe718-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe718-142"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe718-142"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe718-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fe718-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="fe718-144"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fe718-144"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fe718-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fe718-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe718-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe718-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe718-147">IID</span><span class="sxs-lookup"><span data-stu-id="fe718-147">IID</span></span><br/>                      | <span data-ttu-id="fe718-148">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fe718-148">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fe718-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe718-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe718-150">**Ottieni \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="fe718-150">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="fe718-151">**ottenere \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="fe718-151">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="fe718-152">**ottenere il \_ protocollo**</span><span class="sxs-lookup"><span data-stu-id="fe718-152">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="fe718-153">**ottenere \_ lo stato**</span><span class="sxs-lookup"><span data-stu-id="fe718-153">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="fe718-154">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="fe718-154">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="fe718-155">**SCardEstablishContext**</span><span class="sxs-lookup"><span data-stu-id="fe718-155">**SCardEstablishContext**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
