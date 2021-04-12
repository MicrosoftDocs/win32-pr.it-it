---
description: Il metodo di riconnessione Reimposta o reinizializza la smart card.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'Metodo IsValid:: reconnettite (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226605"
---
# <a name="iscardreattach-method"></a><span data-ttu-id="f3acc-103">Metodo IsValid:: reconnetti</span><span class="sxs-lookup"><span data-stu-id="f3acc-103">ISCard::ReAttach method</span></span>

<span data-ttu-id="f3acc-104">\[Il metodo di **riconnessione** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="f3acc-104">\[The **ReAttach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f3acc-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f3acc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f3acc-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f3acc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f3acc-107">Il metodo di **riconnessione** Reimposta o reinizializza la [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f3acc-107">The **ReAttach** method resets, or reinitializes, the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3acc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3acc-108">Syntax</span></span>


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a><span data-ttu-id="f3acc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3acc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3acc-110">*SHAREMODE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3acc-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3acc-111">Modalità di condivisione o esclusiva della connessione alla smart card.</span><span class="sxs-lookup"><span data-stu-id="f3acc-111">Mode in which to share or exclusively own the connection to the smart card.</span></span>



| <span data-ttu-id="f3acc-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f3acc-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="f3acc-113">Significato</span><span class="sxs-lookup"><span data-stu-id="f3acc-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="f3acc-114"><dt>**ESCLUSIVO**</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="f3acc-115">Nessun altro usa questa connessione alla smart card.</span><span class="sxs-lookup"><span data-stu-id="f3acc-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="f3acc-116"><dt>**CONDIVISO**</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="f3acc-117">Questa connessione può essere utilizzata da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f3acc-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="f3acc-118">*InitState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3acc-118">*InitState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3acc-119">Indica le operazioni da eseguire con la scheda.</span><span class="sxs-lookup"><span data-stu-id="f3acc-119">Indicates what to do with the card.</span></span>



| <span data-ttu-id="f3acc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f3acc-120">Value</span></span>                                                                                                                                      | <span data-ttu-id="f3acc-121">Significato</span><span class="sxs-lookup"><span data-stu-id="f3acc-121">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="f3acc-122"><dt>**LASCIARE**</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-122"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="f3acc-123">Lascia la smart card nello [*stato*](../secgloss/s-gly.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="f3acc-123">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="f3acc-124"><dt>**REIMPOSTAZIONE**</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-124"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="f3acc-125">Reimposta la smart card in uno stato noto.</span><span class="sxs-lookup"><span data-stu-id="f3acc-125">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="f3acc-126"><dt>**Non alimentato**</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-126"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="f3acc-127">Rimuove l'alimentazione dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="f3acc-127">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="f3acc-128"><dt>**EJECT**</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-128"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="f3acc-129">Espelle la smart card se il lettore dispone di funzionalità di espulsione.</span><span class="sxs-lookup"><span data-stu-id="f3acc-129">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3acc-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3acc-130">Return value</span></span>

<span data-ttu-id="f3acc-131">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3acc-131">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f3acc-132">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f3acc-132">Return code</span></span>                                                                                  | <span data-ttu-id="f3acc-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3acc-133">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3acc-134"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-134"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f3acc-135">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="f3acc-135">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="f3acc-136"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-136"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f3acc-137">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="f3acc-137">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3acc-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3acc-138">Remarks</span></span>

<span data-ttu-id="f3acc-139">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="f3acc-139">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f3acc-140">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f3acc-140">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f3acc-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="f3acc-141">Examples</span></span>

<span data-ttu-id="f3acc-142">Nell'esempio seguente viene illustrata la reinizializzazione della smart card.</span><span class="sxs-lookup"><span data-stu-id="f3acc-142">The following example shows reinitializing the smart card.</span></span>


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="f3acc-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3acc-143">Requirements</span></span>



| <span data-ttu-id="f3acc-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3acc-144">Requirement</span></span> | <span data-ttu-id="f3acc-145">Valore</span><span class="sxs-lookup"><span data-stu-id="f3acc-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3acc-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3acc-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f3acc-147">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f3acc-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f3acc-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3acc-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f3acc-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3acc-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3acc-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f3acc-150">End of client support</span></span><br/>    | <span data-ttu-id="f3acc-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3acc-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f3acc-152">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f3acc-152">End of server support</span></span><br/>    | <span data-ttu-id="f3acc-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3acc-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f3acc-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3acc-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3acc-155"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-155"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3acc-156">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f3acc-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="f3acc-157"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-157"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f3acc-158">DLL</span><span class="sxs-lookup"><span data-stu-id="f3acc-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3acc-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3acc-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f3acc-160">IID</span><span class="sxs-lookup"><span data-stu-id="f3acc-160">IID</span></span><br/>                      | <span data-ttu-id="f3acc-161">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f3acc-161">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f3acc-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3acc-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3acc-163">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="f3acc-163">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="f3acc-164">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="f3acc-164">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="f3acc-165">**Scollegare**</span><span class="sxs-lookup"><span data-stu-id="f3acc-165">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="f3acc-166">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="f3acc-166">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
