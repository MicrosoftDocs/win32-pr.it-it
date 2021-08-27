---
title: CD3DX12_TILE_REGION_SIZE struttura (D3dx12.h)
description: Struttura helper per consentire l'inizializzazione semplificata di una struttura D3D12 \_ TILE \_ REGION \_ SIZE.
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- CD3DX12_TILE_REGION_SIZE struttura
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
ms.openlocfilehash: 9cc1b96ae4d7d33101068a1ba08f0314b99950146e91a352ab49fea714376471
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119611"
---
# <a name="cd3dx12_tile_region_size-structure"></a>Struttura DIMENSIONI DELL'AREA DEL RIQUADRO CD3DX12 \_ \_ \_

Struttura helper per consentire l'inizializzazione semplificata di [**una struttura D3D12 \_ TILE REGION \_ \_ SIZE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)

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

**DIMENSIONI DELL'AREA DEL RIQUADRO CD3DX12() \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di UN'AREA DEL RIQUADRO CD3DX12. \_ \_ \_

</dd> <dt>

**explicit CD3DX12 \_ TILE \_ REGION \_ SIZE(const D3D12 \_ TILE REGION SIZE &\_ \_ o)**
</dt> <dd>

Crea una nuova istanza di una struttura CD3DX12 TILE REGION SIZE, inizializzata con il contenuto di \_ \_ un'altra struttura \_ [**D3D12 \_ TILE REGION \_ \_ SIZE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)

</dd> <dt>

**CD3DX12 \_ TILE \_ REGION \_ SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**
</dt> <dd>

Crea una nuova istanza di UN'AREA DEL RIQUADRO CD3DX12 \_ \_ \_ SIZE, inizializzando i parametri seguenti:

UINT numTiles

BOOL useBox

Larghezza UINT

Altezza UINT16

Profondità UINT16

</dd> <dt>

**Operatore const D3D12 \_ TILE \_ REGION SIZE \_&() const**
</dt> <dd>

Definisce l& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DIMENSIONI DELL'AREA DEL RIQUADRO D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





