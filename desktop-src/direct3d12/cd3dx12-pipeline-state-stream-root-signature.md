---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere la firma radice come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
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
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323578"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>\_Struttura della \_ \_ \_ firma radice del flusso di stato della pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere la firma radice come singolo oggetto adatto per la descrizione di un flusso.

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

**\_ \_ \_ Firma radice del flusso dello stato \_ della pipeline \_ CD3DX12**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ firma radice del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Firma radice del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ (ID3D12RootSignature \* const &i)**
</dt> <dd>

Crea una nuova istanza di una \_ firma radice del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzata con un tipo di sottooggetto della **\_ \_ \_ \_ \_ \_ firma radice del tipo** di sottooggetto di stato della pipeline D3D12 e i dati di sottooggetti copiati da *i*, una struttura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> <dt>

**operator = (ID3D12RootSignature \* const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore ID3D12RootSignature \* () const**
</dt> <dd>

Conversione implicita in un puntatore alla struttura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ \_ La firma radice del flusso di stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
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

 

