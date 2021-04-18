---
title: Struttura CD3DX12_PACKED_MIP_INFO (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura di informazioni MIP compresso D3D12 \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Struttura CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322260"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>\_Struttura di \_ informazioni MIP compresso \_ CD3DX12

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ informazioni MIP compresso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ Informazioni MIP compresse CD3DX12 \_ ()**
</dt> <dd>

Crea un'istanza nuova, non inizializzata, di un CD3DX12 \_ di \_ informazioni MIP compresso \_ .

</dd> <dt>

**informazioni sul \_ MIP compresse CD3DX12 esplicite \_ \_ (const D3D12- \_ \_ informazioni MIP compresse \_ &o)**
</dt> <dd>

Crea una nuova istanza di un' \_ \_ informazione MIP compressa CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ \_ informazioni MIP compresso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

</dd> <dt>

**\_ \_ Informazioni MIP compresse CD3DX12 \_ (UINT8 NumStandardMips, Uint8 NumPackedMips, UINT NumTilesForPackedMips, uint startTileIndexInOverallResource)**
</dt> <dd>

Crea una nuova istanza di un CD3DX12 \_ di \_ dati MIP compresso \_ , inizializzando i parametri seguenti:

NumStandardMips UINT8

NumPackedMips UINT8

NumTilesForPackedMips UINT

StartTileIndexInOverallResource UINT

</dd> <dt>

**operator const D3D12 \_ compresse di \_ \_ informazioni& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ Informazioni MIP compresse \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





