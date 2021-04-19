---
description: 'Il metodo Unadvise rimuove una richiesta di notifica in sospeso. Questo metodo implementa il metodo IReferenceClock:: Unadvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Metodo CBaseReferenceClock. Unadvise (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332215"
---
# <a name="cbasereferenceclockunadvise-method"></a><span data-ttu-id="436b2-104">Metodo CBaseReferenceClock. Unadvise</span><span class="sxs-lookup"><span data-stu-id="436b2-104">CBaseReferenceClock.Unadvise method</span></span>

<span data-ttu-id="436b2-105">Il `Unadvise` metodo rimuove una richiesta di notifica in sospeso.</span><span class="sxs-lookup"><span data-stu-id="436b2-105">The `Unadvise` method removes a pending advise request.</span></span> <span data-ttu-id="436b2-106">Questo metodo implementa il metodo [**IReferenceClock:: Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .</span><span class="sxs-lookup"><span data-stu-id="436b2-106">This method implements the [**IReferenceClock::Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="436b2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="436b2-107">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="436b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="436b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="436b2-109">*dwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="436b2-109">*dwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="436b2-110">Identificatore della richiesta da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="436b2-110">Identifier of the request to remove.</span></span> <span data-ttu-id="436b2-111">Usare il valore restituito dai metodi [**CBaseReferenceClock:: AdviseTime**](cbasereferenceclock-advisetime.md) o [**CBaseReferenceClock:: AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) nel parametro *pdwAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="436b2-111">Use the value returned by the [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) or [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) methods in the *pdwAdviseToken* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="436b2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="436b2-112">Return value</span></span>

<span data-ttu-id="436b2-113">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="436b2-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="436b2-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="436b2-114">Return code</span></span>                                                                             | <span data-ttu-id="436b2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="436b2-115">Description</span></span>           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="436b2-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="436b2-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="436b2-117">Non trovato.</span><span class="sxs-lookup"><span data-stu-id="436b2-117">Not found.</span></span><br/> |
| <dl> <span data-ttu-id="436b2-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="436b2-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="436b2-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="436b2-119">Success.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="436b2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="436b2-120">Requirements</span></span>



| <span data-ttu-id="436b2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="436b2-121">Requirement</span></span> | <span data-ttu-id="436b2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="436b2-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="436b2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="436b2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="436b2-124"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="436b2-124"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="436b2-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="436b2-125">Library</span></span><br/> | <dl> <span data-ttu-id="436b2-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="436b2-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="436b2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="436b2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="436b2-128">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="436b2-128">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




