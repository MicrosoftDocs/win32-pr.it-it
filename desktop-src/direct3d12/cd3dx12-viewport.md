---
title: CD3DX12_VIEWPORT struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura VIEWPORT D3D12. \_
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- CD3DX12_VIEWPORT struttura
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dce5a009dba6b047b599772586db60a022f4c62126a6d58575166b5ca2bec5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808273"
---
# <a name="cd3dx12_viewport-structure"></a>Struttura VIEWPORT CD3DX12 \_

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Struttura helper per consentire una facile inizializzazione di [**una struttura \_ VIEWPORT D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ VIEWPORT()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un VIEWPORT CD3DX12. \_

</dd> <dt>

**VIEWPORT CD3DX12 \_ esplicito(const D3D12 \_ VIEWPORT& o)**
</dt> <dd>

Crea una nuova istanza di un VIEWPORT CD3DX12, \_ inizializzando i parametri seguenti:

const D3D12 \_ VIEWPORT& o

</dd> <dt>

**VIEWPORT ESPLICITO CD3DX12(FLOAT \_ topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12 \_ MIN \_ DEPTH, FLOAT maxDepth = D3D12 \_ MAX \_ DEPTH)**
</dt> <dd>

Crea una nuova istanza di un VIEWPORT CD3DX12, \_ inizializzando i parametri seguenti:

FLOAT topLeftX

FLOAT topLeftY

Larghezza FLOAT

Altezza FLOAT

FLOAT minDepth = D3D12 \_ MIN \_ DEPTH

FLOAT maxDepth = D3D12 \_ MAX \_ DEPTH

</dd> <dt>

**VIEWPORT ESPLICITO \_ CD3DX12(ID3D12Resource \* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0,0f, FLOAT topLeftY = 0,0f, FLOAT minDepth = D3D12 \_ MIN \_ DEPTH, FLOAT maxDepth = D3D12 \_ MAX \_ DEPTH)**
</dt> <dd>

Crea una nuova istanza di un VIEWPORT CD3DX12, \_ inizializzando i parametri seguenti:

ID3D12Resource \* pResource

UINT mipSlice = 0

FLOAT topLeftX = 0,0f

FLOAT topLeftY = 0,0f

FLOAT minDepth = D3D12 \_ MIN \_ DEPTH

FLOAT maxDepth = D3D12 \_ MAX \_ DEPTH

</dd> <dt>

**~CD3DX12 \_ VIEWPORT()**
</dt> <dd>

Elimina un'istanza di un VIEWPORT D3DX12. \_

</dd> <dt>

**operator const D3D12 \_ VIEWPORT&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





