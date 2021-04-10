---
description: Contiene i dati di input per una \_ query OUTPUTIDCOUNT D3DAUTHENTICATEDQUERY.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 93f58bcd05efb8c173986186d631c713195d8363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127931"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a><span data-ttu-id="07472-103">\_Struttura di input QUERYOUTPUTIDCOUNT di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="07472-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT structure</span></span>

<span data-ttu-id="07472-104">Contiene i dati di input per una query [**\_ OUTPUTIDCOUNT D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="07472-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="07472-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="07472-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="07472-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07472-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a><span data-ttu-id="07472-107">Members</span><span class="sxs-lookup"><span data-stu-id="07472-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="07472-108">**Input**</span><span class="sxs-lookup"><span data-stu-id="07472-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="07472-109">Struttura [**di \_ \_ input della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) che contiene il GUID per la query e altri dati.</span><span class="sxs-lookup"><span data-stu-id="07472-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="07472-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="07472-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="07472-111">Handle per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07472-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="07472-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="07472-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="07472-113">Handle per la sessione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="07472-113">A handle to the cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07472-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07472-114">Requirements</span></span>



| <span data-ttu-id="07472-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="07472-115">Requirement</span></span> | <span data-ttu-id="07472-116">Valore</span><span class="sxs-lookup"><span data-stu-id="07472-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07472-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07472-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07472-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="07472-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="07472-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07472-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07472-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="07472-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="07472-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07472-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="07472-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="07472-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07472-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07472-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07472-124">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="07472-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="07472-125">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="07472-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




