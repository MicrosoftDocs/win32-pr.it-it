---
title: CD3DX12_TEXTURE_COPY_LOCATION struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ TEXTURE \_ COPY \_ LOCATION.
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- CD3DX12_TEXTURE_COPY_LOCATION struttura
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d0a1ee179d2400bc04df9c3214d97d3c7a861357f33b7805e492a24f769bdba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119641"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>Struttura CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ TEXTURE COPY \_ \_ LOCATION.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION()**
</dt> <dd>

Crea una nuova istanza non inizializzata di UN PERCORSO DI COPIA TEXTURE CD3DX12. \_ \_ \_

</dd> <dt>

**explicit CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION(const D3D12 \_ TEXTURE COPY LOCATION &\_ \_ o)**
</dt> <dd>

Crea una nuova istanza di una struttura CD3DX12 TEXTURE COPY LOCATION, inizializzata con il contenuto di un'altra struttura \_ \_ \_ [**D3D12 \_ TEXTURE \_ COPY \_ LOCATION.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)

</dd> <dt>

**CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION(ID3D12Resource \* pRes)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION, inizializzando i parametri seguenti:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Pres

</dd> <dt>

**CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION(ID3D12Resource \* pRes, D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT const& Footprint)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION, inizializzando i parametri seguenti:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Pres

[**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint

</dd> <dt>

**CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION(ID3D12Resource \* pRes, UINT Sub)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION, inizializzando i parametri seguenti:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Pres

UINT Sub

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PERCORSO COPIA TRAMA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





