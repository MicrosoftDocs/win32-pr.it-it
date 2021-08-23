---
title: CD3DX12_RASTERIZER_DESC struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura \_ DESC RASTERIZER D3D12. \_
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- CD3DX12_RASTERIZER_DESC struttura
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
ms.openlocfilehash: faa95dde87aea8e3c61d0d1fb6de6845f33717f6a46db4df7996a23afd7590b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729431"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>Struttura CD3DX12 \_ RASTERIZER \_ DESC

Struttura helper per consentire una facile inizializzazione di [**una struttura \_ \_ DESC RASTERIZER D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)

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

**RASTERIZZAZIONE CD3DX12 \_ \_ DESC()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un OGGETTO CD3DX12 \_ RASTERIZER \_ DESC.

</dd> <dt>

**DESC raSTERIZER CD3DX12 \_ \_ esplicito(const D3D12 \_ RASTERIZER \_ DESC& o)**
</dt> <dd>

Crea una nuova istanza di una struttura CD3DX12 RASTERIZER DESC, inizializzata con il contenuto di un'altra struttura \_ \_ [**\_ \_ DESC RASTERIZER D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)

</dd> <dt>

**DESC RASTERIZER CD3DX12 \_ \_ esplicito(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nuova istanza di un OGGETTO CD3DX12 \_ RASTERIZER \_ DESC, inizializzato con i parametri predefiniti.

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

**EXPLICIT CD3DX12 \_ RASTERIZER \_ DESC(D3D12 \_ FILL MODE \_ fillMode, D3D12 \_ CULL MODE \_ cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12 \_ CONSERVATIVE \_ RASTERIZATION \_ MODE conservativeRaster)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ RASTERIZER \_ DESC, inizializzando i parametri seguenti:

[**D3D12 \_ FILL \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode

[**D3D12 \_ CULL \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode

BOOL frontCounterClockwise

Int depthBias

FLOAT depthBiasClamp

Float slopeScaledDepthBias

Profondità BOOLClipEnable

BoOL multisampleEnable

AntialiasedLineEnable BOOL

UINT forcedSampleCount

[**D3D12 \_ CONSERVATIVE \_ RASTERIZATION \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster

</dd> <dt>

**~CD3DX12 \_ RASTERIZER \_ DESC()**
</dt> <dd>

Elimina un'istanza di un FILE DESC DI RASTERIZER CD3DX12. \_ \_

</dd> <dt>

**operator const D3D12 \_ RASTERIZER \_ DESC&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





