---
description: Fornisce l'inizializzazione su un thread.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: Metodo CMsgThread. OnThreadInit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80e15d6430da77c0f22f5566375394b8fe6994ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325926"
---
# <a name="cmsgthreadonthreadinit-method"></a><span data-ttu-id="cf8ab-103">CMsgThread. OnThreadInit, metodo</span><span class="sxs-lookup"><span data-stu-id="cf8ab-103">CMsgThread.OnThreadInit method</span></span>

<span data-ttu-id="cf8ab-104">Fornisce l'inizializzazione su un thread.</span><span class="sxs-lookup"><span data-stu-id="cf8ab-104">Provides initialization on a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf8ab-105">Syntax</span></span>


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a><span data-ttu-id="cf8ab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf8ab-106">Parameters</span></span>

<span data-ttu-id="cf8ab-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cf8ab-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf8ab-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf8ab-108">Return value</span></span>

<span data-ttu-id="cf8ab-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cf8ab-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf8ab-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf8ab-110">Remarks</span></span>

<span data-ttu-id="cf8ab-111">Eseguire l'override di questa funzione se si desidera eseguire un'inizializzazione specifica all'avvio del thread.</span><span class="sxs-lookup"><span data-stu-id="cf8ab-111">Override this function if you want to do your own specific initialization on thread startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8ab-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf8ab-112">Requirements</span></span>



| <span data-ttu-id="cf8ab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf8ab-113">Requirement</span></span> | <span data-ttu-id="cf8ab-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cf8ab-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8ab-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf8ab-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cf8ab-116"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf8ab-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cf8ab-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="cf8ab-117">Library</span></span><br/> | <dl> <span data-ttu-id="cf8ab-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cf8ab-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8ab-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf8ab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8ab-120">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="cf8ab-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




