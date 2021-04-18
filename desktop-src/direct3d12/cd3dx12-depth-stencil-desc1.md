---
title: Struttura CD3DX12_DEPTH_STENCIL_DESC1 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura DESC1 di D3D12 Depth \_ stencil \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Struttura CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322274"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a>\_ \_ Struttura DESC1 dello stencil CD3DX12 Depth \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**DESC1 di D3D12 \_ Depth \_ stencil \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Stencil Depth \_ CD3DX12 \_ DESC1 ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di uno \_ stencil di profondità CD3DX12 \_ \_ DESC1.

</dd> <dt>

**Explicit CD3DX12 \_ Depth \_ stencil \_ DESC1 (const D3D12 \_ Depth \_ stencil \_ DESC1& o)**
</dt> <dd>

Crea una nuova istanza di uno \_ stencil Depth \_ CD3DX12 \_ DESC1, inizializzato con i valori copiati da una struttura [**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

</dd> <dt>

**Explicit CD3DX12 \_ Depth \_ stencil \_ DESC1 (const D3D12 \_ Depth \_ stencil \_ desc& o)**
</dt> <dd>

Crea una nuova istanza di uno \_ stencil Depth \_ CD3DX12 \_ DESC1, inizializzato con i valori copiati da una struttura [**D3D12 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

e il membro **DepthBoundsTestEnable** aggiuntivo impostato su **false**.

</dd> <dt>

**DESC1 esplicito CD3DX12 \_ Depth \_ stencil \_ (CD3DX12 \_ predefinito)**
</dt> <dd>

Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzato con lo stato predefinito prescritto da D3DX12:

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

**esplicito CD3DX12 \_ Depth \_ stencil \_ DESC1 (bool depthEnable, D3D12 \_ Depth \_ Write \_ mask depthWriteMask, D3D12 \_ Comparison \_ Func depthFunc, bool STENCILENABLE, Uint8 StencilReadMask, Uint8 stencilWriteMask, D3D12 \_ stencil \_ op FrontStencilFailOp, D3D12 \_ stencil \_ op FRONTSTENCILDEPTHFAILOP, D3D12 \_ stencil \_ op frontStencilPassOp, D3D12 \_ Comparison \_ Func frontStencilFunc, D3D12 \_ stencil \_ op BackStencilFailOp, D3D12 \_ stencil \_ op backStencilDepthFailOp, D3D12 \_ stencil \_ op backStencilPassOp, D3D12 \_ Comparison \_ Func backStencilFunc, bool depthBoundsTestEnable)**
</dt> <dd>

Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzata con i valori passati nell'elenco di parametri.

</dd> <dt>

**~ CD3DX12 \_ Depth \_ stencil \_ DESC1 ()**
</dt> <dd>

Elimina un'istanza di uno stencil di \_ profondità \_ D3DX12 \_ DESC1.

</dd> <dt>

**operatore const D3D12 \_ Depth \_ STENCIL \_ DESC1& () const**
</dt> <dd>

Conversione implicita in una \_ struttura DESC1 di D3D12 Depth \_ stencil \_ . Poiché D3D12 \_ Depth \_ stencil \_ DESC1 è il tipo sottostante di CD3DX12 \_ Depth \_ stencil \_ DESC1, l'oggetto viene semplicemente restituito come un riferimento a un D3D12 di profondità const DESC1 \_ \_ \_ a se stesso.

</dd> <dt>

**operator const D3D12 \_ Depth \_ stencil \_ DESC () const**
</dt> <dd>

Conversione implicita in un \_ valore della struttura desc di D3D12 Depth \_ stencil \_ . Poiché D3D12 \_ Depth \_ stencil \_ DESC non è il tipo sottostante di CD3DX12 \_ Depth \_ stencil \_ DESC1, viene creata una nuova istanza di D3D12 \_ Depth \_ stencil \_ DESC, che viene restituita per valore. Si noti che D3D12 \_ Depth \_ stencil DESC non \_ include il membro **DepthBoundsTestEnable** , quindi questo valore viene perso nella conversione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Stencil profondità \_ D3D12 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[**D3D12 \_ Depth \_ stencil \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





