---
title: Struttura CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura di informazioni sull'allocazione delle risorse D3D12 \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Struttura CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322216"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>\_Struttura delle \_ informazioni di allocazione delle risorse CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ informazioni sull'allocazione delle risorse D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Informazioni sull' \_ allocazione delle risorse CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ risorsa di allocazione delle risorse CD3DX12 \_ \_ .

</dd> <dt>

**informazioni sull' \_ allocazione delle risorse CD3DX12 esplicite \_ \_ (const D3D12 \_ Resource \_ allocation \_& o)**
</dt> <dd>

Crea una nuova istanza di un' \_ informazione di \_ allocazione delle risorse CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ \_ informazioni sull'allocazione delle risorse D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

</dd> <dt>

**\_Informazioni sull' \_ allocazione delle risorse CD3DX12 \_ (dimensione UINT64, allineamento UInt64)**
</dt> <dd>

Crea una nuova istanza di una \_ risorsa di \_ allocazione delle risorse CD3DX12 \_ , inizializzando i parametri seguenti:

Dimensioni UINT64

Allineamento UINT64

</dd> <dt>

**operatore const D3D12 \_ Resource \_ allocation \_& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Informazioni sull' \_ allocazione delle risorse D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





