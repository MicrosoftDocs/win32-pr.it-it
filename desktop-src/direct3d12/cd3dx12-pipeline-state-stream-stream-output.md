---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere la descrizione dell'output del flusso come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322224"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>\_Struttura di \_ \_ output del \_ flusso di stato della pipeline \_ CD3DX12

Struttura di supporto utilizzata per descrivere la descrizione dell'output del flusso come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ \_ \_ \_ Output flusso flusso di stato della pipeline CD3DX12**
</dt> <dd>

Crea una nuova istanza non inizializzata di un output del flusso del flusso di \_ stato della pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**Output del flusso di \_ \_ flusso dello stato della pipeline CD3DX12 \_ (output del flusso \_ \_ D3D12 \_ \_ \_ desc const &i)**
</dt> <dd>

Crea una nuova istanza di un output del flusso di flusso di \_ stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzato con un tipo di sottooggetto di output del flusso di **\_ tipo di oggetto di \_ \_ \_ tipo \_ \_ pipeline D3D12** e dati di sottooggetti copiati da *i*, una struttura di [**\_ \_ output \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) del flusso di D3D12.

</dd> <dt>

**operator = ( \_ output flusso \_ D3D12 \_ DESC const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ Stream \_ output \_ DESC () const**
</dt> <dd>

Conversione implicita in una struttura [**\_ desc di \_ output \_ del flusso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ L'output del flusso di flusso dello stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

