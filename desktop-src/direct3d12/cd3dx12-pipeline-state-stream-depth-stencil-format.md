---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere il formato depth stencil come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322256"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a>\_ \_ \_ \_ \_ Struttura formato stencil profondità flusso dello stato della pipeline \_ CD3DX12

Struttura di supporto utilizzata per descrivere il formato depth stencil come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ \_ \_ \_ Formato stencil profondità flusso dello stato della pipeline \_ CD3DX12**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ \_ formato dello stencil di profondità del flusso dello stato della pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ Formato stencil profondità flusso dello stato della pipeline CD3DX12 \_ \_ \_ \_ ( \_ formato DXGI const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ formato dello stencil di profondità del flusso dello stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzato con un tipo di sottooggetto del formato dello stencil di profondità del tipo di sottooggetto **stato della \_ pipeline \_ \_ \_ \_ \_ \_ D3D12** e dati di sottooggetti copiati da i, un'enumerazione di [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> <dt>

**operator = ( \_ formato DXGI const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore DXGI \_ Format () const**
</dt> <dd>

Conversione implicita in un'enumerazione del [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ Il formato dello stencil di profondità del flusso dello stato della pipeline CD3DX12 \_ \_ \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
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

 

