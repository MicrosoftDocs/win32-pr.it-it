---
description: Contiene i dati di input per una \_ query OUTPUTID D3DAUTHENTICATEDQUERY.
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7c64d43261ccc849772372110ad73169c698cd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305441"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a><span data-ttu-id="16b7c-103">\_Struttura di input QUERYOUTPUTID di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="16b7c-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT structure</span></span>

<span data-ttu-id="16b7c-104">Contiene i dati di input per una query [**\_ OUTPUTID D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="16b7c-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="16b7c-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="16b7c-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="16b7c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16b7c-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a><span data-ttu-id="16b7c-107">Members</span><span class="sxs-lookup"><span data-stu-id="16b7c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="16b7c-108">**Input**</span><span class="sxs-lookup"><span data-stu-id="16b7c-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="16b7c-109">Struttura [**di \_ \_ input della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) che contiene il GUID per la query e altri dati.</span><span class="sxs-lookup"><span data-stu-id="16b7c-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="16b7c-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="16b7c-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="16b7c-111">Handle per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16b7c-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="16b7c-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="16b7c-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="16b7c-113">Handle per la sessione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="16b7c-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="16b7c-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="16b7c-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="16b7c-115">Indice dell'ID di output.</span><span class="sxs-lookup"><span data-stu-id="16b7c-115">The index of the output ID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16b7c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16b7c-116">Requirements</span></span>



| <span data-ttu-id="16b7c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b7c-117">Requirement</span></span> | <span data-ttu-id="16b7c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="16b7c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16b7c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16b7c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16b7c-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="16b7c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="16b7c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16b7c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16b7c-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="16b7c-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="16b7c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16b7c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="16b7c-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b7c-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16b7c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16b7c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b7c-126">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="16b7c-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="16b7c-127">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="16b7c-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




