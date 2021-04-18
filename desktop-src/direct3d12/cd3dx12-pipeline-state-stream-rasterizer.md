---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione del rasterizzatore come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322225"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a>\_Struttura del \_ \_ rasterizzatore del flusso di stato della pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere una descrizione del rasterizzatore come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ \_ Rasterizzatore del flusso di stato della pipeline CD3DX12 \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ rasterizzatore del flusso di stato della pipeline CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_ \_ Rasterizzazione flusso di stato della pipeline CD3DX12 \_ \_ (CD3DX12 \_ rasterizzatore \_ desc const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ rasterizzatore del flusso di stato della pipeline CD3DX12 \_ \_ \_ , inizializzato con un tipo di sottooggetto di **\_ \_ \_ \_ \_ rasterizzatore del tipo di sottooggetto dello stato della pipeline D3D12** e dati di oggetti suboggetto copiati da *i*, una struttura [**\_ \_ desc di rasterizzazione CD3DX12**](cd3dx12-rasterizer-desc.md) .

</dd> <dt>

**operator = (CD3DX12 \_ rasterizzator \_ desc const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore CD3DX12 \_ rasterizzatore \_ DESC () const**
</dt> <dd>

Conversione implicita in una struttura [**\_ \_ Desc del rasterizzatore CD3DX12**](cd3dx12-rasterizer-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ Il rasterizzatore del flusso di stato della pipeline CD3DX12 è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
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

 

