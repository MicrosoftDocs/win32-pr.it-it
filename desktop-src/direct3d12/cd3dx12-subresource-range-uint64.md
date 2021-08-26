---
title: CD3DX12_SUBRESOURCE_RANGE_UINT64 struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64.
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- CD3DX12_SUBRESOURCE_RANGE_UINT64 struttura
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df38d5b2e7a4230d023aeba6c8c3517fbd2b9f4e35a09b5e4439269b228eb82e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987991"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>Struttura CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ SUBRESOURCE RANGE \_ \_ UINT64.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un OGGETTO CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64.

</dd> <dt>

**EXPLICIT CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64(const D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64 &o)**
</dt> <dd>

Crea una nuova istanza di un OGGETTO CD3DX12 SUBRESOURCE RANGE UINT64, inizializzato con i valori copiati da una struttura \_ \_ \_ [**\_ \_ \_ UINT64 D3D12 SUBRESOURCE RANGE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64(UINT subresource, const D3D12 \_ RANGE \_ UINT64& range)**
</dt> <dd>

Crea una nuova istanza di un OGGETTO CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1, inizializzato con i valori passati nell'elenco di parametri.

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64(UINT subresource, UINT64 begin, UINT64 end)**
</dt> <dd>

Crea una nuova istanza di un OGGETTO CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1, inizializzato con i valori passati nell'elenco di parametri.

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64&() const**
</dt> <dd>

Conversione implicita in una struttura \_ \_ UINT64 D3D12 SUBRESOURCE \_ RANGE. Poiché D3D12 SUBRESOURCE RANGE UINT64 è il tipo sottostante \_ \_ di CD3DX12 SUBRESOURCE RANGE UINT64, l'oggetto viene semplicemente restituito come riferimento \_ \_ \_ \_ CONST D3D12 \_ DEPTH STENCIL \_ \_ DESC1 a se stesso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





