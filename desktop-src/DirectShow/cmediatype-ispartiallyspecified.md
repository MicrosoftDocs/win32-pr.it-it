---
description: Il metodo IsPartiallySpecified determina se il tipo di supporto è parzialmente definito. Un tipo di supporto è parziale se il tipo principale, il sottotipo o il tipo di formato è \_ null GUID.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Metodo CMediaType. IsPartiallySpecified (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330680"
---
# <a name="cmediatypeispartiallyspecified-method"></a><span data-ttu-id="4eb05-104">CMediaType. IsPartiallySpecified, metodo</span><span class="sxs-lookup"><span data-stu-id="4eb05-104">CMediaType.IsPartiallySpecified method</span></span>

<span data-ttu-id="4eb05-105">Il `IsPartiallySpecified` metodo determina se il tipo di supporto è parzialmente definito.</span><span class="sxs-lookup"><span data-stu-id="4eb05-105">The `IsPartiallySpecified` method determines if the media type is partially defined.</span></span> <span data-ttu-id="4eb05-106">Un tipo di supporto è *parziale* se il tipo principale, il sottotipo o il tipo di formato è \_ null GUID.</span><span class="sxs-lookup"><span data-stu-id="4eb05-106">A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb05-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4eb05-107">Syntax</span></span>


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a><span data-ttu-id="4eb05-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4eb05-108">Parameters</span></span>

<span data-ttu-id="4eb05-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4eb05-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4eb05-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4eb05-110">Return value</span></span>

<span data-ttu-id="4eb05-111">Restituisce **true** se il tipo di supporto è parzialmente specificato.</span><span class="sxs-lookup"><span data-stu-id="4eb05-111">Returns **TRUE** if the media type is partially specified.</span></span> <span data-ttu-id="4eb05-112">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="4eb05-112">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb05-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4eb05-113">Remarks</span></span>

<span data-ttu-id="4eb05-114">Il metodo [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) può accettare tipi di supporti parziali.</span><span class="sxs-lookup"><span data-stu-id="4eb05-114">The [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method can accept partial media types.</span></span>

<span data-ttu-id="4eb05-115">L'implementazione non esegue effettivamente il test del sottotipo.</span><span class="sxs-lookup"><span data-stu-id="4eb05-115">The implementation does not actually test the subtype.</span></span> <span data-ttu-id="4eb05-116">Se è presente un tipo di formato specificato, il tipo di supporto non viene considerato parziale, anche se il sottotipo è \_ null GUID.</span><span class="sxs-lookup"><span data-stu-id="4eb05-116">If there is a specified format type, the media type is not considered partial, even if the subtype is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb05-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4eb05-117">Requirements</span></span>



| <span data-ttu-id="4eb05-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb05-118">Requirement</span></span> | <span data-ttu-id="4eb05-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4eb05-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb05-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4eb05-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4eb05-121"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4eb05-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="4eb05-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="4eb05-122">Library</span></span><br/> | <dl> <span data-ttu-id="4eb05-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4eb05-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb05-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4eb05-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb05-125">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="4eb05-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




