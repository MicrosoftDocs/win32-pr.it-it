---
description: Il \_ metodo Get jitter recupera la deviazione standard del tempo in millisecondi tra ogni frame e il successivo per tutti i frame dall'avvio dello streaming.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Metodo CBaseVideoRenderer.get_Jitter (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326416"
---
# <a name="cbasevideorendererget_jitter-method"></a><span data-ttu-id="3e383-103">Metodo CBaseVideoRenderer. Get \_ jitter</span><span class="sxs-lookup"><span data-stu-id="3e383-103">CBaseVideoRenderer.get\_Jitter method</span></span>

<span data-ttu-id="3e383-104">Il `get_Jitter` metodo recupera la deviazione standard di tempo in millisecondi tra ogni frame e il successivo per tutti i frame dall'avvio dello streaming.</span><span class="sxs-lookup"><span data-stu-id="3e383-104">The `get_Jitter` method retrieves the standard deviation of time in milliseconds between each frame and the next for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e383-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e383-105">Syntax</span></span>


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a><span data-ttu-id="3e383-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e383-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e383-107">*piJitter*</span><span class="sxs-lookup"><span data-stu-id="3e383-107">*piJitter*</span></span> 
</dt> <dd>

<span data-ttu-id="3e383-108">Puntatore alla deviazione standard del tempo di interframe, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="3e383-108">Pointer to the standard deviation of the interframe time, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e383-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e383-109">Return value</span></span>

<span data-ttu-id="3e383-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e383-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e383-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e383-111">Remarks</span></span>

<span data-ttu-id="3e383-112">Questa funzione membro implementa il metodo [**IQualProp:: Get \_ jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .</span><span class="sxs-lookup"><span data-stu-id="3e383-112">This member function implements the [**IQualProp::get\_Jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e383-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e383-113">Requirements</span></span>



| <span data-ttu-id="3e383-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e383-114">Requirement</span></span> | <span data-ttu-id="3e383-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3e383-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e383-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e383-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3e383-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e383-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e383-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e383-118">Library</span></span><br/> | <dl> <span data-ttu-id="3e383-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3e383-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e383-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e383-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e383-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="3e383-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




