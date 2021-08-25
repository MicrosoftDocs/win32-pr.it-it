---
title: CD3DX12_HEAP_DESC struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura DESC HEAP D3D12. \_ \_
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- CD3DX12_HEAP_DESC struttura
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347e44a8516b48dcd779d3ac19fbc9b5bbf5d37ad565f36a0b9b10a083d395c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858371"
---
# <a name="cd3dx12_heap_desc-structure"></a>Struttura \_ DESC HEAP CD3DX12 \_

Struttura helper per consentire una facile inizializzazione di [**una struttura \_ \_ DESC HEAP D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ HEAP \_ DESC()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un DESC HEAP CD3DX12. \_ \_

</dd> <dt>

**DESC heap CD3DX12 \_ \_ esplicito(const D3D12 \_ HEAP \_ DESC &o)**
</dt> <dd>

Crea una nuova istanza di un DESC HEAP CD3DX12, inizializzata con il contenuto di un'altra struttura \_ \_ [**\_ \_ DESC HEAP D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(dimensioni UINT64, proprietà PROPRIETÀ HEAP D3D12, \_ allineamento \_ UINT64 = 0, flag FLAG HEAP D3D12 \_ = FLAG HEAP \_ D3D12 \_ \_ \_ NONE)**
</dt> <dd>

Crea una nuova istanza di un DESC HEAP CD3DX12, \_ \_ inizializzando i parametri seguenti:

Dimensioni di UINT64

[**D3D12 \_ Proprietà \_ HEAP PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

(opt) Allineamento UINT64 = 0

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(dimensioni UINT64, tipo HEAP D3D12, \_ allineamento \_ UINT64 = 0, flag FLAG HEAP D3D12 \_ = FLAG HEAP \_ D3D12 \_ \_ \_ NONE)**
</dt> <dd>

Crea una nuova istanza di un DESC HEAP CD3DX12, \_ \_ inizializzando i parametri seguenti:

Dimensioni di UINT64

[**D3D12 \_ Tipo \_ DI HEAP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) Allineamento UINT64 = 0

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(UINT64 size, D3D12 \_ CPU \_ PAGE \_ PROPERTY cpuPageProperty, D3D12 \_ MEMORY \_ POOL memoryPoolPreference, UINT64 alignment = 0, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nuova istanza di un DESC HEAP CD3DX12, \_ \_ inizializzando i parametri seguenti:

Dimensioni di UINT64

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) Allineamento UINT64 = 0

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ HEAP \_ PROPERTIES properties, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nuova istanza di un DESC HEAP CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Proprietà \_ HEAP PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ HEAP \_ TYPE type, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nuova istanza di un DESC HEAP CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Tipo \_ DI HEAP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ CPU \_ PAGE \_ PROPERTY cpuPageProperty, D3D12 \_ MEMORY \_ POOL memoryPoolPreference, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nuova istanza di un DESC HEAP CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**operator const D3D12 \_ HEAP \_ DESC&() const**
</dt> <dd>

Definisce l& operatore pass-by-reference per il tipo di struttura CD3DX12 \_ HEAP \_ DESC.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ HEAP \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





