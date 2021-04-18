---
title: Struttura CD3DX12_SUBRESOURCE_RANGE_UINT64 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura della SOTTORISORSA D3D12 \_ \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Struttura CD3DX12_SUBRESOURCE_RANGE_UINT64
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
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322199"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>\_ \_ Struttura UInt64 della SOTTOrisorsa CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura della [**\_ sottorisorsa \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

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

**CD3DX12 \_ intervallo di sottorisorse \_ \_ UInt64 ()**
</dt> <dd>

Crea un'istanza nuova, non inizializzata, di un \_ intervallo di SOTTORISORSA CD3DX12 \_ \_ UInt64.

</dd> <dt>

**intervallo di \_ SOTTORISORSA CD3DX12 esplicito \_ \_ UInt64 (const D3D12 \_ subresource \_ Range \_ UInt64 &o)**
</dt> <dd>

Crea una nuova istanza di un \_ intervallo della SOTTORISORSA CD3DX12 \_ \_ , inizializzato con i valori copiati da una struttura di un [**intervallo di \_ sottorisorse di D3D12 \_ \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

</dd> <dt>

**Intervallo \_ di SOTTORISORSE CD3DX12 \_ \_ UInt64 (uint subresource, const D3D12 \_ Range \_ UInt64& Range)**
</dt> <dd>

Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzata con i valori passati nell'elenco di parametri.

</dd> <dt>

**\_Intervallo della SOTTORISORSA CD3DX12 \_ \_ UInt64 (uint subresource, UINT64 Begin, UInt64 end)**
</dt> <dd>

Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzata con i valori passati nell'elenco di parametri.

</dd> <dt>

**operator const D3D12- \_ intervallo di sottorisorse \_ \_ UInt64& () const**
</dt> <dd>

Conversione implicita in una \_ struttura di intervallo di SOTTORISORSE D3D12 \_ \_ . Poiché l' \_ intervallo della SOTTORISORSA D3D12 \_ \_ UInt64 è il tipo sottostante dell' \_ intervallo della sottorisorsa CD3DX12 \_ \_ UInt64, l'oggetto viene semplicemente restituito come un riferimento const D3D12 \_ Depth \_ stencil \_ DESC1 a se stesso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ intervallo di sottorisorse \_ \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





