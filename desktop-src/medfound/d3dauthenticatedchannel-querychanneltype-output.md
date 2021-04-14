---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY CHANNELTYPE.
ms.assetid: 547f7f26-2b9d-48b1-97cc-84a2202c3900
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3120669da69f13359f49d8b8c38ed7d3e211a8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401544"
---
# <a name="d3dauthenticatedchannel_querychanneltype_output-structure"></a><span data-ttu-id="aaad1-103">\_Struttura di output QUERYCHANNELTYPE di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="aaad1-103">D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="aaad1-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) .</span><span class="sxs-lookup"><span data-stu-id="aaad1-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) query.</span></span>

<span data-ttu-id="aaad1-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="aaad1-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="aaad1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aaad1-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DAUTHENTICATEDCHANNELTYPE          ChannelType;
} D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="aaad1-107">Members</span><span class="sxs-lookup"><span data-stu-id="aaad1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aaad1-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="aaad1-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="aaad1-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="aaad1-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="aaad1-110">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="aaad1-110">**ChannelType**</span></span>
</dt> <dd>

<span data-ttu-id="aaad1-111">Valore [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) che specifica il tipo di canale.</span><span class="sxs-lookup"><span data-stu-id="aaad1-111">A [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) value that specifies the channel type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aaad1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaad1-112">Requirements</span></span>



| <span data-ttu-id="aaad1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaad1-113">Requirement</span></span> | <span data-ttu-id="aaad1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="aaad1-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaad1-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaad1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aaad1-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="aaad1-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aaad1-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaad1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aaad1-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="aaad1-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aaad1-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aaad1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaad1-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaad1-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaad1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aaad1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaad1-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="aaad1-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="aaad1-123">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="aaad1-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




