---
title: CD3DX12_PACKED_MIP_INFO struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ PACKED \_ MIP \_ INFO.
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- CD3DX12_PACKED_MIP_INFO struttura
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
ms.openlocfilehash: b32a4b0516560ac553b3ce6acb6972def5d0e3f84a2eb84026a0635f779a2c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752161"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>Struttura CD3DX12 \_ PACKED \_ MIP \_ INFO

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ PACKED \_ MIP \_ INFO.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)

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

**CD3DX12 \_ PACKED \_ MIP \_ INFO()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un'informazione MIP CON PACCHETTO CD3DX12. \_ \_ \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ PACKED \_ MIP \_ INFO(const D3D12 \_ PACKED \_ MIP \_ INFO &o)**
</dt> <dd>

Crea una nuova istanza di una struttura CD3DX12 PACKED MIP INFO, inizializzata con il contenuto di un'altra struttura \_ \_ \_ [**D3D12 \_ PACKED \_ MIP \_ INFO.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)

</dd> <dt>

**CD3DX12 \_ PACKED \_ MIP \_ INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**
</dt> <dd>

Crea una nuova istanza di UN'INFORMAZIONE MIP PACCHETTO CD3DX12, \_ \_ \_ inizializzando i parametri seguenti:

UINT8 numStandardMips

UINT8 numPackedMips

UINT numTilesForPackedMips

UINT startTileIndexInOverallResource

</dd> <dt>

**operator const D3D12 \_ PACKED \_ MIP \_ INFO&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ PACKED \_ MIP \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





