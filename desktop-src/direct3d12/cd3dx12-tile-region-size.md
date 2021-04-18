---
title: Struttura CD3DX12_TILE_REGION_SIZE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di dimensioni dell'area del riquadro D3D12 \_ \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Struttura CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322196"
---
# <a name="cd3dx12_tile_region_size-structure"></a>\_Struttura delle \_ dimensioni dell'area del riquadro CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ dimensioni dell' \_ area \_ del riquadro D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ Dimensioni area riquadro CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ dimensione dell'area del riquadro CD3DX12 \_ \_ .

</dd> <dt>

**dimensioni dell'area del riquadro CD3DX12 esplicite \_ \_ \_ (const D3D12 \_ dimensioni dell' \_ area \_ &o)**
</dt> <dd>

Crea una nuova istanza di una \_ dimensione dell'area del riquadro CD3DX12 \_ \_ , inizializzata con il contenuto di un'altra struttura di dimensioni dell' [**\_ area della sezione \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

</dd> <dt>

**\_Dimensioni area del riquadro CD3DX12 \_ \_ (uint NumTiles, bool useBox, uint width, UINT16 Height, UInt16 Depth)**
</dt> <dd>

Crea una nuova istanza di una \_ dimensione dell'area del riquadro CD3DX12 \_ \_ , inizializzando i parametri seguenti:

NumTiles UINT

BOOL useBox

Lunghezza UINT

Altezza UINT16

Profondità UINT16

</dd> <dt>

**operator const \_ D3D12 \_ dimensioni area del riquadro \_& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ Dimensioni area del riquadro D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





