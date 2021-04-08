---
description: Il metodo AttachByReader apre la smart card nel lettore denominato.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'Metodo IsValid:: AttachByReader (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968292"
---
# <a name="iscardattachbyreader-method"></a><span data-ttu-id="ff52f-103">Metodo IsValid:: AttachByReader</span><span class="sxs-lookup"><span data-stu-id="ff52f-103">ISCard::AttachByReader method</span></span>

<span data-ttu-id="ff52f-104">\[Il metodo **AttachByReader** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ff52f-104">\[The **AttachByReader** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ff52f-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ff52f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ff52f-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ff52f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ff52f-107">Il metodo **AttachByReader** apre la [*Smart Card*](../secgloss/s-gly.md) nel [*lettore*](../secgloss/r-gly.md)denominato.</span><span class="sxs-lookup"><span data-stu-id="ff52f-107">The **AttachByReader** method opens the [*smart card*](../secgloss/s-gly.md) in the named [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff52f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff52f-108">Syntax</span></span>


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="ff52f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff52f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff52f-110">*bstrReaderName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff52f-110">*bstrReaderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff52f-111">**BSTR** che contiene il nome del lettore di smart card.</span><span class="sxs-lookup"><span data-stu-id="ff52f-111">A **BSTR** that contains the name of the smart card reader.</span></span>

</dd> <dt>

<span data-ttu-id="ff52f-112">*SHAREMODE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff52f-112">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff52f-113">Modalità in cui richiedere l'accesso alla smart card.</span><span class="sxs-lookup"><span data-stu-id="ff52f-113">Mode in which to claim access to the smart card.</span></span>



| <span data-ttu-id="ff52f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ff52f-114">Value</span></span>                                                                                                                                            | <span data-ttu-id="ff52f-115">Significato</span><span class="sxs-lookup"><span data-stu-id="ff52f-115">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="ff52f-116"><dt>**ESCLUSIVO**</dt></span><span class="sxs-lookup"><span data-stu-id="ff52f-116"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="ff52f-117">Nessun altro usa questa connessione alla smart card.</span><span class="sxs-lookup"><span data-stu-id="ff52f-117">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="ff52f-118"><dt>**CONDIVISO**</dt></span><span class="sxs-lookup"><span data-stu-id="ff52f-118"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="ff52f-119">Questa connessione può essere utilizzata da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ff52f-119">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="ff52f-120">*PrefProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff52f-120">*PrefProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff52f-121">Valore del protocollo preferito.</span><span class="sxs-lookup"><span data-stu-id="ff52f-121">Preferred protocol value.</span></span>

<dl><span id="T0"></span><span id="t0"></span><dt>

<span data-ttu-id="ff52f-122">**T0**</span><span class="sxs-lookup"><span data-stu-id="ff52f-122">**T0**</span></span>
</dt><span id="T1"></span><span id="t1"></span><dt>

<span data-ttu-id="ff52f-123">**T1**</span><span class="sxs-lookup"><span data-stu-id="ff52f-123">**T1**</span></span>
</dt><span id="RAW"></span><span id="raw"></span><dt>

<span data-ttu-id="ff52f-124">**RAW**</span><span class="sxs-lookup"><span data-stu-id="ff52f-124">**RAW**</span></span>
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

<span data-ttu-id="ff52f-125">**T0 \| T1**</span><span class="sxs-lookup"><span data-stu-id="ff52f-125">**T0\|T1**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff52f-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff52f-126">Return value</span></span>

<span data-ttu-id="ff52f-127">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="ff52f-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ff52f-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ff52f-128">Return code</span></span>                                                                                  | <span data-ttu-id="ff52f-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff52f-129">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff52f-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ff52f-130"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ff52f-131">L'apertura della smart card nel lettore denominato è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ff52f-131">Open on the smart card in the named reader has been completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="ff52f-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ff52f-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ff52f-133">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="ff52f-133">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ff52f-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff52f-134">Remarks</span></span>

<span data-ttu-id="ff52f-135">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ff52f-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ff52f-136">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ff52f-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="ff52f-137">Al termine dell'utilizzo del lettore, rilasciare l'allegato chiamando il metodo [**etach::D**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="ff52f-137">When you have finished using the reader, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="ff52f-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff52f-138">Examples</span></span>

<span data-ttu-id="ff52f-139">Nell'esempio seguente viene illustrata la connessione a una smart card in un lettore di smart card specificato.</span><span class="sxs-lookup"><span data-stu-id="ff52f-139">The following example shows attaching to a smart card in a specified smart card reader.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a><span data-ttu-id="ff52f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff52f-140">Requirements</span></span>



| <span data-ttu-id="ff52f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff52f-141">Requirement</span></span> | <span data-ttu-id="ff52f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ff52f-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff52f-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff52f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ff52f-144">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ff52f-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ff52f-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff52f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ff52f-146">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ff52f-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff52f-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ff52f-147">End of client support</span></span><br/>    | <span data-ttu-id="ff52f-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff52f-148">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ff52f-149">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ff52f-149">End of server support</span></span><br/>    | <span data-ttu-id="ff52f-150">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff52f-150">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ff52f-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff52f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff52f-152"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff52f-152"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff52f-153">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ff52f-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff52f-154"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ff52f-154"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ff52f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="ff52f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff52f-156"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff52f-156"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff52f-157">IID</span><span class="sxs-lookup"><span data-stu-id="ff52f-157">IID</span></span><br/>                      | <span data-ttu-id="ff52f-158">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ff52f-158">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ff52f-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff52f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff52f-160">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="ff52f-160">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="ff52f-161">**Scollegare**</span><span class="sxs-lookup"><span data-stu-id="ff52f-161">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="ff52f-162">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="ff52f-162">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="ff52f-163">**Ricollegare**</span><span class="sxs-lookup"><span data-stu-id="ff52f-163">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
