---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_FLAGS (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere i flag di stato della pipeline come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_FLAGS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323580"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>\_ \_ \_ Struttura flag del flusso di stato della pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere i flag di stato della pipeline come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Flag di \_ flusso dello stato della pipeline \_ CD3DX12 \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ flag del flusso di stato della pipeline CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_Flag di \_ flusso dello stato della pipeline CD3DX12 \_ \_ (flag di \_ stato della pipeline D3D12 \_ \_ const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ flag di flusso di stato della pipeline CD3DX12 \_ \_ \_ , inizializzato con un tipo di sottooggetto dei flag del **\_ \_ \_ \_ tipo \_** di sottooggetto stato della pipeline D3D12 e i dati di sottooggetti copiati da *i*, una struttura di flag di [**\_ \_ stato \_ della pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .

</dd> <dt>

**operator = (D3D12 \_ pipeline \_ state \_ flags const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operator D3D12 \_ pipeline \_ flag di stato \_ () const**
</dt> <dd>

Conversione implicita in una struttura di [**\_ flag di \_ stato \_ della pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ I flag di flusso dello stato della pipeline CD3DX12 \_ sono una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) ed è definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 

