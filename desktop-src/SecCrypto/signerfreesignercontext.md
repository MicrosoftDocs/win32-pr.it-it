---
description: Libera una \_ struttura del contesto del firmatario allocata da una chiamata precedente alla funzione SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerContext (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314691"
---
# <a name="signerfreesignercontext-function"></a><span data-ttu-id="1326d-103">SignerFreeSignerContext (funzione)</span><span class="sxs-lookup"><span data-stu-id="1326d-103">SignerFreeSignerContext function</span></span>

<span data-ttu-id="1326d-104">La funzione **SignerFreeSignerContext** libera una struttura del [**\_ contesto del firmatario**](signer-context.md) allocata da una chiamata precedente alla funzione [**SignerSignEx**](signersignex.md) .</span><span class="sxs-lookup"><span data-stu-id="1326d-104">The **SignerFreeSignerContext** function frees a [**SIGNER\_CONTEXT**](signer-context.md) structure allocated by a previous call to the [**SignerSignEx**](signersignex.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="1326d-105">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="1326d-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="1326d-106">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="1326d-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1326d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1326d-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="1326d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1326d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1326d-109">*pSignerContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1326d-109">*pSignerContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1326d-110">Puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) da liberare.</span><span class="sxs-lookup"><span data-stu-id="1326d-110">A pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1326d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1326d-111">Return value</span></span>

<span data-ttu-id="1326d-112">Se la funzione ha esito positivo, la funzione restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1326d-112">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="1326d-113">Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="1326d-113">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="1326d-114">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="1326d-114">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1326d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1326d-115">Requirements</span></span>



| <span data-ttu-id="1326d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1326d-116">Requirement</span></span> | <span data-ttu-id="1326d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1326d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1326d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1326d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1326d-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1326d-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1326d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1326d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1326d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1326d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1326d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1326d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1326d-123"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1326d-123"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1326d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1326d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1326d-125">**contesto del FIRMATARIo \_**</span><span class="sxs-lookup"><span data-stu-id="1326d-125">**SIGNER\_CONTEXT**</span></span>](signer-context.md)
</dt> <dt>

[<span data-ttu-id="1326d-126">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="1326d-126">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
