---
description: Questo operatore consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'Metodo CMediaType. CMediaType:: operator = (mtype. h)'
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
ms.openlocfilehash: 748ad2efae39fc6a7b26c39d10351c44a5cee8a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332325"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="504d5-103">Metodo CMediaType. CMediaType:: operator = (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="504d5-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="504d5-104">Questo operatore consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="504d5-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="504d5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="504d5-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="504d5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="504d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="504d5-107">*mtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="504d5-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="504d5-108">Riferimento a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="504d5-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="504d5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="504d5-109">Return value</span></span>

<span data-ttu-id="504d5-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="504d5-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="504d5-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="504d5-111">Requirements</span></span>



| <span data-ttu-id="504d5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="504d5-112">Requirement</span></span> | <span data-ttu-id="504d5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="504d5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="504d5-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="504d5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="504d5-115"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="504d5-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="504d5-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="504d5-116">Library</span></span><br/> | <dl> <span data-ttu-id="504d5-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="504d5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="504d5-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="504d5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="504d5-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="504d5-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




