---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione di Blend come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
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
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322258"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>\_ \_ \_ \_ Struttura Desc del flusso di stato della pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere una descrizione di Blend come singolo oggetto adatto per la descrizione di un flusso.

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

**CD3DX12 \_ di \_ \_ Blend del flusso di stato \_ della pipeline \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di una CD3DX12 della \_ pipeline di \_ flusso dello stato della pipeline \_ \_ \_ .

</dd> <dt>

**CD3DX12 \_ pipeline \_ state \_ Stream \_ Blend \_ DESC (CD3DX12 \_ Blend \_ desc const &i)**
</dt> <dd>

Crea una nuova istanza di una CD3DX12 \_ della pipeline di \_ flusso dello stato della pipeline \_ \_ \_ , inizializzata con un tipo di sottooggetto di Blend di tipo di **oggetto di stato della \_ pipeline \_ \_ \_ \_ D3D12** e i dati di sottooggetti copiati da *i*, una struttura di [**CD3DX12 \_ Blend \_ desc**](cd3dx12-blend-desc.md) .

</dd> <dt>

**operator = (CD3DX12 \_ Blend \_ desc deconst& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore CD3DX12 \_ Blend \_ DESC () const**
</dt> <dd>

Conversione implicita in una struttura [**\_ \_ desc di CD3DX12 Blend**](cd3dx12-blend-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_La funzione \_ di flusso di stato della pipeline CD3DX12 \_ \_ \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita nel modo seguente:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

