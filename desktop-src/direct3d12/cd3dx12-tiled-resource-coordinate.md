---
title: Struttura CD3DX12_TILED_RESOURCE_COORDINATE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura di coordinate delle risorse affiancate D3D12 \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Struttura CD3DX12_TILED_RESOURCE_COORDINATE
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
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322186"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>\_ \_ Struttura delle coordinate delle risorse CD3DX12 affiancata \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ coordinate delle risorse affiancate D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

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

**\_Coordinata di risorsa affiancata CD3DX12 \_ \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ \_ coordinata di risorsa CD3DX12 affiancata \_ .

</dd> <dt>

**\_coordinata della risorsa affiancata CD3DX12 esplicita \_ \_ (const D3D12 di \_ risorse affiancate \_ \_ &o)**
</dt> <dd>

Crea una nuova istanza di una \_ \_ coordinata di risorsa CD3DX12 affiancata \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ \_ coordinate della risorsa affiancata D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

</dd> <dt>

**\_Coordinata di risorsa affiancata CD3DX12 \_ \_ (UINT x, UINT y, UINT z, uint subresource)**
</dt> <dd>

Crea una nuova istanza di una \_ \_ coordinata di risorsa CD3DX12 affiancata \_ , inizializzando i parametri seguenti:

UINT x

UINT y

UINT z

Sottorisorsa UINT

</dd> <dt>

**operatore const \_ D3D12 \_ \_ coordinata delle risorse& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Coordinata risorse D3D12 affiancata \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





