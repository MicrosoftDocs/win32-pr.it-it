---
description: Imposta l'assegnazione dei set di CPU selezionati per il thread specificato. Questa assegnazione sostituisce l'assegnazione predefinita del processo, se ne è stata impostata una.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Funzione SetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881702"
---
# <a name="setthreadselectedcpusets-function"></a><span data-ttu-id="eb40b-104">SetThreadSelectedCpuSets (funzione)</span><span class="sxs-lookup"><span data-stu-id="eb40b-104">SetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="eb40b-105">Imposta l'assegnazione dei set di CPU selezionati per il thread specificato.</span><span class="sxs-lookup"><span data-stu-id="eb40b-105">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="eb40b-106">Questa assegnazione sostituisce l'assegnazione predefinita del processo, se ne è stata impostata una.</span><span class="sxs-lookup"><span data-stu-id="eb40b-106">This assignment overrides the process default assignment, if one is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb40b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb40b-107">Syntax</span></span>


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="eb40b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb40b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb40b-109">*Thread* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="eb40b-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb40b-110">Specifica il thread su cui impostare l'assegnazione del set di CPU.</span><span class="sxs-lookup"><span data-stu-id="eb40b-110">Specifies the thread on which to set the CPU Set assignment.</span></span> <span data-ttu-id="eb40b-111">Questo handle deve avere il \_ diritto di \_ accesso limitato alle informazioni per il thread \_ .</span><span class="sxs-lookup"><span data-stu-id="eb40b-111">This handle must have the THREAD\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="eb40b-112">È possibile utilizzare anche il valore restituito da [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) .</span><span class="sxs-lookup"><span data-stu-id="eb40b-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be used.</span></span>

</dd> <dt>

<span data-ttu-id="eb40b-113">*CpuSetIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb40b-113">*CpuSetIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb40b-114">Specifica l'elenco di ID set di CPU da impostare come set di CPU selezionato per il thread.</span><span class="sxs-lookup"><span data-stu-id="eb40b-114">Specifies the list of CPU Set IDs to set as the thread selected CPU set.</span></span> <span data-ttu-id="eb40b-115">Se è NULL, l'API Cancella qualsiasi assegnazione, ripristinando l'assegnazione predefinita se ne è stata impostata una.</span><span class="sxs-lookup"><span data-stu-id="eb40b-115">If this is NULL, the API clears out any assignment, reverting to process default assignment if one is set.</span></span>

</dd> <dt>

<span data-ttu-id="eb40b-116">*CpuSetIdCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb40b-116">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb40b-117">Specifica il numero di ID nell'elenco passato nell'argomento **CpuSetIds** .</span><span class="sxs-lookup"><span data-stu-id="eb40b-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="eb40b-118">Se il valore è NULL, deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="eb40b-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb40b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb40b-119">Return value</span></span>

<span data-ttu-id="eb40b-120">Questa funzione non può avere esito negativo se vengono passati parametri validi.</span><span class="sxs-lookup"><span data-stu-id="eb40b-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb40b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb40b-121">Requirements</span></span>



| <span data-ttu-id="eb40b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb40b-122">Requirement</span></span> | <span data-ttu-id="eb40b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="eb40b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb40b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb40b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eb40b-125">App desktop di Windows 10 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="eb40b-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="eb40b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb40b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eb40b-127">App UWP per \[ app desktop di Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb40b-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="eb40b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb40b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb40b-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb40b-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="eb40b-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb40b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb40b-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb40b-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="eb40b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="eb40b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb40b-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb40b-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
