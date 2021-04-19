---
description: Il Metodo GetFlags recupera i flag di contesto associati al comando posticipato.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Metodo CDeferredCommand. GetFlags (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333477"
---
# <a name="cdeferredcommandgetflags-method"></a><span data-ttu-id="5effe-103">Metodo CDeferredCommand. GetFlags</span><span class="sxs-lookup"><span data-stu-id="5effe-103">CDeferredCommand.GetFlags method</span></span>

<span data-ttu-id="5effe-104">Il `GetFlags` metodo recupera i flag di contesto associati al comando posticipato.</span><span class="sxs-lookup"><span data-stu-id="5effe-104">The `GetFlags` method retrieves the context flags associated with the deferred command.</span></span>

## <a name="syntax"></a><span data-ttu-id="5effe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5effe-105">Syntax</span></span>


```C++
short GetFlags();
```



## <a name="parameters"></a><span data-ttu-id="5effe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5effe-106">Parameters</span></span>

<span data-ttu-id="5effe-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5effe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5effe-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5effe-108">Return value</span></span>

<span data-ttu-id="5effe-109">Restituisce una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5effe-109">Returns one of the following:</span></span>



| <span data-ttu-id="5effe-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5effe-110">Return code</span></span>                                                                                             | <span data-ttu-id="5effe-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5effe-111">Description</span></span>                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5effe-112"><dt>**\_metodo Dispatch**</dt></span><span class="sxs-lookup"><span data-stu-id="5effe-112"><dt>**DISPATCH\_METHOD**</dt></span></span> </dl>         | <span data-ttu-id="5effe-113">Eseguire il membro come metodo.</span><span class="sxs-lookup"><span data-stu-id="5effe-113">Run the member as a method.</span></span> <span data-ttu-id="5effe-114">Se una proprietà ha lo stesso nome, è possibile impostare sia questo che il \_ flag PropertyGet (di invio.</span><span class="sxs-lookup"><span data-stu-id="5effe-114">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span><br/>                                               |
| <dl> <span data-ttu-id="5effe-115"><dt>**\_PROPERTYGET (dispatch**</dt></span><span class="sxs-lookup"><span data-stu-id="5effe-115"><dt>**DISPATCH\_PROPERTYGET**</dt></span></span> </dl>    | <span data-ttu-id="5effe-116">Il membro viene recuperato come una proprietà o un membro dati.</span><span class="sxs-lookup"><span data-stu-id="5effe-116">The member is being retrieved as a property or data member.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="5effe-117"><dt>**\_PROPERTYPUT dispatch**</dt></span><span class="sxs-lookup"><span data-stu-id="5effe-117"><dt>**DISPATCH\_PROPERTYPUT**</dt></span></span> </dl>    | <span data-ttu-id="5effe-118">Il membro viene modificato come una proprietà o un membro dati.</span><span class="sxs-lookup"><span data-stu-id="5effe-118">The member is being changed as a property or data member.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="5effe-119"><dt>**\_PROPERTYPUTREF dispatch**</dt></span><span class="sxs-lookup"><span data-stu-id="5effe-119"><dt>**DISPATCH\_PROPERTYPUTREF**</dt></span></span> </dl> | <span data-ttu-id="5effe-120">Il membro viene modificato tramite un'assegnazione di riferimento, anziché un'assegnazione di valore.</span><span class="sxs-lookup"><span data-stu-id="5effe-120">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="5effe-121">Questo flag è valido solo quando la proprietà accetta un riferimento a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="5effe-121">This flag is valid only when the property accepts a reference to an object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5effe-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5effe-122">Requirements</span></span>



| <span data-ttu-id="5effe-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5effe-123">Requirement</span></span> | <span data-ttu-id="5effe-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5effe-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5effe-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5effe-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5effe-126"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5effe-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5effe-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="5effe-127">Library</span></span><br/> | <dl> <span data-ttu-id="5effe-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5effe-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5effe-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5effe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5effe-130">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="5effe-130">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




