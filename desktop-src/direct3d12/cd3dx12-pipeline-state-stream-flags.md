---
title: CD3DX12_PIPELINE_STATE_STREAM_FLAGS struttura (D3dx12.h)
description: Struttura helper usata per descrivere i flag di stato della pipeline come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8789fb8c393ecaf83e0295654092b22aba7f497abf909c46bac422d442c6fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530710"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>Struttura CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ FLAGS

Struttura helper usata per descrivere i flag di stato della pipeline come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**FLAG DI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di UN FLAG DI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12. \_ \_ \_ \_

</dd> <dt>

**FLAG DI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12(FLAG DI STATO DELLA \_ \_ PIPELINE \_ \_ D3D12 \_ \_ \_ const &i)**
</dt> <dd>

Crea una nuova istanza di UNA PIPELINE CD3DX12 STATE STREAM FLAGS, inizializzata con un tipo di oggetto secondario \_ \_ \_ \_ **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT TYPE \_ \_ FLAGS** e dati di sottooggetto copiati da i , una struttura [**D3D12 \_ PIPELINE STATE \_ \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)

</dd> <dt>

**operator=(D3D12 \_ PIPELINE STATE FLAGS \_ \_ const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ PIPELINE \_ STATE \_ FLAGS() const**
</dt> <dd>

Conversione implicita in [**una struttura D3D12 \_ PIPELINE STATE \_ \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM FLAGS è una specializzazione typedef del modello \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) ed è definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 

