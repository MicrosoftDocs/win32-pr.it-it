---
description: Il metodo AlterQuality notifica al filtro che è richiesta una modifica di qualità.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Metodo CTransformFilter. AlterQuality (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325737"
---
# <a name="ctransformfilteralterquality-method"></a><span data-ttu-id="05a89-103">CTransformFilter. AlterQuality, metodo</span><span class="sxs-lookup"><span data-stu-id="05a89-103">CTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="05a89-104">Il `AlterQuality` metodo notifica al filtro che è richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="05a89-104">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a89-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05a89-105">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="05a89-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="05a89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a89-107">*d*</span><span class="sxs-lookup"><span data-stu-id="05a89-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="05a89-108">Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="05a89-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a89-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05a89-109">Return value</span></span>

<span data-ttu-id="05a89-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05a89-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="05a89-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="05a89-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="05a89-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="05a89-112">Return code</span></span>                                                                             | <span data-ttu-id="05a89-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05a89-113">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05a89-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="05a89-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="05a89-115">Il messaggio di qualità non è stato gestito.</span><span class="sxs-lookup"><span data-stu-id="05a89-115">Did not handle the quality message.</span></span> <span data-ttu-id="05a89-116">Il messaggio deve essere passato a Monte.</span><span class="sxs-lookup"><span data-stu-id="05a89-116">The message should be passed upstream.</span></span><br/> |
| <dl> <span data-ttu-id="05a89-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05a89-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="05a89-118">Ha gestito il messaggio qualitativo.</span><span class="sxs-lookup"><span data-stu-id="05a89-118">Handled the quality message.</span></span> <span data-ttu-id="05a89-119">Non sono richieste ulteriori azioni.</span><span class="sxs-lookup"><span data-stu-id="05a89-119">No further action is necessary.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="05a89-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="05a89-120">Remarks</span></span>

<span data-ttu-id="05a89-121">Eseguire l'override di questo metodo se il filtro è in grado di eseguire il controllo qualità.</span><span class="sxs-lookup"><span data-stu-id="05a89-121">Override this method if the filter can perform quality control.</span></span> <span data-ttu-id="05a89-122">Per altre informazioni, vedere [gestione del controllo di qualità](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="05a89-122">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05a89-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05a89-123">Requirements</span></span>



| <span data-ttu-id="05a89-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="05a89-124">Requirement</span></span> | <span data-ttu-id="05a89-125">Valore</span><span class="sxs-lookup"><span data-stu-id="05a89-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a89-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05a89-126">Header</span></span><br/>  | <dl> <span data-ttu-id="05a89-127"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05a89-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="05a89-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="05a89-128">Library</span></span><br/> | <dl> <span data-ttu-id="05a89-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="05a89-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a89-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05a89-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a89-131">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="05a89-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




