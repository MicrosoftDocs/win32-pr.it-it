---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Metodo CTransformFilter. CheckConnect (Transfrm. h)
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
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325732"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="cb8e4-103">CTransformFilter. CheckConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="cb8e4-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="cb8e4-104">Il `CheckConnect` metodo determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="cb8e4-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb8e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb8e4-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="cb8e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb8e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb8e4-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="cb8e4-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="cb8e4-108">Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica quale pin del filtro sta effettuando la connessione.</span><span class="sxs-lookup"><span data-stu-id="cb8e4-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="cb8e4-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="cb8e4-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="cb8e4-110">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="cb8e4-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb8e4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb8e4-111">Return value</span></span>

<span data-ttu-id="cb8e4-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb8e4-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb8e4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb8e4-113">Remarks</span></span>

<span data-ttu-id="cb8e4-114">I metodi [**CTransformInputPin:: CheckConnect**](ctransforminputpin-checkconnect.md) e [**CTransformOutputPin:: CheckConnect**](ctransformoutputpin-checkconnect.md) chiamano questo metodo durante il processo di connessione del PIN.</span><span class="sxs-lookup"><span data-stu-id="cb8e4-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="cb8e4-115">Questo metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="cb8e4-115">This method does nothing in the base class.</span></span> <span data-ttu-id="cb8e4-116">La classe derivata può eseguire l'override.</span><span class="sxs-lookup"><span data-stu-id="cb8e4-116">The derived class can override it.</span></span> <span data-ttu-id="cb8e4-117">La classe derivata può ad esempio eseguire una query sull'altro pin per una particolare interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cb8e4-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb8e4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb8e4-118">Requirements</span></span>



| <span data-ttu-id="cb8e4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb8e4-119">Requirement</span></span> | <span data-ttu-id="cb8e4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cb8e4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8e4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb8e4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cb8e4-122"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb8e4-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cb8e4-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb8e4-123">Library</span></span><br/> | <dl> <span data-ttu-id="cb8e4-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb8e4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb8e4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb8e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb8e4-126">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="cb8e4-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




