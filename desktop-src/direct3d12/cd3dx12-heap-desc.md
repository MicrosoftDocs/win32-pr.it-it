---
title: Struttura CD3DX12_HEAP_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura desc dell'heap D3D12 \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Struttura CD3DX12_HEAP_DESC
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
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322263"
---
# <a name="cd3dx12_heap_desc-structure"></a>\_Struttura desc dell'heap CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ desc dell'heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

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

**CD3DX12 \_ heap \_ DESC ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ Descrizione dell'heap CD3DX12 \_ .

</dd> <dt>

**heap CD3DX12 esplicito \_ \_ DESC (const D3D12 \_ heap \_ desc &o)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ desc dell'heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (dimensione UInt64, proprietà \_ heap D3D12 \_ proprietà, allineamento UInt64 = 0, flag \_ flag heap D3D12 \_ = D3D12 \_ \_ flag heap \_ nessuno)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:

Dimensioni UINT64

[**D3D12 \_ Proprietà \_ heap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) proprietà

consenso esplicito Allineamento UINT64 = 0

consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (dimensione UInt64, \_ \_ tipo di tipo heap D3D12, allineamento UInt64 = 0, \_ flag \_ flag heap D3D12 = \_ D3D12 \_ flag heap \_ nessuno)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:

Dimensioni UINT64

[**D3D12 \_ Tipo \_ di heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

consenso esplicito Allineamento UINT64 = 0

consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (dimensione UInt64, \_ \_ Proprietà pagina CPU D3D12 \_ cpuPageProperty, D3D12 \_ \_ pool di memoria MEMORYPOOLPREFERENCE, allineamento UInt64 = 0, D3D12 \_ flag heap flag \_ = D3D12 \_ heap flag \_ \_ None)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:

Dimensioni UINT64

[**D3D12 \_ \_ \_ Proprietà della pagina CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference \_ pool di memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

consenso esplicito Allineamento UINT64 = 0

consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 \_ heap \_ Properties Properties, D3D12 \_ heap Flags Flags \_ = D3D12 \_ Heap heap \_ \_ None)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ \_ \_ Informazioni sull'allocazione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Proprietà \_ heap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) proprietà

consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 tipo \_ \_ di heap, D3D12 heap flag Flags \_ \_ = D3D12 \_ Heap heap \_ \_ None)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ \_ \_ Informazioni sull'allocazione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Tipo \_ di heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ Resource \_ allocation \_ info& ResAllocInfo, D3D12 \_ \_ pagina CPU \_ CPUPAGEPROPERTY, D3D12 \_ pool di memoria memoryPoolPreference \_ , D3D12 \_ heap flag Flags \_ = D3D12 \_ heap \_ flag \_ None)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ \_ \_ Informazioni sull'allocazione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ \_ \_ Proprietà della pagina CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference \_ pool di memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None

</dd> <dt>

**operator const D3D12 \_ heap \_ desc& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il \_ tipo di \_ struttura desc dell'heap CD3DX12.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ heap \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





