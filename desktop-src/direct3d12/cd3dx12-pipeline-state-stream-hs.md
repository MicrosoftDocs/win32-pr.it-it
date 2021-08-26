---
title: CD3DX12_PIPELINE_STATE_STREAM_HS struttura (D3dx12.h)
description: Struttura helper usata per descrivere uno hull shader come un singolo oggetto adatto per una descrizione del flusso.
ms.assetid: 4958161D-3E79-4227-ADD7-7F53E34B2175
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_HS struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_HS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b13c32c9da13a3cfce03605494bc8608a233f5979cb7b2757f203571c7901
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028361"
---
# <a name="cd3dx12_pipeline_state_stream_hs-structure"></a>Struttura \_ \_ \_ \_ HS FLUSSO STATO PIPELINE CD3DX12

Struttura helper usata per descrivere uno hull shader come un singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_HS {
                                   CD3DX12_PIPELINE_STATE_STREAM_HS;
                                   CD3DX12_PIPELINE_STATE_STREAM_HS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_HS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**HS FLUSSO STATO PIPELINE CD3DX12 \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un flusso HS FLUSSO STATO PIPELINE CD3DX12. \_ \_ \_ \_

</dd> <dt>

**HS FLUSSO STATO \_ PIPELINE \_ \_ \_ CD3DX12 (D3D12 \_ SHADER \_ BYTECODE const &i)**
</dt> <dd>

Crea una nuova istanza di HS FLUSSO STATO PIPELINE CD3DX12, inizializzata con un tipo di oggetto secondario \_ \_ \_ \_ **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT TYPE \_ \_ HS** e dati di oggetto secondari copiati da i , una struttura [**\_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> <dt>

**operator=(D3D12 \_ SHADER \_ BYTECODE const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**Operatore D3D12 \_ SHADER \_ BYTECODE() const**
</dt> <dd>

Conversione implicita in [**una struttura \_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM HS è una specializzazione typedef del modello \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT PIPELINE STATE STREAM CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_HS>
    CD3DX12_PIPELINE_STATE_STREAM_HS;
          
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

 

