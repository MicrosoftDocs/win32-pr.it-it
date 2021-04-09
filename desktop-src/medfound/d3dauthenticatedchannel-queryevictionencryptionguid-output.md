---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8fa46095c5075b0a36ed691978b73de1e7b8cade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878449"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a><span data-ttu-id="229b6-103">\_Struttura di output QUERYEVICTIONENCRYPTIONGUID di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="229b6-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT structure</span></span>

<span data-ttu-id="229b6-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="229b6-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="229b6-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="229b6-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="229b6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="229b6-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="229b6-107">Members</span><span class="sxs-lookup"><span data-stu-id="229b6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="229b6-108">**\_Output della query D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="229b6-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="229b6-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="229b6-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="229b6-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="229b6-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="229b6-111">Indice del GUID di crittografia.</span><span class="sxs-lookup"><span data-stu-id="229b6-111">The index of the encryption GUID.</span></span>

</dd> <dt>

<span data-ttu-id="229b6-112">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="229b6-112">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="229b6-113">GUID che specifica un tipo di crittografia supportato.</span><span class="sxs-lookup"><span data-stu-id="229b6-113">A GUID that specifies a supported encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="229b6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="229b6-114">Requirements</span></span>



| <span data-ttu-id="229b6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="229b6-115">Requirement</span></span> | <span data-ttu-id="229b6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="229b6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="229b6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="229b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="229b6-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="229b6-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="229b6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="229b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="229b6-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="229b6-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="229b6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="229b6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="229b6-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="229b6-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229b6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="229b6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229b6-124">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="229b6-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="229b6-125">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="229b6-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




