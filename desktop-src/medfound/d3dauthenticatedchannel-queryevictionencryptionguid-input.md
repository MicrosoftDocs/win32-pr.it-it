---
description: Contiene i dati di input per una \_ query ENCRYPTIONWHENACCESSIBLEGUID D3DAUTHENTICATEDQUERY.
ms.assetid: 0e24e393-3f63-4c6f-aca1-f73ced3490ba
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1c4500d27577883f46d00580dcc7e306b4008cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401542"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_input-structure"></a><span data-ttu-id="2c032-103">\_Struttura di input QUERYEVICTIONENCRYPTIONGUID di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="2c032-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT structure</span></span>

<span data-ttu-id="2c032-104">Contiene i dati di input per una query [**\_ ENCRYPTIONWHENACCESSIBLEGUID D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="2c032-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="2c032-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="2c032-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c032-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c032-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                EncryptionGuidIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT;
```



## <a name="members"></a><span data-ttu-id="2c032-107">Members</span><span class="sxs-lookup"><span data-stu-id="2c032-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c032-108">**Input**</span><span class="sxs-lookup"><span data-stu-id="2c032-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="2c032-109">Struttura [**di \_ \_ input della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) che contiene il GUID per la query e altri dati.</span><span class="sxs-lookup"><span data-stu-id="2c032-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="2c032-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="2c032-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2c032-111">Indice del GUID di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2c032-111">The index of the encryption GUID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c032-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c032-112">Requirements</span></span>



| <span data-ttu-id="2c032-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c032-113">Requirement</span></span> | <span data-ttu-id="2c032-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2c032-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c032-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c032-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2c032-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2c032-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c032-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c032-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2c032-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c032-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2c032-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c032-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c032-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c032-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c032-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c032-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c032-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="2c032-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2c032-123">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="2c032-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




