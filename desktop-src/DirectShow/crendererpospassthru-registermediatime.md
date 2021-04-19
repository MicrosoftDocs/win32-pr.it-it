---
description: Il metodo RegisterMediaTime memorizza nella cache i timestamp dell'esempio corrente.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Metodo CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327201"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="625a2-103">Metodo CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="625a2-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="625a2-104">Il metodo **RegisterMediaTime** memorizza nella cache i timestamp dell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="625a2-104">The **RegisterMediaTime** method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="625a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="625a2-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="625a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="625a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="625a2-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="625a2-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="625a2-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="625a2-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="625a2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="625a2-109">Return value</span></span>

<span data-ttu-id="625a2-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="625a2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="625a2-111">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="625a2-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="625a2-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="625a2-112">Return code</span></span>                                                                                                  | <span data-ttu-id="625a2-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="625a2-113">Description</span></span>                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="625a2-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="625a2-114"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="625a2-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="625a2-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="625a2-116"><dt>**\_ \_ tempo medio E \_ \_ non \_ impostato per VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="625a2-116"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="625a2-117">Per l'esempio non è indicato il timestamp.</span><span class="sxs-lookup"><span data-stu-id="625a2-117">The sample is not time-stamped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="625a2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="625a2-118">Remarks</span></span>

<span data-ttu-id="625a2-119">Questo metodo archivia i timestamp dell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="625a2-119">This method stores the time stamps from the current sample.</span></span> <span data-ttu-id="625a2-120">Il metodo [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera gli stessi valori.</span><span class="sxs-lookup"><span data-stu-id="625a2-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="625a2-121">Il filtro deve chiamare questo metodo per ogni campione che riceve.</span><span class="sxs-lookup"><span data-stu-id="625a2-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="625a2-122">Il metodo è sottoposto a overload per accettare un puntatore all'esempio o i valori timestamp stessi.</span><span class="sxs-lookup"><span data-stu-id="625a2-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="625a2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="625a2-123">Requirements</span></span>



| <span data-ttu-id="625a2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="625a2-124">Requirement</span></span> | <span data-ttu-id="625a2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="625a2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="625a2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="625a2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="625a2-127"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="625a2-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="625a2-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="625a2-128">Library</span></span><br/> | <dl> <span data-ttu-id="625a2-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="625a2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




