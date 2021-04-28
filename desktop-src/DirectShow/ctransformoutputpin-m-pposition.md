---
description: 'CTransformOutputPin::m_pPosition: oggetto helper per passare i comandi di ricerca a monte.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: Membro CTransformOutputPin::m_pPosition (Transfrm.h)
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
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084859"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="e6d6a-103">Membro CTransformOutputPin::m \_ pPosition</span><span class="sxs-lookup"><span data-stu-id="e6d6a-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="e6d6a-104">Oggetto helper per passare i comandi di ricerca a monte.</span><span class="sxs-lookup"><span data-stu-id="e6d6a-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d6a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6d6a-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="e6d6a-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e6d6a-106">Remarks</span></span>

<span data-ttu-id="e6d6a-107">Quando il pin viene sottoposto a query per la prima volta per [**l'interfaccia IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) crea e aggrega un oggetto helper [**CPosPassThru.**](cpospassthru.md)</span><span class="sxs-lookup"><span data-stu-id="e6d6a-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d6a-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6d6a-108">Requirements</span></span>



| <span data-ttu-id="e6d6a-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d6a-109">Requirement</span></span> | <span data-ttu-id="e6d6a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e6d6a-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d6a-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6d6a-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e6d6a-112"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d6a-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e6d6a-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6d6a-113">Library</span></span><br/> | <dl> <span data-ttu-id="e6d6a-114"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d6a-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




