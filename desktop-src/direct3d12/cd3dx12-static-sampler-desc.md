---
title: Struttura CD3DX12_STATIC_SAMPLER_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura Desc del campionatore statico D3D12 \_ .
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- Struttura CD3DX12_STATIC_SAMPLER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322201"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a><span data-ttu-id="083a0-104">\_ \_ Struttura Desc del campionatore statico CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="083a0-104">CD3DX12\_STATIC\_SAMPLER\_DESC structure</span></span>

<span data-ttu-id="083a0-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ \_ Desc del campionatore statico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="083a0-105">A helper structure to enable easy initialization of a [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="083a0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="083a0-106">Syntax</span></span>


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="083a0-107">Members</span><span class="sxs-lookup"><span data-stu-id="083a0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="083a0-108">**CD3DX12 \_ statico \_ Sampler \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="083a0-108">**CD3DX12\_STATIC\_SAMPLER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="083a0-109">Crea una nuova istanza non inizializzata di una \_ \_ Descrizione del campionatore statico CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="083a0-109">Creates a new, uninitialized, instance of a CD3DX12\_STATIC\_SAMPLER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="083a0-110">**Explicit CD3DX12 \_ static \_ Sampler \_ DESC (const D3D12 \_ static \_ Sampler \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="083a0-110">**explicit CD3DX12\_STATIC\_SAMPLER\_DESC(const D3D12\_STATIC\_SAMPLER\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="083a0-111">Crea una nuova istanza di una \_ Descrizione del \_ campionatore statico CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura della [**\_ \_ \_ Descrizione del campionatore statico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="083a0-111">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initialized with the contents of another [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="083a0-112">**CD3DX12 \_ static \_ Sampler \_ DESC (uint shaderRegister, D3D12 filter Filter \_ = D3D12 \_ Filter \_ anisotropico, D3D12 \_ texture \_ Address \_ mode AddressList = D3D12 \_ texture address Mode \_ \_ \_ wrap, D3D12 texture address \_ mode \_ \_ addressV = D3D12 texture address \_ mode \_ \_ \_ wrap, D3D12 \_ trama \_ Address \_ mode ADDRESSW = D3D12 \_ trama \_ Address \_ mode \_ wrap, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func ComparisonFunc = D3D12 \_ Comparison \_ Func \_ less \_ uguale, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaque \_ White, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ shader \_ visibility shaderVisibility = D3D12 \_ shader \_ visibility \_ All, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="083a0-112">**CD3DX12\_STATIC\_SAMPLER\_DESC(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="083a0-113">Crea una nuova istanza di una \_ Descrizione del \_ campionatore statico CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="083a0-113">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="083a0-114">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="083a0-114">UINT shaderRegister</span></span>

<span data-ttu-id="083a0-115">consenso esplicito [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotropico</span><span class="sxs-lookup"><span data-stu-id="083a0-115">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="083a0-116">consenso esplicito [**D3D12 \_ \_ \_ Tipo di indirizzo della trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) Address = D3D12 della \_ \_ modalità di indirizzo della trama \_ \_</span><span class="sxs-lookup"><span data-stu-id="083a0-116">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-117">consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ trama \_ Address \_ mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="083a0-117">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-118">consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ trama \_ Address \_ mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="083a0-118">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-119">consenso esplicito FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="083a0-119">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="083a0-120">consenso esplicito UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="083a0-120">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="083a0-121">consenso esplicito [**D3D12 \_ CONFRONTO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ confronto \_ Func \_ meno \_ uguale</span><span class="sxs-lookup"><span data-stu-id="083a0-121">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="083a0-122">consenso esplicito [**D3D12 \_ \_ \_ Colore del bordo statico**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ colore del bordo statico D3D12 \_ \_ \_ \_ bianco opaco</span><span class="sxs-lookup"><span data-stu-id="083a0-122">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="083a0-123">consenso esplicito FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="083a0-123">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="083a0-124">consenso esplicito FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="083a0-124">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="083a0-125">consenso esplicito [**D3D12 \_ SHADER \_ visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="083a0-125">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="083a0-126">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="083a0-126">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="083a0-127">**static inline init (D3D12 \_ static \_ SAMPLER \_ desc &SamplerDesc, uint shaderRegister, D3D12 \_ filter Filter = D3D12 \_ Filter \_ anisotropico, D3D12 \_ texture \_ Address \_ mode Addresse = D3D12 texture address Mode wrap, D3D12 texture address Mode addressV = D3D12 wrapping Mode Address Mode, \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ D3D12 \_ trama \_ Address \_ mode ADDRESSW = D3D12 \_ trama \_ Address \_ mode \_ wrap, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func ComparisonFunc = D3D12 \_ Comparison \_ Func \_ less \_ uguale, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaque \_ White, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ shader \_ visibility shaderVisibility = D3D12 \_ shader \_ visibility \_ All, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="083a0-127">**static inline Init(D3D12\_STATIC\_SAMPLER\_DESC &samplerDesc, UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="083a0-128">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="083a0-128">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="083a0-129">[**D3D12 \_ \_Campionatore statico \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span><span class="sxs-lookup"><span data-stu-id="083a0-129">[**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span></span>

<span data-ttu-id="083a0-130">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="083a0-130">UINT shaderRegister</span></span>

<span data-ttu-id="083a0-131">consenso esplicito [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotropico</span><span class="sxs-lookup"><span data-stu-id="083a0-131">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="083a0-132">consenso esplicito [**D3D12 \_ \_ \_ Tipo di indirizzo della trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) Address = D3D12 della \_ \_ modalità di indirizzo della trama \_ \_</span><span class="sxs-lookup"><span data-stu-id="083a0-132">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-133">consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ trama \_ Address \_ mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="083a0-133">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-134">consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ trama \_ Address \_ mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="083a0-134">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-135">consenso esplicito FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="083a0-135">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="083a0-136">consenso esplicito UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="083a0-136">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="083a0-137">consenso esplicito [**D3D12 \_ CONFRONTO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ confronto \_ Func \_ meno \_ uguale</span><span class="sxs-lookup"><span data-stu-id="083a0-137">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="083a0-138">consenso esplicito [**D3D12 \_ \_ \_ Colore del bordo statico**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ colore del bordo statico D3D12 \_ \_ \_ \_ bianco opaco</span><span class="sxs-lookup"><span data-stu-id="083a0-138">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="083a0-139">consenso esplicito FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="083a0-139">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="083a0-140">consenso esplicito FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="083a0-140">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="083a0-141">consenso esplicito [**D3D12 \_ SHADER \_ visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="083a0-141">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="083a0-142">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="083a0-142">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="083a0-143">**inline init (UINT shaderRegister, D3D12 Filter \_ Filter = D3D12 \_ Filter \_ anisotropico, D3D12 \_ texture \_ Address \_ mode AddressList = D3D12 \_ trama \_ Address \_ mode \_ wrap, D3D12 \_ texture \_ Address \_ mode addressV = D3D12 texture address \_ mode \_ \_ \_ wrap, D3D12 \_ trama \_ Address \_ mode addressW = D3D12 \_ trama \_ Address \_ mode \_ wrap, float MipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonFunc = D3D12 \_ Comparison \_ Func \_ less \_ uguale, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaque \_ White, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ shader \_ visibility shaderVisibility = D3D12 \_ shader \_ visibility \_ All, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="083a0-143">**inline Init(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="083a0-144">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="083a0-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="083a0-145">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="083a0-145">UINT shaderRegister</span></span>

<span data-ttu-id="083a0-146">consenso esplicito [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotropico</span><span class="sxs-lookup"><span data-stu-id="083a0-146">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="083a0-147">consenso esplicito [**D3D12 \_ \_ \_ Tipo di indirizzo della trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) Address = D3D12 della \_ \_ modalità di indirizzo della trama \_ \_</span><span class="sxs-lookup"><span data-stu-id="083a0-147">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-148">consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ trama \_ Address \_ mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="083a0-148">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-149">consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ trama \_ Address \_ mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="083a0-149">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="083a0-150">consenso esplicito FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="083a0-150">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="083a0-151">consenso esplicito UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="083a0-151">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="083a0-152">consenso esplicito [**D3D12 \_ CONFRONTO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ confronto \_ Func \_ meno \_ uguale</span><span class="sxs-lookup"><span data-stu-id="083a0-152">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="083a0-153">consenso esplicito [**D3D12 \_ \_ \_ Colore del bordo statico**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ colore del bordo statico D3D12 \_ \_ \_ \_ bianco opaco</span><span class="sxs-lookup"><span data-stu-id="083a0-153">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="083a0-154">consenso esplicito FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="083a0-154">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="083a0-155">consenso esplicito FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="083a0-155">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="083a0-156">consenso esplicito [**D3D12 \_ SHADER \_ visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ shader \_ visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="083a0-156">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="083a0-157">consenso esplicito UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="083a0-157">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="083a0-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="083a0-158">Requirements</span></span>



| <span data-ttu-id="083a0-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="083a0-159">Requirement</span></span> | <span data-ttu-id="083a0-160">Valore</span><span class="sxs-lookup"><span data-stu-id="083a0-160">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="083a0-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="083a0-161">Header</span></span><br/> | <dl> <span data-ttu-id="083a0-162"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="083a0-162"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="083a0-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="083a0-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="083a0-164">**D3D12 \_ \_ campionatore statico \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="083a0-164">**D3D12\_STATIC\_SAMPLER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[<span data-ttu-id="083a0-165">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="083a0-165">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





