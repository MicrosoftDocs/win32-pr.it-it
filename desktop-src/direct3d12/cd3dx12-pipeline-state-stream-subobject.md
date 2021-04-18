---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT (D3dx12. h)
description: Struttura Helper basata su modelli utilizzata per incapsulare le coppie di dati di tipo sottooggetto e sottooggetto come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
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
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323573"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>\_Struttura del \_ \_ sottooggetto flusso di stato della pipeline CD3DX12 \_

Struttura Helper basata su modelli utilizzata per incapsulare le coppie di dati di tipo sottooggetto e sottooggetto come singolo oggetto adatto per la descrizione di un flusso.

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

**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ \_ sottooggetto flusso di stato della pipeline CD3DX12 \_ \_ .

</dd> <dt>

**CD3DX12 \_ Sottooggetto flusso di stato della PIPELINE \_ \_ \_ (** InnerStructType * * const &i) * *
</dt> <dd>

Crea una nuova \_ \_ \_ \_ istanza del modello di sottooggetto flusso di stato della pipeline CD3DX12, inizializzata con un tipo di sottooggetto del tipo di sottooggetto di [**\_ stato della pipeline \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) e dati di sottooggetti copiati da *i*. Il tipo di dati sottooggetto e il tipo di dati SubObject sono rispettivamente specificati come parametri di modello, **Type** e **InnerStructType**. Per ulteriori informazioni, vedere la sezione Osservazioni di seguito.

</dd> <dt>

**operator = (** InnerStructType * * const& i) * *
</dt> <dd>

Operatore di assegnazione di copia.

</dd> <dt>

**operatore **InnerStructType**() const**
</dt> <dd>

Conversione implicita nel tipo di dati del sottooggetto fornito dal parametro di modello **InnerStructType** .

</dd> </dl>

## <a name="remarks"></a>Commenti

\_ \_ Il sottooggetto flusso di stato della pipeline CD3DX12 \_ \_ è un modello definito come segue:


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



Il parametro di modello **InnerStructType** specifica il tipo di dati del sottooggetto; ovvero i dettagli del sottooggetto da codificare in un flusso. Il **tipo di parametro del** modello specifica il tipo di sottooggetto; ovvero il tipo della struttura specificata dal parametro di modello **InnerStructType**. Il parametro di modello **defaultArg (** specifica un valore facoltativo a cui verranno inizializzati i dati di un sottooggetto quando un'istanza della creazione di istanza del modello corrispondente viene costruita in modo predefinito. ad esempio, per costruire in modo predefinito una [**CD3DX12 della \_ pipeline di \_ flusso dello stato della \_ \_ \_ pipeline**](cd3dx12-pipeline-state-stream-blend-desc.md) inizializzata con le impostazioni predefinite di stato di Blend comuni usando [**CD3DX12 \_ default**](cd3dx12-default.md).

Di seguito sono riportate le creazioni di istanze di modello definite:

-   [**\_Flag di \_ flusso dello stato della pipeline \_ CD3DX12 \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**\_Maschera del \_ nodo del flusso di stato della pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**\_ \_ \_ Firma radice del flusso dello stato \_ della pipeline \_ CD3DX12**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**\_Layout di \_ input del flusso di stato della pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**\_Valore di \_ \_ \_ \_ Strip \_ Cut \_ del flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**\_ \_ \_ Topologia del flusso \_ di stato della pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**\_Confronto tra \_ flusso di stato della pipeline CD3DX12 e \_ \_**](cd3dx12-pipeline-state-stream-vs.md)
-   [**\_ \_ GS flusso di stato della pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-gs.md)
-   [**\_ \_ \_ \_ \_ Output flusso flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**\_ \_ Sa flusso di stato della pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-hs.md)
-   [**\_ \_ DS flusso di stato della pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-ds.md)
-   [**CD3DX12 \_ \_ flusso di stato della pipeline \_ \_**](cd3dx12-pipeline-state-stream-ps.md)
-   [**\_ \_ CS flusso di stato della pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 \_ di \_ \_ Blend del flusso di stato \_ della pipeline \_**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**\_ \_ \_ \_ Stencil profondità flusso dello stato della pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**\_Profondità flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**\_ \_ \_ \_ \_ Formato stencil profondità flusso dello stato della pipeline \_ CD3DX12**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**\_ \_ \_ Rasterizzatore del flusso di stato della pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**\_Formati di \_ \_ destinazione di rendering del flusso di stato \_ della \_ pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**\_Esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**\_Maschera di \_ esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**\_ \_ \_ \_ PSO memorizzato nella cache del flusso di stato della pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-cached-pso.md)

I [**CD3DX12 della \_ pipeline di \_ flusso dello stato \_ \_ \_ della pipeline**](cd3dx12-pipeline-state-stream-blend-desc.md)sono definiti per inizializzare i relativi dati di sottooggetti con le impostazioni predefinite [**comuni che usano \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-rasterizer.md) il [**\_ valore predefinito di CD3DX12 di CD3DX12**](cd3dx12-default.md). [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil.md) [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil1.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

