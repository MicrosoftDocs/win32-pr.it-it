---
description: Crea una superficie compressa per la decodifica DXVA (DirectX Video Acceleration).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'Metodo IDirect3DVideoDevice9:: CreateSurface (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131327"
---
# <a name="idirect3dvideodevice9createsurface-method"></a><span data-ttu-id="4d6be-103">Metodo IDirect3DVideoDevice9:: CreateSurface</span><span class="sxs-lookup"><span data-stu-id="4d6be-103">IDirect3DVideoDevice9::CreateSurface method</span></span>

<span data-ttu-id="4d6be-104">Crea una superficie compressa per la decodifica DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="4d6be-104">Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.</span></span>

<span data-ttu-id="4d6be-105">Per ottenere i requisiti di superficie, chiamare [**IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) ed esaminare le strutture [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) restituite.</span><span class="sxs-lookup"><span data-stu-id="4d6be-105">To get the surface requirements, call [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) and examine the returned [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d6be-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d6be-106">Syntax</span></span>


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a><span data-ttu-id="4d6be-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d6be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d6be-108">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="4d6be-108">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6be-109">Larghezza, in pixel, della superficie.</span><span class="sxs-lookup"><span data-stu-id="4d6be-109">The width of the surface, in pixels.</span></span> <span data-ttu-id="4d6be-110">Impostare questo parametro su **DXVACompBufferInfo. WidthToCreate**.</span><span class="sxs-lookup"><span data-stu-id="4d6be-110">Set this parameter equal to **DXVACompBufferInfo.WidthToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="4d6be-111">*Altezza*</span><span class="sxs-lookup"><span data-stu-id="4d6be-111">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6be-112">Altezza, in pixel, della superficie.</span><span class="sxs-lookup"><span data-stu-id="4d6be-112">The height of the surface, in pixels.</span></span> <span data-ttu-id="4d6be-113">Impostare questo parametro su **DXVACompBufferInfo. HeightToCreate**.</span><span class="sxs-lookup"><span data-stu-id="4d6be-113">Set this parameter equal to **DXVACompBufferInfo.HeightToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="4d6be-114">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="4d6be-114">*BackBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6be-115">Numero di buffer back.</span><span class="sxs-lookup"><span data-stu-id="4d6be-115">The number of back buffers.</span></span> <span data-ttu-id="4d6be-116">Questo parametro può essere zero.</span><span class="sxs-lookup"><span data-stu-id="4d6be-116">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4d6be-117">*Formato*</span><span class="sxs-lookup"><span data-stu-id="4d6be-117">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6be-118">Formato pixel, specificato come valore **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="4d6be-118">The pixel format, specified as a **D3DFORMAT** value.</span></span> <span data-ttu-id="4d6be-119">Impostare questo parametro su **DXVACompBufferInfo. Format**.</span><span class="sxs-lookup"><span data-stu-id="4d6be-119">Set this parameter equal to **DXVACompBufferInfo.Format**.</span></span>

</dd> <dt>

<span data-ttu-id="4d6be-120">*Pool*</span><span class="sxs-lookup"><span data-stu-id="4d6be-120">*Pool*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6be-121">Pool di memoria in cui creare la superficie, specificata come valore **D3DPOOL** .</span><span class="sxs-lookup"><span data-stu-id="4d6be-121">The memory pool in which to create the surface, specified as a **D3DPOOL** value.</span></span> <span data-ttu-id="4d6be-122">Impostare questo parametro su **DXVACompBufferInfo. pool**.</span><span class="sxs-lookup"><span data-stu-id="4d6be-122">Set this parameter equal to **DXVACompBufferInfo.Pool**.</span></span>

</dd> <dt>

<span data-ttu-id="4d6be-123">*Utilizzo*</span><span class="sxs-lookup"><span data-stu-id="4d6be-123">*Usage*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6be-124">**Or** bit per bit di una o più costanti **D3DUSAGE** .</span><span class="sxs-lookup"><span data-stu-id="4d6be-124">A bitwise **OR** of one or more **D3DUSAGE** constants.</span></span> <span data-ttu-id="4d6be-125">Impostare questo parametro su **DXVACompBufferInfo. Usage**.</span><span class="sxs-lookup"><span data-stu-id="4d6be-125">Set this parameter equal to **DXVACompBufferInfo.Usage**.</span></span>

</dd> <dt>

<span data-ttu-id="4d6be-126">*ppSurface*</span><span class="sxs-lookup"><span data-stu-id="4d6be-126">*ppSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6be-127">Riceve un puntatore all'interfaccia **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="4d6be-127">Receives a pointer to the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="4d6be-128">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4d6be-128">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="4d6be-129">*pSharedHandle*</span><span class="sxs-lookup"><span data-stu-id="4d6be-129">*pSharedHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6be-130">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4d6be-130">Reserved.</span></span> <span data-ttu-id="4d6be-131">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="4d6be-131">Set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d6be-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d6be-132">Return value</span></span>

<span data-ttu-id="4d6be-133">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4d6be-133">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d6be-134">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d6be-134">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d6be-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d6be-135">Requirements</span></span>



| <span data-ttu-id="4d6be-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d6be-136">Requirement</span></span> | <span data-ttu-id="4d6be-137">Valore</span><span class="sxs-lookup"><span data-stu-id="4d6be-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4d6be-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d6be-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4d6be-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d6be-139">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d6be-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d6be-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4d6be-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d6be-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4d6be-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d6be-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d6be-143"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d6be-143"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d6be-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d6be-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d6be-145">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="4d6be-145">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




