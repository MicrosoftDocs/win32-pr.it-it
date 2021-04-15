---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY OUTPUTIDCOUNT.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 86a840de2b36b7089b31d15e8375c17a0610b77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484092"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a><span data-ttu-id="6f327-103">\_Struttura di output QUERYOUTPUTIDCOUNT di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="6f327-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="6f327-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="6f327-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="6f327-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="6f327-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f327-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f327-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="6f327-107">Members</span><span class="sxs-lookup"><span data-stu-id="6f327-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f327-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="6f327-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="6f327-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="6f327-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="6f327-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="6f327-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="6f327-111">Handle per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f327-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="6f327-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="6f327-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="6f327-113">Handle per la sessione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="6f327-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="6f327-114">**NumOutputIDs**</span><span class="sxs-lookup"><span data-stu-id="6f327-114">**NumOutputIDs**</span></span>
</dt> <dd>

<span data-ttu-id="6f327-115">Numero di ID di output associati al dispositivo e alla sessione di crittografia specificati.</span><span class="sxs-lookup"><span data-stu-id="6f327-115">The number of output IDs associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f327-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f327-116">Requirements</span></span>



| <span data-ttu-id="6f327-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f327-117">Requirement</span></span> | <span data-ttu-id="6f327-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6f327-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f327-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f327-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f327-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6f327-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6f327-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f327-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f327-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f327-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6f327-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f327-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f327-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f327-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f327-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f327-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f327-126">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="6f327-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="6f327-127">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="6f327-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




