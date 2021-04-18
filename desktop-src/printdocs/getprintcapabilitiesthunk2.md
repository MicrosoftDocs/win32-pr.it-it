---
description: Recupera le funzionalità di stampanti formattate in conformità con lo schema di stampa XML.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313022"
---
# <a name="getprintcapabilitiesthunk2-function"></a><span data-ttu-id="9d897-103">GetPrintCapabilitiesThunk2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="9d897-103">GetPrintCapabilitiesThunk2 function</span></span>

<span data-ttu-id="9d897-104">\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="9d897-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="9d897-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="9d897-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="9d897-106">Recupera le funzionalità della stampante formattate in conformità con lo [schema di stampa](./printschema.md)XML.</span><span class="sxs-lookup"><span data-stu-id="9d897-106">Retrieves the printer's capabilities formatted in compliance with the XML [Print Schema](./printschema.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d897-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d897-107">Syntax</span></span>


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="9d897-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d897-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d897-109">*hProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d897-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d897-110">Handle per un provider di ticket di stampa aperto.</span><span class="sxs-lookup"><span data-stu-id="9d897-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="9d897-111">Questo handle viene restituito dalla funzione [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="9d897-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9d897-112">*pPrintTicket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d897-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d897-113">Buffer che contiene i dati del ticket di stampa, espressi in XML come descritto nello [schema di stampa](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="9d897-113">The buffer that contains the print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d897-114">*cbPrintTicket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d897-114">*cbPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d897-115">Dimensione, in byte, del buffer a cui fa riferimento *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="9d897-115">The size, in bytes, of the buffer referenced by *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="9d897-116">*ppbPrintCapabilities* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d897-116">*ppbPrintCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d897-117">Indirizzo del buffer allocato da questa funzione e contenente le informazioni sulle funzionalità di stampa valide, codificate in formato XML.</span><span class="sxs-lookup"><span data-stu-id="9d897-117">The address of the buffer that is allocated by this function and contains the valid print capabilities information, encoded as XML.</span></span> <span data-ttu-id="9d897-118">Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il buffer.</span><span class="sxs-lookup"><span data-stu-id="9d897-118">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="9d897-119">Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="9d897-119">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="9d897-120">*pcbPrintCapabilitiesLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d897-120">*pcbPrintCapabilitiesLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d897-121">Dimensione, in byte, del buffer a cui fa riferimento *ppbPrintCapabilities*.</span><span class="sxs-lookup"><span data-stu-id="9d897-121">The size, in bytes, of the buffer referenced by *ppbPrintCapabilities*.</span></span>

</dd> <dt>

<span data-ttu-id="9d897-122">*pbstrErrorMessage* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9d897-122">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d897-123">Puntatore a una stringa che specifica l'elemento, se presente, non valido per *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="9d897-123">A pointer to a string that specifies what, if anything, is invalid about *pPrintTicket*.</span></span> <span data-ttu-id="9d897-124">Se è valido, questo valore è **null**.</span><span class="sxs-lookup"><span data-stu-id="9d897-124">If it is valid, this value is **NULL**.</span></span> <span data-ttu-id="9d897-125">Se *pbstrErrorMessage* è diverso da **null** quando la funzione restituisce, il chiamante deve liberare la stringa con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="9d897-125">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d897-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d897-126">Return value</span></span>

<span data-ttu-id="9d897-127">Se il metodo ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d897-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="9d897-128">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="9d897-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d897-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d897-129">Requirements</span></span>



| <span data-ttu-id="9d897-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d897-130">Requirement</span></span> | <span data-ttu-id="9d897-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9d897-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d897-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d897-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9d897-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9d897-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9d897-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d897-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9d897-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d897-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9d897-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9d897-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d897-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d897-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d897-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d897-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d897-139">**PTGetPrintCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9d897-139">**PTGetPrintCapabilities**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[<span data-ttu-id="9d897-140">Stampa schema</span><span class="sxs-lookup"><span data-stu-id="9d897-140">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="9d897-141">Stampa</span><span class="sxs-lookup"><span data-stu-id="9d897-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9d897-142">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="9d897-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

