---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT struttura (D3dx12.h)
description: Struttura helper utilizzata per descrivere il formato depth stencil come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT struttura
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
ms.openlocfilehash: 9658f1df1fbe316fa9f308b9f8e0589f0f93858916c6dbde4607fd11a6f0707f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751951"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a>Struttura IN FORMATO \_ \_ \_ \_ \_ STENCIL \_ PROFONDITÀ FLUSSO STATO PIPELINE CD3DX12

Struttura helper utilizzata per descrivere il formato depth stencil come singolo oggetto adatto per una descrizione del flusso.

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

**\_ \_ \_ FORMATO \_ \_ STENCIL \_ PROFONDITÀ FLUSSO STATO PIPELINE CD3DX12**
</dt> <dd>

Crea una nuova istanza non inizializzata di un formato STENCIL PROFONDITÀ FLUSSO STATO PIPELINE CD3DX12. \_ \_ \_ \_ \_ \_

</dd> <dt>

**FORMATO STENCIL PROFONDITÀ FLUSSO STATO PIPELINE CD3DX12 \_ \_ \_ \_ \_ \_ (FORMATO DXGI \_ const &i)**
</dt> <dd>

Crea una nuova istanza di UN FORMATO STENCIL PROFONDITÀ FLUSSO STATO PIPELINE CD3DX12, inizializzata con un tipo di oggetto secondario \_ \_ \_ \_ \_ \_ **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT TYPE DEPTH STENCIL \_ \_ \_ \_ FORMAT**  [**\_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) e dati degli oggetti secondari copiati da i , un'enumerazione DXGI FORMAT.

</dd> <dt>

**operator=(DXGI \_ FORMAT const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore DXGI \_ FORMAT() const**
</dt> <dd>

Conversione implicita in [**un'enumerazione DXGI \_ FORMAT.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL FORMAT è una specializzazione typedef del modello \_ \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
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

 

