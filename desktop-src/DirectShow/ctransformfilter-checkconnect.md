---
description: 'Metodo CTransformFilter.CheckConnect: il metodo CheckConnect determina se una connessione pin è adatta.'
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Metodo CTransformFilter.CheckConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5927aac2fa58322c93a23489a22dc96a1e2a67f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085099"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="e5d5a-103">Metodo CTransformFilter.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="e5d5a-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="e5d5a-104">Il `CheckConnect` metodo determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="e5d5a-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d5a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5d5a-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="e5d5a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5d5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d5a-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="e5d5a-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="e5d5a-108">Membro del [**tipo enumerato PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica quale pin nel filtro sta effettuando la connessione.</span><span class="sxs-lookup"><span data-stu-id="e5d5a-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e5d5a-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="e5d5a-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="e5d5a-110">Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="e5d5a-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d5a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5d5a-111">Return value</span></span>

<span data-ttu-id="e5d5a-112">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5d5a-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5d5a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5d5a-113">Remarks</span></span>

<span data-ttu-id="e5d5a-114">I [**metodi CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) e [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) chiamano questo metodo durante il processo di connessione del pin.</span><span class="sxs-lookup"><span data-stu-id="e5d5a-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="e5d5a-115">Questo metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="e5d5a-115">This method does nothing in the base class.</span></span> <span data-ttu-id="e5d5a-116">La classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="e5d5a-116">The derived class can override it.</span></span> <span data-ttu-id="e5d5a-117">Ad esempio, la classe derivata potrebbe eseguire una query sull'altro pin per una particolare interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e5d5a-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d5a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5d5a-118">Requirements</span></span>



| <span data-ttu-id="e5d5a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d5a-119">Requirement</span></span> | <span data-ttu-id="e5d5a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e5d5a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d5a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5d5a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e5d5a-122"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5d5a-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e5d5a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5d5a-123">Library</span></span><br/> | <dl> <span data-ttu-id="e5d5a-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e5d5a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5d5a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5d5a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d5a-126">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="e5d5a-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




