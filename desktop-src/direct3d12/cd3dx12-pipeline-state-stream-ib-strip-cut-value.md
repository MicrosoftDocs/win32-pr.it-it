---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere il valore Cut Strip buffer index come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322240"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>\_Struttura del \_ \_ \_ \_ \_ \_ valore del flusso di stato della pipeline CD3DX12

Struttura di supporto utilizzata per descrivere il valore Cut Strip buffer index come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Valore di \_ \_ \_ \_ Strip \_ Cut \_ del flusso di stato della pipeline CD3DX12**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ \_ valore di \_ \_ Strip Cut del flusso di stato della \_ \_ pipeline CD3DX12 \_ .

</dd> <dt>

**Valore di strip \_ Cut del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ \_ \_ (D3D12 \_ index \_ buffer \_ \_ Cut \_ value const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ valore di \_ Strip Cut del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ \_ , inizializzato con un tipo di sottooggetto del tipo di sottooggetto **dello stato della pipeline D3D12 del \_ \_ \_ \_ tipo \_ IB \_ Strip \_ \_ cut** e dei dati degli oggetti suboggetto copiati da *i*, una struttura del [**\_ \_ \_ \_ \_ valore Cut Strip buffer D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> <dt>

**operator = (D3D12 \_ index \_ buffer \_ Strip \_ CUT \_ value const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ index \_ buffer \_ \_ Cut \_ value () const**
</dt> <dd>

Conversione implicita in una struttura del [**\_ \_ \_ \_ \_ valore Cut Strip buffer index D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ \_ \_ \_ Il valore di strip Cut del flusso di stato della pipeline CD3DX12 è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

 

