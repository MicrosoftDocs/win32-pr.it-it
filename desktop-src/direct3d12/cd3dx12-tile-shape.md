---
title: Struttura CD3DX12_TILE_SHAPE (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura di forma del riquadro D3D12 \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Struttura CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322192"
---
# <a name="cd3dx12_tile_shape-structure"></a>\_ \_ Struttura forma sezione CD3DX12

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ forma del riquadro D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Forma riquadro CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ forma affiancata CD3DX12 \_ .

</dd> <dt>

**forma riquadro CD3DX12 esplicita \_ \_ (const D3D12 \_ forma affiancata \_ &o)**
</dt> <dd>

Crea una nuova istanza di una \_ forma affiancata CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura della [**\_ \_ forma affiancata D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

</dd> <dt>

**\_Forma riquadro CD3DX12 \_ (uint WIDTHINTEXELS, uint HEIGHTINTEXELS, uint depthInTexels)**
</dt> <dd>

Crea una nuova istanza di una \_ forma affiancata CD3DX12 \_ , inizializzando i parametri seguenti:

WidthInTexels UINT

HeightInTexels UINT

DepthInTexels UINT

</dd> <dt>

**operatore const \_ D3D12 \_ forma riquadro& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Forma riquadro \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





