---
title: CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT struttura (D3dx12.h)
description: Struttura helper usata per descrivere la descrizione dell'output del flusso come singolo oggetto adatto a una descrizione del flusso.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT struttura
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
ms.openlocfilehash: 5c0dbaf9952575801846adfbbb825c2ddbdc2e90d9d8d64f60f373ea2bcc1be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119671"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>Struttura OUTPUT FLUSSO FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_

Struttura helper usata per descrivere la descrizione dell'output del flusso come singolo oggetto adatto a una descrizione del flusso.

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

**OUTPUT DEL FLUSSO DI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un OUTPUT FLUSSO DI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**OUTPUT DEL FLUSSO DI FLUSSO DELLO STATO DELLA \_ PIPELINE \_ \_ \_ \_ CD3DX12(D3D12 \_ STREAM OUTPUT \_ \_ DESC const &i)**
</dt> <dd>

Crea una nuova istanza di UN OUTPUT STREAM STREAM DELLO STATO DELLA PIPELINE CD3DX12, inizializzata con un tipo di oggetto secondario D3D12 PIPELINE STATE SUBOBJECT TYPE STREAM OUTPUT e dati di sottooggetto copiati da i , una struttura \_ \_ \_ \_ \_  [**\_ \_ \_ DESC D3D12 STREAM OUTPUT.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) **\_ \_ \_ \_ \_ \_**

</dd> <dt>

**operator=(D3D12 \_ STREAM \_ OUTPUT \_ DESC const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ STREAM \_ OUTPUT \_ DESC() const**
</dt> <dd>

Conversione implicita in [**una struttura \_ DESC STREAM OUTPUT \_ D3D12. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM OUTPUT è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

