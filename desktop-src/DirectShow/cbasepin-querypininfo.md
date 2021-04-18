---
description: 'Il metodo QueryPinInfo recupera le informazioni sul pin. Questo metodo implementa il metodo IPin:: QueryPinInfo.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Metodo CBasePin. QueryPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328258"
---
# <a name="cbasepinquerypininfo-method"></a><span data-ttu-id="bf552-104">CBasePin. QueryPinInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="bf552-104">CBasePin.QueryPinInfo method</span></span>

<span data-ttu-id="bf552-105">Il `QueryPinInfo` metodo recupera le informazioni sul pin.</span><span class="sxs-lookup"><span data-stu-id="bf552-105">The `QueryPinInfo` method retrieves information about the pin.</span></span> <span data-ttu-id="bf552-106">Questo metodo implementa il metodo [**Ipin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="bf552-106">This method implements the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf552-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf552-107">Syntax</span></span>


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bf552-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf552-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf552-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="bf552-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="bf552-110">Puntatore a una struttura di [**\_ informazioni sul pin**](/windows/win32/api/strmif/ns-strmif-pin_info) che riceve le informazioni sul pin.</span><span class="sxs-lookup"><span data-stu-id="bf552-110">Pointer to a [**PIN\_INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) structure that receives the pin information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf552-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf552-111">Return value</span></span>

<span data-ttu-id="bf552-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="bf552-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf552-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf552-113">Remarks</span></span>

<span data-ttu-id="bf552-114">Questo metodo usa la variabile membro [**CBasePin:: m \_ pname**](cbasepin-m-pname.md) per il membro **achName** della struttura di \_ informazioni del PIN.</span><span class="sxs-lookup"><span data-stu-id="bf552-114">This method uses the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable for the **achName** member of the PIN\_INFO structure.</span></span>

<span data-ttu-id="bf552-115">Quando il metodo restituisce un risultato, se il membro **pFilter** della \_ struttura di informazioni del PIN è diverso da **null**, è presente un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="bf552-115">When the method returns, if the **pFilter** member of the PIN\_INFO structure is non-**NULL**, it has an outstanding reference count.</span></span> <span data-ttu-id="bf552-116">Al termine, assicurarsi di rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="bf552-116">Be sure to release the interface when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf552-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf552-117">Requirements</span></span>



| <span data-ttu-id="bf552-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf552-118">Requirement</span></span> | <span data-ttu-id="bf552-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bf552-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf552-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf552-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bf552-121"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf552-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bf552-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf552-122">Library</span></span><br/> | <dl> <span data-ttu-id="bf552-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf552-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf552-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf552-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf552-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="bf552-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




