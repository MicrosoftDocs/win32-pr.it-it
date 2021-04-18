---
description: Metodo del costruttore.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Costruttore CSeekingPassThru. CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a93ed9706762b9a1672bfae85550ee4c2aceeead
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324666"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="440e5-103">Costruttore CSeekingPassThru. CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="440e5-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="440e5-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="440e5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="440e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="440e5-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="440e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="440e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="440e5-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="440e5-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="440e5-108">Stringa contenente il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="440e5-108">String containing the name of the object.</span></span> <span data-ttu-id="440e5-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="440e5-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="440e5-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="440e5-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="440e5-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="440e5-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="440e5-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="440e5-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="440e5-113">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="440e5-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="440e5-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="440e5-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="440e5-115">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="440e5-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="440e5-116">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="440e5-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="440e5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="440e5-117">Requirements</span></span>



| <span data-ttu-id="440e5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="440e5-118">Requirement</span></span> | <span data-ttu-id="440e5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="440e5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="440e5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="440e5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="440e5-121"><dt>Seekpt. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="440e5-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="440e5-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="440e5-122">Library</span></span><br/> | <dl> <span data-ttu-id="440e5-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="440e5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="440e5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="440e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="440e5-125">**Classe CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="440e5-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




