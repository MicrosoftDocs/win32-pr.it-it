---
description: Il metodo InitialThreadProc chiama la routine del thread principale.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: Metodo CAMThread.InitialThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330545"
---
# <a name="camthreadinitialthreadproc-method"></a><span data-ttu-id="68a05-103">Metodo tialThreadProc CAMThread.Ini</span><span class="sxs-lookup"><span data-stu-id="68a05-103">CAMThread.InitialThreadProc method</span></span>

<span data-ttu-id="68a05-104">Il `InitialThreadProc` metodo chiama la routine del thread principale.</span><span class="sxs-lookup"><span data-stu-id="68a05-104">The `InitialThreadProc` method calls the main thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a05-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68a05-105">Syntax</span></span>


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="68a05-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="68a05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a05-107">*PV*</span><span class="sxs-lookup"><span data-stu-id="68a05-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="68a05-108">`this` puntatore.</span><span class="sxs-lookup"><span data-stu-id="68a05-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a05-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68a05-109">Return value</span></span>

<span data-ttu-id="68a05-110">Restituisce il **valore DWORD** restituito da [**CAMThread:: ThreadProc**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="68a05-110">Returns the **DWORD** returned by [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="68a05-111">La classe derivata definisce questo valore.</span><span class="sxs-lookup"><span data-stu-id="68a05-111">The derived class defines this value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68a05-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="68a05-112">Remarks</span></span>

<span data-ttu-id="68a05-113">Il metodo [**CAMThread:: create**](camthread-create.md) usa questo metodo per la routine thread quando crea il thread.</span><span class="sxs-lookup"><span data-stu-id="68a05-113">The [**CAMThread::Create**](camthread-create.md) method uses this method for the thread procedure when it creates the thread.</span></span> <span data-ttu-id="68a05-114">Usa il `this` puntatore come argomento del thread.</span><span class="sxs-lookup"><span data-stu-id="68a05-114">It uses the `this` pointer as the thread argument.</span></span>

<span data-ttu-id="68a05-115">Questo metodo chiama il metodo [**CAMThread:: CoInitializeHelper**](camthread-coinitializehelper.md) e quindi ThreadProc.</span><span class="sxs-lookup"><span data-stu-id="68a05-115">This method calls the [**CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) method and then ThreadProc.</span></span>

## <a name="requirements"></a><span data-ttu-id="68a05-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68a05-116">Requirements</span></span>



| <span data-ttu-id="68a05-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="68a05-117">Requirement</span></span> | <span data-ttu-id="68a05-118">Valore</span><span class="sxs-lookup"><span data-stu-id="68a05-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68a05-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68a05-119">Header</span></span><br/>  | <dl> <span data-ttu-id="68a05-120"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68a05-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="68a05-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="68a05-121">Library</span></span><br/> | <dl> <span data-ttu-id="68a05-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="68a05-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a05-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68a05-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a05-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="68a05-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




