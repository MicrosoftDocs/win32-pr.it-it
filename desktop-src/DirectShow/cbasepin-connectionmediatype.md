---
description: 'Il metodo ConnectionMediaType Recupera il tipo di supporto per la connessione pin corrente, se presente. Questo metodo implementa il metodo IPin:: ConnectionMediaType.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Metodo CBasePin. ConnectionMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324690"
---
# <a name="cbasepinconnectionmediatype-method"></a><span data-ttu-id="6363c-104">CBasePin. ConnectionMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="6363c-104">CBasePin.ConnectionMediaType method</span></span>

<span data-ttu-id="6363c-105">Il metodo **ConnectionMediaType** Recupera il tipo di supporto per la connessione pin corrente, se presente.</span><span class="sxs-lookup"><span data-stu-id="6363c-105">The **ConnectionMediaType** method retrieves the media type for the current pin connection, if any.</span></span> <span data-ttu-id="6363c-106">Questo metodo implementa il metodo [**Ipin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .</span><span class="sxs-lookup"><span data-stu-id="6363c-106">This method implements the [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6363c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6363c-107">Syntax</span></span>


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6363c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6363c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6363c-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="6363c-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6363c-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6363c-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6363c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6363c-111">Return value</span></span>

<span data-ttu-id="6363c-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6363c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6363c-113">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6363c-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="6363c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6363c-114">Return code</span></span>                                                                                           | <span data-ttu-id="6363c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6363c-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6363c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6363c-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="6363c-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6363c-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="6363c-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="6363c-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="6363c-119">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="6363c-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="6363c-120"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="6363c-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6363c-121">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="6363c-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="6363c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="6363c-122">Remarks</span></span>

<span data-ttu-id="6363c-123">Se il PIN è connesso, questo metodo copia il tipo di supporto nella struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) specificata da *PMT*. Il chiamante deve liberare il blocco di formato del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6363c-123">If the pin is connected, this method copies the media type into the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specified by *pmt*. The caller must free the media type's format block.</span></span> <span data-ttu-id="6363c-124">È possibile usare la funzione [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) o la funzione di supporto [**FreeMediaType**](freemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6363c-124">You can use the [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function, or the [**FreeMediaType**](freemediatype.md) helper function.</span></span>

<span data-ttu-id="6363c-125">Se il PIN non è connesso, questo metodo Azzera il blocco di memoria specificato da *PMT* e restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="6363c-125">If the pin is not connected, this method zeroes the memory block specified by *pmt* and returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6363c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6363c-126">Requirements</span></span>



| <span data-ttu-id="6363c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6363c-127">Requirement</span></span> | <span data-ttu-id="6363c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6363c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6363c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6363c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6363c-130"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6363c-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6363c-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="6363c-131">Library</span></span><br/> | <dl> <span data-ttu-id="6363c-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6363c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6363c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6363c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6363c-134">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6363c-134">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

