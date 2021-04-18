---
description: Unisce due ticket di stampa e restituisce un ticket di stampa valido ed valido.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318363"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a><span data-ttu-id="f69da-103">MergeAndValidatePrintTicketThunk2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="f69da-103">MergeAndValidatePrintTicketThunk2 function</span></span>

<span data-ttu-id="f69da-104">\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="f69da-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="f69da-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="f69da-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="f69da-106">Unisce due ticket di stampa e restituisce un ticket di stampa valido ed valido.</span><span class="sxs-lookup"><span data-stu-id="f69da-106">Merges two print tickets and returns a valid, viable print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="f69da-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f69da-107">Syntax</span></span>


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="f69da-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f69da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f69da-109">*hProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f69da-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-110">Handle per un provider di ticket di stampa aperto.</span><span class="sxs-lookup"><span data-stu-id="f69da-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="f69da-111">Questo handle viene restituito dalla funzione [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="f69da-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f69da-112">*pBasePrintTicket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f69da-112">*pBasePrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-113">Buffer che contiene i dati del ticket di stampa di base, espressi in XML come descritto nello [schema di stampa](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="f69da-113">The buffer that contains the base print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="f69da-114">*basePrintTicketLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f69da-114">*basePrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-115">Dimensione, in byte, del buffer a cui fa riferimento *pBasePrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f69da-115">The size, in bytes, of the buffer referenced by *pBasePrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="f69da-116">*pDeltaPrintTicket* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f69da-116">*pDeltaPrintTicket* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-117">Buffer che contiene il ticket di stampa da unire.</span><span class="sxs-lookup"><span data-stu-id="f69da-117">The buffer that contains the print ticket to merge.</span></span> <span data-ttu-id="f69da-118">I dati del ticket di stampa sono espressi in XML come descritto nello [schema di stampa](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="f69da-118">The print ticket data is expressed in XML as described in the [Print Schema](./printschema.md).</span></span> <span data-ttu-id="f69da-119">Il valore di questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="f69da-119">The value of this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f69da-120">*deltaPrintTicketLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f69da-120">*deltaPrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-121">Dimensione, in byte, del buffer a cui fa riferimento *pDeltaPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f69da-121">The size, in bytes, of the buffer referenced by *pDeltaPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="f69da-122">*ambito* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f69da-122">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-123">Valore che specifica se l'ambito di *pDeltaPrintTicket* e *ppValidatedPrintTicket* è una singola pagina, un intero documento o tutti i documenti nel processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f69da-123">The value that specifies whether the scope of *pDeltaPrintTicket* and *ppValidatedPrintTicket* is a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="f69da-124">Il valore di questo parametro deve essere un membro dell'enumerazione [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , di cui è stato eseguito il cast come **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f69da-124">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="f69da-125">*ppValidatedPrintTicket* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f69da-125">*ppValidatedPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-126">Indirizzo del buffer che contiene il Print Ticket Unito e convalidato.</span><span class="sxs-lookup"><span data-stu-id="f69da-126">The address of the buffer that contains the merged and validated print ticket.</span></span> <span data-ttu-id="f69da-127">Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il buffer.</span><span class="sxs-lookup"><span data-stu-id="f69da-127">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="f69da-128">Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f69da-128">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="f69da-129">*pValidatedPrintTicketLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f69da-129">*pValidatedPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-130">Dimensione, in byte, del buffer a cui fa riferimento *ppValidatedPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f69da-130">The size, in bytes, of the buffer referenced by *ppValidatedPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="f69da-131">*pbstrErrorMessage* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f69da-131">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f69da-132">Puntatore a una stringa che specifica l'elemento, se presente, non valido sul ticket di stampa in *pBasePrintTicket* o *pDeltaPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f69da-132">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pBasePrintTicket* or *pDeltaPrintTicket*.</span></span> <span data-ttu-id="f69da-133">Se sono entrambi validi, questo valore è **null**.</span><span class="sxs-lookup"><span data-stu-id="f69da-133">If they are both valid, this value is **NULL**.</span></span> <span data-ttu-id="f69da-134">Se *pbstrErrorMessage* è diverso da **null** quando la funzione restituisce, il chiamante deve liberare la stringa con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="f69da-134">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f69da-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f69da-135">Return value</span></span>

<span data-ttu-id="f69da-136">Se il metodo ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f69da-136">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="f69da-137">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f69da-137">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f69da-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f69da-138">Requirements</span></span>



| <span data-ttu-id="f69da-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f69da-139">Requirement</span></span> | <span data-ttu-id="f69da-140">Valore</span><span class="sxs-lookup"><span data-stu-id="f69da-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f69da-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f69da-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f69da-142">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f69da-142">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f69da-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f69da-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f69da-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f69da-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f69da-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f69da-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f69da-146"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f69da-146"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f69da-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f69da-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f69da-148">Stampa schema</span><span class="sxs-lookup"><span data-stu-id="f69da-148">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="f69da-149">**PTMergeAndValidatePrintTicket**</span><span class="sxs-lookup"><span data-stu-id="f69da-149">**PTMergeAndValidatePrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[<span data-ttu-id="f69da-150">Stampa</span><span class="sxs-lookup"><span data-stu-id="f69da-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f69da-151">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="f69da-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

