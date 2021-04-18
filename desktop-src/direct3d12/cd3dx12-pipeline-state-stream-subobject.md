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
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a><span data-ttu-id="90097-104">\_Struttura del \_ \_ sottooggetto flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="90097-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT structure</span></span>

<span data-ttu-id="90097-105">Struttura Helper basata su modelli utilizzata per incapsulare le coppie di dati di tipo sottooggetto e sottooggetto come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="90097-105">A templated helper structure used to encapsulate subobject type and subobject data pairs as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="90097-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90097-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a><span data-ttu-id="90097-107">Members</span><span class="sxs-lookup"><span data-stu-id="90097-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="90097-108">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="90097-109">Crea una nuova istanza non inizializzata di un \_ \_ sottooggetto flusso di stato della pipeline CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="90097-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT.</span></span>

</dd> <dt>

<span data-ttu-id="90097-110">**CD3DX12 \_ Sottooggetto flusso di stato della PIPELINE \_ \_ \_ (** InnerStructType \* \* const &i) \* \*</span><span class="sxs-lookup"><span data-stu-id="90097-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT(** InnerStructType\*\* const &i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="90097-111">Crea una nuova \_ \_ \_ \_ istanza del modello di sottooggetto flusso di stato della pipeline CD3DX12, inizializzata con un tipo di sottooggetto del tipo di sottooggetto di [**\_ stato della pipeline \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) e dati di sottooggetti copiati da *i*.</span><span class="sxs-lookup"><span data-stu-id="90097-111">Creates a new CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template instance, initialized with a subobject type of [**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) and subobject data copied from *i*.</span></span> <span data-ttu-id="90097-112">Il tipo di dati sottooggetto e il tipo di dati SubObject sono rispettivamente specificati come parametri di modello, **Type** e **InnerStructType**.</span><span class="sxs-lookup"><span data-stu-id="90097-112">Both the subobject type and subobject data type are given as template parameters, **Type** and **InnerStructType**, respectively.</span></span> <span data-ttu-id="90097-113">Per ulteriori informazioni, vedere la sezione Osservazioni di seguito.</span><span class="sxs-lookup"><span data-stu-id="90097-113">For more information, see Remarks below.</span></span>

</dd> <dt>

<span data-ttu-id="90097-114">**operator = (** InnerStructType \* \* const& i) \* \*</span><span class="sxs-lookup"><span data-stu-id="90097-114">**operator=(** InnerStructType\*\* const& i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="90097-115">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="90097-115">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="90097-116">**operatore **InnerStructType**() const**</span><span class="sxs-lookup"><span data-stu-id="90097-116">**operator **InnerStructType**() const**</span></span>
</dt> <dd>

<span data-ttu-id="90097-117">Conversione implicita nel tipo di dati del sottooggetto fornito dal parametro di modello **InnerStructType** .</span><span class="sxs-lookup"><span data-stu-id="90097-117">Implicit conversion to the subobject data type given by the **InnerStructType** template parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90097-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="90097-118">Remarks</span></span>

<span data-ttu-id="90097-119">\_ \_ Il sottooggetto flusso di stato della pipeline CD3DX12 \_ \_ è un modello definito come segue:</span><span class="sxs-lookup"><span data-stu-id="90097-119">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT is a template defined as follows:</span></span>


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



<span data-ttu-id="90097-120">Il parametro di modello **InnerStructType** specifica il tipo di dati del sottooggetto; ovvero i dettagli del sottooggetto da codificare in un flusso.</span><span class="sxs-lookup"><span data-stu-id="90097-120">The template parameter **InnerStructType** specifies the subobject data type; that is, the subobject details to be encoded into a stream.</span></span> <span data-ttu-id="90097-121">Il **tipo di parametro del** modello specifica il tipo di sottooggetto; ovvero il tipo della struttura specificata dal parametro di modello **InnerStructType**.</span><span class="sxs-lookup"><span data-stu-id="90097-121">The template parameter **Type** specifies the subobject type; that is, the type of the structure specified by the template parameter **InnerStructType**.</span></span> <span data-ttu-id="90097-122">Il parametro di modello **defaultArg (** specifica un valore facoltativo a cui verranno inizializzati i dati di un sottooggetto quando un'istanza della creazione di istanza del modello corrispondente viene costruita in modo predefinito. ad esempio, per costruire in modo predefinito una [**CD3DX12 della \_ pipeline di \_ flusso dello stato della \_ \_ \_ pipeline**](cd3dx12-pipeline-state-stream-blend-desc.md) inizializzata con le impostazioni predefinite di stato di Blend comuni usando [**CD3DX12 \_ default**](cd3dx12-default.md).</span><span class="sxs-lookup"><span data-stu-id="90097-122">The template parameter **DefaultArg** specifies an optional value that the subobject data will be initialized to when an instance of the corresponding template instantiation is default-constructed; for example, to default-construct a [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) initialized with common blend-state defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

<span data-ttu-id="90097-123">Di seguito sono riportate le creazioni di istanze di modello definite:</span><span class="sxs-lookup"><span data-stu-id="90097-123">Here are the template instantiations that are defined:</span></span>

-   [<span data-ttu-id="90097-124">**\_Flag di \_ flusso dello stato della pipeline \_ CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="90097-124">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>](cd3dx12-pipeline-state-stream-flags.md)
-   [<span data-ttu-id="90097-125">**\_Maschera del \_ nodo del flusso di stato della pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-node-mask.md)
-   [<span data-ttu-id="90097-126">**\_ \_ \_ Firma radice del flusso dello stato \_ della pipeline \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="90097-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>](cd3dx12-pipeline-state-stream-root-signature.md)
-   [<span data-ttu-id="90097-127">**\_Layout di \_ input del flusso di stato della pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-127">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>](cd3dx12-pipeline-state-stream-input-layout.md)
-   [<span data-ttu-id="90097-128">**\_Valore di \_ \_ \_ \_ Strip \_ Cut \_ del flusso di stato della pipeline CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="90097-128">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [<span data-ttu-id="90097-129">**\_ \_ \_ Topologia del flusso \_ di stato della pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="90097-129">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [<span data-ttu-id="90097-130">**\_Confronto tra \_ flusso di stato della pipeline CD3DX12 e \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-130">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>](cd3dx12-pipeline-state-stream-vs.md)
-   [<span data-ttu-id="90097-131">**\_ \_ GS flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-131">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS**</span></span>](cd3dx12-pipeline-state-stream-gs.md)
-   [<span data-ttu-id="90097-132">**\_ \_ \_ \_ \_ Output flusso flusso di stato della pipeline CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="90097-132">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>](cd3dx12-pipeline-state-stream-stream-output.md)
-   [<span data-ttu-id="90097-133">**\_ \_ Sa flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-133">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS**</span></span>](cd3dx12-pipeline-state-stream-hs.md)
-   [<span data-ttu-id="90097-134">**\_ \_ DS flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-134">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>](cd3dx12-pipeline-state-stream-ds.md)
-   [<span data-ttu-id="90097-135">**CD3DX12 \_ \_ flusso di stato della pipeline \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-135">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS**</span></span>](cd3dx12-pipeline-state-stream-ps.md)
-   [<span data-ttu-id="90097-136">**\_ \_ CS flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-136">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>](cd3dx12-pipeline-state-stream-cs.md)
-   [<span data-ttu-id="90097-137">**CD3DX12 \_ di \_ \_ Blend del flusso di stato \_ della pipeline \_**</span><span class="sxs-lookup"><span data-stu-id="90097-137">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [<span data-ttu-id="90097-138">**\_ \_ \_ \_ Stencil profondità flusso dello stato della pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="90097-138">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [<span data-ttu-id="90097-139">**\_Profondità flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="90097-139">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [<span data-ttu-id="90097-140">**\_ \_ \_ \_ \_ Formato stencil profondità flusso dello stato della pipeline \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="90097-140">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [<span data-ttu-id="90097-141">**\_ \_ \_ Rasterizzatore del flusso di stato della pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="90097-141">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [<span data-ttu-id="90097-142">**\_Formati di \_ \_ destinazione di rendering del flusso di stato \_ della \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="90097-142">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [<span data-ttu-id="90097-143">**\_Esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="90097-143">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [<span data-ttu-id="90097-144">**\_Maschera di \_ esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90097-144">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [<span data-ttu-id="90097-145">**\_ \_ \_ \_ PSO memorizzato nella cache del flusso di stato della pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="90097-145">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>](cd3dx12-pipeline-state-stream-cached-pso.md)

<span data-ttu-id="90097-146">I [**CD3DX12 della \_ pipeline di \_ flusso dello stato \_ \_ \_ della pipeline**](cd3dx12-pipeline-state-stream-blend-desc.md)sono definiti per inizializzare i relativi dati di sottooggetti con le impostazioni predefinite [**comuni che usano \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-rasterizer.md) il [**\_ valore predefinito di CD3DX12 di CD3DX12**](cd3dx12-default.md). [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil.md) [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil1.md)</span><span class="sxs-lookup"><span data-stu-id="90097-146">The [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md), and [**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) structures are defined to initialize their subobject data with common defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90097-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90097-147">Requirements</span></span>



| <span data-ttu-id="90097-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="90097-148">Requirement</span></span> | <span data-ttu-id="90097-149">Valore</span><span class="sxs-lookup"><span data-stu-id="90097-149">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90097-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90097-150">Header</span></span><br/> | <dl> <span data-ttu-id="90097-151"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="90097-151"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90097-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90097-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90097-153">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="90097-153">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="90097-154">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="90097-154">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

