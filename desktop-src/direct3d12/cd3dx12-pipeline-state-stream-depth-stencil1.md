---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 struttura (D3dx12.h)
description: Struttura helper usata per descrivere una descrizione depth stencil come singolo oggetto adatto per una descrizione del flusso. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 struttura (D3dx12.h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 struttura
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
ms.openlocfilehash: 3f04064a7ab4a7ca100e48da2446501d4415b693ce6abdf213f121952cc8f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632530"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>Struttura CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1

Struttura helper usata per descrivere una descrizione depth stencil come singolo oggetto adatto per una descrizione del flusso.

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

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL1**
</dt> <dd>

Crea una nuova istanza non inizializzata di un OGGETTO CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1(CD3DX12 \_ DEPTH STENCIL \_ \_ DESC1 const &i)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL1, inizializzato con un tipo di oggetto secondario \_ D3D12 PIPELINE STATE SUBOBJECT TYPE DEPTH1 e dati di sottooggetto copiati da i , una \_ \_ struttura \_ \_ [**CD3DX12 \_ DEPTH STENCIL \_ \_ DESC1.**](cd3dx12-depth-stencil-desc1.md) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1 const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**Operatore CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1() const**
</dt> <dd>

Conversione implicita in [**una struttura CD3DX12 \_ DEPTH STENCIL \_ \_ DESC1.**](cd3dx12-depth-stencil-desc1.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL1 è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
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

 

