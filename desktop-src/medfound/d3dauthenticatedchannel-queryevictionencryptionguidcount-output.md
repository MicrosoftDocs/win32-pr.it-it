---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUIDCOUNT.
ms.assetid: 168f9455-8dc6-473a-ad2c-e51996b63650
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 51668dccdfa15649ec2a062a1231eb0b16e68ff8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305442"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguidcount_output-structure"></a><span data-ttu-id="476ac-103">\_Struttura di output QUERYEVICTIONENCRYPTIONGUIDCOUNT di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="476ac-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="476ac-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="476ac-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) query.</span></span>

<span data-ttu-id="476ac-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="476ac-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="476ac-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="476ac-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  NumEncryptionGuids                   UINT;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="476ac-107">Members</span><span class="sxs-lookup"><span data-stu-id="476ac-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="476ac-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="476ac-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="476ac-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="476ac-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="476ac-110">**UINT**</span><span class="sxs-lookup"><span data-stu-id="476ac-110">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="476ac-111">Numero di GUID di crittografia.</span><span class="sxs-lookup"><span data-stu-id="476ac-111">The number of encryption GUIDs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="476ac-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="476ac-112">Requirements</span></span>



| <span data-ttu-id="476ac-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="476ac-113">Requirement</span></span> | <span data-ttu-id="476ac-114">Valore</span><span class="sxs-lookup"><span data-stu-id="476ac-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="476ac-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="476ac-115">Minimum supported client</span></span><br/> | <span data-ttu-id="476ac-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="476ac-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="476ac-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="476ac-117">Minimum supported server</span></span><br/> | <span data-ttu-id="476ac-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="476ac-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="476ac-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="476ac-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="476ac-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="476ac-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="476ac-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="476ac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="476ac-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="476ac-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="476ac-123">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="476ac-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




