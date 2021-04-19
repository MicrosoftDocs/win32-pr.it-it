---
description: Nota Questa interfaccia è stata deprecata.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interfaccia IAMFilterData (Fil \_ Data. h)
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
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326816"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="fe890-103">Interfaccia IAMFilterData</span><span class="sxs-lookup"><span data-stu-id="fe890-103">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="fe890-104">Questa interfaccia è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="fe890-104">This interface has been deprecated.</span></span> <span data-ttu-id="fe890-105">Le nuove applicazioni devono invece usare l'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="fe890-105">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="fe890-106">L' `IAMFilterData` interfaccia converte le informazioni di filtro in dati binari compressi, che possono essere archiviati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fe890-106">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="fe890-107">L'oggetto filtro Mapper espone questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fe890-107">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="fe890-108">Membri</span><span class="sxs-lookup"><span data-stu-id="fe890-108">Members</span></span>

<span data-ttu-id="fe890-109">L'interfaccia **IAMFilterData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fe890-109">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fe890-110">**IAMFilterData** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fe890-110">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="fe890-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe890-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe890-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe890-112">Methods</span></span>

<span data-ttu-id="fe890-113">L'interfaccia **IAMFilterData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fe890-113">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="fe890-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="fe890-114">Method</span></span>                                                     | <span data-ttu-id="fe890-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe890-115">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="fe890-116">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="fe890-116">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="fe890-117">Crea dati di registro binari per un filtro.</span><span class="sxs-lookup"><span data-stu-id="fe890-117">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="fe890-118">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="fe890-118">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="fe890-119">Decomprime i dati del registro di sistema binario per un filtro.</span><span class="sxs-lookup"><span data-stu-id="fe890-119">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe890-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe890-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe890-121">L'intestazione fil \_ Data. h si trova nella directory degli [esempi del Mapper](mapper-sample.md) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fe890-121">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe890-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe890-122">Requirements</span></span>



| <span data-ttu-id="fe890-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe890-123">Requirement</span></span> | <span data-ttu-id="fe890-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fe890-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe890-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe890-125">Header</span></span><br/> | <dl> <span data-ttu-id="fe890-126"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe890-126"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe890-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe890-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe890-128">Interfacce deprecate</span><span class="sxs-lookup"><span data-stu-id="fe890-128">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
