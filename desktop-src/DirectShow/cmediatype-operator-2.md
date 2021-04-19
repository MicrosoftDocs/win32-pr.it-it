---
description: Questo operatore consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'CMediaType. CMediaType:: operator = Method (mtype. h)-parametro mtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389037"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="015f9-103">Metodo CMediaType. CMediaType:: operator = (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="015f9-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="015f9-104">Questo operatore consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="015f9-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="015f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="015f9-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="015f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="015f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="015f9-107">*mtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="015f9-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="015f9-108">Riferimento a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="015f9-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="015f9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="015f9-109">Return value</span></span>

<span data-ttu-id="015f9-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="015f9-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="015f9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="015f9-111">Requirements</span></span>



| <span data-ttu-id="015f9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="015f9-112">Requirement</span></span> | <span data-ttu-id="015f9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="015f9-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="015f9-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="015f9-114">Header</span></span><br/>  | <dl> <span data-ttu-id="015f9-115"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="015f9-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="015f9-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="015f9-116">Library</span></span><br/> | <dl> <span data-ttu-id="015f9-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="015f9-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="015f9-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="015f9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="015f9-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="015f9-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




