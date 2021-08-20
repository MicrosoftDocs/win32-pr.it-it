---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL struttura (D3dx12.h)
description: Struttura helper usata per descrivere una descrizione depth stencil come singolo oggetto adatto per una descrizione del flusso. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL struttura (D3dx12.h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0b9cc7ba6b37858ae355d9470f321f991e8329f5fbf7aabd23b6f8bcfe7d8fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858181"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>Struttura DELLO STENCIL CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ DEPTH \_

Struttura helper usata per descrivere una descrizione depth stencil come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**STENCIL PROFONDITÀ FLUSSO STATO PIPELINE CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di uno STENCIL CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ \_ DEPTH.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH STENCIL \_ \_ \_ \_ (CD3DX12 \_ DEPTH STENCIL \_ \_ DESC const &i)**
</dt> <dd>

Crea una nuova istanza di UNO STENCIL DI PROFONDITÀ FLUSSO DELLO STATO DELLA PIPELINE CD3DX12, inizializzata con un tipo di oggetto secondario D3D12 PIPELINE STATE SUBOBJECT TYPE DEPTH STENCIL e dati di sottooggetto copiati da \_ i , una struttura \_ \_ \_ \_ [**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC.**](cd3dx12-depth-stencil-desc.md) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**Operatore CD3DX12 \_ DEPTH \_ STENCIL \_ DESC() const**
</dt> <dd>

Conversione implicita in [**una struttura CD3DX12 \_ DEPTH STENCIL \_ \_ DESC.**](cd3dx12-depth-stencil-desc.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 

