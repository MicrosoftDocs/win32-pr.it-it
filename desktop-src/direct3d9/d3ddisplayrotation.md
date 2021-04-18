---
description: Specifica il modo in cui viene ruotato il monitoraggio usato per visualizzare un'applicazione a schermo intero.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: Enumerazione D3DDISPLAYROTATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 28f4d38dca78f0f34daf931a6bf651b40c1b0a78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322393"
---
# <a name="d3ddisplayrotation-enumeration"></a><span data-ttu-id="7a3eb-103">Enumerazione D3DDISPLAYROTATION</span><span class="sxs-lookup"><span data-stu-id="7a3eb-103">D3DDISPLAYROTATION enumeration</span></span>

<span data-ttu-id="7a3eb-104">Specifica il modo in cui viene ruotato il monitoraggio usato per visualizzare un'applicazione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="7a3eb-104">Specifies how the monitor being used to display a full-screen application is rotated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a3eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a3eb-105">Syntax</span></span>


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a><span data-ttu-id="7a3eb-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="7a3eb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7a3eb-107"><span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**Identità di D3DDISPLAYROTATION \_**</span><span class="sxs-lookup"><span data-stu-id="7a3eb-107"><span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION\_IDENTITY**</span></span>
</dt> <dd>

<span data-ttu-id="7a3eb-108">La visualizzazione non viene ruotata.</span><span class="sxs-lookup"><span data-stu-id="7a3eb-108">Display is not rotated.</span></span>

</dd> <dt>

<span data-ttu-id="7a3eb-109"><span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**</span><span class="sxs-lookup"><span data-stu-id="7a3eb-109"><span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION\_90**</span></span>
</dt> <dd>

<span data-ttu-id="7a3eb-110">La visualizzazione è ruotata di 90 gradi.</span><span class="sxs-lookup"><span data-stu-id="7a3eb-110">Display is rotated 90 degrees.</span></span>

</dd> <dt>

<span data-ttu-id="7a3eb-111"><span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**</span><span class="sxs-lookup"><span data-stu-id="7a3eb-111"><span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION\_180**</span></span>
</dt> <dd>

<span data-ttu-id="7a3eb-112">La visualizzazione è ruotata di 180 gradi.</span><span class="sxs-lookup"><span data-stu-id="7a3eb-112">Display is rotated 180 degrees.</span></span>

</dd> <dt>

<span data-ttu-id="7a3eb-113"><span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**</span><span class="sxs-lookup"><span data-stu-id="7a3eb-113"><span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION\_270**</span></span>
</dt> <dd>

<span data-ttu-id="7a3eb-114">La visualizzazione è ruotata di 270 gradi.</span><span class="sxs-lookup"><span data-stu-id="7a3eb-114">Display is rotated 270 degrees.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a3eb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a3eb-115">Remarks</span></span>

<span data-ttu-id="7a3eb-116">Questa enumerazione viene utilizzata in [**IDirect3D9Ex:: GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex:: GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)e [**IDirect3DSwapChain9Ex:: GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).</span><span class="sxs-lookup"><span data-stu-id="7a3eb-116">This enumeration is used in [**IDirect3D9Ex::GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex::GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex), and [**IDirect3DSwapChain9Ex::GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).</span></span>

<span data-ttu-id="7a3eb-117">Le applicazioni possono scegliere di gestire autonomamente la rotazione del monitoraggio usando il [ \_ NOAUTOROTATE D3DPRESENTFLAG](d3dpresentflag.md), nel qual caso l'applicazione deve essere in grado di individuare il modo in cui viene ruotato il monitoraggio in modo che possa modificare di conseguenza il rendering.</span><span class="sxs-lookup"><span data-stu-id="7a3eb-117">Applications may choose to handle monitor rotation themselves by using the [D3DPRESENTFLAG\_NOAUTOROTATE](d3dpresentflag.md), in which case, the application will need to know how the monitor is rotated so that it may adjust its rendering accordingly.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a3eb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a3eb-118">Requirements</span></span>



| <span data-ttu-id="7a3eb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a3eb-119">Requirement</span></span> | <span data-ttu-id="7a3eb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7a3eb-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3eb-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a3eb-121">Header</span></span><br/> | <dl> <span data-ttu-id="7a3eb-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a3eb-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a3eb-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a3eb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a3eb-124">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="7a3eb-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




