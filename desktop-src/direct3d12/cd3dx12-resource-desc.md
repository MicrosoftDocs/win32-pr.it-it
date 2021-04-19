---
title: Struttura CD3DX12_RESOURCE_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di descrizione della risorsa D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Struttura CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323565"
---
# <a name="cd3dx12_resource_desc-structure"></a><span data-ttu-id="97e4f-104">\_Struttura desc della risorsa CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="97e4f-104">CD3DX12\_RESOURCE\_DESC structure</span></span>

<span data-ttu-id="97e4f-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ Descrizione della risorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="97e4f-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e4f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97e4f-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a><span data-ttu-id="97e4f-107">Members</span><span class="sxs-lookup"><span data-stu-id="97e4f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="97e4f-108">**CD3DX12 della \_ risorsa \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="97e4f-108">**CD3DX12\_RESOURCE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-109">Crea un'istanza nuova, non inizializzata, di una \_ Descrizione della risorsa CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="97e4f-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-110">**Descrizione della risorsa CD3DX12 esplicita \_ \_ (const D3D12 \_ Resource \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-110">**explicit CD3DX12\_RESOURCE\_DESC(const D3D12\_RESOURCE\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-111">Crea una nuova istanza di una \_ Descrizione della risorsa CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ Descrizione della risorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="97e4f-111">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initialized with the contents of another [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-112">**CD3DX12 \_ Resource \_ DESC (dimensione della \_ dimensione della risorsa D3D12 \_ , allineamento UInt64, lunghezza UInt64, altezza uint, UInt16 depthOrArraySize, UInt16 mipLevels, \_ formato di formato DXGI, uint sampleCount, uint SAMPLEQUALITY, \_ \_ layout layout trama D3D12, \_ flag flag di risorse D3D12 \_ )**</span><span class="sxs-lookup"><span data-stu-id="97e4f-112">**CD3DX12\_RESOURCE\_DESC(D3D12\_RESOURCE\_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI\_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12\_TEXTURE\_LAYOUT layout, D3D12\_RESOURCE\_FLAGS flags)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-113">Crea una nuova istanza di una \_ Descrizione della risorsa CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="97e4f-113">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="97e4f-114">[**D3D12 \_ Dimensione della \_ dimensione della risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="97e4f-114">[**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) dimension</span></span>

<span data-ttu-id="97e4f-115">Allineamento UINT64</span><span class="sxs-lookup"><span data-stu-id="97e4f-115">UINT64 alignment</span></span>

<span data-ttu-id="97e4f-116">Larghezza UINT64</span><span class="sxs-lookup"><span data-stu-id="97e4f-116">UINT64 width</span></span>

<span data-ttu-id="97e4f-117">Altezza UINT</span><span class="sxs-lookup"><span data-stu-id="97e4f-117">UINT height</span></span>

<span data-ttu-id="97e4f-118">UINT16 depthOrArraySize</span><span class="sxs-lookup"><span data-stu-id="97e4f-118">UINT16 depthOrArraySize</span></span>

<span data-ttu-id="97e4f-119">UINT16 mipLevels</span><span class="sxs-lookup"><span data-stu-id="97e4f-119">UINT16 mipLevels</span></span>

<span data-ttu-id="97e4f-120">[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="97e4f-120">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="97e4f-121">SampleCount UINT</span><span class="sxs-lookup"><span data-stu-id="97e4f-121">UINT sampleCount</span></span>

<span data-ttu-id="97e4f-122">SampleQuality UINT</span><span class="sxs-lookup"><span data-stu-id="97e4f-122">UINT sampleQuality</span></span>

<span data-ttu-id="97e4f-123">[**D3D12 \_ Layout \_ layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)</span><span class="sxs-lookup"><span data-stu-id="97e4f-123">[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout</span></span>

<span data-ttu-id="97e4f-124">[**D3D12 \_ Flag \_ flag di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)</span><span class="sxs-lookup"><span data-stu-id="97e4f-124">[**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-125">**Buffer inline statico (const D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 resource flags \_ \_ Flags = D3D12 \_ Resource \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-125">**static inline Buffer(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-126">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="97e4f-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="97e4f-127">[**D3D12 \_ \_ \_ Informazioni sull'allocazione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="97e4f-127">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="97e4f-128">consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="97e4f-128">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-129">**Buffer inline statico (larghezza UINT64, flag di \_ risorsa D3D12 \_ flag = \_ D3D12 \_ flag \_ di risorsa None, allineamento UInt64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-129">**static inline Buffer(UINT64 width, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-130">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="97e4f-130">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="97e4f-131">Larghezza UINT64</span><span class="sxs-lookup"><span data-stu-id="97e4f-131">UINT64 width</span></span>

<span data-ttu-id="97e4f-132">consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="97e4f-132">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="97e4f-133">consenso esplicito Allineamento UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="97e4f-133">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-134">**static inline Tex1D (formato DXGI \_ , lunghezza UInt64, UInt16 arraySize = 1, UInt16 mipLevels = 0, D3D12 \_ Flags resource flags \_ = D3D12 \_ Resource \_ flag \_ None, D3D12 texture layout layout \_ \_ = D3D12 \_ texture \_ layout \_ Unknown, UInt64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-134">**static inline Tex1D(DXGI\_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-135">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="97e4f-135">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="97e4f-136">[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="97e4f-136">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="97e4f-137">Larghezza UINT64</span><span class="sxs-lookup"><span data-stu-id="97e4f-137">UINT64 width</span></span>

<span data-ttu-id="97e4f-138">consenso esplicito UINT16 arraySize = 1</span><span class="sxs-lookup"><span data-stu-id="97e4f-138">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="97e4f-139">consenso esplicito UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="97e4f-139">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="97e4f-140">consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="97e4f-140">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="97e4f-141">consenso esplicito [**D3D12 \_ Layout \_ layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = \_ layout trama \_ D3D12 \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="97e4f-141">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="97e4f-142">consenso esplicito Allineamento UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="97e4f-142">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-143">**static inline Tex2D (formato DXGI \_ , lunghezza UInt64, altezza uint, UInt16 arraySize = 1, UInt16 mipLevels = 0, uint sampleCount = 1, uint sampleQuality = 0, D3D12 \_ flag di risorse \_ flag = D3D12 \_ Resource \_ flag \_ None, D3D12 \_ texture layout layout \_ = D3D12 \_ texture \_ layout \_ Unknown, UInt64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-143">**static inline Tex2D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-144">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="97e4f-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="97e4f-145">[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="97e4f-145">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="97e4f-146">Larghezza UINT64</span><span class="sxs-lookup"><span data-stu-id="97e4f-146">UINT64 width</span></span>

<span data-ttu-id="97e4f-147">Altezza UINT</span><span class="sxs-lookup"><span data-stu-id="97e4f-147">UINT height</span></span>

<span data-ttu-id="97e4f-148">consenso esplicito UINT16 arraySize = 1</span><span class="sxs-lookup"><span data-stu-id="97e4f-148">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="97e4f-149">consenso esplicito UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="97e4f-149">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="97e4f-150">consenso esplicito UINT sampleCount = 1</span><span class="sxs-lookup"><span data-stu-id="97e4f-150">(opt) UINT sampleCount = 1</span></span>

<span data-ttu-id="97e4f-151">consenso esplicito UINT sampleQuality = 0</span><span class="sxs-lookup"><span data-stu-id="97e4f-151">(opt) UINT sampleQuality = 0</span></span>

<span data-ttu-id="97e4f-152">consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="97e4f-152">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="97e4f-153">consenso esplicito [**D3D12 \_ Layout \_ layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = \_ layout trama \_ D3D12 \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="97e4f-153">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="97e4f-154">consenso esplicito Allineamento UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="97e4f-154">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-155">**static inline Tex3D (formato DXGI \_ , lunghezza UInt64, altezza uint, profondità UInt16, UInt16 mipLevels = 0, D3D12 \_ flag di risorsa \_ flag = D3D12 \_ Resource \_ flag \_ None, D3D12 \_ texture layout layout \_ = D3D12 \_ texture \_ layout \_ Unknown, UInt64 allineamento = 0)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-155">**static inline Tex3D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-156">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="97e4f-156">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="97e4f-157">[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="97e4f-157">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="97e4f-158">Larghezza UINT64</span><span class="sxs-lookup"><span data-stu-id="97e4f-158">UINT64 width</span></span>

<span data-ttu-id="97e4f-159">Altezza UINT</span><span class="sxs-lookup"><span data-stu-id="97e4f-159">UINT height</span></span>

<span data-ttu-id="97e4f-160">Profondità UINT16</span><span class="sxs-lookup"><span data-stu-id="97e4f-160">UINT16 depth</span></span>

<span data-ttu-id="97e4f-161">consenso esplicito UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="97e4f-161">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="97e4f-162">consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="97e4f-162">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="97e4f-163">consenso esplicito [**D3D12 \_ Layout \_ layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = \_ layout trama \_ D3D12 \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="97e4f-163">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="97e4f-164">consenso esplicito Allineamento UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="97e4f-164">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-165">**Profondità inline () const**</span><span class="sxs-lookup"><span data-stu-id="97e4f-165">**inline Depth() const**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-166">Se Dimension = = [**D3D12 \_ della \_ dimensione della risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, restituisce DepthOrArraySize.</span><span class="sxs-lookup"><span data-stu-id="97e4f-166">If Dimension == [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="97e4f-167">Se Dimension! = D3D12 \_ della \_ dimensione della risorsa \_ TEXTURE3D, restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="97e4f-167">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-168">**inline ArraySize () const**</span><span class="sxs-lookup"><span data-stu-id="97e4f-168">**inline ArraySize() const**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-169">Se Dimension! = D3D12 \_ della \_ dimensione della risorsa \_ TEXTURE3D, restituisce DepthOrArraySize.</span><span class="sxs-lookup"><span data-stu-id="97e4f-169">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="97e4f-170">Se Dimension = = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="97e4f-170">If Dimension == D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span> <span data-ttu-id="97e4f-171">Vedere [**la \_ \_ dimensione della risorsa D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.</span><span class="sxs-lookup"><span data-stu-id="97e4f-171">See [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D.</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-172">**inline PlaneCount (ID3D12Device \* PDEVICE) const**</span><span class="sxs-lookup"><span data-stu-id="97e4f-172">**inline PlaneCount(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-173">Restituisce D3D12GetFormatPlaneCount (pDevice, Format).</span><span class="sxs-lookup"><span data-stu-id="97e4f-173">Returns D3D12GetFormatPlaneCount(pDevice, Format).</span></span> <span data-ttu-id="97e4f-174">Vedere [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) e [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="97e4f-174">See [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-175">**sottorisorse inline (ID3D12Device \* PDEVICE) const**</span><span class="sxs-lookup"><span data-stu-id="97e4f-175">**inline Subresources(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-176">Restituisce il numero di sottorisorse, calcolato come MipLevels \* ArraySize () \* PlaneCount (PDEVICE).</span><span class="sxs-lookup"><span data-stu-id="97e4f-176">Returns the number of subresources, calculated as MipLevels \* ArraySize() \* PlaneCount(pDevice).</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-177">**inline CalcSubresource (UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-177">**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-178">Consente di calcolare un indice di una sottorisorsa usando [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span><span class="sxs-lookup"><span data-stu-id="97e4f-178">Calculates a subresource index, by using [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-179">**operator const D3D12 \_ Resource \_ desc& () const**</span><span class="sxs-lookup"><span data-stu-id="97e4f-179">**operator const D3D12\_RESOURCE\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-180">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="97e4f-180">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-181">**operator = = (const D3D12 \_ Resource \_ desc& l, const D3D12 \_ Resource \_ desc& r)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-181">**operator == (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-182">Restituisce true se tutti i membri di ogni struttura sono identici.</span><span class="sxs-lookup"><span data-stu-id="97e4f-182">Returns true if all members of each structure are identical.</span></span>

</dd> <dt>

<span data-ttu-id="97e4f-183">**operator! = (const D3D12 \_ Resource \_ desc& l, const D3D12 \_ Resource \_ desc& r)**</span><span class="sxs-lookup"><span data-stu-id="97e4f-183">**operator != (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="97e4f-184">Restituisce false se tutti i membri di ogni struttura sono identici.</span><span class="sxs-lookup"><span data-stu-id="97e4f-184">Returns false if all members of each structure are identical.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97e4f-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97e4f-185">Requirements</span></span>



| <span data-ttu-id="97e4f-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e4f-186">Requirement</span></span> | <span data-ttu-id="97e4f-187">Valore</span><span class="sxs-lookup"><span data-stu-id="97e4f-187">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="97e4f-188">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97e4f-188">Header</span></span><br/> | <dl> <span data-ttu-id="97e4f-189"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="97e4f-189"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e4f-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97e4f-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e4f-191">**\_Descrizione della risorsa D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="97e4f-191">**D3D12\_RESOURCE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[<span data-ttu-id="97e4f-192">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="97e4f-192">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

