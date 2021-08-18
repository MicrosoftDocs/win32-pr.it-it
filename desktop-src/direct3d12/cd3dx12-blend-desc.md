---
title: CD3DX12_BLEND_DESC struttura (D3dx12.h)
description: Struttura helper per consentire un'inizializzazione semplice di una struttura DESC BLEND D3D12. \_ \_
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- CD3DX12_BLEND_DESC struttura
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
ms.openlocfilehash: 40acdedbe428d808a576b68645a3e662dc71389b4d6dd0c19424278f28deb93a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989951"
---
# <a name="cd3dx12_blend_desc-structure"></a>Struttura DESC CD3DX12 \_ BLEND \_

Struttura helper per consentire un'inizializzazione semplice di [**una struttura \_ \_ DESC BLEND D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)

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

**CD3DX12 \_ BLEND \_ DESC()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un'istanza DISS BLEND CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ BLEND \_ DESC(const D3D12 \_ BLEND \_ DESC& o)**
</dt> <dd>

Crea una nuova istanza di cd3DX12 BLEND DESC, inizializzata con il contenuto di \_ \_ un'altra struttura [**D3D12 \_ BLEND \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)

</dd> <dt>

**explicit CD3DX12 \_ BLEND \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nuova istanza di cd3DX12 \_ BLEND \_ DESC, inizializzata con i parametri predefiniti.



| State                                   | Valore predefinito                    |
|-----------------------------------------|----------------------------------|
| AlphaToCoverageEnable                   | **FALSE**                        |
| IndependentBlendEnable                  | **FALSE**                        |
| RenderTarget \[ \] 0. BlendEnable           | **FALSE**                        |
| RenderTarget \[ \] 0. LogicOpEnable         | **FALSE**                        |
| RenderTarget \[ \] 0. SrcBlend              | D3D12 \_ BLEND \_ ONE                |
| RenderTarget \[ \] 0. DestBlend             | D3D12 \_ BLEND \_ ZERO               |
| RenderTarget \[ \] 0. BlendOp               | D3D12 \_ BLEND \_ OP \_ ADD            |
| RenderTarget \[ \] 0. SrcBlendAlpha         | D3D12 \_ BLEND \_ ONE                |
| RenderTarget \[ \] 0. DestBlendAlpha        | D3D12 \_ BLEND \_ ZERO               |
| RenderTarget \[ \] 0. BlendOpAlpha          | D3D12 \_ BLEND \_ OP \_ ADD            |
| RenderTarget \[ \] 0. LogicOp               | D3D12 \_ LOGIC \_ OP \_ NOOP           |
| RenderTarget \[ \] 0. RenderTargetWriteMask | D3D12 \_ COLOR \_ WRITE \_ ENABLE \_ ALL |



 

</dd> <dt>

**~CD3DX12 \_ BLEND \_ DESC()**
</dt> <dd>

Elimina un'istanza di un'istanza di BLEND DESC CD3DX12. \_ \_

</dd> <dt>

**Operatore const D3D12 \_ BLEND \_ DESC&() const**
</dt> <dd>

Definisce l& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





