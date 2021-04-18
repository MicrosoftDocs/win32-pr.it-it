---
title: Struttura CD3DX12_SUBRESOURCE_TILING (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura di affiancamento della SOTTORISORSA D3D12 \_ .
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Struttura CD3DX12_SUBRESOURCE_TILING
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322198"
---
# <a name="cd3dx12_subresource_tiling-structure"></a>\_Struttura di affiancamento di SOTTORISORSE CD3DX12 \_

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ affiancamento della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Affiancamento di SOTTORISORSE CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ affiancamento della SOTTORISORSA CD3DX12 \_ .

</dd> <dt>

**\_affiancamento della SOTTORISORSA CD3DX12 esplicita \_ (const D3D12 \_ \_ &o)**
</dt> <dd>

Crea una nuova istanza di un \_ affiancamento della SOTTORISORSA CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ affiancamento della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

</dd> <dt>

**CD3DX12 \_ subresource \_ affiancamento (uint WIDTHINTILES, UInt16 HEIGHTINTILES, UInt16 DEPTHINTILES, uint startTileIndexInOverallResource)**
</dt> <dd>

Crea una nuova istanza di un \_ affiancamento della SOTTORISORSA CD3DX12 \_ , inizializzando i parametri seguenti:

WidthInTiles UINT

UINT16 heightInTiles

UINT16 depthInTiles

StartTileIndexInOverallResource UINT

</dd> <dt>

**operatore const D3D12 \_ sottorisorse \_& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Affiancamento di SOTTORISORSE D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





