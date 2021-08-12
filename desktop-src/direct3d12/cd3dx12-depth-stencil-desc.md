---
title: CD3DX12_DEPTH_STENCIL_DESC struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ DEPTH \_ STENCIL \_ DESC.
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- CD3DX12_DEPTH_STENCIL_DESC struttura
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbd7184ad6fc432beb5ba8e9585c2e9a93486acc604f875ff3a70f72e8ec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531107"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>Struttura CD3DX12 \_ DEPTH \_ STENCIL \_ DESC

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ DEPTH STENCIL \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un file D3DX12 \_ DEPTH \_ STENCIL \_ DESC.

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(const D3D12 \_ DEPTH STENCIL \_ \_ DESC& o)**
</dt> <dd>

Crea una nuova istanza di una struttura D3DX12 DEPTH STENCIL DESC, inizializzata con il contenuto di un'altra struttura \_ \_ \_ [**D3D12 \_ DEPTH \_ STENCIL \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nuova istanza di D3DX12 \_ DEPTH \_ STENCIL \_ DESC, inizializzata con i parametri predefiniti.

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(BOOL depthEnable, D3D12 \_ DEPTH WRITE MASK \_ \_ depthWriteMask, \_ D3D12 COMPARISON \_ FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12 \_ STENCIL OP \_ frontStencilFailOp, D3D12 \_ STENCIL OP \_ frontStencilDepthFailOp, D3D12 STENCIL OP frontStencilDepthFailOp, D3D12 STENCIL OP frontStencilDepthFailOp, \_ \_ D3D12 STENCIL OP frontStencilPassOp, D3D12 \_ COMPARISON \_ FUNC frontStencilFunc, D3D12 \_ STENCIL OP \_ backStencilFailOp, D3D12 \_ STENCIL OP \_ backStencilDepthFailOp, D3D12 \_ STENCIL OP \_ backStencilPassOp, D3D12 \_ COMPARISON \_ FUNC backStencilFunc)**
</dt> <dd>

Crea una nuova istanza di D3DX12 \_ DEPTH \_ STENCIL \_ DESC, inizializzando i parametri seguenti:

Profondità BOOLEnable

[**D3D12 \_ DEPTH \_ WRITE \_ MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc

Stencil BOOLEnable

Stencil UINT8ReadMask

Stencil UINT8WriteMask

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc

</dd> <dt>

**~CD3DX12 \_ \_ DEPTH STENCIL \_ DESC()**
</dt> <dd>

Elimina un'istanza di un FILE CD3DX12 \_ DEPTH \_ STENCIL \_ DESC.

</dd> <dt>

**operator const D3D12 \_ DEPTH \_ STENCIL \_ DESC&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





