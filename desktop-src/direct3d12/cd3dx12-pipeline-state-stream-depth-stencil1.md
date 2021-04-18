---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione depth stencil come singolo oggetto adatto per la descrizione di un flusso. | Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322245"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>\_ \_ \_ \_ Struttura STENCIL1 della profondità del flusso dello stato della pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere una descrizione depth stencil come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Profondità flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ STENCIL1.

</dd> <dt>

**CD3DX12 \_ - \_ profondità flusso di stato della pipeline \_ \_ \_ STENCIL1 (CD3DX12 \_ Depth \_ stencil \_ DESC1 const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ STENCIL1, inizializzata con un tipo di oggetto suboggetto di **D3D12 la profondità del tipo di \_ \_ sottooggetto stato della pipeline \_ \_ \_ \_ STENCIL1** e dati di sottooggetti copiati da *i*, una struttura CD3DX12 [**\_ Depth \_ stencil \_ DESC1**](cd3dx12-depth-stencil-desc1.md) .

</dd> <dt>

**operator = (CD3DX12 \_ Depth \_ stencil \_ DESC1 const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore CD3DX12 \_ Depth \_ stencil \_ DESC1 () const**
</dt> <dd>

Conversione implicita in una struttura [**DESC1 di CD3DX12 \_ Depth \_ stencil \_**](cd3dx12-depth-stencil-desc1.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ La profondità del flusso di stato della pipeline CD3DX12 \_ STENCIL1 è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
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

 

