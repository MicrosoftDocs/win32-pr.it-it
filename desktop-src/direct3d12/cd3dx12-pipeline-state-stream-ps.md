---
title: CD3DX12_PIPELINE_STATE_STREAM_PS struttura (D3dx12.h)
description: Struttura helper usata per descrivere un pixel shader come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: A71E2ABE-5B52-41B4-ACE0-25CA63EF2565
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PS struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a3ea2393482f09b233cd7bb8a404cc55ed39588a44ba334fd85e11d3bfb16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734023"
---
# <a name="cd3dx12_pipeline_state_stream_ps-structure"></a>Struttura PS FLUSSO STATO PIPELINE CD3DX12 \_ \_ \_ \_

Struttura helper usata per descrivere un pixel shader come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PS {
                                   CD3DX12_PIPELINE_STATE_STREAM_PS;
                                   CD3DX12_PIPELINE_STATE_STREAM_PS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**PS FLUSSO STATO PIPELINE CD3DX12 \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un FLUSSO DI STATO DELLA PIPELINE CD3DX12. \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ PS(D3D12 \_ SHADER \_ BYTECODE const &i)**
</dt> <dd>

Crea una nuova istanza di UN FLUSSO DI STATO DELLA PIPELINE CD3DX12, inizializzata con un tipo di oggetto secondario D3D12 PIPELINE STATE SUBOBJECT TYPE PS e dati di oggetto secondario copiati da i , una struttura \_ \_ \_ \_ [**\_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) **\_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(D3D12 \_ SHADER \_ BYTECODE const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**Operatore D3D12 \_ SHADER \_ BYTECODE() const**
</dt> <dd>

Conversione implicita in [**una struttura \_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM PS è una specializzazione typedef del modello \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PS>
    CD3DX12_PIPELINE_STATE_STREAM_PS;
          
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

 

