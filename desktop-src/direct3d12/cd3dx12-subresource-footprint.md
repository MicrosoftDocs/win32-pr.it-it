---
title: CD3DX12_SUBRESOURCE_FOOTPRINT struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ SUBRESOURCE \_ FOOTPRINT.
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- CD3DX12_SUBRESOURCE_FOOTPRINT struttura
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32c3da3e133a5509543ffaa4fbf80b4c565730f13d3b9e92753658c96efcfcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069731"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>Struttura CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ SUBRESOURCE \_ FOOTPRINT.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT()**
</dt> <dd>

Crea una nuova istanza non inizializzata di cd3DX12 \_ SUBRESOURCE \_ FOOTPRINT.

</dd> <dt>

**EXPLICIT CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(const D3D12 \_ SUBRESOURCE \_ FOOTPRINT &o)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 SUBRESOURCE FOOTPRINT, inizializzata con il contenuto di un'altra struttura \_ \_ [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(formato DXGI, \_ larghezza UINT, altezza UINT, profondità UINT, UINT rowPitch)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT, inizializzando i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Larghezza UINT

Altezza UINT

Profondità UINT

UINT rowPitch

</dd> <dt>

**EXPLICIT CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(const D3D12 \_ RESOURCE \_ DESC& resDesc, UINT rowPitch)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT, inizializzando i parametri seguenti:

[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc

UINT rowPitch

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_ FOOTPRINT&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FOOTPRINT DELLE SOTTORISORSE D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

