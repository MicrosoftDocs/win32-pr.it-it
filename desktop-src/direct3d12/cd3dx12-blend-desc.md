---
title: Struttura CD3DX12_BLEND_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura desc di D3D12 Blend \_ .
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Struttura CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322284"
---
# <a name="cd3dx12_blend_desc-structure"></a>\_ \_ Struttura desc di CD3DX12 Blend

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ desc di D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ Blend \_ DESC ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ Descrizione di Blend CD3DX12 \_ .

</dd> <dt>

**Explicit CD3DX12 \_ Blend \_ DESC (const D3D12 \_ Blend \_ desc& o)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ Blend \_ DESC, inizializzata con il contenuto di un'altra struttura di [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

</dd> <dt>

**Explicit CD3DX12 \_ Blend \_ DESC ( \_ impostazione predefinita CD3DX12)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ Blend \_ DESC, inizializzata con parametri predefiniti.



| State                                   | Valore predefinito                    |
|-----------------------------------------|----------------------------------|
| AlphaToCoverageEnable                   | **FALSE**                        |
| IndependentBlendEnable                  | **FALSE**                        |
| RenderTarget \[ 0 \] . BlendEnable           | **FALSE**                        |
| RenderTarget \[ 0 \] . LogicOpEnable         | **FALSE**                        |
| RenderTarget \[ 0 \] . SrcBlend              | D3D12 \_ Blend \_ One                |
| RenderTarget \[ 0 \] . DestBlend             | D3D12 \_ Blend \_ zero               |
| RenderTarget \[ 0 \] . BlendOp               | D3D12 \_ Blend \_ op \_ Add            |
| RenderTarget \[ 0 \] . SrcBlendAlpha         | D3D12 \_ Blend \_ One                |
| RenderTarget \[ 0 \] . DestBlendAlpha        | D3D12 \_ Blend \_ zero               |
| RenderTarget \[ 0 \] . BlendOpAlpha          | D3D12 \_ Blend \_ op \_ Add            |
| RenderTarget \[ 0 \] . LogicOp               | \_ \_ NoOp op per la logica D3D12 \_           |
| RenderTarget \[ 0 \] . RenderTargetWriteMask | D3D12 \_ Color \_ Write \_ Abilita \_ tutto |



 

</dd> <dt>

**~ CD3DX12 \_ Blend \_ DESC ()**
</dt> <dd>

Elimina un'istanza di una descrizione di \_ Blend CD3DX12 \_ .

</dd> <dt>

**operator const D3D12 \_ Blend \_ desc& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





