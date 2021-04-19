---
description: Restituisce il valore corrente di un contatore delle prestazioni e, facoltativamente, la frequenza del contatore delle prestazioni.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326091"
---
# <a name="ntqueryperformancecounter-function"></a><span data-ttu-id="15d71-103">NtQueryPerformanceCounter (funzione)</span><span class="sxs-lookup"><span data-stu-id="15d71-103">NtQueryPerformanceCounter function</span></span>

<span data-ttu-id="15d71-104">\[Questa funzione non è supportata e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="15d71-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="15d71-105">Usare invece le funzioni **QueryPerformanceCounter** e **QueryPerformanceFrequency** .\]</span><span class="sxs-lookup"><span data-stu-id="15d71-105">Use the **QueryPerformanceCounter** and **QueryPerformanceFrequency** functions instead.\]</span></span>

<span data-ttu-id="15d71-106">Restituisce il valore corrente di un contatore delle prestazioni e, facoltativamente, la frequenza del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="15d71-106">Returns the current value of a performance counter and, optionally, the frequency of the performance counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d71-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15d71-107">Syntax</span></span>


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a><span data-ttu-id="15d71-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="15d71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15d71-109">*PerformanceCounter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="15d71-109">*PerformanceCounter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15d71-110">Indirizzo di una variabile per la ricezione del valore corrente del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="15d71-110">The address of a variable to receive the current performance counter value.</span></span>

</dd> <dt>

<span data-ttu-id="15d71-111">*PerformanceFrequency* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="15d71-111">*PerformanceFrequency* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15d71-112">Indirizzo di una variabile per la ricezione della frequenza del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="15d71-112">The address of a variable to receive the performance counter frequency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15d71-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15d71-113">Return value</span></span>

<span data-ttu-id="15d71-114">Se la funzione ha esito positivo, restituisce lo stato del codice **NTSTATUS** . in caso contrario, restituisce un codice di errore, ad esempio **\_** **\_ \_ violazione di accesso allo stato**.</span><span class="sxs-lookup"><span data-stu-id="15d71-114">If the function succeeds, it returns the **NTSTATUS** code **STATUS\_SUCCESS**; otherwise, it returns an error code such as **STATUS\_ACCESS\_VIOLATION**.</span></span>

## <a name="remarks"></a><span data-ttu-id="15d71-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="15d71-115">Remarks</span></span>

<span data-ttu-id="15d71-116">Nessun file di intestazione disponibile per **NtQueryPerformanceCounter**.</span><span class="sxs-lookup"><span data-stu-id="15d71-116">No header file is available for **NtQueryPerformanceCounter**.</span></span> <span data-ttu-id="15d71-117">È consigliabile usare le funzioni alternative indicate sopra, sebbene sia anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="15d71-117">You should use the alternative functions named above, although you can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

<span data-ttu-id="15d71-118">La frequenza delle prestazioni è la frequenza del contatore delle prestazioni in Hertz, in particolare nei conteggi al secondo.</span><span class="sxs-lookup"><span data-stu-id="15d71-118">Performance frequency is the frequency of the performance counter in hertz, specifically in counts per second.</span></span> <span data-ttu-id="15d71-119">Questo valore è dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="15d71-119">This value is implementation dependent.</span></span> <span data-ttu-id="15d71-120">Se l'implementazione di non dispone di hardware per supportare la tempistica delle prestazioni, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="15d71-120">If the implementation does not have hardware to support performance timing, the value returned is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d71-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15d71-121">Requirements</span></span>



| <span data-ttu-id="15d71-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d71-122">Requirement</span></span> | <span data-ttu-id="15d71-123">Valore</span><span class="sxs-lookup"><span data-stu-id="15d71-123">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15d71-124">DLL</span><span class="sxs-lookup"><span data-stu-id="15d71-124">DLL</span></span><br/> | <dl> <span data-ttu-id="15d71-125"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15d71-125"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15d71-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15d71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d71-127">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="15d71-127">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[<span data-ttu-id="15d71-128">**QueryPerformanceFrequency**</span><span class="sxs-lookup"><span data-stu-id="15d71-128">**QueryPerformanceFrequency**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
