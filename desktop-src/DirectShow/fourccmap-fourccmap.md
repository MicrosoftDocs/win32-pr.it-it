---
description: Metodo del costruttore che fornisce il mapping tra i tipi DWORD di formato multimediale obsoleti e i sottotipi GUID. Questo metodo non usa parametri.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Costruttore FOURCCMap:: FOURCCMap (fourcc. h)-nessun parametro'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323829"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a><span data-ttu-id="74402-104">Costruttore FOURCCMap:: FOURCCMap (fourcc. h)-nessun parametro</span><span class="sxs-lookup"><span data-stu-id="74402-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - No parameters</span></span>

<span data-ttu-id="74402-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="74402-105">Constructor method.</span></span> <span data-ttu-id="74402-106">Costruttore fornisce il mapping tra i tipi **DWORD** di formato multimediale obsoleti e i sottotipi **GUID** .</span><span class="sxs-lookup"><span data-stu-id="74402-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="74402-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74402-107">Syntax</span></span>


```C++
FOURCCMap();
```



## <a name="parameters"></a><span data-ttu-id="74402-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="74402-108">Parameters</span></span>

<span data-ttu-id="74402-109">Questo costruttore non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="74402-109">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="74402-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="74402-110">Remarks</span></span>

<span data-ttu-id="74402-111">Se questo oggetto viene costruito con il codice **fourcc** , viene creato un **GUID** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="74402-111">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="74402-112">Se questo oggetto viene creato con un **GUID** esistente, il valore **fourcc** dell'oggetto viene impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="74402-112">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="74402-113">Successivamente, è possibile impostare o recuperare il valore **fourcc** usando rispettivamente le funzioni membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC**](fourccmap-getfourcc.md) .</span><span class="sxs-lookup"><span data-stu-id="74402-113">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="74402-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74402-114">Requirements</span></span>


| <span data-ttu-id="74402-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="74402-115">Requirement</span></span> | <span data-ttu-id="74402-116">Valore</span><span class="sxs-lookup"><span data-stu-id="74402-116">Value</span></span> |
|-|-|
| <span data-ttu-id="74402-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74402-117">Header</span></span>  | <span data-ttu-id="74402-118">FourCC. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="74402-118">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="74402-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="74402-119">Library</span></span> | <span data-ttu-id="74402-120">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="74402-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



## <a name="see-also"></a><span data-ttu-id="74402-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74402-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74402-122">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="74402-122">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




