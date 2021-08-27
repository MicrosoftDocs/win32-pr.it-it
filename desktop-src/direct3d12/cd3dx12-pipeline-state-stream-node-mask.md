---
title: CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK struttura (D3dx12.h)
description: Struttura helper utilizzata per descrivere una maschera di nodo come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4850ff986f2006c506d79a8ece1ced873529c2a4939869cd704a4b7c3c4b03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119681"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>Struttura DELLA MASCHERA DEL NODO FLUSSO STATO PIPELINE CD3DX12 \_ \_ \_ \_ \_

Struttura helper utilizzata per descrivere una maschera di nodo come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**MASCHERA DEL NODO DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di una MASCHERA DEL NODO FLUSSO STATO PIPELINE CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**MASCHERA NODO FLUSSO STATO PIPELINE CD3DX12(UINT \_ \_ \_ \_ \_ const &i)**
</dt> <dd>

Crea una nuova istanza di UNA MASCHERA NODO FLUSSO STATO PIPELINE CD3DX12, inizializzata con un tipo di oggetto secondario \_ \_ \_ \_ \_ **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT TYPE NODE \_ \_ \_ MASK**   e dati di oggetto secondario copiati da i , una maschera del nodo UINT.

</dd> <dt>

**operator=(UINT const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore UINT() const**
</dt> <dd>

Conversione implicita in **una maschera di nodo UINT.**

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM NODE MASK è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT PIPELINE STATE STREAM CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
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

 

