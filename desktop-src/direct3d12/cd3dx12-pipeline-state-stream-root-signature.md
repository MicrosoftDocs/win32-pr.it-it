---
title: CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE struttura (D3dx12.h)
description: Struttura helper utilizzata per descrivere la firma radice come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccddd5663b6a079656823efed4cb48b3183d88d0688149c7ae05d96e8dc1cdd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530701"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>Struttura DELLA FIRMA RADICE DEL FLUSSO \_ \_ DI \_ STATO \_ DELLA PIPELINE CD3DX12 \_

Struttura helper utilizzata per descrivere la firma radice come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**FIRMA RADICE DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di una FIRMA RADICE FLUSSO STATO PIPELINE CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**FIRMA RADICE FLUSSO STATO \_ PIPELINE \_ \_ \_ \_ CD3DX12(ID3D12RootSignature \* const &i)**
</dt> <dd>

Crea una nuova istanza di UNA FIRMA RADICE FLUSSO STATO PIPELINE CD3DX12, inizializzata con un tipo di oggetto secondario D3D12 PIPELINE STATE SUBOBJECT TYPE ROOT SIGNATURE e i dati degli oggetti secondari copiati da i , una struttura \_ \_ \_ \_ \_ **\_ \_ \_ \_ \_ \_** [**ID3D12RootSignature.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) 

</dd> <dt>

**operator=(ID3D12RootSignature \* const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operator ID3D12RootSignature \* () const**
</dt> <dd>

Conversione implicita in un puntatore alla struttura [**ID3D12RootSignature.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM ROOT SIGNATURE è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
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

 

