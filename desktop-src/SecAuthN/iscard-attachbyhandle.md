---
description: Connette l'oggetto scheda a un handle di smart card aperto e configurato.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'Metodo IsValid:: AttachByHandle (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317068"
---
# <a name="iscardattachbyhandle-method"></a><span data-ttu-id="2e6a2-103">Metodo IsValid:: AttachByHandle</span><span class="sxs-lookup"><span data-stu-id="2e6a2-103">ISCard::AttachByHandle method</span></span>

<span data-ttu-id="2e6a2-104">\[Il metodo **AttachByHandle** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2e6a2-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2e6a2-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2e6a2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2e6a2-107">Il metodo **AttachByHandle** connette l'oggetto di [**scheda**](iscard.md) a un handle di [*Smart Card*](../secgloss/s-gly.md) aperto e configurato.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-107">The **AttachByHandle** method attaches the [**ISCard**](iscard.md) object to an open and configured [*smart card*](../secgloss/s-gly.md) handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e6a2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e6a2-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a><span data-ttu-id="2e6a2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e6a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e6a2-110">*hCard* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e6a2-110">*hCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e6a2-111">Handle per una connessione aperta a una smart card.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-111">A handle to an open connection to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e6a2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e6a2-112">Return value</span></span>

<span data-ttu-id="2e6a2-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2e6a2-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2e6a2-114">Return code</span></span>                                                                                  | <span data-ttu-id="2e6a2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e6a2-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="2e6a2-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2e6a2-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2e6a2-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="2e6a2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2e6a2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2e6a2-119">Il parametro *hCard* non è valido.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-119">The *hCard* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e6a2-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e6a2-120">Remarks</span></span>

<span data-ttu-id="2e6a2-121">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-121">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2e6a2-122">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2e6a2-122">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="2e6a2-123">Al termine dell'utilizzo dell'handle, rilasciare l'allegato chiamando il metodo [**etach::D**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="2e6a2-123">When you have finished using the handle, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2e6a2-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="2e6a2-124">Examples</span></span>

<span data-ttu-id="2e6a2-125">Nell'esempio seguente viene illustrata la connessione a un handle di smart card.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-125">The following example shows attaching to a smart card handle.</span></span>


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a><span data-ttu-id="2e6a2-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e6a2-126">Requirements</span></span>



| <span data-ttu-id="2e6a2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e6a2-127">Requirement</span></span> | <span data-ttu-id="2e6a2-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2e6a2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6a2-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e6a2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2e6a2-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2e6a2-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2e6a2-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e6a2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2e6a2-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e6a2-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e6a2-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2e6a2-133">End of client support</span></span><br/>    | <span data-ttu-id="2e6a2-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e6a2-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2e6a2-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2e6a2-135">End of server support</span></span><br/>    | <span data-ttu-id="2e6a2-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e6a2-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2e6a2-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e6a2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e6a2-138"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e6a2-138"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e6a2-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2e6a2-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e6a2-140"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2e6a2-140"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2e6a2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2e6a2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e6a2-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e6a2-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2e6a2-143">IID</span><span class="sxs-lookup"><span data-stu-id="2e6a2-143">IID</span></span><br/>                      | <span data-ttu-id="2e6a2-144">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2e6a2-144">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2e6a2-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e6a2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6a2-146">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="2e6a2-146">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="2e6a2-147">**Scollegare**</span><span class="sxs-lookup"><span data-stu-id="2e6a2-147">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="2e6a2-148">**ottenere \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="2e6a2-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="2e6a2-149">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="2e6a2-149">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="2e6a2-150">**Ricollegare**</span><span class="sxs-lookup"><span data-stu-id="2e6a2-150">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
