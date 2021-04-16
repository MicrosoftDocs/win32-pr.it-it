---
description: Crea oggetti di output protetti per un dispositivo di visualizzazione.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: CreateOPMProtectedOutputs (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524618"
---
# <a name="createopmprotectedoutputs-function"></a><span data-ttu-id="9e60b-103">CreateOPMProtectedOutputs (funzione)</span><span class="sxs-lookup"><span data-stu-id="9e60b-103">CreateOPMProtectedOutputs function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e60b-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9e60b-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="9e60b-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9e60b-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="9e60b-106">Crea oggetti di output protetti per un dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9e60b-106">Creates protected output objects for a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e60b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e60b-107">Syntax</span></span>


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a><span data-ttu-id="9e60b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e60b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e60b-109">*pstrDeviceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e60b-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e60b-110">Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9e60b-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="9e60b-111">*vos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e60b-111">*vos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e60b-112">Membro dell'enumerazione **DXGKMDT \_ OPM \_ video \_ output \_ semantica** , che specifica se l'output protetto avrà la semantica COPP (Certified Output Protocol) o la semantica OPM.</span><span class="sxs-lookup"><span data-stu-id="9e60b-112">A member of the **DXGKMDT\_OPM\_VIDEO\_OUTPUT\_SEMANTICS** enumeration, specifying whether the protected output will have Certified Output Protection Protocol (COPP) semantics or OPM semantics.</span></span>

</dd> <dt>

<span data-ttu-id="9e60b-113">*dwOPMProtectedOutputArraySize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e60b-113">*dwOPMProtectedOutputArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e60b-114">Numero di elementi nella matrice *pohOPMProtectedOutputArray* .</span><span class="sxs-lookup"><span data-stu-id="9e60b-114">The number of elements in the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="9e60b-115">*pdwNumOPMProtectedOutputsInArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e60b-115">*pdwNumOPMProtectedOutputsInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e60b-116">Riceve il numero di elementi che la funzione copia nella matrice *pohOPMProtectedOutputArray* .</span><span class="sxs-lookup"><span data-stu-id="9e60b-116">Receives the number of items that the function copies to the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="9e60b-117">*pohOPMProtectedOutputArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e60b-117">*pohOPMProtectedOutputArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e60b-118">Matrice che riceve handle per gli oggetti di output protetti.</span><span class="sxs-lookup"><span data-stu-id="9e60b-118">An array that receives handles to the protected output objects.</span></span> <span data-ttu-id="9e60b-119">Ogni handle deve essere rilasciato chiamando [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span><span class="sxs-lookup"><span data-stu-id="9e60b-119">Each handle must be released by calling [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e60b-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e60b-120">Return value</span></span>

<span data-ttu-id="9e60b-121">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="9e60b-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="9e60b-122">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="9e60b-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e60b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e60b-123">Remarks</span></span>

<span data-ttu-id="9e60b-124">Anziché utilizzare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e60b-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="9e60b-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="9e60b-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [<span data-ttu-id="9e60b-126">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="9e60b-126">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

<span data-ttu-id="9e60b-127">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="9e60b-127">This function has no associated import library.</span></span> <span data-ttu-id="9e60b-128">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="9e60b-128">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e60b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e60b-129">Requirements</span></span>



| <span data-ttu-id="9e60b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e60b-130">Requirement</span></span> | <span data-ttu-id="9e60b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9e60b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9e60b-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e60b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9e60b-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e60b-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9e60b-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e60b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9e60b-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e60b-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9e60b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9e60b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e60b-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e60b-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e60b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e60b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e60b-139">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="9e60b-139">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="9e60b-140">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="9e60b-140">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
