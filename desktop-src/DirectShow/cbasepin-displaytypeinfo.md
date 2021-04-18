---
description: Il metodo DisplayTypeInfo Visualizza le informazioni sul tipo di supporto durante il debug.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Metodo CBasePin. DisplayTypeInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329539"
---
# <a name="cbasepindisplaytypeinfo-method"></a><span data-ttu-id="f7792-103">CBasePin. DisplayTypeInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="f7792-103">CBasePin.DisplayTypeInfo method</span></span>

<span data-ttu-id="f7792-104">Il `DisplayTypeInfo` Metodo Visualizza le informazioni sul tipo di supporto durante il debug.</span><span class="sxs-lookup"><span data-stu-id="f7792-104">The `DisplayTypeInfo` method displays media type information during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7792-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7792-105">Syntax</span></span>


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="f7792-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7792-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7792-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="f7792-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f7792-108">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="f7792-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f7792-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="f7792-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f7792-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f7792-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7792-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7792-111">Return value</span></span>

<span data-ttu-id="f7792-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f7792-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7792-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7792-113">Remarks</span></span>

<span data-ttu-id="f7792-114">Nelle compilazioni di debug questo metodo chiama la funzione [**DbgLog**](dbglog.md) per visualizzare il tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="f7792-114">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to display the specified media type.</span></span> <span data-ttu-id="f7792-115">Nelle compilazioni finali, questo metodo non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="f7792-115">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7792-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7792-116">Requirements</span></span>



| <span data-ttu-id="f7792-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7792-117">Requirement</span></span> | <span data-ttu-id="f7792-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f7792-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7792-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7792-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f7792-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7792-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f7792-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7792-121">Library</span></span><br/> | <dl> <span data-ttu-id="f7792-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f7792-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7792-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7792-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7792-124">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="f7792-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




