---
description: Rilascia un oggetto di output protetto.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: DestroyOPMProtectedOutput (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 0a7ce8551cc5e01e7a2801dd129d5dc6903af697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305411"
---
# <a name="destroyopmprotectedoutput-function"></a><span data-ttu-id="f00d1-103">DestroyOPMProtectedOutput (funzione)</span><span class="sxs-lookup"><span data-stu-id="f00d1-103">DestroyOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f00d1-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f00d1-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="f00d1-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="f00d1-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="f00d1-106">Rilascia un oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="f00d1-106">Releases a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f00d1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f00d1-107">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a><span data-ttu-id="f00d1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f00d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f00d1-109">*opoOPMProtectedOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f00d1-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f00d1-110">Handle per l'oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="f00d1-110">A handle to the protected output object.</span></span> <span data-ttu-id="f00d1-111">Questo handle viene ottenuto chiamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="f00d1-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f00d1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f00d1-112">Return value</span></span>

<span data-ttu-id="f00d1-113">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="f00d1-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="f00d1-114">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="f00d1-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f00d1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f00d1-115">Remarks</span></span>

<span data-ttu-id="f00d1-116">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="f00d1-116">This function has no associated import library.</span></span> <span data-ttu-id="f00d1-117">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="f00d1-117">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f00d1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f00d1-118">Requirements</span></span>



| <span data-ttu-id="f00d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f00d1-119">Requirement</span></span> | <span data-ttu-id="f00d1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f00d1-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f00d1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f00d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f00d1-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f00d1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f00d1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f00d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f00d1-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f00d1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f00d1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f00d1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f00d1-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f00d1-126"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f00d1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f00d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f00d1-128">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="f00d1-128">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="f00d1-129">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="f00d1-129">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
