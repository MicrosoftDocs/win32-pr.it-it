---
description: Rappresenta un acceleratore hardware per DirectX Video Acceleration (DXVA) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interfaccia IDirect3DDXVADevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310836"
---
# <a name="idirect3ddxvadevice9-interface"></a><span data-ttu-id="775ba-103">Interfaccia IDirect3DDXVADevice9</span><span class="sxs-lookup"><span data-stu-id="775ba-103">IDirect3DDXVADevice9 interface</span></span>

<span data-ttu-id="775ba-104">Rappresenta un acceleratore hardware per DirectX Video Acceleration (DXVA) 1,0.</span><span class="sxs-lookup"><span data-stu-id="775ba-104">Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.</span></span>

## <a name="members"></a><span data-ttu-id="775ba-105">Membri</span><span class="sxs-lookup"><span data-stu-id="775ba-105">Members</span></span>

<span data-ttu-id="775ba-106">L'interfaccia **IDirect3DDXVADevice9** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="775ba-106">The **IDirect3DDXVADevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="775ba-107">**IDirect3DDXVADevice9** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="775ba-107">**IDirect3DDXVADevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="775ba-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="775ba-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="775ba-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="775ba-109">Methods</span></span>

<span data-ttu-id="775ba-110">L'interfaccia **IDirect3DDXVADevice9** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="775ba-110">The **IDirect3DDXVADevice9** interface has these methods.</span></span>



| <span data-ttu-id="775ba-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="775ba-111">Method</span></span>                                                  | <span data-ttu-id="775ba-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="775ba-112">Description</span></span>                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="775ba-113">**BeginFrame**</span><span class="sxs-lookup"><span data-stu-id="775ba-113">**BeginFrame**</span></span>](idirect3ddxvadevice9-beginframe.md)   | <span data-ttu-id="775ba-114">Inizia l'elaborazione per creare un'immagine decodificata.</span><span class="sxs-lookup"><span data-stu-id="775ba-114">Begins the processing to create a decoded picture.</span></span><br/>         |
| [<span data-ttu-id="775ba-115">**EndFrame**</span><span class="sxs-lookup"><span data-stu-id="775ba-115">**EndFrame**</span></span>](idirect3ddxvadevice9-endframe.md)       | <span data-ttu-id="775ba-116">Termina l'elaborazione per creare un'immagine decodificata.</span><span class="sxs-lookup"><span data-stu-id="775ba-116">Ends the processing to create a decoded picture.</span></span><br/>           |
| [<span data-ttu-id="775ba-117">**Execute**</span><span class="sxs-lookup"><span data-stu-id="775ba-117">**Execute**</span></span>](idirect3ddxvadevice9-execute.md)         | <span data-ttu-id="775ba-118">Esegue un'operazione di decodifica DXVA.</span><span class="sxs-lookup"><span data-stu-id="775ba-118">Performs a DXVA decoding operation.</span></span> <br/>                       |
| [<span data-ttu-id="775ba-119">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="775ba-119">**QueryStatus**</span></span>](idirect3ddxvadevice9-querystatus.md) | <span data-ttu-id="775ba-120">Esegue una query sullo stato di lettura/scrittura di una superficie di decodifica DXVA.</span><span class="sxs-lookup"><span data-stu-id="775ba-120">Queries the read/write status of a DXVA decoding surface.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="775ba-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="775ba-121">Remarks</span></span>

<span data-ttu-id="775ba-122">Per ottenere un puntatore a questa interfaccia, chiamare [**IDirect3DVideoDevice9:: CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span><span class="sxs-lookup"><span data-stu-id="775ba-122">To get a pointer to this interface, call [**IDirect3DVideoDevice9::CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="775ba-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="775ba-123">Requirements</span></span>



| <span data-ttu-id="775ba-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="775ba-124">Requirement</span></span> | <span data-ttu-id="775ba-125">Valore</span><span class="sxs-lookup"><span data-stu-id="775ba-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="775ba-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="775ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="775ba-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="775ba-127">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="775ba-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="775ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="775ba-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="775ba-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="775ba-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="775ba-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="775ba-131"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="775ba-131"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="775ba-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="775ba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="775ba-133">Interfacce video Direct3D</span><span class="sxs-lookup"><span data-stu-id="775ba-133">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> </dl>

 

 
