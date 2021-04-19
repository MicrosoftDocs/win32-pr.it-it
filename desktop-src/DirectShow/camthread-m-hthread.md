---
description: Handle per il thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Membro CAMThread:: m_hThread (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333380"
---
# <a name="camthreadm_hthread-member"></a><span data-ttu-id="960dd-103">Membro hThread di CAMThread:: m \_</span><span class="sxs-lookup"><span data-stu-id="960dd-103">CAMThread::m\_hThread member</span></span>

<span data-ttu-id="960dd-104">Handle per il thread.</span><span class="sxs-lookup"><span data-stu-id="960dd-104">Handle to the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="960dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="960dd-105">Syntax</span></span>


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a><span data-ttu-id="960dd-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="960dd-106">Remarks</span></span>

<span data-ttu-id="960dd-107">Questa variabile è inizializzata come **null**.</span><span class="sxs-lookup"><span data-stu-id="960dd-107">This variable is initialized as **NULL**.</span></span> <span data-ttu-id="960dd-108">Il metodo [**CAMThread:: create**](camthread-create.md) imposta questa variabile sull'handle del thread.</span><span class="sxs-lookup"><span data-stu-id="960dd-108">The [**CAMThread::Create**](camthread-create.md) method sets this variable to the thread handle.</span></span> <span data-ttu-id="960dd-109">Per determinare se il thread esiste, chiamare il metodo [**CAMThread:: ThreadExists**](camthread-threadexists.md) .</span><span class="sxs-lookup"><span data-stu-id="960dd-109">To determine whether the thread exists, call the [**CAMThread::ThreadExists**](camthread-threadexists.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="960dd-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="960dd-110">Requirements</span></span>



| <span data-ttu-id="960dd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="960dd-111">Requirement</span></span> | <span data-ttu-id="960dd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="960dd-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="960dd-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="960dd-113">Header</span></span><br/>  | <dl> <span data-ttu-id="960dd-114"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="960dd-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="960dd-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="960dd-115">Library</span></span><br/> | <dl> <span data-ttu-id="960dd-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="960dd-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="960dd-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="960dd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960dd-118">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="960dd-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




