---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione di esempio come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323576"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a>\_ \_ \_ \_ Struttura desc di esempio del flusso di stato della pipeline CD3DX12 \_

Struttura di supporto utilizzata per descrivere una descrizione di esempio come singolo oggetto adatto per la descrizione di un flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ DESC**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ desc.

</dd> <dt>

**\_Esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ DESC ( \_ esempio DXGI \_ desc const &i)**
</dt> <dd>

Crea una nuova istanza di un \_ esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ DESC, inizializzato con un tipo di sottooggetto di **esempio di tipo di \_ \_ \_ oggetto sottooggetto stato della pipeline D3D12 \_ \_ \_ desc** e dati di sottooggetti copiati da *i*, una struttura di [**\_ esempio \_ desc DXGI**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .

</dd> <dt>

**operator = ( \_ esempio DXGI \_ desc const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore DXGI \_ Sample \_ DESC () const**
</dt> <dd>

Conversione implicita in una struttura [**\_ \_ desc di esempio DXGI**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ Esempio di flusso di stato della pipeline CD3DX12 \_ \_ DESC è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
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

 

