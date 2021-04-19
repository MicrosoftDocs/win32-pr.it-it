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
# <a name="cd3dx12_static_sampler_desc-structure"></a>\_ \_ Struttura Desc del campionatore statico CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ \_ Desc del campionatore statico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ statico \_ Sampler \_ DESC ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ \_ Descrizione del campionatore statico CD3DX12 \_ .

</dd> <dt>

**Explicit CD3DX12 \_ static \_ Sampler \_ DESC (const D3D12 \_ static \_ Sampler \_ desc &o)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione del \_ campionatore statico CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura della [**\_ \_ \_ Descrizione del campionatore statico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

</dd> <dt>

**CD3DX12 \_ static \_ Sampler \_ DESC (uint shaderRegister, D3D12 filter Filter \_ = D3D12 \_ Filter \_ anisotropico, D3D12 \_ texture \_ Address \_ mode AddressList = D3D12 \_ texture address Mode \_ \_ \_ wrap, D3D12 texture address \_ mode \_ \_ addressV = D3D12 texture address \_ mode \_ \_ \_ wrap, D3D12 \_ trama \_ Address \_ mode ADDRESSW = D3D12 \_ trama \_ Address \_ mode \_ wrap, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func ComparisonFunc = D3D12 \_ Comparison \_ Func \_ less \_ uguale, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaque \_ White, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ shader \_ visibility shaderVisibility = D3D12 \_ shader \_ visibility \_ All, uint registerSpace = 0)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione del \_ campionatore statico CD3DX12 \_ , inizializzando i parametri seguenti:

ShaderRegister UINT

consenso esplicito [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotropico

consenso esplicito [**D3D12 \_ \_ \_ Tipo di indirizzo della trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) Address = D3D12 della \_ \_ modalità di indirizzo della trama \_ \_

consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ trama \_ Address \_ mode \_ Wrap

consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ trama \_ Address \_ mode \_ Wrap

consenso esplicito FLOAT mipLODBias = 0

consenso esplicito UINT maxAnisotropy = 16

consenso esplicito [**D3D12 \_ CONFRONTO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ confronto \_ Func \_ meno \_ uguale

consenso esplicito [**D3D12 \_ \_ \_ Colore del bordo statico**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ colore del bordo statico D3D12 \_ \_ \_ \_ bianco opaco

consenso esplicito FLOAT minLOD = 0. f

consenso esplicito FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

consenso esplicito [**D3D12 \_ SHADER \_ visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ shader \_ visibility \_ All

consenso esplicito UINT registerSpace = 0

</dd> <dt>

**static inline init (D3D12 \_ static \_ SAMPLER \_ desc &SamplerDesc, uint shaderRegister, D3D12 \_ filter Filter = D3D12 \_ Filter \_ anisotropico, D3D12 \_ texture \_ Address \_ mode Addresse = D3D12 texture address Mode wrap, D3D12 texture address Mode addressV = D3D12 wrapping Mode Address Mode, \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ D3D12 \_ trama \_ Address \_ mode ADDRESSW = D3D12 \_ trama \_ Address \_ mode \_ wrap, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func ComparisonFunc = D3D12 \_ Comparison \_ Func \_ less \_ uguale, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaque \_ White, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ shader \_ visibility shaderVisibility = D3D12 \_ shader \_ visibility \_ All, uint registerSpace = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Campionatore statico \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc

ShaderRegister UINT

consenso esplicito [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotropico

consenso esplicito [**D3D12 \_ \_ \_ Tipo di indirizzo della trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) Address = D3D12 della \_ \_ modalità di indirizzo della trama \_ \_

consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ trama \_ Address \_ mode \_ Wrap

consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ trama \_ Address \_ mode \_ Wrap

consenso esplicito FLOAT mipLODBias = 0

consenso esplicito UINT maxAnisotropy = 16

consenso esplicito [**D3D12 \_ CONFRONTO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ confronto \_ Func \_ meno \_ uguale

consenso esplicito [**D3D12 \_ \_ \_ Colore del bordo statico**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ colore del bordo statico D3D12 \_ \_ \_ \_ bianco opaco

consenso esplicito FLOAT minLOD = 0. f

consenso esplicito FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

consenso esplicito [**D3D12 \_ SHADER \_ visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ shader \_ visibility \_ All

consenso esplicito UINT registerSpace = 0

</dd> <dt>

**inline init (UINT shaderRegister, D3D12 Filter \_ Filter = D3D12 \_ Filter \_ anisotropico, D3D12 \_ texture \_ Address \_ mode AddressList = D3D12 \_ trama \_ Address \_ mode \_ wrap, D3D12 \_ texture \_ Address \_ mode addressV = D3D12 texture address \_ mode \_ \_ \_ wrap, D3D12 \_ trama \_ Address \_ mode addressW = D3D12 \_ trama \_ Address \_ mode \_ wrap, float MipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonFunc = D3D12 \_ Comparison \_ Func \_ less \_ uguale, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaque \_ White, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ shader \_ visibility shaderVisibility = D3D12 \_ shader \_ visibility \_ All, uint registerSpace = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

consenso esplicito [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotropico

consenso esplicito [**D3D12 \_ \_ \_ Tipo di indirizzo della trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) Address = D3D12 della \_ \_ modalità di indirizzo della trama \_ \_

consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ trama \_ Address \_ mode \_ Wrap

consenso esplicito [**D3D12 \_ TEXTURE \_ Address \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ trama \_ Address \_ mode \_ Wrap

consenso esplicito FLOAT mipLODBias = 0

consenso esplicito UINT maxAnisotropy = 16

consenso esplicito [**D3D12 \_ CONFRONTO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ confronto \_ Func \_ meno \_ uguale

consenso esplicito [**D3D12 \_ \_ \_ Colore del bordo statico**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ colore del bordo statico D3D12 \_ \_ \_ \_ bianco opaco

consenso esplicito FLOAT minLOD = 0. f

consenso esplicito FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

consenso esplicito [**D3D12 \_ SHADER \_ visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ shader \_ visibility \_ All

consenso esplicito UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ \_ campionatore statico \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





