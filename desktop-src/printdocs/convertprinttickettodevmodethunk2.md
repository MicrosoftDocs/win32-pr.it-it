---
description: Converte un ticket di stampa in una struttura DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057907"
---
# <a name="convertprinttickettodevmodethunk2-function"></a><span data-ttu-id="65b36-103">ConvertPrintTicketToDevModeThunk2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="65b36-103">ConvertPrintTicketToDevModeThunk2 function</span></span>

<span data-ttu-id="65b36-104">\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="65b36-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="65b36-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="65b36-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="65b36-106">Converte un ticket di stampa in una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="65b36-106">Converts a print ticket to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b36-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65b36-107">Syntax</span></span>


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a><span data-ttu-id="65b36-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="65b36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b36-109">*hProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65b36-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b36-110">Handle per un provider di ticket di stampa aperto.</span><span class="sxs-lookup"><span data-stu-id="65b36-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="65b36-111">Questo handle viene restituito dalla funzione [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="65b36-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="65b36-112">*pPrintTicket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65b36-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b36-113">Buffer che contiene il ticket di stampa da convertire.</span><span class="sxs-lookup"><span data-stu-id="65b36-113">The buffer that contains the print ticket to convert.</span></span>

</dd> <dt>

<span data-ttu-id="65b36-114">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65b36-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b36-115">Dimensione, in byte, del buffer passato in *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="65b36-115">The size, in bytes, of the buffer passed in *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="65b36-116">*baseType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65b36-116">*baseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b36-117">Valore che indica se l'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predefinito dell'utente o l'oggetto **DEVMODE** della coda di stampa viene utilizzato per fornire i valori alla **DEVMODE** di output quando *pPrintTicket* non specifica tutte le impostazioni possibili per un oggetto **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="65b36-117">A value indicating whether the user's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) or the print queue's default **DEVMODE** is used to provide values to the output **DEVMODE** when *pPrintTicket* does not specify every possible setting for a **DEVMODE**.</span></span> <span data-ttu-id="65b36-118">Il valore di questo parametro deve essere un membro dell'enumerazione [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , di cui è stato eseguito il cast come **int**.</span><span class="sxs-lookup"><span data-stu-id="65b36-118">The value of this parameter must be a member of the [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) enumeration, cast as an **INT**.</span></span>

</dd> <dt>

<span data-ttu-id="65b36-119">*ambito* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65b36-119">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b36-120">Valore che specifica l'ambito di *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="65b36-120">A value that specifies the scope of *pPrintTicket*.</span></span> <span data-ttu-id="65b36-121">Questo valore può specificare una singola pagina, un intero documento o tutti i documenti nel processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="65b36-121">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="65b36-122">Il valore di questo parametro deve essere un membro dell'enumerazione [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , di cui è stato eseguito il cast come **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="65b36-122">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="65b36-123">*ppDevmode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65b36-123">*ppDevmode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65b36-124">Indirizzo dell'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)appena creato.</span><span class="sxs-lookup"><span data-stu-id="65b36-124">The address of the newly created [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span> <span data-ttu-id="65b36-125">Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il buffer.</span><span class="sxs-lookup"><span data-stu-id="65b36-125">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="65b36-126">Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="65b36-126">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="65b36-127">*pcbDevModeLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65b36-127">*pcbDevModeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65b36-128">Dimensione, in byte, dell'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituito in *ppDevmode*.</span><span class="sxs-lookup"><span data-stu-id="65b36-128">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) returned in *ppDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="65b36-129">*errmsg* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="65b36-129">*errMsg* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65b36-130">Puntatore a una stringa che specifica il valore che, se presente, non è valido per il ticket di stampa in *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="65b36-130">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pPrintTicket*.</span></span> <span data-ttu-id="65b36-131">Se è valido, questo valore è **null**.</span><span class="sxs-lookup"><span data-stu-id="65b36-131">If it is valid, this is **NULL**.</span></span> <span data-ttu-id="65b36-132">Se *errmsg* è diverso da **null** quando la funzione restituisce, il chiamante deve liberare la stringa con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="65b36-132">If *errMsg* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b36-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65b36-133">Return value</span></span>

<span data-ttu-id="65b36-134">Se il metodo ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65b36-134">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="65b36-135">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="65b36-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65b36-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65b36-136">Requirements</span></span>



| <span data-ttu-id="65b36-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b36-137">Requirement</span></span> | <span data-ttu-id="65b36-138">Valore</span><span class="sxs-lookup"><span data-stu-id="65b36-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65b36-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65b36-139">Minimum supported client</span></span><br/> | <span data-ttu-id="65b36-140">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="65b36-140">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="65b36-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65b36-141">Minimum supported server</span></span><br/> | <span data-ttu-id="65b36-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65b36-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="65b36-143">DLL</span><span class="sxs-lookup"><span data-stu-id="65b36-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b36-144"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b36-144"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b36-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65b36-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b36-146">Stampa schema</span><span class="sxs-lookup"><span data-stu-id="65b36-146">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="65b36-147">**PTConvertPrintTicketToDevMode**</span><span class="sxs-lookup"><span data-stu-id="65b36-147">**PTConvertPrintTicketToDevMode**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[<span data-ttu-id="65b36-148">Stampa</span><span class="sxs-lookup"><span data-stu-id="65b36-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="65b36-149">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="65b36-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

