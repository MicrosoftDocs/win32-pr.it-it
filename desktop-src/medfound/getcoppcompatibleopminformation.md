---
description: Invia una richiesta di stato COPP (Certified Output Protocol) a un oggetto di output protetto.
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: GetCOPPCompatibleOPMInformation (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225802"
---
# <a name="getcoppcompatibleopminformation-function"></a><span data-ttu-id="da86b-103">GetCOPPCompatibleOPMInformation (funzione)</span><span class="sxs-lookup"><span data-stu-id="da86b-103">GetCOPPCompatibleOPMInformation function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da86b-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="da86b-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="da86b-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="da86b-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="da86b-106">Invia una richiesta di stato COPP (Certified Output Protocol) a un oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="da86b-106">Sends a Certified Output Protection Protocol (COPP) status request to a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="da86b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da86b-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a><span data-ttu-id="da86b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="da86b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da86b-109">*opoOPMProtectedOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da86b-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da86b-110">Handle per l'oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="da86b-110">A handle to the protected output object.</span></span> <span data-ttu-id="da86b-111">Questo handle viene ottenuto chiamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="da86b-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="da86b-112">*pParameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da86b-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da86b-113">Un puntatore a una struttura di **\_ \_ \_ \_ \_ \_ parametri Get Info compatibile con DXGKMDT OPM Copp** che contiene i dati di input per la richiesta di stato.</span><span class="sxs-lookup"><span data-stu-id="da86b-113">A pointer to a **DXGKMDT\_OPM\_COPP\_COMPATIBLE\_GET\_INFO\_PARAMETERS** structure that contains input data for the status request.</span></span>

</dd> <dt>

<span data-ttu-id="da86b-114">*pRequestedInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="da86b-114">*pRequestedInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da86b-115">Puntatore a una struttura **di \_ \_ \_ informazioni richiesta da DXGKMDT OPM** che riceve i risultati della richiesta di stato.</span><span class="sxs-lookup"><span data-stu-id="da86b-115">A pointer to a **DXGKMDT\_OPM\_REQUESTED\_INFORMATION** structure that receives the results of the status request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da86b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da86b-116">Return value</span></span>

<span data-ttu-id="da86b-117">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="da86b-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="da86b-118">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="da86b-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da86b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="da86b-119">Remarks</span></span>

<span data-ttu-id="da86b-120">Le applicazioni devono chiamare [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) anziché chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="da86b-120">Applications should call [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) instead of calling this function.</span></span>

<span data-ttu-id="da86b-121">L'oggetto di output protetto deve essere creato con la semantica COPP.</span><span class="sxs-lookup"><span data-stu-id="da86b-121">The protected output object must be created with COPP semantics.</span></span> <span data-ttu-id="da86b-122">Vedere [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="da86b-122">See [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

<span data-ttu-id="da86b-123">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="da86b-123">This function has no associated import library.</span></span> <span data-ttu-id="da86b-124">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="da86b-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="da86b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da86b-125">Requirements</span></span>



| <span data-ttu-id="da86b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="da86b-126">Requirement</span></span> | <span data-ttu-id="da86b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="da86b-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="da86b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da86b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="da86b-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da86b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="da86b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da86b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="da86b-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da86b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="da86b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="da86b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da86b-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da86b-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da86b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da86b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da86b-135">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="da86b-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="da86b-136">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="da86b-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
