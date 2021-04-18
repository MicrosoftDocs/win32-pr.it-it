---
description: Il metodo MatchesPartial determina se il tipo di supporto corrisponde a un tipo di supporto parzialmente specificato.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Metodo CMediaType. MatchesPartial (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330674"
---
# <a name="cmediatypematchespartial-method"></a><span data-ttu-id="f054c-103">CMediaType. MatchesPartial, metodo</span><span class="sxs-lookup"><span data-stu-id="f054c-103">CMediaType.MatchesPartial method</span></span>

<span data-ttu-id="f054c-104">Il `MatchesPartial` metodo determina se il tipo di supporto corrisponde a un tipo di supporto parzialmente specificato.</span><span class="sxs-lookup"><span data-stu-id="f054c-104">The `MatchesPartial` method determines if this media type matches a partially specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f054c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f054c-105">Syntax</span></span>


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a><span data-ttu-id="f054c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f054c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f054c-107">*ppartial*</span><span class="sxs-lookup"><span data-stu-id="f054c-107">*ppartial*</span></span> 
</dt> <dd>

<span data-ttu-id="f054c-108">Puntatore al tipo di supporto da confrontare.</span><span class="sxs-lookup"><span data-stu-id="f054c-108">Pointer to the media type to match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f054c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f054c-109">Return value</span></span>

<span data-ttu-id="f054c-110">Restituisce **true** se i tipi di supporto corrispondono.</span><span class="sxs-lookup"><span data-stu-id="f054c-110">Returns **TRUE** if the media types match.</span></span> <span data-ttu-id="f054c-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="f054c-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f054c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f054c-112">Remarks</span></span>

<span data-ttu-id="f054c-113">Il tipo di supporto specificato da *ppartial* può avere un valore GUID \_ null per il tipo principale, il sottotipo o il tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="f054c-113">The media type specified by *ppartial* can have a value of GUID\_NULL for the major type, subtype, or format type.</span></span> <span data-ttu-id="f054c-114">I membri con \_ valori null GUID non vengono sottoposti a test.</span><span class="sxs-lookup"><span data-stu-id="f054c-114">Any members with GUID\_NULL values are not tested.</span></span> <span data-ttu-id="f054c-115">(In effetti, GUID \_ NULL funge da carattere jolly). I membri con valori diversi da GUID \_ null devono corrispondere per il tipo di supporto di cui trovare la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="f054c-115">(In effect, GUID\_NULL acts as a wildcard.) Members with values other than GUID\_NULL must match for the media type to match.</span></span>

## <a name="requirements"></a><span data-ttu-id="f054c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f054c-116">Requirements</span></span>



| <span data-ttu-id="f054c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f054c-117">Requirement</span></span> | <span data-ttu-id="f054c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f054c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f054c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f054c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f054c-120"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f054c-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f054c-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="f054c-121">Library</span></span><br/> | <dl> <span data-ttu-id="f054c-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f054c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f054c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f054c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f054c-124">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="f054c-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




