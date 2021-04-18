---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY CRYPTOSESSION.
ms.assetid: df9d9b41-8188-4597-9e83-d14065eb7fc7
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fb4e6ccad999f183e71f0f57d64544a70cef5534
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305444"
---
# <a name="d3dauthenticatedchannel_querycryptosession_output-structure"></a><span data-ttu-id="230de-103">\_Struttura di output QUERYCRYPTOSESSION di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="230de-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT structure</span></span>

<span data-ttu-id="230de-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="230de-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="230de-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="230de-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="230de-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="230de-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DXVA2DecodeHandle;
  HANDLE                               CryptoSessionHandle;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="230de-107">Members</span><span class="sxs-lookup"><span data-stu-id="230de-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="230de-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="230de-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="230de-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="230de-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="230de-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="230de-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="230de-111">Handle per un dispositivo di decodificatore DirectX Video Acceleration 2 (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="230de-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="230de-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="230de-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="230de-113">Handle per la sessione di crittografia associata al dispositivo di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="230de-113">A handle to the cryptographic session that is associated with the decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="230de-114">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="230de-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="230de-115">Handle per il dispositivo Direct3D associato al dispositivo di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="230de-115">A handle to the Direct3D device that is associated with the decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="230de-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="230de-116">Requirements</span></span>



| <span data-ttu-id="230de-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="230de-117">Requirement</span></span> | <span data-ttu-id="230de-118">Valore</span><span class="sxs-lookup"><span data-stu-id="230de-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="230de-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="230de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="230de-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="230de-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="230de-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="230de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="230de-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="230de-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="230de-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="230de-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="230de-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="230de-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="230de-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="230de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230de-126">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="230de-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="230de-127">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="230de-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




