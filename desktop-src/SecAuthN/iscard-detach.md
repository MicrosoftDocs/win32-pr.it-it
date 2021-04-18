---
description: Chiude la connessione aperta alla smart card.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: Scheda::D Metodo etach (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317066"
---
# <a name="iscarddetach-method"></a><span data-ttu-id="a0af9-103">Scheda::D Metodo etach</span><span class="sxs-lookup"><span data-stu-id="a0af9-103">ISCard::Detach method</span></span>

<span data-ttu-id="a0af9-104">\[Il metodo **Detach** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a0af9-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a0af9-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a0af9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0af9-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a0af9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a0af9-107">Il metodo **Detach** chiude la connessione aperta alla [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a0af9-107">The **Detach** method closes the open connection to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0af9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0af9-108">Syntax</span></span>


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="a0af9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0af9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0af9-110">*Disposizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0af9-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0af9-111">Indica le operazioni da eseguire con la scheda del [*lettore*](../secgloss/r-gly.md)connesso.</span><span class="sxs-lookup"><span data-stu-id="a0af9-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="a0af9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a0af9-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="a0af9-113">Significato</span><span class="sxs-lookup"><span data-stu-id="a0af9-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="a0af9-114"><dt>**LASCIARE**</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="a0af9-115">Lascia la smart card nello [*stato*](../secgloss/s-gly.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="a0af9-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="a0af9-116"><dt>**REIMPOSTAZIONE**</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="a0af9-117">Reimposta la smart card in uno stato noto.</span><span class="sxs-lookup"><span data-stu-id="a0af9-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="a0af9-118"><dt>**Non alimentato**</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="a0af9-119">Rimuove l'alimentazione dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="a0af9-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="a0af9-120"><dt>**EJECT**</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="a0af9-121">Espelle la smart card se il lettore dispone di funzionalità di espulsione.</span><span class="sxs-lookup"><span data-stu-id="a0af9-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0af9-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0af9-122">Return value</span></span>

<span data-ttu-id="a0af9-123">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0af9-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a0af9-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a0af9-124">Return code</span></span>                                                                                  | <span data-ttu-id="a0af9-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0af9-125">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a0af9-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a0af9-127">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a0af9-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a0af9-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a0af9-129">*Disposizione* non valida.</span><span class="sxs-lookup"><span data-stu-id="a0af9-129">*Disposition* is not valid.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="a0af9-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0af9-130">Remarks</span></span>

<span data-ttu-id="a0af9-131">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a0af9-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a0af9-132">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a0af9-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a0af9-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="a0af9-133">Examples</span></span>

<span data-ttu-id="a0af9-134">Nell'esempio seguente viene illustrata la chiusura della connessione alla smart card.</span><span class="sxs-lookup"><span data-stu-id="a0af9-134">The following example shows closing the connection to the smart card.</span></span>


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a0af9-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0af9-135">Requirements</span></span>



| <span data-ttu-id="a0af9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0af9-136">Requirement</span></span> | <span data-ttu-id="a0af9-137">Valore</span><span class="sxs-lookup"><span data-stu-id="a0af9-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0af9-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0af9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a0af9-139">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0af9-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a0af9-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0af9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a0af9-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0af9-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0af9-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a0af9-142">End of client support</span></span><br/>    | <span data-ttu-id="a0af9-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0af9-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a0af9-144">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a0af9-144">End of server support</span></span><br/>    | <span data-ttu-id="a0af9-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0af9-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a0af9-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0af9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0af9-147"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0af9-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a0af9-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0af9-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a0af9-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a0af9-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0af9-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0af9-152">IID</span><span class="sxs-lookup"><span data-stu-id="a0af9-152">IID</span></span><br/>                      | <span data-ttu-id="a0af9-153">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a0af9-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a0af9-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0af9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0af9-155">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="a0af9-155">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="a0af9-156">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="a0af9-156">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="a0af9-157">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="a0af9-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="a0af9-158">**Ricollegare**</span><span class="sxs-lookup"><span data-stu-id="a0af9-158">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
