---
title: CD3DX12_PIPELINE_STATE_STREAM struttura (D3dx12.h)
description: Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata. Vedere D3D12 \_ GRAPHICS PIPELINE STATE DESC (STATO DELLA PIPELINE GRAFICA \_ \_ \_ D3D12) e D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC (STATO DELLA PIPELINE DI CALCOLO D3D12). | CD3DX12_PIPELINE_STATE_STREAM struttura (D3dx12.h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- CD3DX12_PIPELINE_STATE_STREAM struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e45c46c39a21aaeb53a2980fa3c082947e92cd5bb4ab3eccbbb225001a6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733983"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>Struttura DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_

Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata. Vedere [**D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC (STATO DELLA PIPELINE GRAFICA D3D12) e**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) [**D3D12 COMPUTE PIPELINE STATE \_ \_ \_ \_ DESC (STATO DELLA PIPELINE DI CALCOLO D3D12).**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)

CD3DX12 PIPELINE STATE STREAM supporta Windows 10 Creators Update e più recente, ma non supporta le nuove funzionalità di \_ \_ Fall Creators Update, ad esempio la creazione di istanze \_ di visualizzazione. Per supportare le funzionalità dell'aggiornamento di Fall Creators, usare [**INVECE CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1.**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a>Members

<dl> <dt>

**FLUSSO DI STATO DELLA PIPELINE CD3DX12() \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un FLUSSO DI STATO DELLA PIPELINE CD3DX12. \_ \_ \_

</dd> <dt>

**FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ (const D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC& Desc)**
</dt> <dd>

Crea una nuova istanza di un FLUSSO DI STATO DELLA PIPELINE CD3DX12, inizializzata con i valori copiati da una \_ \_ struttura \_ **CD3DX12 \_ PIPELINE STATE \_ \_ STREAM.**

</dd> <dt>

**FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ (const D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC& Desc)**
</dt> <dd>

Crea una nuova istanza di un FLUSSO DI STATO DELLA PIPELINE CD3DX12, inizializzata con i valori copiati da una \_ \_ struttura \_ **CD3DX12 \_ PIPELINE STATE \_ \_ STREAM.**

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

restituisce il contenuto dell'oggetto CD3DX12 PIPELINE STATE STREAM come struttura \_ \_ \_ DESC D3D12 \_ GRAPHICS PIPELINE STATE per \_ \_ \_ valore. Si noti che D3D12 GRAPHICS PIPELINE STATE DESC non include il membro CS, quindi questo \_ valore viene perso nella \_ \_ \_ conversione. 

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

restituisce il contenuto dell'oggetto CD3DX12 PIPELINE STATE STREAM come struttura \_ \_ \_ DESC D3D12 \_ COMPUTE PIPELINE STATE per \_ \_ \_ valore. Si noti che D3D12 COMPUTE PIPELINE STATE DESC non include i membri \_ \_ \_ \_ **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** o **SampleMask,** quindi questi valori vengono persi nella conversione.

</dd> <dt>

**Flag**
</dt> <dd>

Descrive i flag di stato della pipeline, che controllano funzionalità come "debug dello strumento".

</dd> <dt>

**Maschera di nodo**
</dt> <dd>

Descrive la maschera del nodo dello stato della pipeline, usata per identificare i nodi (schede fisiche del dispositivo) a cui si applica PSO negli scenari con più adattatori. ogni bit nella maschera corrisponde a un singolo nodo. Per gli scenari a scheda singola, impostare questo valore su 0.

</dd> <dt>

**pRootSignature**
</dt> <dd>

Descrive la firma radice.

</dd> <dt>

**InputLayout**
</dt> <dd>

Descrive il formato del buffer di input per la fase input-assembler

</dd> <dt>

**IBStripCutValue**
</dt> <dd>

Descrive il valore di indice speciale del buffer di input che indica un taglio (discontinuità) quando si usa la topologia a striscia triangolare.

</dd> <dt>

**PrimitiveTopologyType**
</dt> <dd>

Descrive la topologia primitiva e il relativo ordine.

</dd> <dt>

**Vs**
</dt> <dd>

Descrive il vertex shader.

</dd> <dt>

**GS**
</dt> <dd>

Descrive lo shader geometry.

</dd> <dt>

**StreamOutput**
</dt> <dd>

Descrive il buffer di output di streaming.

</dd> <dt>

**Hs**
</dt> <dd>

Descrive lo shader di tipo hull.

</dd> <dt>

**DS**
</dt> <dd>

Descrive lo shader del dominio.

</dd> <dt>

**Ps**
</dt> <dd>

Viene descritta la pixel shader.

</dd> <dt>

**CS**
</dt> <dd>

Descrive il compute shader.

</dd> <dt>

**BlendState**
</dt> <dd>

Descrive lo stato di blend.

</dd> <dt>

**DepthStencilState**
</dt> <dd>

Descrive lo stato dello stencil di profondità.

</dd> <dt>

**Formato DSV**
</dt> <dd>

Descrive il formato dello stencil di profondità.

</dd> <dt>

**Stato rasterizzazione**
</dt> <dd>

Descrive lo stato di rasterizzazione.

</dd> <dt>

**RTVFormats**
</dt> <dd>

Descrive i formati di destinazione di rendering.

</dd> <dt>

**SampleDesc**
</dt> <dd>

Descrive il numero e la qualità dei campioni.

</dd> <dt>

**Maschera di esempio**
</dt> <dd>

Descrive la maschera di esempio usata con lo stato di blend.

</dd> <dt>

**CachedPSO**
</dt> <dd>

Descrive un oggetto PSO memorizzato nella cache.

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 PIPELINE STATE STREAM supporta Windows 10 Creators Update e più recente, ma non supporta i tipi di oggetti secondari aggiunti \_ \_ in Windows 10 Fall Creators Update, ad esempio per le istanze di \_ visualizzazione. Per supportare i tipi di oggetto secondari aggiunti nell'aggiornamento di Fall Creators, usare [**INVECE CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1.**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**)

Le variabili membro accessibili di questa struttura sono tutti typedef del modello SUBOBJECT CD3DX12 PIPELINE STATE STREAM, che combina i dati del tipo di oggetto secondario e del sottooggetto in un singolo oggetto adatto per una descrizione del \_ \_ \_ \_ flusso.

I typedef sono:

<dl> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**FLUSSO STATO PIPELINE CD3DX121 \_ \_ \_**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





