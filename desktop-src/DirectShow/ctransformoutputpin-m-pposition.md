---
description: Oggetto helper per passare i comandi Seek upstream.
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Membro CTransformOutputPin:: m_pPosition (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330842"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="fbd35-103">Membro pPosition di CTransformOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="fbd35-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="fbd35-104">Oggetto helper per passare i comandi Seek upstream.</span><span class="sxs-lookup"><span data-stu-id="fbd35-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd35-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbd35-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="fbd35-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="fbd35-106">Remarks</span></span>

<span data-ttu-id="fbd35-107">Quando il PIN viene prima sottoposto a query per l'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , crea e aggrega un oggetto helper [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd35-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd35-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbd35-108">Requirements</span></span>



| <span data-ttu-id="fbd35-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbd35-109">Requirement</span></span> | <span data-ttu-id="fbd35-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fbd35-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd35-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbd35-111">Header</span></span><br/>  | <dl> <span data-ttu-id="fbd35-112"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbd35-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fbd35-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="fbd35-113">Library</span></span><br/> | <dl> <span data-ttu-id="fbd35-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fbd35-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




