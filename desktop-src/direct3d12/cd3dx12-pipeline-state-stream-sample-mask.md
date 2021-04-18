---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una maschera di esempio come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323572"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a>\_Struttura della \_ \_ maschera di esempio del flusso di stato della \_ pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere una maschera di esempio come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Maschera di \_ esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ maschera di esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Maschera di esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ (uint const &i)**
</dt> <dd>

Crea una nuova istanza di una \_ maschera di esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzata con un tipo di sottooggetto del **tipo di \_ \_ \_ \_ \_ esempio \_ maschera di stato della pipeline D3D12** e dati di sottooggetti copiati da *i*, una maschera di esempio **uint** .

</dd> <dt>

**operator = (UINT const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore UINT () const**
</dt> <dd>

Conversione implicita in una maschera di esempio **uint** .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ La maschera di esempio del flusso di stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita nel modo seguente:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
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

 

