---
description: Configura un oggetto di output protetto.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: ConfigureOPMProtectedOutput (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: d72f3d8bbb7d3063fe6982c6d1de99b2f721f005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401548"
---
# <a name="configureopmprotectedoutput-function"></a><span data-ttu-id="aeab1-103">ConfigureOPMProtectedOutput (funzione)</span><span class="sxs-lookup"><span data-stu-id="aeab1-103">ConfigureOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aeab1-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="aeab1-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="aeab1-106">Configura un oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="aeab1-106">Configures a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeab1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aeab1-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a><span data-ttu-id="aeab1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aeab1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeab1-109">*opoOPMProtectedOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aeab1-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeab1-110">Handle per l'oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="aeab1-110">A handle to the protected output object.</span></span> <span data-ttu-id="aeab1-111">Questo handle viene ottenuto chiamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="aeab1-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeab1-112">*pParameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aeab1-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeab1-113">Puntatore a una struttura **di \_ \_ \_ parametri** di configurazione di DXGKMDT OPM che contiene il comando di configurazione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-113">A pointer to a **DXGKMDT\_OPM\_CONFIGURE\_PARAMETERS** structure that contains the configuration command.</span></span>

</dd> <dt>

<span data-ttu-id="aeab1-114">*ulAdditionalParametersSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aeab1-114">*ulAdditionalParametersSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeab1-115">Dimensioni in byte del buffer *pbAdditionalParameters* .</span><span class="sxs-lookup"><span data-stu-id="aeab1-115">The size of the *pbAdditionalParameters* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aeab1-116">*pbAdditionalParameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aeab1-116">*pbAdditionalParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeab1-117">Puntatore a un buffer che contiene informazioni aggiuntive per il comando.</span><span class="sxs-lookup"><span data-stu-id="aeab1-117">A pointer to a buffer that contains additional information for the command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeab1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aeab1-118">Return value</span></span>

<span data-ttu-id="aeab1-119">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="aeab1-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="aeab1-120">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="aeab1-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeab1-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="aeab1-121">Remarks</span></span>

<span data-ttu-id="aeab1-122">Le applicazioni devono chiamare [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) anziché chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-122">Applications should call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) instead of calling this function.</span></span>

<span data-ttu-id="aeab1-123">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-123">This function has no associated import library.</span></span> <span data-ttu-id="aeab1-124">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="aeab1-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeab1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aeab1-125">Requirements</span></span>



| <span data-ttu-id="aeab1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeab1-126">Requirement</span></span> | <span data-ttu-id="aeab1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="aeab1-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab1-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeab1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aeab1-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aeab1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aeab1-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeab1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aeab1-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aeab1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aeab1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="aeab1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeab1-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeab1-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeab1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aeab1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeab1-135">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="aeab1-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="aeab1-136">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="aeab1-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
