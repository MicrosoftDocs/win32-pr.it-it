---
description: Restituisce l'assegnazione esplicita del set di CPU del thread specificato, se è stata impostata un'assegnazione utilizzando l'API SetThreadSelectedCpuSets. Se non è impostata alcuna assegnazione esplicita, RequiredIdCount viene impostata su 0 e la funzione restituisce TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Funzione GetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050016"
---
# <a name="getthreadselectedcpusets-function"></a><span data-ttu-id="4f258-104">GetThreadSelectedCpuSets (funzione)</span><span class="sxs-lookup"><span data-stu-id="4f258-104">GetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="4f258-105">Restituisce l'assegnazione esplicita del set di CPU del thread specificato, se è stata impostata un'assegnazione utilizzando l'API [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) .</span><span class="sxs-lookup"><span data-stu-id="4f258-105">Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API.</span></span> <span data-ttu-id="4f258-106">Se non è impostata alcuna assegnazione esplicita, **RequiredIdCount** viene impostata su 0 e la funzione restituisce true.</span><span class="sxs-lookup"><span data-stu-id="4f258-106">If no explicit assignment is set, **RequiredIdCount** is set to 0 and the function returns TRUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f258-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f258-107">Syntax</span></span>


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="4f258-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f258-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f258-109">*Thread* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4f258-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f258-110">Specifica il thread per il quale eseguire una query sui set di CPU selezionati.</span><span class="sxs-lookup"><span data-stu-id="4f258-110">Specifies the thread for which to query the selected CPU Sets.</span></span> <span data-ttu-id="4f258-111">Questo handle deve avere il \_ diritto di \_ accesso limitato alle informazioni di query del thread \_ .</span><span class="sxs-lookup"><span data-stu-id="4f258-111">This handle must have the THREAD\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="4f258-112">Il valore restituito da [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) può anche essere specificato qui.</span><span class="sxs-lookup"><span data-stu-id="4f258-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="4f258-113">*CpuSetIds* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4f258-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f258-114">Specifica un buffer facoltativo per recuperare l'elenco degli identificatori del set di CPU.</span><span class="sxs-lookup"><span data-stu-id="4f258-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="4f258-115">*CpuSetIdCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f258-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f258-116">Specifica la capacità del buffer specificato in **CpuSetIds**.</span><span class="sxs-lookup"><span data-stu-id="4f258-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="4f258-117">Se il buffer è NULL, deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="4f258-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="4f258-118">*RequiredIdCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f258-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f258-119">Specifica la capacità necessaria del buffer per memorizzare l'intero elenco di set di CPU selezionati per il thread.</span><span class="sxs-lookup"><span data-stu-id="4f258-119">Specifies the required capacity of the buffer to hold the entire list of thread selected CPU Sets.</span></span> <span data-ttu-id="4f258-120">In esito positivo, specifica il numero di ID inseriti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="4f258-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f258-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f258-121">Return value</span></span>

<span data-ttu-id="4f258-122">Questa API restituisce TRUE in seguito all'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4f258-122">This API returns TRUE on success.</span></span> <span data-ttu-id="4f258-123">Se il buffer non è sufficientemente grande, il valore **GetLastError** è errore \_ buffer insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="4f258-123">If the buffer is not large enough, the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="4f258-124">Questa API non può avere esito negativo se vengono passati parametri validi e il buffer restituito è sufficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="4f258-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f258-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f258-125">Requirements</span></span>



| <span data-ttu-id="4f258-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f258-126">Requirement</span></span> | <span data-ttu-id="4f258-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4f258-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f258-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f258-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4f258-129">App desktop di Windows 10 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4f258-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="4f258-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f258-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4f258-131">App UWP per \[ app desktop di Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="4f258-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="4f258-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f258-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f258-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f258-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="4f258-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f258-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f258-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f258-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="4f258-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4f258-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f258-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f258-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

