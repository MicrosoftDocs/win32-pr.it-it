---
description: Imposta l'assegnazione predefinita dei set di CPU per i thread nel processo specificato. I thread creati, che non hanno set di CPU impostati in modo esplicito tramite SetThreadSelectedCpuSets, erediteranno automaticamente i set specificati da SetProcessDefaultCpuSets.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Funzione SetProcessDefaultCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311958"
---
# <a name="setprocessdefaultcpusets-function"></a><span data-ttu-id="c7656-104">SetProcessDefaultCpuSets (funzione)</span><span class="sxs-lookup"><span data-stu-id="c7656-104">SetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="c7656-105">Imposta l'assegnazione predefinita dei set di CPU per i thread nel processo specificato.</span><span class="sxs-lookup"><span data-stu-id="c7656-105">Sets the default CPU Sets assignment for threads in the specified process.</span></span> <span data-ttu-id="c7656-106">I thread creati, che non hanno set di CPU impostati in modo esplicito tramite [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), erediteranno automaticamente i set specificati da **SetProcessDefaultCpuSets** .</span><span class="sxs-lookup"><span data-stu-id="c7656-106">Threads that are created, which don’t have CPU Sets explicitly set using [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), will inherit the sets specified by **SetProcessDefaultCpuSets** automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7656-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7656-107">Syntax</span></span>


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a><span data-ttu-id="c7656-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7656-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7656-109">*Processo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c7656-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7656-110">Specifica il processo per il quale impostare i set di CPU predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c7656-110">Specifies the process for which to set the default CPU Sets.</span></span> <span data-ttu-id="c7656-111">Questo handle deve avere il \_ diritto di \_ \_ accesso limitato alle informazioni di processo.</span><span class="sxs-lookup"><span data-stu-id="c7656-111">This handle must have the PROCESS\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="c7656-112">Il valore restituito da [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può anche essere specificato qui.</span><span class="sxs-lookup"><span data-stu-id="c7656-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="c7656-113">*CpuSetIds* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c7656-113">*CpuSetIds* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7656-114">Specifica l'elenco di ID set di CPU da impostare come set di CPU predefinito del processo.</span><span class="sxs-lookup"><span data-stu-id="c7656-114">Specifies the list of CPU Set IDs to set as the process default CPU set.</span></span> <span data-ttu-id="c7656-115">Se il valore è NULL, il **SetProcessDefaultCpuSets** Cancella tutte le assegnazioni.</span><span class="sxs-lookup"><span data-stu-id="c7656-115">If this is NULL, the **SetProcessDefaultCpuSets** clears out any assignment.</span></span>

</dd> <dt>

<span data-ttu-id="c7656-116">*CpuSetIdCound* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7656-116">*CpuSetIdCound* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7656-117">Specifica il numero di ID nell'elenco passato nell'argomento **CpuSetIds** .</span><span class="sxs-lookup"><span data-stu-id="c7656-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="c7656-118">Se il valore è NULL, deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="c7656-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7656-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7656-119">Return value</span></span>

<span data-ttu-id="c7656-120">Questa funzione non può avere esito negativo se vengono passati parametri validi.</span><span class="sxs-lookup"><span data-stu-id="c7656-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7656-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7656-121">Requirements</span></span>



| <span data-ttu-id="c7656-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7656-122">Requirement</span></span> | <span data-ttu-id="c7656-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c7656-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7656-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7656-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c7656-125">App desktop di Windows 10 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7656-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="c7656-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7656-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c7656-127">App UWP per \[ app desktop di Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="c7656-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="c7656-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7656-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7656-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7656-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="c7656-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="c7656-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7656-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7656-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="c7656-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c7656-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7656-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7656-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
