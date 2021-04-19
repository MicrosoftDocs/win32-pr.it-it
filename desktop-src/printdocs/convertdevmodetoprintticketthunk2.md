---
description: Converte una struttura DEVMODE in un Print Ticket.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311556"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a><span data-ttu-id="0cde1-103">ConvertDevModeToPrintTicketThunk2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="0cde1-103">ConvertDevModeToPrintTicketThunk2 function</span></span>

<span data-ttu-id="0cde1-104">\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="0cde1-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="0cde1-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="0cde1-106">Converte una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in un Print Ticket.</span><span class="sxs-lookup"><span data-stu-id="0cde1-106">Converts a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to a print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cde1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cde1-107">Syntax</span></span>


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a><span data-ttu-id="0cde1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cde1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cde1-109">*hProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cde1-110">Handle per un provider di ticket di stampa aperto.</span><span class="sxs-lookup"><span data-stu-id="0cde1-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="0cde1-111">Questo handle viene restituito dalla funzione [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="0cde1-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0cde1-112">*pDevmode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-112">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cde1-113">Puntatore alla [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) da convertire.</span><span class="sxs-lookup"><span data-stu-id="0cde1-113">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to convert.</span></span>

</dd> <dt>

<span data-ttu-id="0cde1-114">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cde1-115">Dimensione, in byte, del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passato in *pDevmode*.</span><span class="sxs-lookup"><span data-stu-id="0cde1-115">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="0cde1-116">*ambito* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-116">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cde1-117">Valore che specifica l'ambito di *ppPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="0cde1-117">A value that specifies the scope of *ppPrintTicket*.</span></span> <span data-ttu-id="0cde1-118">Questo valore può specificare una singola pagina, un intero documento o tutti i documenti nel processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="0cde1-118">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="0cde1-119">Il valore di questo parametro deve essere un membro dell'enumerazione [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , di cui è stato eseguito il cast come **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="0cde1-119">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="0cde1-120">*ppPrintTicket* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-120">*ppPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cde1-121">Indirizzo del buffer contenente un ticket di stampa che rappresenta l'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passato in *pDevmode*.</span><span class="sxs-lookup"><span data-stu-id="0cde1-121">The address of the buffer that contains a print ticket that represents the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span> <span data-ttu-id="0cde1-122">Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il buffer.</span><span class="sxs-lookup"><span data-stu-id="0cde1-122">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="0cde1-123">Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="0cde1-123">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="0cde1-124">*pcbPrintTicketLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-124">*pcbPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cde1-125">Dimensione, in byte, del ticket di stampa restituito in *ppPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="0cde1-125">The size, in bytes, of the print ticket returned in *ppPrintTicket*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cde1-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cde1-126">Return value</span></span>

<span data-ttu-id="0cde1-127">Se il metodo ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cde1-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="0cde1-128">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="0cde1-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cde1-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cde1-129">Requirements</span></span>



| <span data-ttu-id="0cde1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cde1-130">Requirement</span></span> | <span data-ttu-id="0cde1-131">Valore</span><span class="sxs-lookup"><span data-stu-id="0cde1-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cde1-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cde1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0cde1-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0cde1-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cde1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0cde1-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0cde1-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0cde1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0cde1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cde1-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cde1-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cde1-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cde1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cde1-139">Stampa schema</span><span class="sxs-lookup"><span data-stu-id="0cde1-139">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="0cde1-140">**PTConvertDevModeToPrintTicket**</span><span class="sxs-lookup"><span data-stu-id="0cde1-140">**PTConvertDevModeToPrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[<span data-ttu-id="0cde1-141">Stampa</span><span class="sxs-lookup"><span data-stu-id="0cde1-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0cde1-142">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="0cde1-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

