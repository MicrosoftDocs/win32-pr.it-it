---
description: Informazioni sull'interfaccia IAMFilterData, che converte le informazioni di filtro in dati binari imballati. Questa interfaccia è stata deprecata.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interfaccia IAMFilterData (Fil \_ data.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1e43e0f16ddfdee596f0dc6bd736ed86fc6fa37d
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989436"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="d5230-104">Interfaccia IAMFilterData</span><span class="sxs-lookup"><span data-stu-id="d5230-104">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="d5230-105">Questa interfaccia è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="d5230-105">This interface has been deprecated.</span></span> <span data-ttu-id="d5230-106">Le nuove applicazioni devono usare invece [**l'interfaccia IFilterMapper2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)</span><span class="sxs-lookup"><span data-stu-id="d5230-106">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="d5230-107">`IAMFilterData`L'interfaccia converte le informazioni di filtro in dati binari imballati, che possono essere archiviati nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d5230-107">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="d5230-108">L'oggetto Filter Mapper espone questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d5230-108">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="d5230-109">Membri</span><span class="sxs-lookup"><span data-stu-id="d5230-109">Members</span></span>

<span data-ttu-id="d5230-110">**L'interfaccia IAMFilterData** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="d5230-110">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5230-111">**IAMFilterData** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d5230-111">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="d5230-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="d5230-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5230-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="d5230-113">Methods</span></span>

<span data-ttu-id="d5230-114">**L'interfaccia IAMFilterData** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d5230-114">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="d5230-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="d5230-115">Method</span></span>                                                     | <span data-ttu-id="d5230-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5230-116">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="d5230-117">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="d5230-117">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="d5230-118">Crea dati binari del Registro di sistema per un filtro.</span><span class="sxs-lookup"><span data-stu-id="d5230-118">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="d5230-119">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="d5230-119">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="d5230-120">Decomprime i dati binari del Registro di sistema per un filtro.</span><span class="sxs-lookup"><span data-stu-id="d5230-120">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5230-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5230-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5230-122">L'intestazione Fil \_ data.h si trova nella directory [Mapper Sample](mapper-sample.md) nella Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d5230-122">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d5230-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5230-123">Requirements</span></span>



| <span data-ttu-id="d5230-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5230-124">Requirement</span></span> | <span data-ttu-id="d5230-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d5230-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5230-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5230-126">Header</span></span><br/> | <dl> <span data-ttu-id="d5230-127"><dt>Fil \_ data.h</dt></span><span class="sxs-lookup"><span data-stu-id="d5230-127"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5230-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5230-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5230-129">Interfacce deprecate</span><span class="sxs-lookup"><span data-stu-id="d5230-129">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
