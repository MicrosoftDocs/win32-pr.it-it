---
title: CD3DX12_PIPELINE_STATE_STREAM1 struttura (D3dx12.h)
description: Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata. Vedere [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- CD3DX12_PIPELINE_STATE_STREAM1 struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219b198ae5c2da6d6e74db933d4c26771aa63975
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812532"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a>CD3DX12_PIPELINE_STATE_STREAM1 struttura

Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata. Vedere [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

CD3DX12_PIPELINE_STATE_STREAM1 supporta l'Windows 10 Fall Creators Update con nuove funzionalità, ad esempio la creazione di istanze di visualizzazione.

Vedere [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream2.md) per il supporto per la build del sistema operativo 19041+ (in cui è presente una pipeline mesh shader).

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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

**CD3DX12_PIPELINE_STATE_STREAM1()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un CD3DX12_PIPELINE_STATE_STREAM1.

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc)**
</dt> <dd>

Crea una nuova istanza di un CD3DX12_PIPELINE_STATE_STREAM1, inizializzata con i valori copiati da una **CD3DX12_PIPELINE_STATE_STREAM1** struttura .

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc)**
</dt> <dd>

Crea una nuova istanza di un CD3DX12_PIPELINE_STATE_STREAM1, inizializzata con i valori copiati da una **CD3DX12_PIPELINE_STATE_STREAM1** struttura .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

restituisce il contenuto dell'oggetto CD3DX12_PIPELINE_STATE_STREAM1 come D3D12_GRAPHICS_PIPELINE_STATE_DESC struttura in base al valore. Si noti D3D12_GRAPHICS_PIPELINE_STATE_DESC non include il **membro CS,** quindi questo valore viene perso nella conversione.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

restituisce il contenuto dell'oggetto CD3DX12_PIPELINE_STATE_STREAM1 come D3D12_COMPUTE_PIPELINE_STATE_DESC struttura in base al valore. Si noti che D3D12_COMPUTE_PIPELINE_STATE_DESC non include i membri **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** o **SampleMask,** quindi questi valori vengono persi nella conversione.

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

[CD3DX12_PIPELINE_STATE_STREAM](cd3dx12-pipeline-state-stream.md) supporta l'Windows 10 Fall Creators Update, ma non supporta i tipi di oggetti secondari aggiunti in Windows 10 Fall Creators Update, ad esempio per la creazione di istanze di visualizzazione. Per supportare i nuovi tipi di oggetto secondario, **usare CD3DX12_PIPELINE_STATE_STREAM1.**

Le variabili membro accessibili di questa struttura sono tutti typedef del modello CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT, che combina i dati type-marker e subobject del sottooggetto in un singolo oggetto adatto per una [**descrizione**](/windows/win32/direct3d12/cd3dx12-pipeline-state-stream-subobject) del flusso.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [Strutture helper per D3D12](helper-structures-for-d3d12.md)
* [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md)
* [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
* [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
