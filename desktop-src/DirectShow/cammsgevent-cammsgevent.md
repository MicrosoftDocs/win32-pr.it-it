---
description: 'Costruttore CAMMsgEvent.CAMMsgEvent : metodo del costruttore.'
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Costruttore CAMMsgEvent.CAMMsgEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096536"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="5e054-103">Costruttore CAMMsgEvent.CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="5e054-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="5e054-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="5e054-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e054-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e054-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="5e054-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e054-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e054-107">*Phr*</span><span class="sxs-lookup"><span data-stu-id="5e054-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5e054-108">Puntatore a **un valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5e054-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="5e054-109">Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="5e054-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="5e054-110">In questo caso, l'oggetto non è in uno stato valido.</span><span class="sxs-lookup"><span data-stu-id="5e054-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="5e054-111">Per compatibilità con le versioni precedenti di strmbase.lib, il valore predefinito di questo parametro è **NULL.**</span><span class="sxs-lookup"><span data-stu-id="5e054-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="5e054-112">È tuttavia preferibile passare un valore non **NULL,** in modo che il chiamante possa controllare lo stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5e054-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e054-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e054-113">Requirements</span></span>



| <span data-ttu-id="5e054-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e054-114">Requirement</span></span> | <span data-ttu-id="5e054-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5e054-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e054-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e054-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5e054-117"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e054-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5e054-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e054-118">Library</span></span><br/> | <dl> <span data-ttu-id="5e054-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5e054-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e054-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e054-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e054-121">**Classe CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="5e054-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




