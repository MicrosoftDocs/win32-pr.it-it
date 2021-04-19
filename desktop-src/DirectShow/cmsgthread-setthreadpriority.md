---
description: Usa la funzione SetThreadPriority di Microsoft Win32 per impostare la priorità del thread su un nuovo valore.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Metodo CMsgThread. SetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333317"
---
# <a name="cmsgthreadsetthreadpriority-method"></a><span data-ttu-id="e4217-103">CMsgThread. SetThreadPriority, metodo</span><span class="sxs-lookup"><span data-stu-id="e4217-103">CMsgThread.SetThreadPriority method</span></span>

<span data-ttu-id="e4217-104">Usa la funzione **SetThreadPriority** di Microsoft Win32 per impostare la priorità del thread su un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="e4217-104">Uses the Microsoft Win32 **SetThreadPriority** function to set the priority of the thread to a new value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4217-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4217-105">Syntax</span></span>


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a><span data-ttu-id="e4217-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4217-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4217-107">*nPriority*</span><span class="sxs-lookup"><span data-stu-id="e4217-107">*nPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="e4217-108">Priorità del thread.</span><span class="sxs-lookup"><span data-stu-id="e4217-108">Priority of the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4217-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4217-109">Return value</span></span>

<span data-ttu-id="e4217-110">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4217-110">Returns one of the following values.</span></span>



| <span data-ttu-id="e4217-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e4217-111">Return code</span></span>                                                                              | <span data-ttu-id="e4217-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4217-112">Description</span></span>                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e4217-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e4217-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="e4217-114">La priorità è stata impostata correttamente.</span><span class="sxs-lookup"><span data-stu-id="e4217-114">Priority was successfully set.</span></span><br/> |
| <dl> <span data-ttu-id="e4217-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e4217-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="e4217-116">La priorità non è stata impostata.</span><span class="sxs-lookup"><span data-stu-id="e4217-116">Priority was not set.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="e4217-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4217-117">Remarks</span></span>

<span data-ttu-id="e4217-118">Il client e il thread di lavoro possono chiamare questa funzione membro.</span><span class="sxs-lookup"><span data-stu-id="e4217-118">The client and the worker thread can call this member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4217-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4217-119">Requirements</span></span>



| <span data-ttu-id="e4217-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4217-120">Requirement</span></span> | <span data-ttu-id="e4217-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e4217-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4217-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4217-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e4217-123"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4217-123"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4217-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4217-124">Library</span></span><br/> | <dl> <span data-ttu-id="e4217-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e4217-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4217-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4217-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4217-127">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="e4217-127">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




