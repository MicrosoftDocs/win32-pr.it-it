---
title: CD3DX12_RANGE_UINT64 struttura (D3dx12.h)
description: Struttura helper per consentire l'inizializzazione semplice di una struttura D3D12 \_ RANGE \_ UINT64.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- CD3DX12_RANGE_UINT64 struttura
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a07cb6a095c707b06b5b9982d29d73bb7bb9b6a32fca02233c50298a9804065a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098700"
---
# <a name="cd3dx12_range_uint64-structure"></a>Struttura CD3DX12 \_ RANGE \_ UINT64

Struttura helper per consentire l'inizializzazione semplice di [**una struttura D3D12 \_ RANGE \_ UINT64.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ RANGE \_ UINT64()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un OGGETTO CD3DX12 \_ RANGE \_ UINT64.

</dd> <dt>

**explicit CD3DX12 \_ RANGE \_ UINT64(const D3D12 \_ RANGE \_ UINT64 &o)**
</dt> <dd>

Crea una nuova istanza di un OGGETTO CD3DX12 RANGE UINT64, inizializzato con i valori copiati da una \_ \_ struttura [**D3D12 \_ RANGE \_ UINT64.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)

</dd> <dt>

**CD3DX12 \_ RANGE \_ UINT64(UINT64 begin, UINT64 end)**
</dt> <dd>

Crea una nuova istanza di UN STENCIL CD3DX12 \_ DEPTH \_ DESC1, inizializzata con i valori passati \_ nell'elenco di parametri.

</dd> <dt>

**Operatore const D3D12 \_ RANGE \_ UINT64&() const**
</dt> <dd>

Conversione implicita in una struttura D3D12 \_ RANGE \_ UINT64. Poiché D3D12 RANGE UINT64 è il tipo sottostante di CD3DX12 RANGE UINT64, l'oggetto viene semplicemente restituito come riferimento \_ \_ \_ \_ \_ UINT64 const D3D12 RANGE a se \_ stesso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ RANGE \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





