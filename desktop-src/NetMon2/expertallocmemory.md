---
description: La funzione ExpertAllocMemory alloca memoria per l'esperto.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Funzione ExpertAllocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750106"
---
# <a name="expertallocmemory-function"></a><span data-ttu-id="51fd8-103">ExpertAllocMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="51fd8-103">ExpertAllocMemory function</span></span>

<span data-ttu-id="51fd8-104">La funzione **ExpertAllocMemory** alloca memoria per l'esperto.</span><span class="sxs-lookup"><span data-stu-id="51fd8-104">The **ExpertAllocMemory** function allocates memory for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fd8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51fd8-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="51fd8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51fd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51fd8-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="51fd8-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="51fd8-108">Identificatore univoco dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="51fd8-108">Unique expert identifier.</span></span> <span data-ttu-id="51fd8-109">Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="51fd8-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="51fd8-110">*nBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51fd8-110">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51fd8-111">Memoria allocata, misurata in byte.</span><span class="sxs-lookup"><span data-stu-id="51fd8-111">Allocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="51fd8-112">*perror* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="51fd8-112">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51fd8-113">Indicatore di errore.</span><span class="sxs-lookup"><span data-stu-id="51fd8-113">Error indicator.</span></span> <span data-ttu-id="51fd8-114">Se la funzione ha esito negativo, il parametro *nBytes* contiene il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="51fd8-114">If the function fails, the *nBytes* parameter contains the error code.</span></span> <span data-ttu-id="51fd8-115">Se il codice di errore è NMERR \_ Expert \_ Terminate, l'esperto deve effettuare la pulizia e restituire immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="51fd8-115">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean-up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51fd8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51fd8-116">Return value</span></span>

<span data-ttu-id="51fd8-117">Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="51fd8-117">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="51fd8-118">Se la funzione ha esito negativo, il valore restituito è **null** e *perror* fornisce un codice di errore che indica il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="51fd8-118">If the function is unsuccessful, the return value is **NULL**, and *pError* provides an error code that indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="51fd8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="51fd8-119">Remarks</span></span>

<span data-ttu-id="51fd8-120">È importante notare che un esperto deve usare le funzioni di allocazione della memoria Network Monitor (incluso [ExpertReallocMemory](expertreallocmemory.md)) per la gestione della memoria.</span><span class="sxs-lookup"><span data-stu-id="51fd8-120">It is important to note that an expert should use the Network Monitor memory allocation functions (including [ExpertReallocMemory](expertreallocmemory.md)) for memory management.</span></span> <span data-ttu-id="51fd8-121">Se l'esperto non riesce in fase di esecuzione, l'uso di queste funzioni consentirà Network Monitor di liberare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="51fd8-121">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fd8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51fd8-122">Requirements</span></span>



| <span data-ttu-id="51fd8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="51fd8-123">Requirement</span></span> | <span data-ttu-id="51fd8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="51fd8-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51fd8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51fd8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="51fd8-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51fd8-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="51fd8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51fd8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="51fd8-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51fd8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="51fd8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51fd8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="51fd8-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="51fd8-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="51fd8-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="51fd8-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="51fd8-132"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51fd8-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="51fd8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="51fd8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51fd8-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51fd8-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




