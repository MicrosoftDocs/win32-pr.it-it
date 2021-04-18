---
description: Contiene i dati di input per un \_ comando D3DAUTHENTICATEDCONFIGURE CRYPTOSESSION.
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2b1cca13bcd37e488cd0ed455098afa62492579f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305455"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a><span data-ttu-id="e077e-103">\_Struttura D3DAUTHENTICATEDCHANNEL CONFIGURECRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="e077e-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION structure</span></span>

<span data-ttu-id="e077e-104">Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="e077e-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) command.</span></span>

<span data-ttu-id="e077e-105">Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="e077e-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="e077e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e077e-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a><span data-ttu-id="e077e-107">Members</span><span class="sxs-lookup"><span data-stu-id="e077e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e077e-108">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="e077e-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="e077e-109">D3DAUTHENTICATEDCHANNEL configura la struttura di [**\_ \_ input**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.</span><span class="sxs-lookup"><span data-stu-id="e077e-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="e077e-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="e077e-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="e077e-111">Handle per il dispositivo di decodificatore DirectX Video Acceleration 2 (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="e077e-111">A handle to the DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="e077e-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="e077e-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="e077e-113">Handle per la sessione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e077e-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="e077e-114">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="e077e-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="e077e-115">Handle per il dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e077e-115">A handle to the Direct3D device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e077e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e077e-116">Requirements</span></span>



| <span data-ttu-id="e077e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e077e-117">Requirement</span></span> | <span data-ttu-id="e077e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e077e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e077e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e077e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e077e-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e077e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e077e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e077e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e077e-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e077e-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e077e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e077e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e077e-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e077e-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e077e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e077e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e077e-126">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="e077e-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="e077e-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="e077e-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




