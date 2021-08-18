---
title: CD3DX12_PIPELINE_STATE_STREAM_VS struttura (D3dx12.h)
description: Struttura helper usata per descrivere un vertex shader come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_VS struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4361cf50a97cd3d7bf2abc6995182e9ca24bad6b824505408aca98bd4b3ead42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045729"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a>Struttura VS FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_

Struttura helper usata per descrivere un vertex shader come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CONFRONTO TRA FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un flusso DI STATO DELLA PIPELINE CD3DX12. \_ \_ \_ \_

</dd> <dt>

**FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ VS(D3D12 \_ SHADER \_ BYTECODE const &i)**
</dt> <dd>

Crea una nuova istanza di un oggetto VS CD3DX12 PIPELINE STATE STREAM, inizializzato con un tipo di oggetto secondario D3D12 PIPELINE STATE SUBOBJECT TYPE VS e dati di sottooggetto copiati da i , una struttura \_ \_ \_ \_ [**\_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) **\_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(D3D12 \_ SHADER \_ BYTECODE const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ SHADER \_ BYTECODE() const**
</dt> <dd>

Conversione implicita in [**una struttura \_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM VS è una specializzazione typedef del modello \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
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

 

