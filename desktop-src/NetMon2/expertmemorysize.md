---
description: La funzione ExpertMemorySize restituisce la quantità di memoria allocata dalla funzione ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Funzione ExpertMemorySize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878662"
---
# <a name="expertmemorysize-function"></a><span data-ttu-id="00212-103">ExpertMemorySize (funzione)</span><span class="sxs-lookup"><span data-stu-id="00212-103">ExpertMemorySize function</span></span>

<span data-ttu-id="00212-104">La funzione **ExpertMemorySize** restituisce la quantità di memoria allocata dalla funzione [ExpertAllocMemory](expertallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="00212-104">The **ExpertMemorySize** function returns the amount of memory allocated by the [ExpertAllocMemory](expertallocmemory.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="00212-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00212-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a><span data-ttu-id="00212-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00212-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00212-107">*hExpertKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00212-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00212-108">Identificatore univoco dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="00212-108">Unique expert identifier.</span></span> <span data-ttu-id="00212-109">Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="00212-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="00212-110">*pOriginalMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00212-110">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00212-111">Puntatore all'indirizzo di memoria dell'esperto allocato da [ExpertAllocMemory](expertallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="00212-111">Pointer to the memory address of the expert allocated by [ExpertAllocMemory](expertallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00212-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00212-112">Return value</span></span>

<span data-ttu-id="00212-113">La funzione restituisce la quantità di memoria allocata in byte.</span><span class="sxs-lookup"><span data-stu-id="00212-113">The function returns the amount of allocated memory   in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="00212-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="00212-114">Remarks</span></span>

<span data-ttu-id="00212-115">Per informazioni sul tipo di dati **size \_ T** restituito da **ExpertMemorySize** , vedere tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="00212-115">For information on the **SIZE\_T** data type that **ExpertMemorySize** returns, see Data Types.</span></span>

## <a name="requirements"></a><span data-ttu-id="00212-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00212-116">Requirements</span></span>



| <span data-ttu-id="00212-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="00212-117">Requirement</span></span> | <span data-ttu-id="00212-118">Valore</span><span class="sxs-lookup"><span data-stu-id="00212-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00212-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00212-119">Minimum supported client</span></span><br/> | <span data-ttu-id="00212-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00212-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="00212-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00212-121">Minimum supported server</span></span><br/> | <span data-ttu-id="00212-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00212-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="00212-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00212-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="00212-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="00212-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="00212-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="00212-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="00212-126"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00212-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="00212-127">DLL</span><span class="sxs-lookup"><span data-stu-id="00212-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00212-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00212-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




