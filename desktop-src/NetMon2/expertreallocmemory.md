---
description: La funzione ExpertReallocMemory consente di aumentare o diminuire la quantità di memoria allocata dal Network Monitor.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Funzione ExpertReallocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305946"
---
# <a name="expertreallocmemory-function"></a><span data-ttu-id="61872-103">ExpertReallocMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="61872-103">ExpertReallocMemory function</span></span>

<span data-ttu-id="61872-104">La funzione **ExpertReallocMemory** consente di aumentare o diminuire la quantità di memoria allocata dal Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="61872-104">The **ExpertReallocMemory** function increases or decreases the amount of memory allocated by Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="61872-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61872-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="61872-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="61872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61872-107">*hExpertKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61872-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61872-108">Identificatore univoco passato all'esperto in fase di [**esecuzione**](run.md) o [**configurazione**](configure.md).</span><span class="sxs-lookup"><span data-stu-id="61872-108">Unique identifier passed to the expert at [**Run**](run.md) or [**Configure**](configure.md).</span></span>

</dd> <dt>

<span data-ttu-id="61872-109">*pOriginalMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61872-109">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61872-110">Puntatore alla memoria allocata dal Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="61872-110">Pointer to the memory allocated by Network Monitor.</span></span> <span data-ttu-id="61872-111">Il puntatore *pOriginalMemory* può essere restituito da una precedente chiamata a [**ExpertAllocMemory**](expertallocmemory.md) o **ExpertReallocMemory**.</span><span class="sxs-lookup"><span data-stu-id="61872-111">The *pOriginalMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or **ExpertReallocMemory**.</span></span>

</dd> <dt>

<span data-ttu-id="61872-112">*nBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61872-112">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61872-113">Dimensione della memoria riallocata.</span><span class="sxs-lookup"><span data-stu-id="61872-113">Size of reallocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="61872-114">*perror* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61872-114">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61872-115">Al ritorno, un codice di errore se la funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="61872-115">On return, an error code if the function fails.</span></span> <span data-ttu-id="61872-116">Se il codice di errore è NMERR \_ Expert \_ Terminate, l'esperto deve effettuare la pulizia e restituire immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="61872-116">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61872-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61872-117">Return value</span></span>

<span data-ttu-id="61872-118">Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="61872-118">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="61872-119">Se la funzione ha esito negativo, il valore restituito è **null** e *perror* (se è un valore non **null** ) indica il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="61872-119">If the function is unsuccessful, the return value is **NULL**, and *pError* (if it is a non-**NULL** value) indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="61872-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="61872-120">Remarks</span></span>

<span data-ttu-id="61872-121">È importante notare che un esperto deve usare le funzioni di allocazione della memoria Network Monitor per la gestione della memoria.</span><span class="sxs-lookup"><span data-stu-id="61872-121">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="61872-122">Se l'esperto non riesce in fase di esecuzione, l'uso di queste funzioni consentirà Network Monitor di liberare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="61872-122">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="61872-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61872-123">Requirements</span></span>



| <span data-ttu-id="61872-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="61872-124">Requirement</span></span> | <span data-ttu-id="61872-125">Valore</span><span class="sxs-lookup"><span data-stu-id="61872-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="61872-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61872-126">Minimum supported client</span></span><br/> | <span data-ttu-id="61872-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="61872-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="61872-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61872-128">Minimum supported server</span></span><br/> | <span data-ttu-id="61872-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="61872-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="61872-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61872-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="61872-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="61872-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="61872-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="61872-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="61872-133"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61872-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="61872-134">DLL</span><span class="sxs-lookup"><span data-stu-id="61872-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61872-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61872-135"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




