---
description: Il metodo GetMediaPositionInterface recupera i puntatori dell'interfaccia IMediaPosition e IMediaSeeking del filtro.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Metodo CBaseRenderer. GetMediaPositionInterface (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325521"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a><span data-ttu-id="6673e-103">CBaseRenderer. GetMediaPositionInterface, metodo</span><span class="sxs-lookup"><span data-stu-id="6673e-103">CBaseRenderer.GetMediaPositionInterface method</span></span>

<span data-ttu-id="6673e-104">Il `GetMediaPositionInterface` metodo recupera i puntatori dell'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro.</span><span class="sxs-lookup"><span data-stu-id="6673e-104">The `GetMediaPositionInterface` method retrieves the filter's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6673e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6673e-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="6673e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6673e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6673e-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="6673e-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="6673e-108">Identificatore di riferimento dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6673e-108">Reference identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="6673e-109">*PPV*</span><span class="sxs-lookup"><span data-stu-id="6673e-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="6673e-110">Indirizzo di una variabile che riceve il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6673e-110">Address of a variable that receives the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6673e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6673e-111">Return value</span></span>

<span data-ttu-id="6673e-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6673e-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6673e-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6673e-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6673e-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6673e-114">Return code</span></span>                                                                                   | <span data-ttu-id="6673e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6673e-115">Description</span></span>                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="6673e-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6673e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6673e-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6673e-117">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="6673e-118"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="6673e-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6673e-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="6673e-119">Insufficient memory.</span></span><br/>     |
| <dl> <span data-ttu-id="6673e-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="6673e-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="6673e-121">Interfaccia non supportata.</span><span class="sxs-lookup"><span data-stu-id="6673e-121">Interface not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6673e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="6673e-122">Remarks</span></span>

<span data-ttu-id="6673e-123">Il filtro delega tutti i comandi di ricerca a un oggetto [**CRendererPosPassThru**](crendererpospassthru.md) , che li passa a upstream.</span><span class="sxs-lookup"><span data-stu-id="6673e-123">The filter delegates all seeking commands to a [**CRendererPosPassThru**](crendererpospassthru.md) object, which passes them upstream.</span></span> <span data-ttu-id="6673e-124">Questo metodo crea l'oggetto **CRendererPosPassThru** , se non esiste ancora, ed esegue una query per l'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="6673e-124">This method creates the **CRendererPosPassThru** object, if it does not yet exist, and queries it for the requested interface.</span></span>

<span data-ttu-id="6673e-125">La variabile membro [**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md) archivia un puntatore all'oggetto **CRendererPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="6673e-125">The [**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md) member variable stores a pointer to the **CRendererPosPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6673e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6673e-126">Requirements</span></span>



| <span data-ttu-id="6673e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6673e-127">Requirement</span></span> | <span data-ttu-id="6673e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6673e-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6673e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6673e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6673e-130"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6673e-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6673e-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="6673e-131">Library</span></span><br/> | <dl> <span data-ttu-id="6673e-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6673e-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6673e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6673e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6673e-134">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="6673e-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




