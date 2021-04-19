---
description: 'Il metodo QueryFilterInfo recupera le informazioni sul filtro. Questo metodo implementa il metodo IBaseFilter:: QueryFilterInfo.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Metodo CBaseFilter. QueryFilterInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333492"
---
# <a name="cbasefilterqueryfilterinfo-method"></a><span data-ttu-id="87a7e-104">CBaseFilter. QueryFilterInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="87a7e-104">CBaseFilter.QueryFilterInfo method</span></span>

<span data-ttu-id="87a7e-105">Il `QueryFilterInfo` metodo recupera le informazioni sul filtro.</span><span class="sxs-lookup"><span data-stu-id="87a7e-105">The `QueryFilterInfo` method retrieves information about the filter.</span></span> <span data-ttu-id="87a7e-106">Questo metodo implementa il metodo [**IBaseFilter:: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .</span><span class="sxs-lookup"><span data-stu-id="87a7e-106">This method implements the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a7e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87a7e-107">Syntax</span></span>


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="87a7e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="87a7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a7e-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="87a7e-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="87a7e-110">Puntatore a una struttura di [**\_ informazioni sul filtro**](/windows/win32/api/strmif/ns-strmif-filter_info) .</span><span class="sxs-lookup"><span data-stu-id="87a7e-110">Pointer to a [**FILTER\_INFO**](/windows/win32/api/strmif/ns-strmif-filter_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a7e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87a7e-111">Return value</span></span>

<span data-ttu-id="87a7e-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="87a7e-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="87a7e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="87a7e-113">Remarks</span></span>

<span data-ttu-id="87a7e-114">Questo metodo copia il nome del filtro dalla variabile membro [**CBaseFilter:: m \_ pname**](cbasefilter-m-pname.md) nel membro **achName** della struttura delle informazioni sul filtro \_ .</span><span class="sxs-lookup"><span data-stu-id="87a7e-114">This method copies the filter's name from the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable into the **achName** member of the FILTER\_INFO structure.</span></span> <span data-ttu-id="87a7e-115">Se **m \_ pname** è **null**, il metodo imposta **achName** su L' \\ 0'.</span><span class="sxs-lookup"><span data-stu-id="87a7e-115">If **m\_pName** is **NULL**, the method sets **achName** to L'\\0'.</span></span>

<span data-ttu-id="87a7e-116">Il metodo imposta il membro **pGraph** della struttura di \_ informazioni sul filtro uguale alla variabile membro [**\_ pGraph di CBaseFilter:: m**](cbasefilter-m-pgraph.md) e incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="87a7e-116">The method sets the **pGraph** member of the FILTER\_INFO structure equal to the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable, and increments the reference count.</span></span> <span data-ttu-id="87a7e-117">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="87a7e-117">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a7e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87a7e-118">Requirements</span></span>



| <span data-ttu-id="87a7e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="87a7e-119">Requirement</span></span> | <span data-ttu-id="87a7e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="87a7e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a7e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87a7e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="87a7e-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87a7e-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87a7e-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="87a7e-123">Library</span></span><br/> | <dl> <span data-ttu-id="87a7e-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="87a7e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a7e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87a7e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a7e-126">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="87a7e-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




