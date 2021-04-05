---
title: CENUMOBJ. CPP
description: Nel componente provider di esempio, l'enumerazione di un oggetto contenitore usa le routine, da cenumobj. cpp, elencate nella tabella seguente.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730194"
---
# <a name="cenumobjcpp"></a><span data-ttu-id="7cc5f-103">CENUMOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="7cc5f-103">CENUMOBJ.CPP</span></span>

<span data-ttu-id="7cc5f-104">Nel componente provider di esempio, l'enumerazione di un oggetto contenitore usa le routine, da cenumobj. cpp, elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-104">In the example provider component, the enumeration of a container object uses the routines, from cenumobj.cpp, listed in the following table.</span></span>



| <span data-ttu-id="7cc5f-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="7cc5f-105">Method</span></span>                                                 | <span data-ttu-id="7cc5f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cc5f-106">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc5f-107">**CSampleDSGenObjectEnum:: create**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-107">**CSampleDSGenObjectEnum::Create**</span></span>                     | <span data-ttu-id="7cc5f-108">Creare un oggetto per abilitare l'enumerazione degli oggetti Active Directory generici.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-108">Create an object to enable enumeration of generic Active Directory objects.</span></span>                                                                                           |
| <span data-ttu-id="7cc5f-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span></span>     | <span data-ttu-id="7cc5f-110">Inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-110">Initialization.</span></span>                                                                                                                                                       |
| <span data-ttu-id="7cc5f-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="7cc5f-112">Gestire il recupero di oggetti.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-112">Manage retrieval of objects.</span></span>                                                                                                                                          |
| <span data-ttu-id="7cc5f-113">**CSampleDSGenObjectEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-113">**CSampleDSGenObjectEnum::FetchObjects**</span></span>               | <span data-ttu-id="7cc5f-114">Recuperare il set di puntatori [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che corrispondono al filtro.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-114">Retrieve the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers that match the filter.</span></span>                                                             |
| <span data-ttu-id="7cc5f-115">**CSampleDSGenObjectEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-115">**CSampleDSGenObjectEnum::FetchNextObject**</span></span>            | <span data-ttu-id="7cc5f-116">Recuperare un oggetto e confrontarlo con il filtro.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-116">Retrieve an object and match against the filter.</span></span> <span data-ttu-id="7cc5f-117">Se corrisponde a, eseguire il wrapping in un oggetto generico e restituire un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7cc5f-117">If it matches, wrap it in generic object and return a [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |
| <span data-ttu-id="7cc5f-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="7cc5f-119">Gestire il recupero degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-119">Manage retrieving the objects.</span></span>                                                                                                                                        |
| <span data-ttu-id="7cc5f-120">**CSampleDSGenObjectEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-120">**CSampleDSGenObjectEnum::Next**</span></span>                       | <span data-ttu-id="7cc5f-121">Recupera il numero specificato di elementi dall'oggetto di enumerazione indicato.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-121">Retrieve the specified number of elements from the enumeration object indicated.</span></span>                                                                                      |
| <span data-ttu-id="7cc5f-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span></span>            | <span data-ttu-id="7cc5f-123">Verificare che la classe di oggetti corrisponda a una nell'elenco di filtri.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-123">Verify that object class matches one in the filter list.</span></span>                                                                                                              |
| <span data-ttu-id="7cc5f-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span></span>         | <span data-ttu-id="7cc5f-125">Gestire la matrice di filtri.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-125">Manage the filter array.</span></span>                                                                                                                                              |
| <span data-ttu-id="7cc5f-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span></span> | <span data-ttu-id="7cc5f-127">Aggiungere una nuova classe di oggetti al filtro e impostare il filtro come contiguo.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-127">Add a new object class to the filter and set the filter as contiguous.</span></span>                                                                                                |
| <span data-ttu-id="7cc5f-128">**FreeFilterList**</span><span class="sxs-lookup"><span data-stu-id="7cc5f-128">**FreeFilterList**</span></span>                                     | <span data-ttu-id="7cc5f-129">Liberare il filtro.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-129">Free the filter.</span></span>                                                                                                                                                      |



 

 

 