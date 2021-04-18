---
description: Specifica il tipo di canale autenticato Direct3D.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: Enumerazione D3DAUTHENTICATEDCHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305433"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a><span data-ttu-id="a0037-103">Enumerazione D3DAUTHENTICATEDCHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="a0037-103">D3DAUTHENTICATEDCHANNELTYPE enumeration</span></span>

<span data-ttu-id="a0037-104">Specifica il tipo di canale autenticato Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a0037-104">Specifies the type of Direct3D authenticated channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0037-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0037-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a><span data-ttu-id="a0037-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="a0037-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a0037-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**\_D3d9 D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="a0037-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
</dt> <dd>

<span data-ttu-id="a0037-108">Canale Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a0037-108">Direct3D 9 channel.</span></span> <span data-ttu-id="a0037-109">Questo canale fornisce la comunicazione con il runtime di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a0037-109">This channel provides communication with the Direct3D runtime.</span></span>

</dd> <dt>

<span data-ttu-id="a0037-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="a0037-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>
</dt> <dd>

<span data-ttu-id="a0037-111">Canale driver software.</span><span class="sxs-lookup"><span data-stu-id="a0037-111">Software driver channel.</span></span> <span data-ttu-id="a0037-112">Questo canale fornisce la comunicazione con un driver che implementa i meccanismi di protezione del contenuto nel software.</span><span class="sxs-lookup"><span data-stu-id="a0037-112">This channel provides communication with a driver that implements content protection mechanisms in software.</span></span>

</dd> <dt>

<span data-ttu-id="a0037-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="a0037-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
</dt> <dd>

<span data-ttu-id="a0037-114">Canale driver hardware.</span><span class="sxs-lookup"><span data-stu-id="a0037-114">Hardware driver channel.</span></span> <span data-ttu-id="a0037-115">Questo canale fornisce la comunicazione con un driver che implementa i meccanismi di protezione del contenuto nell'hardware della GPU.</span><span class="sxs-lookup"><span data-stu-id="a0037-115">This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0037-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0037-116">Requirements</span></span>



| <span data-ttu-id="a0037-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0037-117">Requirement</span></span> | <span data-ttu-id="a0037-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a0037-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0037-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0037-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0037-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a0037-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a0037-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0037-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0037-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0037-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a0037-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0037-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0037-124"><dt>D3d9types. h (include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0037-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0037-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0037-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0037-126">Enumerazioni video Direct3D</span><span class="sxs-lookup"><span data-stu-id="a0037-126">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> <dt>

[<span data-ttu-id="a0037-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span><span class="sxs-lookup"><span data-stu-id="a0037-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




