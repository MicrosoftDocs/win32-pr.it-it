---
description: Recupera il numero del processore sul quale era in esecuzione il thread corrente durante la chiamata a questa funzione.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: NtGetCurrentProcessorNumber (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332257"
---
# <a name="ntgetcurrentprocessornumber-function"></a><span data-ttu-id="431c4-103">NtGetCurrentProcessorNumber (funzione)</span><span class="sxs-lookup"><span data-stu-id="431c4-103">NtGetCurrentProcessorNumber function</span></span>

<span data-ttu-id="431c4-104">\[**NtGetCurrentProcessorNumber** può essere modificato o non disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="431c4-104">\[**NtGetCurrentProcessorNumber** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="431c4-105">Le applicazioni devono invece usare la funzione [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) .\]</span><span class="sxs-lookup"><span data-stu-id="431c4-105">Applications should use the [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) function instead.\]</span></span>

<span data-ttu-id="431c4-106">Recupera il numero del processore sul quale era in esecuzione il thread corrente durante la chiamata a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="431c4-106">Retrieves the number of the processor the current thread was running on during the call to this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="431c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="431c4-107">Syntax</span></span>


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a><span data-ttu-id="431c4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="431c4-108">Parameters</span></span>

<span data-ttu-id="431c4-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="431c4-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="431c4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="431c4-110">Return value</span></span>

<span data-ttu-id="431c4-111">La funzione restituisce il numero del processore corrente.</span><span class="sxs-lookup"><span data-stu-id="431c4-111">The function returns the current processor number.</span></span>

## <a name="remarks"></a><span data-ttu-id="431c4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="431c4-112">Remarks</span></span>

<span data-ttu-id="431c4-113">Questa funzione viene utilizzata per fornire informazioni per stimare le prestazioni del processo.</span><span class="sxs-lookup"><span data-stu-id="431c4-113">This function is used to provide information for estimating process performance.</span></span>

<span data-ttu-id="431c4-114">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="431c4-114">This function has no associated import library.</span></span> <span data-ttu-id="431c4-115">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="431c4-115">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="431c4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="431c4-116">Requirements</span></span>



| <span data-ttu-id="431c4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="431c4-117">Requirement</span></span> | <span data-ttu-id="431c4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="431c4-118">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="431c4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="431c4-119">DLL</span></span><br/> | <dl> <span data-ttu-id="431c4-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="431c4-120"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431c4-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="431c4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431c4-122">Processori multipli</span><span class="sxs-lookup"><span data-stu-id="431c4-122">Multiple Processors</span></span>](multiple-processors.md)
</dt> <dt>

[<span data-ttu-id="431c4-123">Funzioni di processi e thread</span><span class="sxs-lookup"><span data-stu-id="431c4-123">Process and Thread Functions</span></span>](process-and-thread-functions.md)
</dt> <dt>

[<span data-ttu-id="431c4-124">Processi</span><span class="sxs-lookup"><span data-stu-id="431c4-124">Processes</span></span>](child-processes.md)
</dt> </dl>

 

 
