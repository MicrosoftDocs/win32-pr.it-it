---
description: La funzione ExpertFreeMemory libera la memoria acquisita dalle chiamate alle funzioni ExpertAllocMemory e ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Funzione ExpertFreeMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305950"
---
# <a name="expertfreememory-function"></a><span data-ttu-id="711e0-103">ExpertFreeMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="711e0-103">ExpertFreeMemory function</span></span>

<span data-ttu-id="711e0-104">La funzione **ExpertFreeMemory** libera la memoria acquisita dalle chiamate alle funzioni [**ExpertAllocMemory**](expertallocmemory.md) e [**ExpertReallocMemory**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="711e0-104">The **ExpertFreeMemory** function frees memory acquired by calls to the [**ExpertAllocMemory**](expertallocmemory.md) and [**ExpertReallocMemory**](expertreallocmemory.md) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="711e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="711e0-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="711e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="711e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711e0-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="711e0-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="711e0-108">Identificatore univoco dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="711e0-108">Unique expert identifier.</span></span> <span data-ttu-id="711e0-109">Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="711e0-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="711e0-110">*pMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="711e0-110">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711e0-111">Puntatore alla memoria allocata da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="711e0-111">Pointer to the memory that Network Monitor allocates.</span></span> <span data-ttu-id="711e0-112">Il puntatore *pMemory* può essere restituito da una precedente chiamata a [**ExpertAllocMemory**](expertallocmemory.md) o [**ExpertReallocMemory**](expertreallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="711e0-112">The *pMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or [**ExpertReallocMemory**](expertreallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711e0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="711e0-113">Return value</span></span>

<span data-ttu-id="711e0-114">Se la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="711e0-114">If the function is successful.</span></span> <span data-ttu-id="711e0-115">il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="711e0-115">the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="711e0-116">Se la funzione ha esito negativo, il valore restituito indica il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="711e0-116">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="711e0-117">Se il valore restituito è NMERR \_ Expert \_ Terminate, l'esperto viene immediatamente ripulito e restituito.</span><span class="sxs-lookup"><span data-stu-id="711e0-117">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="remarks"></a><span data-ttu-id="711e0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="711e0-118">Remarks</span></span>

<span data-ttu-id="711e0-119">È importante notare che un esperto deve usare le funzioni di allocazione della memoria Network Monitor per la gestione della memoria.</span><span class="sxs-lookup"><span data-stu-id="711e0-119">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="711e0-120">Se l'esperto non riesce in fase di esecuzione, l'uso di queste funzioni consentirà Network Monitor di liberare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="711e0-120">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="711e0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="711e0-121">Requirements</span></span>



| <span data-ttu-id="711e0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="711e0-122">Requirement</span></span> | <span data-ttu-id="711e0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="711e0-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="711e0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="711e0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="711e0-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="711e0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="711e0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="711e0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="711e0-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="711e0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="711e0-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="711e0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="711e0-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="711e0-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="711e0-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="711e0-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="711e0-131"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="711e0-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="711e0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="711e0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="711e0-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="711e0-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




