---
title: CD3DX12_TILED_RESOURCE_COORDINATE struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ TILED \_ RESOURCE \_ COORDINATE.
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- CD3DX12_TILED_RESOURCE_COORDINATE struttura
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 784955545fe8e71227ffae6c5eec54acfd65b4a0ab0867f5c7de99a148976861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987851"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>Struttura CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ TILED RESOURCE \_ \_ COORDINATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**COORDINATE DI RISORSA IN RIQUADRI CD3DX12() \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un oggetto CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE.

</dd> <dt>

**COORDINATE DI RISORSA AFFIANCATE ESPLICITE CD3DX12(const \_ \_ \_ D3D12 \_ TILED \_ RESOURCE COORDINATE &\_ o)**
</dt> <dd>

Crea una nuova istanza di una struttura CD3DX12 TILED RESOURCE COORDINATE, inizializzata con il contenuto di un'altra struttura \_ \_ \_ [**D3D12 \_ TILED \_ RESOURCE \_ COORDINATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)

</dd> <dt>

**CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**
</dt> <dd>

Crea una nuova istanza di un OGGETTO CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE, inizializzando i parametri seguenti:

UINT x

UINT y

UINT z

Sottorisorsa UINT

</dd> <dt>

**operator const D3D12 \_ TILED \_ RESOURCE COORDINATE \_&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COORDINATA DI RISORSA \_ AFFIANCATA D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





