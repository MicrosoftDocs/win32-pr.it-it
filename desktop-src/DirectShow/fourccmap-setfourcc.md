---
description: Imposta la parte FOURCC dell'oggetto FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'Metodo FOURCCMap:: SetFOURCC (fourcc. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329956"
---
# <a name="fourccmapsetfourcc-method"></a><span data-ttu-id="14c14-103">Metodo FOURCCMap:: SetFOURCC</span><span class="sxs-lookup"><span data-stu-id="14c14-103">FOURCCMap::SetFOURCC method</span></span>

<span data-ttu-id="14c14-104">Imposta la parte **fourcc** dell'oggetto [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="14c14-104">Sets the **FOURCC** portion of the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c14-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14c14-105">Syntax</span></span>


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="14c14-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14c14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c14-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="14c14-107">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="14c14-108">Puntatore alla parte dell'identificatore univoco globale (**GUID**) restituita dell'oggetto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="14c14-108">Pointer to the returned globally unique identifier (**GUID**) part of the **FOURCCMap** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c14-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14c14-109">Return value</span></span>

<span data-ttu-id="14c14-110">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="14c14-110">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c14-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14c14-111">Requirements</span></span>



| <span data-ttu-id="14c14-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c14-112">Requirement</span></span> | <span data-ttu-id="14c14-113">Valore</span><span class="sxs-lookup"><span data-stu-id="14c14-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c14-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14c14-114">Header</span></span><br/>  | <dl> <span data-ttu-id="14c14-115"><dt>FourCC. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14c14-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="14c14-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="14c14-116">Library</span></span><br/> | <dl> <span data-ttu-id="14c14-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="14c14-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c14-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14c14-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c14-119">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="14c14-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




