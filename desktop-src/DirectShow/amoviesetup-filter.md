---
description: La \_ struttura del filtro AMOVIESETUP contiene informazioni per la registrazione di un filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Struttura AMOVIESETUP_FILTER (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331709"
---
# <a name="amoviesetup_filter-structure"></a><span data-ttu-id="ed514-103">\_Struttura del filtro AMOVIESETUP</span><span class="sxs-lookup"><span data-stu-id="ed514-103">AMOVIESETUP\_FILTER structure</span></span>

<span data-ttu-id="ed514-104">La struttura del **\_ filtro AMOVIESETUP** contiene informazioni per la registrazione di un filtro.</span><span class="sxs-lookup"><span data-stu-id="ed514-104">The **AMOVIESETUP\_FILTER** structure contains information for registering a filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed514-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed514-105">Syntax</span></span>


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a><span data-ttu-id="ed514-106">Members</span><span class="sxs-lookup"><span data-stu-id="ed514-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed514-107">**clsID**</span><span class="sxs-lookup"><span data-stu-id="ed514-107">**clsID**</span></span>
</dt> <dd>

<span data-ttu-id="ed514-108">Identificatore di classe del filtro.</span><span class="sxs-lookup"><span data-stu-id="ed514-108">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="ed514-109">**strName**</span><span class="sxs-lookup"><span data-stu-id="ed514-109">**strName**</span></span>
</dt> <dd>

<span data-ttu-id="ed514-110">Nome del filtro.</span><span class="sxs-lookup"><span data-stu-id="ed514-110">Name of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="ed514-111">**dwMerit**</span><span class="sxs-lookup"><span data-stu-id="ed514-111">**dwMerit**</span></span>
</dt> <dd>

<span data-ttu-id="ed514-112">Valore del filtro.</span><span class="sxs-lookup"><span data-stu-id="ed514-112">Filter merit.</span></span> <span data-ttu-id="ed514-113">Utilizzato dall'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) quando si crea un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="ed514-113">Used by the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface when constructing a filter graph.</span></span> <span data-ttu-id="ed514-114">Per un elenco di valori di Merit, vedere [Merit](merit.md).</span><span class="sxs-lookup"><span data-stu-id="ed514-114">For a list of merit values, see [Merit](merit.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed514-115">**nPins**</span><span class="sxs-lookup"><span data-stu-id="ed514-115">**nPins**</span></span>
</dt> <dd>

<span data-ttu-id="ed514-116">Numero di elementi nella matrice *lpPin* .</span><span class="sxs-lookup"><span data-stu-id="ed514-116">Number of elements in the *lpPin* array.</span></span> <span data-ttu-id="ed514-117">Se *lpPin* è **null**, impostare questo membro su zero.</span><span class="sxs-lookup"><span data-stu-id="ed514-117">If *lpPin* is **NULL**, set this member to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ed514-118">**lpPin**</span><span class="sxs-lookup"><span data-stu-id="ed514-118">**lpPin**</span></span>
</dt> <dd>

<span data-ttu-id="ed514-119">Puntatore a una matrice di strutture [**AMOVIESETUP \_ pin**](amoviesetup-pin.md) di dimensioni *nPins*.</span><span class="sxs-lookup"><span data-stu-id="ed514-119">Pointer to an array of [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structures, of size *nPins*.</span></span> <span data-ttu-id="ed514-120">Ogni membro di questa matrice descrive un pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="ed514-120">Each member of this array describes a pin on the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed514-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed514-121">Remarks</span></span>

<span data-ttu-id="ed514-122">Per informazioni sull'uso di questa struttura, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ed514-122">For information about using this structure, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="ed514-123">Utilizzare questa struttura solo per i filtri registrati nella categoria di filtro predefinita (CLSID \_ LegacyAmFilterCategory).</span><span class="sxs-lookup"><span data-stu-id="ed514-123">Use this structure only for filters that are registered in the default filter category (CLSID\_LegacyAmFilterCategory).</span></span> <span data-ttu-id="ed514-124">Per registrare un filtro in una categoria diversa, usare il metodo [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , come descritto in [implementazione di DllRegisterServer](implementing-dllregisterserver.md).</span><span class="sxs-lookup"><span data-stu-id="ed514-124">To register a filter in a different category, use the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method, as described in [Implementing DllRegisterServer](implementing-dllregisterserver.md).</span></span>

> [!Note]  
> <span data-ttu-id="ed514-125">Il file di intestazione ComBase. h viene fornito con le [classi base di DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ed514-125">The header file combase.h is provided with the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ed514-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed514-126">Requirements</span></span>



| <span data-ttu-id="ed514-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed514-127">Requirement</span></span> | <span data-ttu-id="ed514-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ed514-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed514-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed514-129">Header</span></span><br/> | <dl> <span data-ttu-id="ed514-130"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed514-130"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed514-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed514-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed514-132">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="ed514-132">DirectShow Structures</span></span>](directshow-structures.md)
</dt> </dl>

 

 




