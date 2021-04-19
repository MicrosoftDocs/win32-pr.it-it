---
description: Questo operatore assegna una nuova ora di riferimento.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: Metodo COARefTime. Operator = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330237"
---
# <a name="coareftimeoperator-method-ctlutilh"></a><span data-ttu-id="0ba6e-103">Metodo COARefTime. Operator = (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="0ba6e-103">COARefTime.operator= method (Ctlutil.h)</span></span>

<span data-ttu-id="0ba6e-104">Questo operatore assegna una nuova ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ba6e-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a><span data-ttu-id="0ba6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ba6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba6e-107">*Desktop remoto* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="0ba6e-107">*rd* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0ba6e-108">Riferimento a un valore **Double** che specifica il nuovo tempo di riferimento in secondi.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-108">Reference to a **double** value that specifies the new reference time in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba6e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ba6e-109">Return value</span></span>

<span data-ttu-id="0ba6e-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba6e-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ba6e-111">Requirements</span></span>



| <span data-ttu-id="0ba6e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba6e-112">Requirement</span></span> | <span data-ttu-id="0ba6e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0ba6e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba6e-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ba6e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0ba6e-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba6e-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ba6e-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ba6e-116">Library</span></span><br/> | <dl> <span data-ttu-id="0ba6e-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba6e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba6e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ba6e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba6e-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="0ba6e-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




