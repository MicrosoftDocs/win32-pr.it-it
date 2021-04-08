---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESSCOUNT.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749314"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a><span data-ttu-id="36300-103">\_Struttura di output QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="36300-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="36300-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .</span><span class="sxs-lookup"><span data-stu-id="36300-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) query.</span></span>

<span data-ttu-id="36300-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="36300-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="36300-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36300-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="36300-107">Members</span><span class="sxs-lookup"><span data-stu-id="36300-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="36300-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="36300-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="36300-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="36300-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="36300-110">**NumRestrictedSharedResourceProcesses**</span><span class="sxs-lookup"><span data-stu-id="36300-110">**NumRestrictedSharedResourceProcesses**</span></span>
</dt> <dd>

<span data-ttu-id="36300-111">Numero di processi a cui è consentito aprire risorse condivise con accesso limitato.</span><span class="sxs-lookup"><span data-stu-id="36300-111">The number of processes allowed to open shared resources that have restricted access.</span></span> <span data-ttu-id="36300-112">Un processo non può aprire una risorsa di questo tipo, a meno che al processo non sia stato concesso l'accesso.</span><span class="sxs-lookup"><span data-stu-id="36300-112">A process cannot open such a resource unless the process has been granted access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36300-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36300-113">Requirements</span></span>



| <span data-ttu-id="36300-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="36300-114">Requirement</span></span> | <span data-ttu-id="36300-115">Valore</span><span class="sxs-lookup"><span data-stu-id="36300-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36300-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36300-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36300-117">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36300-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="36300-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36300-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36300-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="36300-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36300-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36300-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="36300-121"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="36300-121"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36300-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36300-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36300-123">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="36300-123">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="36300-124">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="36300-124">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




