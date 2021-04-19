---
description: Metodo del costruttore che fornisce il mapping tra i tipi DWORD di formato multimediale obsoleti e i sottotipi GUID. Questo metodo usa il parametro ' FourCC '.
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Costruttore FOURCCMap:: FOURCCMap (fourcc. h)-parametro FourCC'
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
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323861"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a><span data-ttu-id="5114c-104">Costruttore FOURCCMap:: FOURCCMap (fourcc. h)-parametro FourCC</span><span class="sxs-lookup"><span data-stu-id="5114c-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - Fourcc parameter</span></span>

<span data-ttu-id="5114c-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="5114c-105">Constructor method.</span></span> <span data-ttu-id="5114c-106">Costruttore fornisce il mapping tra i tipi **DWORD** di formato multimediale obsoleti e i sottotipi **GUID** .</span><span class="sxs-lookup"><span data-stu-id="5114c-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5114c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5114c-107">Syntax</span></span>


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a><span data-ttu-id="5114c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5114c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5114c-109">*FourCC*</span><span class="sxs-lookup"><span data-stu-id="5114c-109">*Fourcc*</span></span> 
</dt> <dd>

<span data-ttu-id="5114c-110">**DWORD** che specifica il FourCC.</span><span class="sxs-lookup"><span data-stu-id="5114c-110">**DWORD** that specifies the FOURCC.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5114c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5114c-111">Remarks</span></span>

<span data-ttu-id="5114c-112">Se questo oggetto viene costruito con il codice **fourcc** , viene creato un **GUID** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5114c-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="5114c-113">Se questo oggetto viene creato con un **GUID** esistente, il valore **fourcc** dell'oggetto viene impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="5114c-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="5114c-114">Successivamente, è possibile impostare o recuperare il valore **fourcc** usando rispettivamente le funzioni membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC**](fourccmap-getfourcc.md) .</span><span class="sxs-lookup"><span data-stu-id="5114c-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="5114c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5114c-115">Requirements</span></span>

| <span data-ttu-id="5114c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5114c-116">Requirement</span></span> | <span data-ttu-id="5114c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5114c-117">Value</span></span> |
|-|-|
| <span data-ttu-id="5114c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5114c-118">Header</span></span>  | <span data-ttu-id="5114c-119">FourCC. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="5114c-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="5114c-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="5114c-120">Library</span></span> | <span data-ttu-id="5114c-121">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="5114c-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5114c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5114c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5114c-123">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="5114c-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




