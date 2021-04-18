---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere la topologia primitiva come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
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
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322236"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>\_Struttura della \_ \_ \_ \_ topologia del flusso di stato della pipeline CD3DX12

Struttura di supporto utilizzata per descrivere la topologia primitiva come singolo oggetto adatto per la descrizione di un flusso.

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

**\_ \_ \_ Topologia del flusso \_ di stato della pipeline CD3DX12 \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ \_ \_ \_ topologia primitiva del flusso di stato della pipeline CD3DX12 \_ .

</dd> <dt>

**\_Topologia del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ ( \_ tipo di topologia primitiva D3D12 \_ \_ const &i)**
</dt> <dd>

Crea una nuova istanza di una \_ \_ topologia primitiva del flusso di stato della pipeline CD3DX12 \_ \_ \_ , inizializzata con un tipo di sottooggetto della **\_ \_ \_ \_ \_ \_ topologia primitiva del tipo della pipeline D3D12** e dei dati di sottooggetti copiati da *i*, una struttura del [**\_ \_ \_ tipo di topologia primitiva D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> <dt>

**operator = ( \_ tipo di \_ topologia primitiva D3D12 \_ const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ primitive \_ tipo di topologia \_ () const**
</dt> <dd>

Conversione implicita in una struttura di [**\_ \_ \_ tipo topologia primitiva di D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ \_ La topologia primitiva del flusso di stato della pipeline CD3DX12 è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) ed è definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

