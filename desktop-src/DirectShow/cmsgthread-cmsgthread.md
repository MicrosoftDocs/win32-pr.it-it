---
description: Metodo del costruttore.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Costruttore CMsgThread. CMsgThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328835"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="5732d-103">Costruttore CMsgThread. CMsgThread</span><span class="sxs-lookup"><span data-stu-id="5732d-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="5732d-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="5732d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5732d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5732d-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="5732d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5732d-106">Parameters</span></span>

<span data-ttu-id="5732d-107">Questo costruttore non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="5732d-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5732d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="5732d-108">Remarks</span></span>

<span data-ttu-id="5732d-109">La costruzione di un oggetto thread di messaggio non crea automaticamente il thread.</span><span class="sxs-lookup"><span data-stu-id="5732d-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="5732d-110">Per creare il thread, è necessario chiamare la funzione membro [**CMsgThread:: CreateThread**](cmsgthread-createthread.md) .</span><span class="sxs-lookup"><span data-stu-id="5732d-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="5732d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5732d-111">Requirements</span></span>



| <span data-ttu-id="5732d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5732d-112">Requirement</span></span> | <span data-ttu-id="5732d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5732d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5732d-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5732d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5732d-115"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5732d-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5732d-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="5732d-116">Library</span></span><br/> | <dl> <span data-ttu-id="5732d-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5732d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5732d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5732d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5732d-119">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="5732d-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




