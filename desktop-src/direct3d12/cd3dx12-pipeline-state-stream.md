---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
description: Struttura di supporto per la creazione e l'utilizzo degli Stati della pipeline di calcolo e di grafica tramite un'interfaccia combinata. Vedere D3D12 \_ Graphics \_ pipeline \_ state \_ DESC e D3D12 \_ Compute \_ pipeline \_ state \_ desc. | Struttura CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM
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
ms.openlocfilehash: 8d52b9090fa1d3870027bbe360164627472c039e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322220"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>\_Struttura del \_ flusso di stato della pipeline CD3DX12 \_

Struttura di supporto per la creazione e l'utilizzo degli Stati della pipeline di calcolo e di grafica tramite un'interfaccia combinata. Vedere [**D3D12 \_ Graphics \_ pipeline \_ state \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12 \_ Compute \_ pipeline \_ state \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

\_ \_ \_ Il flusso di stato della pipeline CD3DX12 supporta Windows 10 Creators Update e versioni successive, ma non supporta le nuove funzionalità di Fall Creators Update, ad esempio Visualizza istanze. Per supportare le funzionalità dell'aggiornamento Fall Creators, usare invece [**\_ lo stato della pipeline CD3DX12 \_ \_ stream1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .

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

**\_Flusso di stato della pipeline CD3DX12 \_ \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ flusso di stato della pipeline CD3DX12 \_ \_ .

</dd> <dt>

**\_Flusso di stato della pipeline CD3DX12 \_ \_ (const D3D12 \_ GRAPHICS \_ pipeline \_ state \_ desc& DESC)**
</dt> <dd>

Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ \_ , inizializzata con i valori copiati da una struttura del flusso di **\_ stato della pipeline \_ \_ CD3DX12** .

</dd> <dt>

**\_Flusso di stato della pipeline CD3DX12 \_ \_ (const D3D12 \_ compute \_ \_ state pipeline \_ desc& DESC)**
</dt> <dd>

Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ \_ , inizializzata con i valori copiati da una struttura del flusso di **\_ stato della pipeline \_ \_ CD3DX12** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

Restituisce il contenuto dell' \_ oggetto flusso di stato della pipeline CD3DX12 \_ \_ come \_ \_ struttura di stato della pipeline grafica D3D12 \_ \_ per valore. Si noti che \_ lo \_ stato della pipeline grafica D3D12 \_ \_ DESC non include il membro **CS** , quindi questo valore viene perso nella conversione.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

Restituisce il contenuto dell' \_ oggetto flusso di stato della pipeline CD3DX12 \_ \_ come \_ \_ \_ struttura desc di stato della pipeline di calcolo D3D12 \_ per valore. Si noti che \_ \_ \_ la descrizione dello stato della pipeline di calcolo D3D12 \_ non include i membri **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** o **SampleMask** , quindi questi valori vengono persi nella conversione.

</dd> <dt>

**Flag**
</dt> <dd>

Vengono descritti i flag di stato della pipeline, che controllano le funzionalità di, ad esempio "strumento Debug".

</dd> <dt>

**Node mask**
</dt> <dd>

Viene descritta la maschera del nodo dello stato della pipeline, che consente di identificare i nodi (schede fisiche del dispositivo) a cui si applica il PSO negli scenari con più adapter. ogni bit nella maschera corrisponde a un singolo nodo. Per gli scenari a singolo adattatore, impostare questo valore su 0.

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

Descrive il valore di indice speciale del buffer di input che indica una riduzione (discontinuità) quando si utilizza la topologia a strisce triangolare.

</dd> <dt>

**PrimitiveTopologyType**
</dt> <dd>

Descrive la topologia primitiva e il relativo ordine.

</dd> <dt>

**VS**
</dt> <dd>

Descrive il vertex shader.

</dd> <dt>

**GS**
</dt> <dd>

Descrive il geometry shader.

</dd> <dt>

**StreamOutput**
</dt> <dd>

Descrive il buffer di output del flusso.

</dd> <dt>

**HS**
</dt> <dd>

Descrive Hull shader.

</dd> <dt>

**DS**
</dt> <dd>

Descrive il Domain shader.

</dd> <dt>

**PS**
</dt> <dd>

Descrive il pixel shader.

</dd> <dt>

**CS**
</dt> <dd>

Descrive il compute shader.

</dd> <dt>

**BlendState**
</dt> <dd>

Descrive lo stato di Blend.

</dd> <dt>

**DepthStencilState**
</dt> <dd>

Descrive lo stato di stencil Depth.

</dd> <dt>

**DSVFormat**
</dt> <dd>

Descrive il formato di stencil Depth.

</dd> <dt>

**RasterizerState**
</dt> <dd>

Descrive lo stato di rasterizzazione.

</dd> <dt>

**RTVFormats**
</dt> <dd>

Descrive i formati della destinazione di rendering.

</dd> <dt>

**SampleDesc**
</dt> <dd>

Descrive il numero di campioni e la qualità.

</dd> <dt>

**SampleMask**
</dt> <dd>

Viene descritta la maschera di esempio utilizzata con lo stato Blend.

</dd> <dt>

**CachedPSO**
</dt> <dd>

Descrive un oggetto PSO memorizzato nella cache.

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ \_ Il flusso di stato della pipeline CD3DX12 supporta Windows 10 Creators Update e versioni successive, ma non supporta i tipi di sottooggetti aggiunti in Windows 10 Fall Creators Update, ad esempio per le istanze di visualizzazione. Per supportare i tipi di sottooggetti aggiunti nell'aggiornamento Fall Creators, usare [**invece \_ \_ lo stato \_ della pipeline CD3DX12 stream1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .

Le variabili membro accessibili di questa struttura sono tutti typedef del \_ \_ modello di sottooggetto flusso di stato della pipeline CD3DX12 \_ \_ , che combina i dati del marcatore del tipo di sottooggetto e i dati di sottooggetto in un singolo oggetto adatto per la descrizione di un flusso.

Questi typedef sono:

<dl> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_ \_ Stream1 stato pipeline \_ CD3DX12**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**\_ \_ \_ Descrizione dello stato della pipeline grafica D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**\_ \_ Desc stato della pipeline di calcolo \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





