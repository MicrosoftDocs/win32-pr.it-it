---
description: 'Il metodo Skip ignora un numero specificato di pin nella sequenza di enumerazione. Questo metodo implementa il metodo IEnumPins:: Skip.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Metodo CEnumPins. Skip (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329833"
---
# <a name="cenumpinsskip-method"></a><span data-ttu-id="916a6-104">Metodo CEnumPins. Skip</span><span class="sxs-lookup"><span data-stu-id="916a6-104">CEnumPins.Skip method</span></span>

<span data-ttu-id="916a6-105">Il `Skip` metodo ignora un numero specificato di pin nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="916a6-105">The `Skip` method skips over a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="916a6-106">Questo metodo implementa il metodo [**IEnumPins:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .</span><span class="sxs-lookup"><span data-stu-id="916a6-106">This method implements the [**IEnumPins::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="916a6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="916a6-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a><span data-ttu-id="916a6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="916a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="916a6-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="916a6-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="916a6-110">Numero di pin da ignorare.</span><span class="sxs-lookup"><span data-stu-id="916a6-110">Number of pins to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="916a6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="916a6-111">Return value</span></span>

<span data-ttu-id="916a6-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="916a6-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="916a6-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="916a6-113">Return code</span></span>                                                                                                | <span data-ttu-id="916a6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="916a6-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="916a6-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="916a6-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="916a6-116">Ignorato oltre la fine della sequenza.</span><span class="sxs-lookup"><span data-stu-id="916a6-116">Skipped past the end of the sequence.</span></span><br/>                                       |
| <dl> <span data-ttu-id="916a6-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="916a6-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="916a6-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="916a6-118">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="916a6-119"><dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt></span><span class="sxs-lookup"><span data-stu-id="916a6-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="916a6-120">Lo stato del filtro è stato modificato ed è ora incoerente con l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="916a6-120">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="916a6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="916a6-121">Requirements</span></span>



| <span data-ttu-id="916a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="916a6-122">Requirement</span></span> | <span data-ttu-id="916a6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="916a6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="916a6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="916a6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="916a6-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="916a6-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="916a6-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="916a6-126">Library</span></span><br/> | <dl> <span data-ttu-id="916a6-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="916a6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="916a6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="916a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="916a6-129">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="916a6-129">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




