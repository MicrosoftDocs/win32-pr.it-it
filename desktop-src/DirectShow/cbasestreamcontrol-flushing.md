---
description: Il metodo di scaricamento notifica alla classe di base che il pin ha avviato o interrotto lo svuotamento.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Metodo CBaseStreamControl. Flushing (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330526"
---
# <a name="cbasestreamcontrolflushing-method"></a><span data-ttu-id="1b9fa-103">Metodo CBaseStreamControl. Flushing</span><span class="sxs-lookup"><span data-stu-id="1b9fa-103">CBaseStreamControl.Flushing method</span></span>

<span data-ttu-id="1b9fa-104">Il `Flushing` metodo notifica alla classe di base che il pin ha avviato o interrotto lo svuotamento.</span><span class="sxs-lookup"><span data-stu-id="1b9fa-104">The `Flushing` method notifies the base class that the pin has started or stopped flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b9fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b9fa-105">Syntax</span></span>


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a><span data-ttu-id="1b9fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b9fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b9fa-107">*bInProgress*</span><span class="sxs-lookup"><span data-stu-id="1b9fa-107">*bInProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="1b9fa-108">Specifica un valore booleano che indica se il PIN sta per essere scaricato.</span><span class="sxs-lookup"><span data-stu-id="1b9fa-108">Specifies a Boolean value that indicates whether the pin is flushing.</span></span> <span data-ttu-id="1b9fa-109">Usare il valore **true** quando il pin inizia un'operazione di scaricamento e **false** quando il pin termina un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="1b9fa-109">Use the value **TRUE** when the pin begins a flush operation, and **FALSE** when the pin ends a flush operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b9fa-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b9fa-110">Return value</span></span>

<span data-ttu-id="1b9fa-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1b9fa-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b9fa-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b9fa-112">Remarks</span></span>

<span data-ttu-id="1b9fa-113">Il PIN deve chiamare questo metodo dall'interno dei metodi [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="1b9fa-113">The pin must call this method from within its [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span> <span data-ttu-id="1b9fa-114">Specificare **true** in **BeginFlush** e **false** in **EndFlush**.</span><span class="sxs-lookup"><span data-stu-id="1b9fa-114">Specify **TRUE** in **BeginFlush** and **FALSE** in **EndFlush**.</span></span>

<span data-ttu-id="1b9fa-115">Questo metodo fa in modo che il metodo [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) interrompa l'attesa.</span><span class="sxs-lookup"><span data-stu-id="1b9fa-115">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="1b9fa-116">Durante lo scaricamento del PIN, **CheckStreamState** restituisce sempre lo \_ scarto del flusso.</span><span class="sxs-lookup"><span data-stu-id="1b9fa-116">While the pin is flushing, **CheckStreamState** always returns STREAM\_DISCARDING.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b9fa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b9fa-117">Requirements</span></span>



| <span data-ttu-id="1b9fa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b9fa-118">Requirement</span></span> | <span data-ttu-id="1b9fa-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9fa-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9fa-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b9fa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1b9fa-121"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b9fa-121"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1b9fa-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="1b9fa-122">Library</span></span><br/> | <dl> <span data-ttu-id="1b9fa-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1b9fa-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b9fa-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b9fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b9fa-125">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="1b9fa-125">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




