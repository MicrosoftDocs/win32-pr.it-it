---
title: CD3DX12_TILE_SHAPE struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura TILE SHAPE D3D12. \_ \_
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- CD3DX12_TILE_SHAPE struttura
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b02f699ab06ef93f3eeace3ce515b0947030e4824e2cb0fa51034c3e33f51dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987871"
---
# <a name="cd3dx12_tile_shape-structure"></a>Struttura CD3DX12 \_ TILE \_ SHAPE

Struttura helper per consentire una facile inizializzazione di [**una struttura TILE \_ \_ SHAPE D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ TILE \_ SHAPE()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un oggetto CD3DX12 \_ TILE \_ SHAPE.

</dd> <dt>

**EXPLICIT CD3DX12 \_ TILE \_ SHAPE(const D3D12 \_ TILE SHAPE &\_ o)**
</dt> <dd>

Crea una nuova istanza di una struttura CD3DX12 TILE SHAPE, inizializzata con il contenuto di un'altra struttura \_ \_ TILE [**\_ \_ SHAPE D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)

</dd> <dt>

**CD3DX12 \_ TILE \_ SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 \_ TILE \_ SHAPE, inizializzando i parametri seguenti:

UiNT widthInTexels

UINT heightInTexels

UINT depthInTexels

</dd> <dt>

**operator const D3D12 \_ TILE \_ SHAPE&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FORMA RIQUADRO D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





