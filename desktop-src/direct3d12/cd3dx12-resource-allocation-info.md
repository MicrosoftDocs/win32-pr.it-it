---
title: CD3DX12_RESOURCE_ALLOCATION_INFO struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO.
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- CD3DX12_RESOURCE_ALLOCATION_INFO struttura
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
ms.openlocfilehash: 63915f2fa05950ad96bc621b9887b1c4fe23149e22ba408767d111f7b74d6927
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729221"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>Struttura CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO

Struttura helper per consentire una facile inizializzazione di una [**struttura D3D12 \_ RESOURCE ALLOCATION \_ \_ INFO.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)

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

**INFORMAZIONI SULL'ALLOCAZIONE DELLE RISORSE CD3DX12() \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di UN'INFORMAZIONE DI ALLOCAZIONE RISORSE CD3DX12. \_ \_ \_

</dd> <dt>

**INFORMAZIONI esplicite sull'ALLOCAZIONE DELLE RISORSE \_ \_ \_ CD3DX12(const D3D12 \_ RESOURCE ALLOCATION INFO& \_ \_ o)**
</dt> <dd>

Crea una nuova istanza di una struttura CD3DX12 RESOURCE ALLOCATION INFO, inizializzata con il contenuto di un'altra struttura \_ \_ \_ [**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)

</dd> <dt>

**CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO(UINT64 size, UINT64 alignment)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO, inizializzando i parametri seguenti:

Dimensioni di UINT64

Allineamento UINT64

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ ALLOCATION INFO \_&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SULL'ALLOCAZIONE DELLE RISORSE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





