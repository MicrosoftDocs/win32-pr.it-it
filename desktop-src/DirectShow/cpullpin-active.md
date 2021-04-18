---
description: Il metodo attivo crea un thread di lavoro che estrae i dati dal pin di output. Questo metodo consente inoltre di eseguire il commit dell'allocatore.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Metodo CPullPin. Active (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333716"
---
# <a name="cpullpinactive-method"></a><span data-ttu-id="9a6d7-104">Metodo CPullPin. Active</span><span class="sxs-lookup"><span data-stu-id="9a6d7-104">CPullPin.Active method</span></span>

<span data-ttu-id="9a6d7-105">Il metodo **attivo** crea un thread di lavoro che estrae i dati dal pin di output.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-105">The **Active** method creates a worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="9a6d7-106">Questo metodo consente inoltre di eseguire il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-106">This method also commits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a6d7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a6d7-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="9a6d7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a6d7-108">Parameters</span></span>

<span data-ttu-id="9a6d7-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a6d7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a6d7-110">Return value</span></span>

<span data-ttu-id="9a6d7-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a6d7-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9a6d7-112">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-112">Possible values include the following.</span></span>



| <span data-ttu-id="9a6d7-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9a6d7-113">Return code</span></span>                                                                                  | <span data-ttu-id="9a6d7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a6d7-114">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a6d7-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a6d7-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9a6d7-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="9a6d7-117"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="9a6d7-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="9a6d7-118">La connessione del PIN non è stata stabilita correttamente.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-118">The pin connection was not established correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="9a6d7-119"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="9a6d7-119"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="9a6d7-120">Non è stato possibile creare il thread oppure il thread esiste già.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-120">Could not create the thread, or the thread already exists.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a6d7-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a6d7-121">Remarks</span></span>

<span data-ttu-id="9a6d7-122">Chiamare questo metodo quando il filtro proprietario diventa attivo.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-122">Call this method when the owning filter becomes active.</span></span> <span data-ttu-id="9a6d7-123">Se il pin di input deriva da [**CBasePin**](cbasepin.md), eseguire l'override del metodo [**CBasePin:: Active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="9a6d7-123">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Active**](cbasepin-active.md) method.)</span></span>

<span data-ttu-id="9a6d7-124">Prima di chiamare questo metodo, chiamare il metodo [**CPullPin:: Connect**](cpullpin-connect.md) per stabilire la connessione con il pin di output.</span><span class="sxs-lookup"><span data-stu-id="9a6d7-124">Before calling this method, call the [**CPullPin::Connect**](cpullpin-connect.md) method to establish the connection with the output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a6d7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a6d7-125">Requirements</span></span>



| <span data-ttu-id="9a6d7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a6d7-126">Requirement</span></span> | <span data-ttu-id="9a6d7-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9a6d7-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6d7-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a6d7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9a6d7-129"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a6d7-129"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="9a6d7-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a6d7-130">Library</span></span><br/> | <dl> <span data-ttu-id="9a6d7-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9a6d7-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a6d7-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a6d7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a6d7-133">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="9a6d7-133">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




