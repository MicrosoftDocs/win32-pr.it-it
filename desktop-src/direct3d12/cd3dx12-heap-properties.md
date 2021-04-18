---
title: Struttura CD3DX12_HEAP_PROPERTIES (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura delle proprietà dell'heap D3D12 \_ .
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Struttura CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322261"
---
# <a name="cd3dx12_heap_properties-structure"></a>Struttura delle proprietà dell' \_ heap CD3DX12 \_

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura delle [**\_ \_ proprietà dell'heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Proprietà heap CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ proprietà dell'heap CD3DX12 \_ .

</dd> <dt>

**Proprietà heap CD3DX12 esplicite \_ \_ (proprietà dell'heap const D3D12 \_ \_ &o)**
</dt> <dd>

Crea una nuova istanza di una \_ proprietà dell'heap CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ proprietà dell'heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

</dd> <dt>

**\_Proprietà heap CD3DX12 \_ ( \_ Proprietà pagina CPU D3D12 \_ \_ CPUPAGEPROPERTY, \_ pool di memoria D3D12 \_ MEMORYPOOLPREFERENCE, uint creationNodeMask = 1, uint node mask = 1)**
</dt> <dd>

Crea una nuova istanza di una \_ proprietà dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ \_ \_ Proprietà della pagina CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference \_ pool di memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

consenso esplicito UINT creationNodeMask = 1

consenso esplicito UINT node mask = 1

</dd> <dt>

**Proprietà heap CD3DX12 esplicite \_ \_ ( \_ \_ tipo di heap D3D12, uint CREATIONNODEMASK = 1, uint node mask = 1)**
</dt> <dd>

Crea una nuova istanza di una \_ proprietà dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ Tipo \_ di heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

consenso esplicito UINT creationNodeMask = 1

consenso esplicito UINT node mask = 1

</dd> <dt>

**operator const \_ D3D12 \_ proprietà heap& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> <dt>

**operatore inline = = (proprietà dell'heap const D3D12 \_ \_& l, proprietà dell'heap const D3D12 \_ \_& r)**
</dt> <dd>

Verifica l'uguaglianza tra le \_ istanze delle proprietà dell'heap D3D12 specificate \_ , in base all'uguaglianza dei campi di tutti i membri.

</dd> <dt>

**operatore inline! = (const D3D12 \_ heap \_ Properties& l, const D3D12 \_ heap \_ Properties& r)**
</dt> <dd>

Verifica la disuguaglianza tra le istanze delle proprietà dell'heap D3D12 specificate \_ \_ . Implementato utilizzando l'inverso del valore **operator = =** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Proprietà heap \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





