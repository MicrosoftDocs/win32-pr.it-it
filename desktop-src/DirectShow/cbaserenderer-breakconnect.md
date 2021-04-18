---
description: Il metodo BreakConnect rilascia il pin di input da una connessione.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Metodo CBaseRenderer. BreakConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329404"
---
# <a name="cbaserendererbreakconnect-method"></a><span data-ttu-id="84a9f-103">CBaseRenderer. BreakConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="84a9f-103">CBaseRenderer.BreakConnect method</span></span>

<span data-ttu-id="84a9f-104">Il `BreakConnect` metodo rilascia il pin di input da una connessione.</span><span class="sxs-lookup"><span data-stu-id="84a9f-104">The `BreakConnect` method releases the input pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a9f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84a9f-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="84a9f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84a9f-106">Parameters</span></span>

<span data-ttu-id="84a9f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="84a9f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84a9f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84a9f-108">Return value</span></span>

<span data-ttu-id="84a9f-109">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="84a9f-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="84a9f-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="84a9f-110">Return code</span></span>                                                                                         | <span data-ttu-id="84a9f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84a9f-111">Description</span></span>                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="84a9f-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="84a9f-112"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="84a9f-113">Il PIN non era connesso.</span><span class="sxs-lookup"><span data-stu-id="84a9f-113">The pin was not connected.</span></span><br/>  |
| <dl> <span data-ttu-id="84a9f-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="84a9f-114"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="84a9f-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="84a9f-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="84a9f-116"><dt>**VFW \_ E \_ non \_ arrestato**</dt></span><span class="sxs-lookup"><span data-stu-id="84a9f-116"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="84a9f-117">Il filtro è ancora attivo.</span><span class="sxs-lookup"><span data-stu-id="84a9f-117">The filter is still active.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84a9f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="84a9f-118">Remarks</span></span>

<span data-ttu-id="84a9f-119">Il pin di input del filtro chiama questo metodo dall'interno del proprio `BreakConnect` metodo.</span><span class="sxs-lookup"><span data-stu-id="84a9f-119">The filter's input pin calls this method from inside its own `BreakConnect` method.</span></span> <span data-ttu-id="84a9f-120">Per ulteriori informazioni, vedere [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md). Il filtro esegue una contabilità interna, ad esempio la reimpostazione del flag di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="84a9f-120">(For more information, see [**CBasePin::BreakConnect**](cbasepin-breakconnect.md).) The filter performs some internal bookkeeping, such as resetting the end-of-stream flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="84a9f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84a9f-121">Requirements</span></span>



| <span data-ttu-id="84a9f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a9f-122">Requirement</span></span> | <span data-ttu-id="84a9f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="84a9f-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a9f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84a9f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="84a9f-125"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84a9f-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="84a9f-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="84a9f-126">Library</span></span><br/> | <dl> <span data-ttu-id="84a9f-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="84a9f-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a9f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84a9f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a9f-129">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="84a9f-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




