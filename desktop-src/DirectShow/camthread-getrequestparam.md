---
description: Il metodo GetRequestParam recupera la richiesta più recente.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Metodo CAMThread. GetRequestParam (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330706"
---
# <a name="camthreadgetrequestparam-method"></a><span data-ttu-id="0dd9b-103">CAMThread. GetRequestParam, metodo</span><span class="sxs-lookup"><span data-stu-id="0dd9b-103">CAMThread.GetRequestParam method</span></span>

<span data-ttu-id="0dd9b-104">Il `GetRequestParam` metodo recupera la richiesta più recente.</span><span class="sxs-lookup"><span data-stu-id="0dd9b-104">The `GetRequestParam` method retrieves the latest request.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd9b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dd9b-105">Syntax</span></span>


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a><span data-ttu-id="0dd9b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dd9b-106">Parameters</span></span>

<span data-ttu-id="0dd9b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0dd9b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0dd9b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0dd9b-108">Return value</span></span>

<span data-ttu-id="0dd9b-109">Restituisce il valore del parametro passato più di recente al metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd9b-109">Returns the value of the parameter that was passed most recently to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd9b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dd9b-110">Requirements</span></span>



| <span data-ttu-id="0dd9b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dd9b-111">Requirement</span></span> | <span data-ttu-id="0dd9b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0dd9b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd9b-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0dd9b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="0dd9b-114"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0dd9b-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0dd9b-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="0dd9b-115">Library</span></span><br/> | <dl> <span data-ttu-id="0dd9b-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0dd9b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dd9b-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dd9b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd9b-118">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="0dd9b-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




