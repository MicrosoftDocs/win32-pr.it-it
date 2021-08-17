---
title: CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY struttura (D3dx12.h)
description: Struttura helper utilizzata per descrivere la topologia primitiva come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a828ef50956d9ab5336dfe88fa12bed9f7541633ec4589a9c556511e8487a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734263"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>Struttura DELLA TOPOLOGIA PRIMITIVA DEL FLUSSO \_ \_ DI STATO \_ \_ DELLA \_ PIPELINE CD3DX12

Struttura helper utilizzata per descrivere la topologia primitiva come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**TOPOLOGIA PRIMITIVA DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di una TOPOLOGIA PRIMITIVA FLUSSO DI STATO PIPELINE CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**TOPOLOGIA PRIMITIVA FLUSSO DI STATO DELLA \_ PIPELINE \_ \_ \_ \_ CD3DX12 (TIPO DI TOPOLOGIA PRIMITIVA D3D12 \_ &\_ \_ i)**
</dt> <dd>

Crea una nuova istanza di una TOPOLOGIA PRIMITIVA FLUSSO STATO PIPELINE CD3DX12, inizializzata con un tipo di oggetto secondario \_ \_ \_ \_ \_ **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT TYPE \_ \_ PRIMITIVE \_ TOPOLOGY** e dati di oggetti secondari copiati da i , una struttura [**D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)

</dd> <dt>

**operator=(D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE() const**
</dt> <dd>

Conversione implicita in [**una struttura D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM PRIMITIVE TOPOLOGY è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT PIPELINE STATE STREAM CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**OGGETTO SECONDARIO FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**TIPO DI OGGETTO SECONDARIO STATO PIPELINE D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

