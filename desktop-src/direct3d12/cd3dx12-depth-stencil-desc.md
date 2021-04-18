---
title: Struttura CD3DX12_DEPTH_STENCIL_DESC (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura D3D12 depth stencil \_ desc.
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Struttura CD3DX12_DEPTH_STENCIL_DESC
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
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322278"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>\_Struttura CD3DX12 Depth \_ stencil \_ DESC

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura [**D3D12 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

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

**CD3DX12 \_ Depth \_ stencil \_ DESC ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ Descrizione di stencil Depth \_ D3DX12 \_ .

</dd> <dt>

**esplicito CD3DX12 \_ Depth \_ stencil \_ DESC (const D3D12 \_ Depth \_ stencil \_ desc& o)**
</dt> <dd>

Crea una nuova istanza di D3DX12 \_ Depth \_ stencil \_ DESC, inizializzata con il contenuto di un'altra struttura [**D3D12 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

</dd> <dt>

**esplicito CD3DX12 \_ Depth \_ stencil \_ DESC ( \_ impostazione predefinita CD3DX12)**
</dt> <dd>

Crea una nuova istanza di D3DX12 \_ Depth \_ stencil \_ DESC, inizializzata con parametri predefiniti.

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

**esplicito CD3DX12 \_ Depth \_ stencil \_ DESC (bool depthEnable, D3D12 \_ Depth \_ Write \_ mask depthWriteMask, D3D12 \_ Comparison \_ Func depthFunc, bool STENCILENABLE, Uint8 StencilReadMask, Uint8 stencilWriteMask, D3D12 \_ stencil \_ op FrontStencilFailOp, D3D12 \_ stencil \_ op FRONTSTENCILDEPTHFAILOP, D3D12 \_ stencil \_ op frontStencilPassOp, D3D12 \_ Comparison \_ Func frontStencilFunc, D3D12 \_ stencil \_ op backStencilFailOp, D3D12 \_ stencil \_ op backStencilDepthFailOp, D3D12 \_ stencil \_ op backStencilPassOp, D3D12 \_ Comparison \_ Func backStencilFunc)**
</dt> <dd>

Crea una nuova istanza di una \_ desc D3DX12 Depth \_ stencil \_ , inizializzando i parametri seguenti:

BOOL depthEnable

[**D3D12 \_ \_ \_ Maschera di scrittura profondità**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask

[**D3D12 \_ DepthFunc \_ Func confronto**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

BOOL stencilEnable

StencilReadMask UINT8

StencilWriteMask UINT8

[**D3D12 \_ FrontStencilFailOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ FrontStencilDepthFailOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ FrontStencilPassOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ FrontStencilFunc \_ Func confronto**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

[**D3D12 \_ BackStencilFailOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ BackStencilDepthFailOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ BackStencilPassOp \_ op stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ BackStencilFunc \_ Func confronto**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

</dd> <dt>

**~ CD3DX12 \_ Depth \_ stencil \_ DESC ()**
</dt> <dd>

Elimina un'istanza di una desc CD3DX12 \_ Depth \_ stencil \_ .

</dd> <dt>

**operator const D3D12 \_ Depth \_ STENCIL \_ desc& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ Depth \_ stencil \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





