---
description: Ottiene la dimensione della matrice che deve essere allocata prima di chiamare CreateOPMProtectedOutputs.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: GetSuggestedOPMProtectedOutputArraySize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 87139f0b485ef3c01e5196db85b36faeb662e4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127878"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a><span data-ttu-id="30c72-103">GetSuggestedOPMProtectedOutputArraySize (funzione)</span><span class="sxs-lookup"><span data-stu-id="30c72-103">GetSuggestedOPMProtectedOutputArraySize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30c72-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="30c72-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="30c72-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="30c72-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="30c72-106">Ottiene la dimensione della matrice che deve essere allocata prima di chiamare [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="30c72-106">Gets the size of the array that should be allocated before calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30c72-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30c72-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="30c72-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="30c72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c72-109">*pstrDeviceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30c72-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c72-110">Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="30c72-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="30c72-111">*pdwSuggestedOPMProtectedOutputArraySize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30c72-111">*pdwSuggestedOPMProtectedOutputArraySize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30c72-112">Riceve le dimensioni che devono essere allocate per la matrice, in numero di elementi di matrice.</span><span class="sxs-lookup"><span data-stu-id="30c72-112">Receives the size that should be allocated for the array, in number of array elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c72-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30c72-113">Return value</span></span>

<span data-ttu-id="30c72-114">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="30c72-114">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="30c72-115">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="30c72-115">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30c72-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="30c72-116">Remarks</span></span>

<span data-ttu-id="30c72-117">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="30c72-117">This function has no associated import library.</span></span> <span data-ttu-id="30c72-118">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="30c72-118">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="30c72-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30c72-119">Requirements</span></span>



| <span data-ttu-id="30c72-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="30c72-120">Requirement</span></span> | <span data-ttu-id="30c72-121">Valore</span><span class="sxs-lookup"><span data-stu-id="30c72-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30c72-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30c72-122">Minimum supported client</span></span><br/> | <span data-ttu-id="30c72-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30c72-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30c72-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30c72-124">Minimum supported server</span></span><br/> | <span data-ttu-id="30c72-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30c72-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30c72-126">DLL</span><span class="sxs-lookup"><span data-stu-id="30c72-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30c72-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c72-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30c72-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30c72-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c72-129">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="30c72-129">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="30c72-130">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="30c72-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
