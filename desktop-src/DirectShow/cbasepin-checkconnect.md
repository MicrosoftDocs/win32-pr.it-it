---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Metodo CBasePin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d5c221da417fd1fc2b3f9f140536f825b2f9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332769"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="d07e8-103">CBasePin. CheckConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="d07e8-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="d07e8-104">Il `CheckConnect` metodo determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="d07e8-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d07e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d07e8-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="d07e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d07e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d07e8-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="d07e8-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d07e8-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.</span><span class="sxs-lookup"><span data-stu-id="d07e8-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d07e8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d07e8-109">Return value</span></span>

<span data-ttu-id="d07e8-110">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d07e8-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d07e8-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d07e8-111">Return code</span></span>                                                                                               | <span data-ttu-id="d07e8-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d07e8-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="d07e8-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d07e8-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="d07e8-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d07e8-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="d07e8-115"><dt>**\_direzione VFW E \_ non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d07e8-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="d07e8-116">Le direzioni del PIN non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="d07e8-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d07e8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d07e8-117">Remarks</span></span>

<span data-ttu-id="d07e8-118">Questo metodo viene chiamato su entrambi i pin all'avvio del processo di connessione.</span><span class="sxs-lookup"><span data-stu-id="d07e8-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="d07e8-119">Il pin di connessione lo chiama dall'interno del metodo [**CBasePin:: Connect**](cbasepin-connect.md) e il pin ricevente lo chiama dall'interno del metodo [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="d07e8-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="d07e8-120">Utilizzare questo metodo per determinare se il PIN specificato dal parametro *pPin* è adatto a una connessione.</span><span class="sxs-lookup"><span data-stu-id="d07e8-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="d07e8-121">La classe base restituisce un errore se entrambi i pin hanno la stessa direzione (sia di input sia di output).</span><span class="sxs-lookup"><span data-stu-id="d07e8-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="d07e8-122">Le classi derivate possono eseguire l'override di questo metodo per verificare altre funzionalità nel pin.</span><span class="sxs-lookup"><span data-stu-id="d07e8-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="d07e8-123">Ad esempio, la classe [**CBaseOutputPin**](cbaseoutputpin.md) esegue una query sul pin di input per la relativa interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="d07e8-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="d07e8-124">Se questo metodo ha esito negativo, la connessione ha esito negativo e il pin chiama il metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="d07e8-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="d07e8-125">Usare **BreakConnect** per liberare le risorse ottenute in `CheckConnect` .</span><span class="sxs-lookup"><span data-stu-id="d07e8-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="d07e8-126">Se, ad esempio, `CheckConnect` chiama il metodo **QueryInterface** , **BreakConnect** deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d07e8-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d07e8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d07e8-127">Requirements</span></span>



| <span data-ttu-id="d07e8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d07e8-128">Requirement</span></span> | <span data-ttu-id="d07e8-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d07e8-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07e8-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d07e8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d07e8-131"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d07e8-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d07e8-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="d07e8-132">Library</span></span><br/> | <dl> <span data-ttu-id="d07e8-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d07e8-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d07e8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d07e8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d07e8-135">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="d07e8-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




