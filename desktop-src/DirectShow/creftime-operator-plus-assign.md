---
description: L'operatore + = aggiunge due tempi di riferimento.
ms.assetid: 016d3dac-4d7c-490a-83aa-1d88a2080748
title: Metodo CRefTime. Operator + = (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5e0d9a5a16a963b67643823e5e3b547a1076fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329047"
---
# <a name="creftimeoperator-method"></a><span data-ttu-id="57e04-103">CRefTime. Operator + = (metodo)</span><span class="sxs-lookup"><span data-stu-id="57e04-103">CRefTime.operator+= method</span></span>

<span data-ttu-id="57e04-104">L'operatore + = aggiunge due tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="57e04-104">The += operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="57e04-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57e04-105">Syntax</span></span>


```C++
CRefTime& operator+=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="57e04-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="57e04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57e04-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="57e04-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="57e04-108">Riferimento a un oggetto **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="57e04-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57e04-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57e04-109">Return value</span></span>

<span data-ttu-id="57e04-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57e04-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="57e04-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57e04-111">Requirements</span></span>



| <span data-ttu-id="57e04-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="57e04-112">Requirement</span></span> | <span data-ttu-id="57e04-113">Valore</span><span class="sxs-lookup"><span data-stu-id="57e04-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e04-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57e04-114">Header</span></span><br/>  | <dl> <span data-ttu-id="57e04-115"><dt>Reftime. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57e04-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57e04-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="57e04-116">Library</span></span><br/> | <dl> <span data-ttu-id="57e04-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="57e04-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




