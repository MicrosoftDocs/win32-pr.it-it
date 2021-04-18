---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione depth stencil come singolo oggetto adatto per la descrizione di un flusso. | Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
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
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322252"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>\_ \_ \_ \_ Struttura stencil profondità flusso dello stato della pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere una descrizione depth stencil come singolo oggetto adatto per la descrizione di un flusso.

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

**\_ \_ \_ \_ Stencil profondità flusso dello stato della pipeline CD3DX12 \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di uno \_ stencil di profondità del \_ flusso dello stato della pipeline CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_ \_ Stencil profondità flusso di stato della pipeline CD3DX12 \_ \_ \_ (CD3DX12 \_ Depth \_ stencil \_ desc const &i)**
</dt> <dd>

Crea una nuova istanza di uno \_ stencil di \_ profondità del flusso dello stato della pipeline CD3DX12 \_ \_ \_ , inizializzato con un tipo di sottooggetto dello stencil di profondità del tipo di sottooggetto **\_ \_ dello stato \_ \_ \_ \_** della pipeline D3D12 e dati di sottooggetti copiati da i, una struttura di [**\_ \_ stencil \_ depth di CD3DX12**](cd3dx12-depth-stencil-desc.md) .

</dd> <dt>

**operator = (CD3DX12 \_ Depth \_ stencil \_ DESC const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore CD3DX12 \_ Depth \_ stencil \_ DESC () const**
</dt> <dd>

Conversione implicita in una struttura [**CD3DX12 \_ Depth \_ stencil \_ desc**](cd3dx12-depth-stencil-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ Lo \_ stencil profondità flusso dello stato della pipeline CD3DX12 \_ \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 

