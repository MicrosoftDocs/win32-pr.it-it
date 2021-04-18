---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY ACCESSIBILITYATTRIBUTES.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305440"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a><span data-ttu-id="c0665-103">\_Struttura di output QUERYINFOBUSTYPE di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="c0665-103">D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="c0665-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="c0665-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) query.</span></span>

<span data-ttu-id="c0665-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="c0665-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0665-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0665-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="c0665-107">Members</span><span class="sxs-lookup"><span data-stu-id="c0665-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0665-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="c0665-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="c0665-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="c0665-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="c0665-110">**BusType**</span><span class="sxs-lookup"><span data-stu-id="c0665-110">**BusType**</span></span>
</dt> <dd>

<span data-ttu-id="c0665-111">**Operatore OR** bit per bit dei flag dell'enumerazione [**D3DBUSTYPE**](d3dbustype.md) .</span><span class="sxs-lookup"><span data-stu-id="c0665-111">A bitwise **OR** of flags from the [**D3DBUSTYPE**](d3dbustype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="c0665-112">**bAccessibleInContiguousBlocks**</span><span class="sxs-lookup"><span data-stu-id="c0665-112">**bAccessibleInContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="c0665-113">Se **true**, i blocchi di memoria video contigui possono essere accessibili alla CPU o al bus.</span><span class="sxs-lookup"><span data-stu-id="c0665-113">If **TRUE**, contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> <dt>

<span data-ttu-id="c0665-114">**bAccessibleInNonContiguousBlocks**</span><span class="sxs-lookup"><span data-stu-id="c0665-114">**bAccessibleInNonContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="c0665-115">Se **true**, i blocchi di memoria video non contigui possono essere accessibili alla CPU o al bus.</span><span class="sxs-lookup"><span data-stu-id="c0665-115">If **TRUE**, non-contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0665-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0665-116">Requirements</span></span>



| <span data-ttu-id="c0665-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0665-117">Requirement</span></span> | <span data-ttu-id="c0665-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c0665-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0665-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0665-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0665-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c0665-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c0665-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0665-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0665-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0665-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c0665-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0665-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0665-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0665-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0665-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0665-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0665-126">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="c0665-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="c0665-127">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="c0665-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




