---
title: CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT struttura (D3dx12.h)
description: Struttura helper usata per descrivere un layout di input come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d467d60444588001a115f9b1ad3667f35fc9edab69a64402f42b4885d70a86d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912960"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>Struttura DEL LAYOUT DI INPUT DEL FLUSSO \_ \_ DI \_ STATO \_ DELLA PIPELINE CD3DX12 \_

Struttura helper usata per descrivere un layout di input come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**LAYOUT DI \_ \_ \_ \_ \_ INPUT DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12**
</dt> <dd>

Crea una nuova istanza non inizializzata di un LAYOUT DI INPUT DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**LAYOUT DI INPUT FLUSSO DI STATO DELLA \_ PIPELINE \_ \_ \_ \_ CD3DX12 (LAYOUT DI INPUT D3D12 \_ \_ \_ DESC &i)**
</dt> <dd>

Crea una nuova istanza di un LAYOUT INPUT FLUSSO STATO PIPELINE CD3DX12, inizializzato con un tipo di oggetto secondario D3D12 PIPELINE STATE SUBOBJECT TYPE INPUT LAYOUT e dati di oggetto secondario copiati da i , una struttura \_ \_ \_ \_ \_ [**\_ \_ \_ DESC INPUT LAYOUT D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(D3D12 \_ INPUT \_ LAYOUT \_ DESC const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore D3D12 \_ INPUT \_ LAYOUT \_ DESC() const**
</dt> <dd>

Conversione implicita in [**una struttura D3D12 \_ INPUT LAYOUT \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM INPUT LAYOUT è una specializzazione typedef del modello \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

 

