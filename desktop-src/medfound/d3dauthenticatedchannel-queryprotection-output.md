---
description: Contiene la risposta a una \_ query di protezione D3DAUTHENTICATEDQUERY.
ms.assetid: eb99089a-5e8e-4970-9c40-7f6a9662b5ec
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: d68cafdf545d93a290e90c54be134977e51de4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524602"
---
# <a name="d3dauthenticatedchannel_queryprotection_output-structure"></a><span data-ttu-id="0ce4f-103">\_Struttura di output QUERYPROTECTION di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="0ce4f-103">D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT structure</span></span>

<span data-ttu-id="0ce4f-104">Contiene la risposta a una query di [**\_ protezione D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="0ce4f-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_PROTECTION**](d3dauthenticatedquery-protection.md) query.</span></span>

<span data-ttu-id="0ce4f-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="0ce4f-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce4f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ce4f-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT     Output;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS ProtectionFlags;
} D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="0ce4f-107">Members</span><span class="sxs-lookup"><span data-stu-id="0ce4f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ce4f-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="0ce4f-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="0ce4f-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="0ce4f-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="0ce4f-110">**ProtectionFlags**</span><span class="sxs-lookup"><span data-stu-id="0ce4f-110">**ProtectionFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0ce4f-111">Struttura [**di \_ \_ flag di protezione D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) che specifica il livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="0ce4f-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ce4f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ce4f-112">Requirements</span></span>



| <span data-ttu-id="0ce4f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ce4f-113">Requirement</span></span> | <span data-ttu-id="0ce4f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0ce4f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce4f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ce4f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0ce4f-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0ce4f-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0ce4f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ce4f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0ce4f-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ce4f-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0ce4f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ce4f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ce4f-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ce4f-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ce4f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ce4f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce4f-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="0ce4f-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="0ce4f-123">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="0ce4f-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




