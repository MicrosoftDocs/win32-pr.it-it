---
title: CD3DX12_HEAP_PROPERTIES (D3dx12.h)
description: Struttura helper per consentire un'inizializzazione semplice di una struttura PROPRIETÀ HEAP D3D12. \_ \_
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- CD3DX12_HEAP_PROPERTIES struttura
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
ms.openlocfilehash: 36a4d2241568d98957ecd809f33f27c343bb0e73d0d246284e5635f22a594108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752321"
---
# <a name="cd3dx12_heap_properties-structure"></a>Struttura DELLE PROPRIETÀ HEAP CD3DX12 \_ \_

Struttura helper per consentire un'inizializzazione semplice di una [**struttura PROPRIETÀ \_ HEAP \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

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

**PROPRIETÀ HEAP CD3DX12() \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un heap CD3DX12 \_ \_ PROPERTIES.

</dd> <dt>

**explicit CD3DX12 \_ HEAP \_ PROPERTIES(const D3D12 \_ HEAP PROPERTIES &\_ o)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 HEAP PROPERTIES, inizializzato con il contenuto di \_ \_ un'altra struttura [**D3D12 \_ HEAP \_ PROPERTIES.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

</dd> <dt>

**PROPRIETÀ HEAP \_ CD3DX12(D3D12 \_ CPU PAGE PROPERTY \_ \_ \_ cpuPageProperty, D3D12 \_ MEMORY POOL \_ memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**
</dt> <dd>

Crea una nuova istanza di un HEAP PROPERTIES CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(scelta esplicita) UINT creationNodeMask = 1

(scelta esplicita) UINT nodeMask = 1

</dd> <dt>

**explicit CD3DX12 \_ HEAP \_ PROPERTIES(D3D12 \_ HEAP TYPE \_ type, UINT creationNodeMask = 1, UINT nodeMask = 1)**
</dt> <dd>

Crea una nuova istanza di un HEAP PROPERTIES CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**D3D12 \_ Tipo \_ HEAP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(scelta esplicita) UINT creationNodeMask = 1

(scelta esplicita) UINT nodeMask = 1

</dd> <dt>

**Operatore const D3D12 \_ HEAP \_ PROPERTIES&() const**
</dt> <dd>

Definisce l& o operatore pass-by-reference per il tipo di struttura padre.

</dd> <dt>

**inline operator==( const D3D12 \_ HEAP \_ PROPERTIES& l, const D3D12 \_ HEAP PROPERTIES& r \_ )**
</dt> <dd>

Verifica l'uguaglianza tra le istanze di PROPRIETÀ HEAP D3D12 specificate, in base \_ \_ all'uguaglianza di tutti i campi membro.

</dd> <dt>

**inline operator!=( const D3D12 \_ HEAP \_ PROPERTIES& l, const D3D12 \_ HEAP PROPERTIES& r \_ )**
</dt> <dd>

Verifica la disuguaglianza tra le istanze di PROPRIETÀ HEAP D3D12 \_ \_ specificate. Implementato prendendo l'inverso del **valore operator==.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PROPRIETÀ HEAP D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





