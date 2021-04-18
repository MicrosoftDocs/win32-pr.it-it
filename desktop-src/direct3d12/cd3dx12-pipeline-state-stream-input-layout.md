---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere un layout di input come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322239"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>\_Struttura di \_ \_ layout di input del flusso di stato della \_ pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere un layout di input come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Layout di \_ input del flusso di stato della pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ layout di input del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Layout di input del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ ( \_ layout input D3D12 \_ \_ desc const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ layout di input del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzata con un tipo di oggetto suboggetto di un **\_ \_ \_ \_ \_ \_ layout di input del tipo** di sottooggetto D3D12 di stato della pipeline e i dati di sottooggetti copiati da *i*, una struttura di [**\_ \_ layout \_ di input D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> <dt>

**operator = ( \_ layout input \_ D3D12 \_ DESC const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ input \_ layout \_ DESC () const**
</dt> <dd>

Conversione implicita in una struttura [**\_ \_ \_ desc di layout input D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ \_ Il layout di input del flusso di stato della pipeline CD3DX12 è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

 

