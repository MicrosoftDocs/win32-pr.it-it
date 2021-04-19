---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere i formati della destinazione di rendering come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322223"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a>\_Struttura del \_ \_ formato di \_ destinazione di rendering del flusso di \_ stato della pipeline \_ CD3DX12

Struttura di supporto utilizzata per descrivere i formati della destinazione di rendering come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Formati di \_ \_ destinazione di rendering del flusso di stato \_ della \_ pipeline CD3DX12 \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ flusso di destinazione di rendering del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ \_ .

</dd> <dt>

**\_Formati di destinazione per il rendering del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ \_ (D3D12 \_ RT \_ Format \_ Array Const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ flusso di destinazione di rendering del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ \_ , inizializzata con un tipo di sottooggetto di tipi di destinazione di rendering dei tipi di oggetto sottooggetto di **\_ stato della pipeline \_ \_ \_ \_ \_ \_ D3D12** e dati di sottooggetti copiati da i, una struttura di [**\_ \_ \_ matrice di formato D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)

</dd> <dt>

**operator = (D3D12 \_ RT \_ Format \_ ARRAY const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ RT \_ Format \_ Array () const**
</dt> <dd>

Conversione implicita in una struttura di [**\_ matrici di \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ \_ I formati di destinazione per il rendering del flusso di stato della pipeline CD3DX12 \_ sono una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) ed è definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
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

 

