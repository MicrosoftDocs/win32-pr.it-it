---
title: CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT struttura (D3dx12.h)
description: Struttura helper modello usata per incapsulare coppie di dati di sottooggetto e sottooggetto come singolo oggetto adatto per una descrizione del flusso.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d945296ae4ee09710b74b9fdf2259251632d25fb309ede2983858c0c59be72d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729481"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>Struttura \_ \_ \_ \_ SUBOBJECT FLUSSO DI STATO DELLA PIPELINE CD3DX12

Struttura helper modello usata per incapsulare coppie di dati di sottooggetto e sottooggetto come singolo oggetto adatto per una descrizione del flusso.

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**SOTTOOGGETTO FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di UN SUBOBJECT FLUSSO DI STATO DELLA PIPELINE CD3DX12. \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT(** InnerStructType** const &i)**
</dt> <dd>

Crea una nuova istanza del modello SUBOBJECT CD3DX12 PIPELINE STATE STREAM, inizializzata con un tipo di oggetto secondario \_ \_ \_ \_ [**D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) e dati di sottooggetto copiati da i . Sia il tipo di oggetto secondario che il tipo di dati subobject vengono specificati rispettivamente come parametri di modello, **Type** e **InnerStructType.** Per altre informazioni, vedere Note di seguito.

</dd> <dt>

**operator=(** InnerStructType** const& i)**
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore **InnerStructType**() const**
</dt> <dd>

Conversione implicita nel tipo di dati subobject specificato dal **parametro di modello InnerStructType.**

</dd> </dl>

## <a name="remarks"></a>Commenti

CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT è un modello definito come segue:


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



Il parametro del modello **InnerStructType** specifica il tipo di dati subobject. cio, i dettagli del sottooggetto da codificare in un flusso. Il parametro di **modello Type** specifica il tipo di oggetto secondario. cio, il tipo della struttura specificata dal parametro di modello **InnerStructType**. Il parametro del modello **DefaultArg** specifica un valore facoltativo su cui verranno inizializzati i dati del sottooggetto quando un'istanza della creazione di istanze del modello corrispondente viene costruita come predefinita. ad esempio, per costruire per impostazione predefinita [**una PIPELINE CD3DX12 \_ STATE STREAM BLEND \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) inizializzata con valori predefiniti comuni dello stato di blend usando [**CD3DX12 \_ DEFAULT**](cd3dx12-default.md).

Ecco le istanze del modello definite:

-   [**FLAG DI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**MASCHERA DEL NODO FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**FIRMA RADICE FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**LAYOUT DI INPUT DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ IB \_ STRIP \_ CUT \_ VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**TOPOLOGIA PRIMITIVA DEL FLUSSO DI \_ \_ STATO \_ \_ DELLA \_ PIPELINE CD3DX12**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**CONFRONTO TRA FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-vs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ GS**](cd3dx12-pipeline-state-stream-gs.md)
-   [**OUTPUT DEL FLUSSO DI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**DS FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-ds.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CS**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**STENCIL PROFONDITÀ FLUSSO STATO PIPELINE CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**FORMATO \_ \_ DELLO \_ \_ \_ STENCIL \_ DELLA PROFONDITÀ DEL FLUSSO DELLO STATO DELLA PIPELINE CD3DX12**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**RASTERIZZAZIONE DEL FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**FORMATI DI DESTINAZIONE DI RENDERING DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**ESEMPIO DI FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**MASCHERA DI ESEMPIO DEL FLUSSO DI STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**PSO MEMORIZZATO NELLA CACHE DEL FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-cached-pso.md)

Le strutture [**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC,**](cd3dx12-pipeline-state-stream-blend-desc.md) [**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL,**](cd3dx12-pipeline-state-stream-depth-stencil.md) [**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)e [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) sono definite per inizializzare i dati del sottooggetto con valori predefiniti comuni usando [**CD3DX12 \_ DEFAULT.**](cd3dx12-default.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**TIPO DI SOTTOOGGETTO STATO PIPELINE D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

