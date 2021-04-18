---
description: Il metodo CheckRequest controlla se è presente una richiesta di thread senza blocco.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Metodo CSourceStream. CheckRequest (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329030"
---
# <a name="csourcestreamcheckrequest-method"></a><span data-ttu-id="ec952-103">CSourceStream. CheckRequest, metodo</span><span class="sxs-lookup"><span data-stu-id="ec952-103">CSourceStream.CheckRequest method</span></span>

<span data-ttu-id="ec952-104">Il `CheckRequest` metodo verifica se è presente una richiesta di thread senza blocco.</span><span class="sxs-lookup"><span data-stu-id="ec952-104">The `CheckRequest` method checks if there is a thread request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec952-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec952-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a><span data-ttu-id="ec952-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec952-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec952-107">*MOCF*</span><span class="sxs-lookup"><span data-stu-id="ec952-107">*pCom*</span></span> 
</dt> <dd>

<span data-ttu-id="ec952-108">Puntatore a una variabile che riceve il valore passato nell'ultima chiamata al metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="ec952-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec952-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec952-109">Return value</span></span>

<span data-ttu-id="ec952-110">Restituisce **true** se è presente una richiesta in sospeso; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="ec952-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec952-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec952-111">Remarks</span></span>

<span data-ttu-id="ec952-112">Questo metodo esegue l'override del metodo [**CAMThread:: CheckRequest**](camthread-checkrequest.md) per eseguire il controllo dei tipi.</span><span class="sxs-lookup"><span data-stu-id="ec952-112">This method overrides the [**CAMThread::CheckRequest**](camthread-checkrequest.md) method to perform type-checking.</span></span> <span data-ttu-id="ec952-113">La classe **CSourceStream** definisce il tipo enumerato seguente per il parametro *MOCF* :</span><span class="sxs-lookup"><span data-stu-id="ec952-113">The **CSourceStream** class defines the following enumerated type for the *pCom* parameter:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="ec952-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec952-114">Requirements</span></span>



| <span data-ttu-id="ec952-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec952-115">Requirement</span></span> | <span data-ttu-id="ec952-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ec952-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec952-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec952-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ec952-118"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec952-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ec952-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec952-119">Library</span></span><br/> | <dl> <span data-ttu-id="ec952-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec952-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec952-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec952-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec952-122">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="ec952-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




