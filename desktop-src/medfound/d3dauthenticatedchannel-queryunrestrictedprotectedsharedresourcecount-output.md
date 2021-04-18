---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT.
ms.assetid: c283833d-e98c-4f01-b623-21027a6b90e8
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fd30cff59d35f845903e7f4fdb08cdff61df3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305434"
---
# <a name="d3dauthenticatedchannel_queryunrestrictedprotectedsharedresourcecount_output-structure"></a><span data-ttu-id="63b81-103">\_Struttura di output QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="63b81-103">D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="63b81-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) .</span><span class="sxs-lookup"><span data-stu-id="63b81-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) query.</span></span>

<span data-ttu-id="63b81-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="63b81-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="63b81-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63b81-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumUnrestrictedProtectedSharedResources;
} D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="63b81-107">Members</span><span class="sxs-lookup"><span data-stu-id="63b81-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="63b81-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="63b81-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="63b81-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="63b81-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="63b81-110">**NumUnrestrictedProtectedSharedResources**</span><span class="sxs-lookup"><span data-stu-id="63b81-110">**NumUnrestrictedProtectedSharedResources**</span></span>
</dt> <dd>

<span data-ttu-id="63b81-111">Il numero di risorse condivise protette che possono essere aperte da qualsiasi processo senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="63b81-111">The number of protected, shared resources that can be opened by any process without restrictions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63b81-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63b81-112">Requirements</span></span>



| <span data-ttu-id="63b81-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="63b81-113">Requirement</span></span> | <span data-ttu-id="63b81-114">Valore</span><span class="sxs-lookup"><span data-stu-id="63b81-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63b81-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63b81-115">Minimum supported client</span></span><br/> | <span data-ttu-id="63b81-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63b81-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="63b81-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63b81-117">Minimum supported server</span></span><br/> | <span data-ttu-id="63b81-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="63b81-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="63b81-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63b81-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b81-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b81-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63b81-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63b81-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b81-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="63b81-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="63b81-123">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="63b81-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




