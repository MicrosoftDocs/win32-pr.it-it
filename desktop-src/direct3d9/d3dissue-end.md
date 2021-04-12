---
description: Questa macro crea un valore utilizzato da Issue per emettere una query end.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355084"
---
# <a name="d3dissue_end"></a><span data-ttu-id="2babc-103">\_Fine D3DISSUE</span><span class="sxs-lookup"><span data-stu-id="2babc-103">D3DISSUE\_END</span></span>

<span data-ttu-id="2babc-104">Questa macro crea un valore utilizzato da [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) per emettere una query end.</span><span class="sxs-lookup"><span data-stu-id="2babc-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query end.</span></span>

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a><span data-ttu-id="2babc-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2babc-105">Parameters</span></span>





 

## <a name="remarks"></a><span data-ttu-id="2babc-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="2babc-106">Remarks</span></span>

<span data-ttu-id="2babc-107">Questa macro imposta lo stato della query su non segnalato.</span><span class="sxs-lookup"><span data-stu-id="2babc-107">This macro changes the query state to nonsignaled.</span></span>

<span data-ttu-id="2babc-108">D3DISSUE \_ end è valido per i tipi di query seguenti.</span><span class="sxs-lookup"><span data-stu-id="2babc-108">D3DISSUE\_END is valid for the following query types.</span></span>

-   <span data-ttu-id="2babc-109">\_VCACHE D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="2babc-109">D3DQUERYTYPE\_VCACHE</span></span>
-   <span data-ttu-id="2babc-110">\_RESOURCEMANAGER D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="2babc-110">D3DQUERYTYPE\_ResourceManager</span></span>
-   <span data-ttu-id="2babc-111">\_VERTEXSTATS D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="2babc-111">D3DQUERYTYPE\_VERTEXSTATS</span></span>
-   <span data-ttu-id="2babc-112">\_Evento D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="2babc-112">D3DQUERYTYPE\_EVENT</span></span>
-   <span data-ttu-id="2babc-113">\_Occlusione D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="2babc-113">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="2babc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2babc-114">Requirements</span></span>



| <span data-ttu-id="2babc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2babc-115">Requirement</span></span> | <span data-ttu-id="2babc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2babc-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2babc-117">Header</span></span><br/> | <dl> <span data-ttu-id="2babc-118"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2babc-118"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2babc-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2babc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2babc-120">Macro</span><span class="sxs-lookup"><span data-stu-id="2babc-120">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="2babc-121">**\_Inizio D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="2babc-121">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md)
</dt> <dt>

[<span data-ttu-id="2babc-122">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="2babc-122">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 
