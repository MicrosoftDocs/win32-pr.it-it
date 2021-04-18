---
title: Struttura CD3DX12_TEXTURE_COPY_LOCATION (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura del percorso di copia della trama D3D12 \_ \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Struttura CD3DX12_TEXTURE_COPY_LOCATION
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
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322197"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>\_Struttura del \_ percorso della copia di trama CD3DX12 \_

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura del [**\_ percorso di \_ Copia \_ della trama D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

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

**\_ \_ Percorso copia trama CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ percorso di copia della trama CD3DX12 \_ \_ .

</dd> <dt>

**\_percorso copia trama CD3DX12 esplicita \_ \_ (const D3D12 \_ texture \_ copy \_ location &o)**
</dt> <dd>

Crea una nuova istanza di un \_ percorso di copia di trama CD3DX12 \_ \_ , inizializzato con il contenuto di un'altra struttura del percorso di [**\_ copia della trama \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

</dd> <dt>

**\_ \_ Posizione copia trama CD3DX12 \_ (ID3D12Resource \* pRes)**
</dt> <dd>

Crea una nuova istanza di un \_ percorso di copia di trama CD3DX12 \_ \_ , inizializzando i parametri seguenti:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

</dd> <dt>

**\_Posizione della \_ copia di trama CD3DX12 \_ (ID3D12RESOURCE \* pRes, D3D12 \_ posto \_ footprint delle risorse subresource \_& footprint)**
</dt> <dd>

Crea una nuova istanza di un \_ percorso di copia di trama CD3DX12 \_ \_ , inizializzando i parametri seguenti:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

[**D3D12 \_ \_ \_ Footprint delle risorse SOTTOrisorse posizionate**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)& footprint

</dd> <dt>

**\_ \_ Percorso copia trama CD3DX12 \_ (ID3D12RESOURCE \* pRes, uint Sub)**
</dt> <dd>

Crea una nuova istanza di un \_ percorso di copia di trama CD3DX12 \_ \_ , inizializzando i parametri seguenti:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

Sub UINT

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ Percorso copia trama \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





