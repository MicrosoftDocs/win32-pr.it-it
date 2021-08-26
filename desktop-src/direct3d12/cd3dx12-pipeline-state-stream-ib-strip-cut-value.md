---
title: CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE struttura (D3dx12.h)
description: Struttura helper usata per descrivere il valore index buffer strip cut come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE struttura
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
ms.openlocfilehash: 1e204b4f89cced7cf0bd5cdcb21702c37c241a81abfbc12d8644eafdb3c7c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988411"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>Struttura CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ IB STRIP CUT \_ \_ \_ VALUE

Struttura helper usata per descrivere il valore index buffer strip cut come singolo oggetto adatto per una descrizione del flusso.

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

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ IB \_ STRIP \_ CUT \_ VALUE**
</dt> <dd>

Crea una nuova istanza non inizializzata di un VALORE CUT IB STRIP STREAM DI PIPELINE CD3DX12. \_ \_ \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ IB STRIP CUT \_ \_ \_ VALUE(D3D12 \_ INDEX BUFFER STRIP CUT VALUE \_ \_ \_ \_ const &i)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 PIPELINE STATE STREAM IB STRIP CUT VALUE, inizializzato con un tipo di oggetto secondario \_ \_ \_ \_ \_ \_ \_ **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT TYPE \_ \_ IB STRIP CUT \_ \_ \_ VALUE** e i dati del sottooggetto copiati da i , una struttura [**D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)

</dd> <dt>

**operator=(D3D12 \_ INDEX BUFFER STRIP CUT VALUE \_ \_ \_ \_ const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE() const**
</dt> <dd>

Conversione implicita in [**una struttura D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM IB STRIP CUT VALUE è una specializzazione typedef del modello \_ \_ \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

 

