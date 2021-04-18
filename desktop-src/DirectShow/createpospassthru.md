---
description: La funzione CreatePosPassThru crea un oggetto CPosPassThru o un oggetto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Funzione CreatePosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331313"
---
# <a name="createpospassthru-function"></a><span data-ttu-id="d68a5-103">CreatePosPassThru (funzione)</span><span class="sxs-lookup"><span data-stu-id="d68a5-103">CreatePosPassThru function</span></span>

<span data-ttu-id="d68a5-104">La `CreatePosPassThru` funzione crea un oggetto [**CPosPassThru**](cpospassthru.md) o un oggetto [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="d68a5-104">The `CreatePosPassThru` function creates a [**CPosPassThru**](cpospassthru.md) object or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d68a5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d68a5-105">Syntax</span></span>


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a><span data-ttu-id="d68a5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d68a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d68a5-107">*pAgg*</span><span class="sxs-lookup"><span data-stu-id="d68a5-107">*pAgg*</span></span> 
</dt> <dd>

<span data-ttu-id="d68a5-108">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68a5-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="d68a5-109">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="d68a5-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="d68a5-110">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="d68a5-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d68a5-111">*bRenderer*</span><span class="sxs-lookup"><span data-stu-id="d68a5-111">*bRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="d68a5-112">Valore booleano che specifica se il filtro è un renderer.</span><span class="sxs-lookup"><span data-stu-id="d68a5-112">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="d68a5-113">Usare il valore **true** se il filtro è un renderer oppure **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d68a5-113">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span> <span data-ttu-id="d68a5-114">Se il valore è **true**, questo metodo crea un'istanza della classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="d68a5-114">If the value is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="d68a5-115">Se il valore è **false**, il metodo crea un'istanza della classe **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="d68a5-115">If the value is **FALSE**, the method creates an instance of the **CPosPassThru** class.</span></span>

</dd> <dt>

<span data-ttu-id="d68a5-116">*pPin*</span><span class="sxs-lookup"><span data-stu-id="d68a5-116">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d68a5-117">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) sul pin di input del filtro.</span><span class="sxs-lookup"><span data-stu-id="d68a5-117">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> <dt>

<span data-ttu-id="d68a5-118">*ppPassThru*</span><span class="sxs-lookup"><span data-stu-id="d68a5-118">*ppPassThru*</span></span> 
</dt> <dd>

<span data-ttu-id="d68a5-119">Indirizzo di una variabile che riceve un puntatore all'interfaccia **IUnknown** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68a5-119">Address of a variable that receives a pointer to the object's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d68a5-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d68a5-120">Return value</span></span>

<span data-ttu-id="d68a5-121">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d68a5-121">Returns S\_OK if successful.</span></span> <span data-ttu-id="d68a5-122">In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="d68a5-122">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d68a5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d68a5-123">Remarks</span></span>

<span data-ttu-id="d68a5-124">Questo metodo utilizza l'interfaccia [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68a5-124">This method uses the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface to create the object.</span></span> <span data-ttu-id="d68a5-125">L'oggetto viene caricato dinamicamente da Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="d68a5-125">The object is loaded dynamically from Quartz.dll.</span></span>

<span data-ttu-id="d68a5-126">Se la funzione ha esito positivo, l'interfaccia **IUnknown** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="d68a5-126">If the function succeeds, the returned **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="d68a5-127">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d68a5-127">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d68a5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d68a5-128">Requirements</span></span>



| <span data-ttu-id="d68a5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d68a5-129">Requirement</span></span> | <span data-ttu-id="d68a5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d68a5-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d68a5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d68a5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d68a5-132"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d68a5-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d68a5-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="d68a5-133">Library</span></span><br/> | <dl> <span data-ttu-id="d68a5-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d68a5-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d68a5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d68a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d68a5-136">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="d68a5-136">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




