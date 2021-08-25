---
title: CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC struttura (D3dx12.h)
description: Struttura helper usata per descrivere una descrizione di blend come un singolo oggetto adatto per una descrizione del flusso.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300506d2c41be5a5380f4f0f64c93779185fd59ced2e0dd613d926f8397ea85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752171"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>Struttura \_ \_ \_ \_ \_ DESC DI BLEND DI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12

Struttura helper usata per descrivere una descrizione di blend come un singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ BLEND \_ DESC**
</dt> <dd>

Crea una nuova istanza non inizializzata di una PIPELINE CD3DX12 \_ \_ STATE STREAM BLEND \_ \_ \_ DESC.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC(CD3DX12 \_ BLEND \_ DESC const &i)**
</dt> <dd>

Crea una nuova istanza di UNA PIPELINE CD3DX12 PIPELINE STATE STREAM BLEND DESC, inizializzata con un tipo di oggetto secondario D3D12 PIPELINE STATE SUBOBJECT TYPE BLEND e dati di sottooggetto copiati da \_ i , una struttura \_ \_ \_ \_ [**CD3DX12 \_ BLEND \_ DESC.**](cd3dx12-blend-desc.md) **\_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ BLEND \_ DESC const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**Operatore CD3DX12 \_ BLEND \_ DESC() const**
</dt> <dd>

Conversione implicita in [**una struttura CD3DX12 \_ BLEND \_ DESC.**](cd3dx12-blend-desc.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM BLEND DESC è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

