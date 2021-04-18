---
description: L'operatore = assegna una nuova ora di riferimento.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: Metodo CRefTime. Operator = (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331458"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="450e5-103">Metodo CRefTime. Operator = (Reftime. h)</span><span class="sxs-lookup"><span data-stu-id="450e5-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="450e5-104">L'operatore = assegna una nuova ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="450e5-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="450e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="450e5-105">Syntax</span></span>


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="450e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="450e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="450e5-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="450e5-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="450e5-108">Riferimento a un oggetto **CRefTime** che specifica la nuova ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="450e5-108">Reference to a **CRefTime** object that specifies the new reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="450e5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="450e5-109">Return value</span></span>

<span data-ttu-id="450e5-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="450e5-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="450e5-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="450e5-111">Requirements</span></span>



| <span data-ttu-id="450e5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="450e5-112">Requirement</span></span> | <span data-ttu-id="450e5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="450e5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="450e5-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="450e5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="450e5-115"><dt>Reftime. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="450e5-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="450e5-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="450e5-116">Library</span></span><br/> | <dl> <span data-ttu-id="450e5-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="450e5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




