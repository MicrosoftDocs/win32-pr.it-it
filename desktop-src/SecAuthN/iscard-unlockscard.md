---
description: Rilascia accesso esclusivo alla smart card.
ms.assetid: 12256c91-faf2-4a06-9501-f00d0115a069
title: 'Metodo IsValid:: UnlockSCard (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.UnlockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 68907e157e60518d1df3855fbca69709f2c21437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754186"
---
# <a name="iscardunlockscard-method"></a><span data-ttu-id="5a23c-103">Metodo IsValid:: UnlockSCard</span><span class="sxs-lookup"><span data-stu-id="5a23c-103">ISCard::UnlockSCard method</span></span>

<span data-ttu-id="5a23c-104">\[Il metodo **UnlockScard** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="5a23c-104">\[The **UnlockScard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5a23c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5a23c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a23c-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="5a23c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5a23c-107">Il metodo **UnlockScard** rilascia l'accesso esclusivo alla [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5a23c-107">The **UnlockScard** method releases exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a23c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a23c-108">Syntax</span></span>


```C++
HRESULT UnlockSCard(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="5a23c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a23c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a23c-110">*Disposizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a23c-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a23c-111">Indica le operazioni da eseguire con la scheda del [*lettore*](../secgloss/r-gly.md)connesso.</span><span class="sxs-lookup"><span data-stu-id="5a23c-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="5a23c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5a23c-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="5a23c-113">Significato</span><span class="sxs-lookup"><span data-stu-id="5a23c-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="5a23c-114"><dt>**LASCIARE**</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="5a23c-115">Lascia la smart card nello [*stato*](../secgloss/s-gly.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="5a23c-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="5a23c-116"><dt>**REIMPOSTAZIONE**</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="5a23c-117">Reimposta la smart card in uno stato noto.</span><span class="sxs-lookup"><span data-stu-id="5a23c-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="5a23c-118"><dt>**Non alimentato**</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="5a23c-119">Rimuove l'alimentazione dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="5a23c-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="5a23c-120"><dt>**EJECT**</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="5a23c-121">Espelle la smart card se il lettore dispone di funzionalità di espulsione.</span><span class="sxs-lookup"><span data-stu-id="5a23c-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a23c-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a23c-122">Return value</span></span>

<span data-ttu-id="5a23c-123">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a23c-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5a23c-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a23c-124">Return code</span></span>                                                                                  | <span data-ttu-id="5a23c-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a23c-125">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="5a23c-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5a23c-127">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="5a23c-127">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="5a23c-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5a23c-129">Il parametro *Disposition* non è valido</span><span class="sxs-lookup"><span data-stu-id="5a23c-129">The *Disposition* parameter is not valid</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a23c-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a23c-130">Remarks</span></span>

<span data-ttu-id="5a23c-131">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5a23c-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5a23c-132">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5a23c-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5a23c-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="5a23c-133">Examples</span></span>

<span data-ttu-id="5a23c-134">Nell'esempio seguente viene illustrato il rilascio dell'accesso esclusivo alla smart card.</span><span class="sxs-lookup"><span data-stu-id="5a23c-134">The following example shows releasing exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Unlock the smart card.
hr = pISCard->UnlockSCard(LEAVE);
if (FAILED(hr))
{
   printf("Failed UnlockSCard\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="5a23c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a23c-135">Requirements</span></span>



| <span data-ttu-id="5a23c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a23c-136">Requirement</span></span> | <span data-ttu-id="5a23c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5a23c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a23c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a23c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5a23c-139">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5a23c-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5a23c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a23c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5a23c-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a23c-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5a23c-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5a23c-142">End of client support</span></span><br/>    | <span data-ttu-id="5a23c-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a23c-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5a23c-144">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5a23c-144">End of server support</span></span><br/>    | <span data-ttu-id="5a23c-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a23c-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5a23c-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a23c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a23c-147"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a23c-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5a23c-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a23c-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5a23c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5a23c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a23c-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a23c-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a23c-152">IID</span><span class="sxs-lookup"><span data-stu-id="5a23c-152">IID</span></span><br/>                      | <span data-ttu-id="5a23c-153">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5a23c-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5a23c-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a23c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a23c-155">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="5a23c-155">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="5a23c-156">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="5a23c-156">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> </dl>

 

 
