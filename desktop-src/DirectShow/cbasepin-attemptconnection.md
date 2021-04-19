---
description: Il metodo AttemptConnection si connette a un altro PIN usando un tipo di supporto specificato.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Metodo CBasePin. AttemptConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332772"
---
# <a name="cbasepinattemptconnection-method"></a><span data-ttu-id="25799-103">CBasePin. AttemptConnection, metodo</span><span class="sxs-lookup"><span data-stu-id="25799-103">CBasePin.AttemptConnection method</span></span>

<span data-ttu-id="25799-104">Il `AttemptConnection` metodo si connette a un altro PIN utilizzando un tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="25799-104">The `AttemptConnection` method connects to another pin using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="25799-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25799-105">Syntax</span></span>


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="25799-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25799-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25799-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="25799-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="25799-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di ricezione.</span><span class="sxs-lookup"><span data-stu-id="25799-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="25799-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="25799-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="25799-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="25799-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25799-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25799-111">Return value</span></span>

<span data-ttu-id="25799-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25799-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="25799-113">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="25799-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="25799-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="25799-114">Return code</span></span>                                                                                                | <span data-ttu-id="25799-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25799-115">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="25799-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25799-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="25799-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="25799-117">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="25799-118"><dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt></span><span class="sxs-lookup"><span data-stu-id="25799-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="25799-119">Il tipo di supporto non è accettabile.</span><span class="sxs-lookup"><span data-stu-id="25799-119">The media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25799-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="25799-120">Remarks</span></span>

<span data-ttu-id="25799-121">Questo metodo tenta di connettere i due pin con un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="25799-121">This method attempts to connect the two pins with a specific media type.</span></span> <span data-ttu-id="25799-122">Se il tipo non è accettabile, il metodo ha esito negativo senza provare altri tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="25799-122">If the type is not acceptable, the method fails without trying other media types.</span></span>

<span data-ttu-id="25799-123">Se il tipo di supporto è accettabile, questo metodo chiama il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN di ricezione.</span><span class="sxs-lookup"><span data-stu-id="25799-123">If the media type is acceptable, this method calls the receiving pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="25799-124">Chiama quindi il metodo [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) per completare la connessione.</span><span class="sxs-lookup"><span data-stu-id="25799-124">Then it calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method to complete the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="25799-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25799-125">Requirements</span></span>



| <span data-ttu-id="25799-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="25799-126">Requirement</span></span> | <span data-ttu-id="25799-127">Valore</span><span class="sxs-lookup"><span data-stu-id="25799-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25799-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25799-128">Header</span></span><br/>  | <dl> <span data-ttu-id="25799-129"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25799-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="25799-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="25799-130">Library</span></span><br/> | <dl> <span data-ttu-id="25799-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="25799-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25799-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25799-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25799-133">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="25799-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




