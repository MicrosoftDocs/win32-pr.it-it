---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12. h)
description: Struttura helper utilizzata per descrivere un oggetto PSO memorizzato nella cache come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322262"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>\_ \_ \_ \_ Struttura PSO memorizzato nella cache del flusso di stato della pipeline CD3DX12 \_

Struttura helper utilizzata per descrivere un oggetto PSO memorizzato nella cache come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ \_ \_ PSO memorizzato nella cache del flusso di stato della pipeline CD3DX12 \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ memorizzato nella cache di un oggetto \_ PSO.

</dd> <dt>

**CD3DX12 della \_ pipeline del flusso di stato della pipeline \_ \_ \_ \_ (D3D12 della \_ pipeline memorizzato nella cache \_ \_ const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ memorizzato nella cache di un oggetto \_ \_ \_ PSO, inizializzato con un tipo di SOTTOoggetto del **tipo di \_ \_ oggetto sottooggetto stato della pipeline D3D12 \_ \_ \_ memorizzato nella cache \_ PSO** e dati di oggetti suboggetto copiati da *i*, una struttura di [**\_ \_ \_ stato della pipeline D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)

</dd> <dt>

**operator = ( \_ stato della pipeline D3D12 memorizzato nella cache \_ \_ const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ memorizzato nella cache- \_ stato della pipeline \_ () const**
</dt> <dd>

Conversione implicita in una struttura di [**\_ stato della \_ pipeline \_ D3D12 memorizzata nella cache**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ L'oggetto PSO memorizzato nella cache del flusso di stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

