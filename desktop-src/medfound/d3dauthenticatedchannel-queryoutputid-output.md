---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY OUTPUTID.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049313"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a><span data-ttu-id="e94da-103">\_Struttura di output QUERYROUTPUTID di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="e94da-103">D3DAUTHENTICATEDCHANNEL\_QUERYROUTPUTID\_OUTPUT structure</span></span>

<span data-ttu-id="e94da-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="e94da-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="e94da-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="e94da-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="e94da-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e94da-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="e94da-107">Members</span><span class="sxs-lookup"><span data-stu-id="e94da-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e94da-108">**\_Output della query D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="e94da-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="e94da-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="e94da-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="e94da-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="e94da-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="e94da-111">Handle per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e94da-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="e94da-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="e94da-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="e94da-113">Handle per la sessione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e94da-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="e94da-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="e94da-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e94da-115">Indice dell'ID di output specificato nel membro **outputID** .</span><span class="sxs-lookup"><span data-stu-id="e94da-115">The index of the output ID given in the **OutputID** member.</span></span>

</dd> <dt>

<span data-ttu-id="e94da-116">**OutputID**</span><span class="sxs-lookup"><span data-stu-id="e94da-116">**OutputID**</span></span>
</dt> <dd>

<span data-ttu-id="e94da-117">ID di output associato al dispositivo e alla sessione di crittografia specificati.</span><span class="sxs-lookup"><span data-stu-id="e94da-117">An output ID that is associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e94da-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e94da-118">Requirements</span></span>



| <span data-ttu-id="e94da-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e94da-119">Requirement</span></span> | <span data-ttu-id="e94da-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e94da-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e94da-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e94da-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e94da-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e94da-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e94da-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e94da-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e94da-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e94da-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e94da-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e94da-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e94da-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e94da-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e94da-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e94da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e94da-128">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="e94da-128">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="e94da-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="e94da-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




