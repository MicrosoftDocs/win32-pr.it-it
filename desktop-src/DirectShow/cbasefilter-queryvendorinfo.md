---
description: 'Il metodo QueryVendorInfo recupera una stringa contenente informazioni sul fornitore. Questo metodo implementa il metodo IBaseFilter:: QueryVendorInfo.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Metodo CBaseFilter. QueryVendorInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333491"
---
# <a name="cbasefilterqueryvendorinfo-method"></a><span data-ttu-id="0eccc-104">CBaseFilter. QueryVendorInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="0eccc-104">CBaseFilter.QueryVendorInfo method</span></span>

<span data-ttu-id="0eccc-105">Il `QueryVendorInfo` metodo recupera una stringa contenente le informazioni sul fornitore.</span><span class="sxs-lookup"><span data-stu-id="0eccc-105">The `QueryVendorInfo` method retrieves a string containing vendor information.</span></span> <span data-ttu-id="0eccc-106">Questo metodo implementa il metodo [**IBaseFilter:: QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .</span><span class="sxs-lookup"><span data-stu-id="0eccc-106">This method implements the [**IBaseFilter::QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eccc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0eccc-107">Syntax</span></span>


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0eccc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0eccc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eccc-109">*pVendorInfo*</span><span class="sxs-lookup"><span data-stu-id="0eccc-109">*pVendorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0eccc-110">Indirizzo di una variabile che riceve un puntatore a una stringa di caratteri wide contenente le informazioni sul fornitore.</span><span class="sxs-lookup"><span data-stu-id="0eccc-110">Address of a variable that receives a pointer to a wide-character string containing the vendor information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eccc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0eccc-111">Return value</span></span>

<span data-ttu-id="0eccc-112">Restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="0eccc-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eccc-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0eccc-113">Remarks</span></span>

<span data-ttu-id="0eccc-114">Per fornire informazioni sul fornitore per un filtro, eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0eccc-114">To provide vendor information for a filter, override this method.</span></span> <span data-ttu-id="0eccc-115">Se si implementa questo metodo, utilizzare la funzione **CoTaskMemAlloc** per allocare memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="0eccc-115">If you implement this method, use the **CoTaskMemAlloc** function to allocate memory for the string.</span></span> <span data-ttu-id="0eccc-116">Il chiamante è responsabile della chiamata della funzione **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="0eccc-116">The caller is responsible for calling the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eccc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0eccc-117">Requirements</span></span>



| <span data-ttu-id="0eccc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eccc-118">Requirement</span></span> | <span data-ttu-id="0eccc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0eccc-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eccc-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0eccc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0eccc-121"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0eccc-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0eccc-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="0eccc-122">Library</span></span><br/> | <dl> <span data-ttu-id="0eccc-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0eccc-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eccc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0eccc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eccc-125">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="0eccc-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




