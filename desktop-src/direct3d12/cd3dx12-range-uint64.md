---
title: Struttura CD3DX12_RANGE_UINT64 (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una struttura D3D12 dell' \_ intervallo \_ UInt64.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Struttura CD3DX12_RANGE_UINT64
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
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323571"
---
# <a name="cd3dx12_range_uint64-structure"></a>Struttura CD3DX12 dell' \_ intervallo \_ UInt64

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura [**D3D12 dell' \_ intervallo \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

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

**\_Intervallo CD3DX12 \_ UInt64 ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ intervallo CD3DX12 \_ UInt64.

</dd> <dt>

**intervallo CD3DX12 esplicito \_ \_ UInt64 (const D3D12 \_ Range \_ UInt64 &o)**
</dt> <dd>

Crea una nuova istanza di un intervallo di CD3DX12 \_ \_ UInt64, inizializzato con i valori copiati da un [**\_ intervallo D3D12 \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) struttura.

</dd> <dt>

**CD3DX12 \_ Range \_ UINT64 (UInt64 Begin, UInt64 end)**
</dt> <dd>

Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzata con i valori passati nell'elenco di parametri.

</dd> <dt>

**operatore const D3D12 \_ Range \_ UInt64& () const**
</dt> <dd>

Conversione implicita in una \_ struttura D3D12 dell'intervallo \_ UInt64. Poiché l' \_ intervallo \_ di D3D12 UInt64 è il tipo sottostante dell'intervallo di CD3DX12 \_ \_ UInt64, l'oggetto viene semplicemente restituito come \_ riferimento a un intervallo const D3D12 \_ a se stesso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Intervallo D3D12 \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





