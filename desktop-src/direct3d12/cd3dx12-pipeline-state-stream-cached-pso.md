---
title: CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO struttura (D3dx12.h)
description: Struttura helper usata per descrivere un oggetto PSO memorizzato nella cache come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO struttura
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
ms.openlocfilehash: a11cb4e7a784b89a825f1e1b64083c50cc77731bbadf84d248106d69da9cf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751921"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>Struttura \_ \_ \_ \_ \_ PSO MEMORIZZATA NELLA CACHE DEL FLUSSO DELLO STATO DELLA PIPELINE CD3DX12

Struttura helper usata per descrivere un oggetto PSO memorizzato nella cache come singolo oggetto adatto per una descrizione del flusso.

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

**PSO MEMORIZZATO NELLA CACHE DEL FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un oggetto PSO CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ \_ CACHED.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ CACHED \_ PSO(D3D12 \_ CACHED PIPELINE STATE \_ \_ const &i)**
</dt> <dd>

Crea una nuova istanza di un oggetto PSO CD3DX12 PIPELINE STATE STREAM CACHED, inizializzato con un tipo di oggetto secondario \_ \_ \_ \_ \_ **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT TYPE \_ \_ CACHED \_ PSO** e dati di sottooggetto copiati da i , una struttura [**D3D12 \_ CACHED PIPELINE \_ \_ STATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)

</dd> <dt>

**operator=(D3D12 \_ CACHED \_ PIPELINE STATE \_ const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ CACHED \_ PIPELINE \_ STATE() const**
</dt> <dd>

Conversione implicita in [**una struttura D3D12 \_ CACHED PIPELINE \_ \_ STATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM CACHED PSO è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**SOTTOOGGETTO FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**TIPO DI SOTTOOGGETTO STATO PIPELINE D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

