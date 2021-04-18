---
title: Struttura CD3DX12_RASTERIZER_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura Desc del rasterizzatore D3D12 \_ .
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Struttura CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322218"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>\_Struttura Desc del rasterizzatore CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ Desc del rasterizzatore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Rasterizzatore CD3DX12 \_ DESC ()**
</dt> <dd>

Crea un'istanza nuova, non inizializzata, di un \_ rasterizzatore CD3DX12 \_ desc.

</dd> <dt>

**rasterizzatore esplicito CD3DX12 \_ \_ DESC (const D3D12 \_ rasterizzator \_ desc& o)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione del rasterizzatore CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ desc di rasterizzazione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

</dd> <dt>

**rasterizzatore CD3DX12 esplicito \_ \_ DESC ( \_ impostazione predefinita CD3DX12)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione di rasterizzazione CD3DX12 \_ , inizializzata con parametri predefiniti.

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

**rasterizzazione CD3DX12 esplicita \_ \_ DESC ( \_ \_ modalità di riempimento D3D12 FillMode, \_ modalità di abbattimento D3D12 \_ CullMode, bool FrontCounterClockwise, int DepthBias, float DepthBiasClamp, float slopeScaledDepthBias, bool DepthClipEnable, bool multisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, D3D12 \_ Conservation \_ mode di rasterizzazione conservativeRaster \_ )**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione del rasterizzatore CD3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ FillMode \_ modalità riempimento**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode)

[**D3D12 \_ CullMode \_ modalità di eliminazione**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)

BOOL frontCounterClockwise

INT depthBias

FLOAT depthBiasClamp

FLOAT slopeScaledDepthBias

BOOL depthClipEnable

BOOL multisampleEnable

BOOL antialiasedLineEnable

ForcedSampleCount UINT

[**D3D12 \_ \_ \_ Modalità di RASTERIZZAzione conservativa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster

</dd> <dt>

**~ CD3DX12 \_ rasterizzatore \_ DESC ()**
</dt> <dd>

Elimina un'istanza di una descrizione del \_ rasterizzatore CD3DX12 \_ .

</dd> <dt>

**operator const D3D12 \_ rasterizzatore \_ desc& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ rasterizzatore \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





