---
title: Effetti personalizzati
description: Viene illustrato come scrivere effetti personalizzati usando HLSL standard.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118403"
---
# <a name="custom-effects"></a><span data-ttu-id="b8930-103">Effetti personalizzati</span><span class="sxs-lookup"><span data-stu-id="b8930-103">Custom effects</span></span>

<span data-ttu-id="b8930-104">[Direct2D](./direct2d-portal.md) viene fornito con una raccolta di effetti che eseguono una serie di operazioni di immagine comuni.</span><span class="sxs-lookup"><span data-stu-id="b8930-104">[Direct2D](./direct2d-portal.md) ships with a library of effects that perform a variety of common image operations.</span></span> <span data-ttu-id="b8930-105">Per l'elenco completo degli effetti, vedere l'argomento relativo agli [effetti predefiniti](built-in-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="b8930-105">See the [built-in effects](built-in-effects.md) topic for the complete list of effects.</span></span> <span data-ttu-id="b8930-106">Per le funzionalità che non possono essere ottenute con gli effetti predefiniti, Direct2D consente di scrivere effetti personalizzati usando [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)standard.</span><span class="sxs-lookup"><span data-stu-id="b8930-106">For functionality that cannot be achieved with the built-in effects, Direct2D allows you to write your own custom effects using standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl).</span></span> <span data-ttu-id="b8930-107">È possibile utilizzare questi effetti personalizzati insieme agli effetti predefiniti forniti con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="b8930-107">You can use these custom effects alongside the built-in effects that ship with Direct2D.</span></span>

<span data-ttu-id="b8930-108">Per visualizzare esempi di un effetto completo su pixel, vertex e compute shader, vedere l' [esempio D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="b8930-108">To see examples of a complete pixel, vertex, and compute shader effect, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="b8930-109">In questo argomento vengono illustrati i passaggi e i concetti necessari per progettare e creare un effetto personalizzato con funzionalità complete.</span><span class="sxs-lookup"><span data-stu-id="b8930-109">In this topic, we show you the steps and concepts you need to design and create a fully-featured custom effect.</span></span>

## <a name="introduction-what-is-inside-an-effect"></a><span data-ttu-id="b8930-110">Introduzione: che cosa si trova all'interno di un effetto?</span><span class="sxs-lookup"><span data-stu-id="b8930-110">Introduction: What is inside an effect?</span></span>

![diagramma effetto ombreggiatura.](images/custom-effects1.png)

<span data-ttu-id="b8930-112">A livello concettuale, un effetto [Direct2D](./direct2d-portal.md) esegue un'attività di creazione dell'immagine, ad esempio la modifica della luminosità, la desaturazione di un'immagine o, come illustrato in precedenza, la creazione di un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="b8930-112">Conceptually, a [Direct2D](./direct2d-portal.md) effect performs an imaging task, like changing brightness, de-saturating an image, or as shown above, creating a drop shadow.</span></span> <span data-ttu-id="b8930-113">All'app sono semplici.</span><span class="sxs-lookup"><span data-stu-id="b8930-113">To the app, they are simple.</span></span> <span data-ttu-id="b8930-114">Possono accettare zero o più immagini di input, esporre più proprietà che controllano l'operazione e generare un'unica immagine di output.</span><span class="sxs-lookup"><span data-stu-id="b8930-114">They can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="b8930-115">Sono disponibili quattro parti diverse di un effetto personalizzato di cui l'autore di un effetto è responsabile:</span><span class="sxs-lookup"><span data-stu-id="b8930-115">There are four different parts of a custom effect that an effect author is responsible for:</span></span>

1.  <span data-ttu-id="b8930-116">Interfaccia Effect: l'interfaccia Effect definisce concettualmente il modo in cui un'app interagisce con un effetto personalizzato, ad esempio il numero di input accettati dall'effetto e le proprietà disponibili.</span><span class="sxs-lookup"><span data-stu-id="b8930-116">Effect Interface: The effect interface conceptually defines how an app interacts with a custom effect (like how many inputs the effect accepts and what properties are available).</span></span> <span data-ttu-id="b8930-117">L'interfaccia Effect gestisce un grafico di trasformazione, che contiene le operazioni di creazione di immagini effettive.</span><span class="sxs-lookup"><span data-stu-id="b8930-117">The effect interface manages a transform graph, which contains the actual imaging operations.</span></span>
2.  <span data-ttu-id="b8930-118">Transform Graph: ogni effetto crea un grafico di trasformazione interno costituito da singole trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="b8930-118">Transform graph: Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="b8930-119">Ogni trasformazione rappresenta una singola operazione di immagine.</span><span class="sxs-lookup"><span data-stu-id="b8930-119">Each transform represents a single image operation.</span></span> <span data-ttu-id="b8930-120">L'effetto è responsabile del collegamento di queste trasformazioni in un grafico per l'esecuzione dell'effetto della creazione di immagini desiderato.</span><span class="sxs-lookup"><span data-stu-id="b8930-120">The effect is responsible for linking these transforms together into a graph to perform the intended imaging effect.</span></span> <span data-ttu-id="b8930-121">Un effetto può aggiungere, rimuovere, modificare e riordinare le trasformazioni in risposta alle modifiche apportate alle proprietà esterne dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-121">An effect can add, remove, modify, and reorder transforms in response to changes to the effect's external properties.</span></span>
3.  <span data-ttu-id="b8930-122">Transform: una trasformazione rappresenta una singola operazione di immagine.</span><span class="sxs-lookup"><span data-stu-id="b8930-122">Transform: A transform represents a single image operation.</span></span> <span data-ttu-id="b8930-123">Lo scopo principale è quello di ospitare gli shader eseguiti per ogni pixel di output.</span><span class="sxs-lookup"><span data-stu-id="b8930-123">Its main purpose is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="b8930-124">A tal fine, è responsabile del calcolo delle nuove dimensioni dell'immagine di output in base alla logica nei relativi shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-124">To that end, it is responsible for calculating the new size of its output image based on logic in its shaders.</span></span> <span data-ttu-id="b8930-125">Deve inoltre calcolare l'area dell'immagine di input da cui gli shader devono leggere per eseguire il rendering dell'area di output richiesta.</span><span class="sxs-lookup"><span data-stu-id="b8930-125">It also must calculate which area of its input image the shaders need to read from to render the requested output region.</span></span>
4.  <span data-ttu-id="b8930-126">Shader: uno shader viene eseguito sull'input della trasformazione sulla GPU (o CPU se viene specificato il rendering del software quando l'app crea il dispositivo Direct3D).</span><span class="sxs-lookup"><span data-stu-id="b8930-126">Shader: A shader is executed against the transform's input on the GPU (or CPU if software rendering is specified when the app creates the Direct3D device).</span></span> <span data-ttu-id="b8930-127">Gli shader degli effetti sono scritti in[HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)(High Level Shading Language) e vengono compilati in codice byte durante la compilazione dell'effetto, che viene quindi caricato dall'effetto in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b8930-127">Effect shaders are written in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) and are compiled into byte code during the effect's compilation, which is then loaded by the effect during run-time.</span></span> <span data-ttu-id="b8930-128">In questo documento di riferimento viene descritto come scrivere HLSL conformi a [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b8930-128">This reference document describes how to write [Direct2D](./direct2d-portal.md)-compliant HLSL.</span></span> <span data-ttu-id="b8930-129">La documentazione di Direct3D contiene una panoramica di base di HLSL.</span><span class="sxs-lookup"><span data-stu-id="b8930-129">The Direct3D documentation contains a basic HLSL overview.</span></span>

## <a name="creating-an-effect-interface"></a><span data-ttu-id="b8930-130">Creazione di un'interfaccia di effetto</span><span class="sxs-lookup"><span data-stu-id="b8930-130">Creating an effect interface</span></span>

<span data-ttu-id="b8930-131">L'interfaccia Effect definisce il modo in cui un'app interagisce con l'effetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b8930-131">The effect interface defines how an app interacts with the custom effect.</span></span> <span data-ttu-id="b8930-132">Per creare un'interfaccia effetto, una classe deve implementare ID2D1EffectImpl, definire i metadati che descrivono l'effetto, ad esempio il nome, il numero di input e le proprietà, e creare metodi che registrano l'effetto personalizzato per l'uso con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b8930-132">To create an effect interface, a class must implement ID2D1EffectImpl, define metadata that describes the effect (such as its name, input count and properties), and create methods that register the custom effect for use with [Direct2D](./direct2d-portal.md).</span></span>

<span data-ttu-id="b8930-133">Una volta implementati tutti i componenti per un'interfaccia di effetto, l'intestazione della classe sarà simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="b8930-133">Once all of the components for an effect interface have been implemented, the class' header will appear like this:</span></span>


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a><span data-ttu-id="b8930-134">Implementare ID2D1EffectImpl</span><span class="sxs-lookup"><span data-stu-id="b8930-134">Implement ID2D1EffectImpl</span></span>

<span data-ttu-id="b8930-135">L'interfaccia [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) contiene tre metodi che è necessario implementare:</span><span class="sxs-lookup"><span data-stu-id="b8930-135">The [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) interface contains three methods that you must implement:</span></span>

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a><span data-ttu-id="b8930-136">Initialize (ID2D1EffectContext \* pContextInternal, ID2D1TransformGraph \* pTransformGraph)</span><span class="sxs-lookup"><span data-stu-id="b8930-136">Initialize(ID2D1EffectContext \*pContextInternal, ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="b8930-137">[Direct2D](./direct2d-portal.md) chiama il metodo [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) dopo che il metodo [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) è stato chiamato dall'app.</span><span class="sxs-lookup"><span data-stu-id="b8930-137">[Direct2D](./direct2d-portal.md) calls the [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method after the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method has been called by the app.</span></span> <span data-ttu-id="b8930-138">È possibile utilizzare questo metodo per eseguire l'inizializzazione interna o qualsiasi altra operazione necessaria per l'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-138">You can use this method to perform internal initialization or any other operations needed for the effect.</span></span> <span data-ttu-id="b8930-139">Inoltre, è possibile usarlo per creare il grafico di trasformazione iniziale dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-139">Additionally, you can use it to create the effect's initial transform graph.</span></span>

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a><span data-ttu-id="b8930-140">Segraph (ID2D1TransformGraph \* pTransformGraph)</span><span class="sxs-lookup"><span data-stu-id="b8930-140">SetGraph(ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="b8930-141">[Direct2D](./direct2d-portal.md) chiama il metodo [**segraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) quando viene modificato il numero di input per l'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-141">[Direct2D](./direct2d-portal.md) calls the [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) method when the number of inputs to the effect is changed.</span></span> <span data-ttu-id="b8930-142">Mentre la maggior parte degli effetti ha un numero costante di input, altri come l' [effetto composito](composite.md) supportano un numero variabile di input.</span><span class="sxs-lookup"><span data-stu-id="b8930-142">While most effects have a constant number of inputs, others like the [Composite effect](composite.md) support a variable number of inputs.</span></span> <span data-ttu-id="b8930-143">Questo metodo consente a questi effetti di aggiornare il grafico di trasformazione in risposta a un conteggio di input modificabile.</span><span class="sxs-lookup"><span data-stu-id="b8930-143">This method allows these effects to update their transform graph in response to a changing input count.</span></span> <span data-ttu-id="b8930-144">Se un effetto non supporta un numero di input variabile, questo metodo può semplicemente restituire E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="b8930-144">If an effect does not support a variable input count, this method can simply return E\_NOTIMPL.</span></span>

### <a name="prepareforrender-d2d1_change_type-changetype"></a><span data-ttu-id="b8930-145">PrepareForRender ( \_ tipo di modifica d2d1 \_ ChangeType)</span><span class="sxs-lookup"><span data-stu-id="b8930-145">PrepareForRender (D2D1\_CHANGE\_TYPE changeType)</span></span>

<span data-ttu-id="b8930-146">Il metodo [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) consente agli effetti di eseguire qualsiasi operazione in risposta a modifiche esterne.</span><span class="sxs-lookup"><span data-stu-id="b8930-146">The [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method provides an opportunity for effects to perform any operations in response to external changes.</span></span> <span data-ttu-id="b8930-147">[Direct2D](./direct2d-portal.md) chiama questo metodo appena prima di eseguire il rendering di un effetto se almeno una di queste condizioni è vera:</span><span class="sxs-lookup"><span data-stu-id="b8930-147">[Direct2D](./direct2d-portal.md) calls this method just before it renders an effect if at least one of these is true:</span></span>

-   <span data-ttu-id="b8930-148">L'effetto è stato inizializzato in precedenza ma non ancora creato.</span><span class="sxs-lookup"><span data-stu-id="b8930-148">The effect has been previously initialized but not yet drawn.</span></span>
-   <span data-ttu-id="b8930-149">Una proprietà Effect è stata modificata dopo l'ultima chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-149">An effect property has changed since the last draw call.</span></span>
-   <span data-ttu-id="b8930-150">Lo stato del contesto [Direct2D](./direct2d-portal.md) chiamante (ad esempio dpi) è stato modificato dopo l'ultima chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-150">The state of the calling [Direct2D](./direct2d-portal.md) context (like DPI) has changed since the last draw call.</span></span>

### <a name="implement-the-effect-registration-and-callback-methods"></a><span data-ttu-id="b8930-151">Implementare i metodi di registrazione e callback degli effetti</span><span class="sxs-lookup"><span data-stu-id="b8930-151">Implement the effect registration and callback methods</span></span>

<span data-ttu-id="b8930-152">È necessario che le app registrino gli effetti con [Direct2D](./direct2d-portal.md) prima di crearne un'istanza.</span><span class="sxs-lookup"><span data-stu-id="b8930-152">Apps must register effects with [Direct2D](./direct2d-portal.md) before instantiating them.</span></span> <span data-ttu-id="b8930-153">Questa registrazione ha come ambito un'istanza di una factory Direct2D e deve essere ripetuta ogni volta che l'app viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="b8930-153">This registration is scoped to an instance of a Direct2D factory, and must be repeated each time the app is run.</span></span> <span data-ttu-id="b8930-154">Per abilitare questa registrazione, un effetto personalizzato definisce un GUID univoco, un metodo pubblico che registra l'effetto e un metodo di callback privato che restituisce un'istanza dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-154">To enable this registration, a custom effect defines a unique GUID, a public method that registers the effect, and a private callback method that returns an instance of the effect.</span></span>

### <a name="define-a-guid"></a><span data-ttu-id="b8930-155">Definire un GUID</span><span class="sxs-lookup"><span data-stu-id="b8930-155">Define a GUID</span></span>

<span data-ttu-id="b8930-156">È necessario definire un GUID che identifichi in modo univoco l'effetto per la registrazione con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b8930-156">You must define a GUID that uniquely identifies the effect for registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="b8930-157">L'app usa lo stesso per identificare l'effetto quando chiama [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span><span class="sxs-lookup"><span data-stu-id="b8930-157">The app uses the same to identify the effect when it calls [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span></span>

<span data-ttu-id="b8930-158">Questo codice illustra la definizione di un GUID di questo tipo per un effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-158">This code demonstrates defining such a GUID for an effect.</span></span> <span data-ttu-id="b8930-159">È necessario creare un proprio GUID univoco usando uno strumento di generazione GUID, ad esempio guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="b8930-159">You must create its own unique GUID using a GUID generation tool such as guidgen.exe.</span></span>


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a><span data-ttu-id="b8930-160">Definire un metodo di registrazione pubblico</span><span class="sxs-lookup"><span data-stu-id="b8930-160">Define a public registration method</span></span>

<span data-ttu-id="b8930-161">Definire quindi un metodo pubblico che l'app deve chiamare per registrare l'effetto con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b8930-161">Next, define a public method for the app to call to register the effect with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="b8930-162">Poiché la registrazione degli effetti è specifica di un'istanza di una factory Direct2D, il metodo accetta un'interfaccia [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) come parametro.</span><span class="sxs-lookup"><span data-stu-id="b8930-162">Because effect registration is specific to an instance of a Direct2D factory, the method accepts an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface as a parameter.</span></span> <span data-ttu-id="b8930-163">Per registrare l'effetto, il metodo chiama quindi l'API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) sul parametro **ID2D1Factory1** .</span><span class="sxs-lookup"><span data-stu-id="b8930-163">To register the effect, the method then calls the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API on the **ID2D1Factory1** parameter.</span></span>

<span data-ttu-id="b8930-164">Questa API accetta una stringa XML che descrive i metadati, gli input e le proprietà dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-164">This API accepts an XML string that describes the metadata, inputs, and properties of the effect.</span></span> <span data-ttu-id="b8930-165">I metadati per un effetto sono solo a scopo informativo e possono essere sottoposti a query dall'app tramite l'interfaccia [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) .</span><span class="sxs-lookup"><span data-stu-id="b8930-165">The metadata for an effect is for informational purposes only, and can be queried by the app through the [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) interface.</span></span> <span data-ttu-id="b8930-166">I dati di input e delle proprietà, d'altra parte, vengono usati da [Direct2D](./direct2d-portal.md) e rappresentano la funzionalità dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-166">The input and property data, on the other hand, is used by [Direct2D](./direct2d-portal.md) and represents the effect's functionality.</span></span>

<span data-ttu-id="b8930-167">Di seguito è riportata una stringa XML per un effetto di esempio minimo.</span><span class="sxs-lookup"><span data-stu-id="b8930-167">An XML string for a minimal sample effect is shown here.</span></span> <span data-ttu-id="b8930-168">L'aggiunta di proprietà personalizzate al codice XML viene analizzata nella sezione aggiunta di proprietà personalizzate a un effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-168">Adding custom properties to the XML is covered in the Adding custom properties to an effect section.</span></span>


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a><span data-ttu-id="b8930-169">Definire un metodo di callback Factory degli effetti</span><span class="sxs-lookup"><span data-stu-id="b8930-169">Define an effect factory callback method</span></span>

<span data-ttu-id="b8930-170">L'effetto deve inoltre fornire un metodo di callback privato che restituisca un'istanza dell'effetto tramite un singolo \* \* parametro IUnknown.</span><span class="sxs-lookup"><span data-stu-id="b8930-170">The effect must also provide a private callback method that returns an instance of the effect through a single IUnknown\*\* parameter.</span></span> <span data-ttu-id="b8930-171">Un puntatore a questo metodo viene fornito a [Direct2D](./direct2d-portal.md) quando l'effetto viene registrato tramite l'API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) tramite il [**parametro \_ \_ Factory Effect PD2D1**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .</span><span class="sxs-lookup"><span data-stu-id="b8930-171">A pointer to this method is provided to [Direct2D](./direct2d-portal.md) when the effect is registered via the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API through the [**PD2D1\_EFFECT\_FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)\\ parameter.</span></span>


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a><span data-ttu-id="b8930-172">Implementare l'interfaccia IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8930-172">Implement the IUnknown interface</span></span>

<span data-ttu-id="b8930-173">Infine, l'effetto deve implementare l'interfaccia IUnknown per la compatibilità con COM.</span><span class="sxs-lookup"><span data-stu-id="b8930-173">Finally, the effect must implement the IUnknown interface for compatibility with COM.</span></span>

## <a name="creating-the-effects-transform-graph"></a><span data-ttu-id="b8930-174">Creazione del grafico di trasformazione dell'effetto</span><span class="sxs-lookup"><span data-stu-id="b8930-174">Creating the effect's transform graph</span></span>

<span data-ttu-id="b8930-175">Un effetto può utilizzare diverse trasformazioni (singole operazioni di immagine) per creare l'effetto di imaging desiderato.</span><span class="sxs-lookup"><span data-stu-id="b8930-175">An effect can use several different transforms (individual image operations) to create its desired imaging effect.</span></span> <span data-ttu-id="b8930-176">Per controllare l'ordine in cui queste trasformazioni vengono applicate all'immagine di input, l'effetto li dispone in un grafico di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-176">To control the order in which these transforms are applied to the input image, the effect arranges them into a transform graph.</span></span> <span data-ttu-id="b8930-177">Un grafico di trasformazione può usare gli effetti e le trasformazioni inclusi in [Direct2D](./direct2d-portal.md) , nonché le trasformazioni personalizzate create dall'autore dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-177">A transform graph can make use of the effects and transforms included in [Direct2D](./direct2d-portal.md) as well as custom transforms created by the effect author.</span></span>

### <a name="using-transforms-included-with-direct2d"></a><span data-ttu-id="b8930-178">Uso delle trasformazioni incluse con Direct2D</span><span class="sxs-lookup"><span data-stu-id="b8930-178">Using transforms included with Direct2D</span></span>

<span data-ttu-id="b8930-179">Queste sono le trasformazioni usate più di frequente fornite con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b8930-179">These are the most commonly used transforms provided with [Direct2D](./direct2d-portal.md).</span></span>

-   <span data-ttu-id="b8930-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): questa trasformazione unisce un numero arbitrario di input in base a una descrizione di Blend, vedere l'argomento della [**\_ \_ Descrizione di d2d1 Blend**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) e l' [esempio di modalità effetto composito Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) per esempi di Blend.</span><span class="sxs-lookup"><span data-stu-id="b8930-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): This transform blends an arbitrary number of inputs together based on a blend description, see the [**D2D1\_BLEND\_DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) topic and the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) for blending examples.</span></span> <span data-ttu-id="b8930-181">Questa trasformazione viene restituita dal metodo [**ID2D1EffectContext:: CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .</span><span class="sxs-lookup"><span data-stu-id="b8930-181">This transform is returned by the [**ID2D1EffectContext::CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) method.</span></span>
-   <span data-ttu-id="b8930-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): questa trasformazione espande le dimensioni di output di un'immagine in base [**alla \_ \_ modalità di estensione d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specificata.</span><span class="sxs-lookup"><span data-stu-id="b8930-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): This transform expands an image's output size according to the [**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specified.</span></span> <span data-ttu-id="b8930-183">Questa trasformazione viene restituita dal metodo [**ID2D1EffectContext:: CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .</span><span class="sxs-lookup"><span data-stu-id="b8930-183">This transform is returned by the [**ID2D1EffectContext::CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) method.</span></span>
-   <span data-ttu-id="b8930-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): questa trasformazione compensa (converte) l'input in base a un numero intero di pixel.</span><span class="sxs-lookup"><span data-stu-id="b8930-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): This transform offsets (translates) its input by any whole number of pixels.</span></span> <span data-ttu-id="b8930-185">Questa trasformazione viene restituita dal metodo [**ID2D1EffectContext:: CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .</span><span class="sxs-lookup"><span data-stu-id="b8930-185">This transform is returned by the [**ID2D1EffectContext::CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) method.</span></span>
-   <span data-ttu-id="b8930-186">Qualsiasi effetto esistente può essere trattato come una trasformazione allo scopo di trasformare la creazione di grafici tramite il metodo [**ID2D1EffectContext:: CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .</span><span class="sxs-lookup"><span data-stu-id="b8930-186">Any existing effect can be treated as a transform for the purposes of transform graph creation by using the [**ID2D1EffectContext::CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) method.</span></span>

### <a name="creating-a-single-node-transform-graph"></a><span data-ttu-id="b8930-187">Creazione di un grafico di trasformazione a nodo singolo</span><span class="sxs-lookup"><span data-stu-id="b8930-187">Creating a single-node transform graph</span></span>

<span data-ttu-id="b8930-188">Dopo aver creato una trasformazione, l'input dell'effetto deve essere connesso all'input della trasformazione e l'output della trasformazione deve essere connesso all'output dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-188">Once you create a transform, the effect's input needs to be connected to the transform's input, and the transform's output needs to be connected to the effect's output.</span></span> <span data-ttu-id="b8930-189">Quando un effetto contiene una sola trasformazione, è possibile usare il metodo [**ID2D1TransformGraph:: SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) per eseguire facilmente questa operazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-189">When an effect only contains a single transform, you can use the [**ID2D1TransformGraph::SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) method to easily accomplish this.</span></span>

<span data-ttu-id="b8930-190">È possibile creare o modificare una trasformazione nei metodi [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) o [**segraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) dell'effetto usando il parametro ID2D1TransformGraph specificato.</span><span class="sxs-lookup"><span data-stu-id="b8930-190">You can create or modify a transform in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) or [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) methods using the provided ID2D1TransformGraph parameter.</span></span> <span data-ttu-id="b8930-191">Se un effetto deve apportare modifiche al grafico di trasformazione in un altro metodo in cui questo parametro non è disponibile, l'effetto può salvare il parametro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) come variabile membro della classe e accedervi altrove, ad esempio [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) o un metodo di callback di proprietà personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b8930-191">If an effect needs to make changes to the transform graph in another method where this parameter is not available, the effect can save the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter as a member variable of the class and access it elsewhere, such as [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) or a custom property callback method.</span></span>

<span data-ttu-id="b8930-192">Di seguito è riportato un esempio di metodo [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) .</span><span class="sxs-lookup"><span data-stu-id="b8930-192">A sample [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method is shown here.</span></span> <span data-ttu-id="b8930-193">Questo metodo crea un grafico di trasformazione a nodo singolo che compensa l'immagine di 100 pixel in ogni asse.</span><span class="sxs-lookup"><span data-stu-id="b8930-193">This method creates a single-node transform graph that offsets the image by one hundred pixels in each axis.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a><span data-ttu-id="b8930-194">Creazione di un grafico di trasformazione a più nodi</span><span class="sxs-lookup"><span data-stu-id="b8930-194">Creating a multi-node transform graph</span></span>

<span data-ttu-id="b8930-195">L'aggiunta di più trasformazioni al grafico di trasformazione di un effetto consente agli effetti di eseguire internamente più operazioni di immagine presentate a un'app come singolo effetto unificato.</span><span class="sxs-lookup"><span data-stu-id="b8930-195">Adding multiple transforms to an effect's transform graph allows effects to internally perform multiple image operations that are presented to an app as a single unified effect.</span></span>

<span data-ttu-id="b8930-196">Come indicato in precedenza, il grafico di trasformazione dell'effetto può essere modificato in qualsiasi metodo di effetto usando il parametro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) ricevuto nel metodo [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-196">As noted above, the effect's transform graph may be edited in any effect method using the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter received in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method.</span></span> <span data-ttu-id="b8930-197">Le API seguenti su tale interfaccia possono essere utilizzate per creare o modificare il grafico di trasformazione di un effetto:</span><span class="sxs-lookup"><span data-stu-id="b8930-197">The following APIs on that interface can be used to create or modify an effect's transform graph:</span></span>

### <a name="addnodeid2d1transformnode-pnode"></a><span data-ttu-id="b8930-198">AddNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="b8930-198">AddNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="b8930-199">Il metodo [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , in pratica,' Registra ' la trasformazione con l'effetto e deve essere chiamato prima che la trasformazione possa essere usata con qualsiasi altro metodo di trasformazione Graph.</span><span class="sxs-lookup"><span data-stu-id="b8930-199">The [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) method, in effect, 'registers' the transform with the effect, and must be called before the transform can be used with any of the other transform graph methods.</span></span>

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a><span data-ttu-id="b8930-200">ConnectToEffectInput (UINT32 toEffectInputIndex, ID2D1TransformNode \* pNode, UInt32 toNodeInputIndex)</span><span class="sxs-lookup"><span data-stu-id="b8930-200">ConnectToEffectInput(UINT32 toEffectInputIndex, ID2D1TransformNode \*pNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="b8930-201">Il metodo [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) connette l'input dell'immagine dell'effetto all'input di una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-201">The [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) method connects the effect's image input to a transform's input.</span></span> <span data-ttu-id="b8930-202">Lo stesso input di effetto può essere connesso a più trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="b8930-202">The same effect input can be connected to multiple transforms.</span></span>

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a><span data-ttu-id="b8930-203">ConnectNode (ID2D1TransformNode \* pFromNode, ID2D1TransformNode \* PTONODE, UInt32 toNodeInputIndex)</span><span class="sxs-lookup"><span data-stu-id="b8930-203">ConnectNode(ID2D1TransformNode \*pFromNode, ID2D1TransformNode \*pToNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="b8930-204">Il metodo [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) connette l'output di una trasformazione a un altro input della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-204">The [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) method connects a transform's output to another transform's input.</span></span> <span data-ttu-id="b8930-205">Un output di trasformazione può essere connesso a più trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="b8930-205">A transform output can be connected to multiple transforms.</span></span>

### <a name="setoutputnodeid2d1transformnode-pnode"></a><span data-ttu-id="b8930-206">SetOutputNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="b8930-206">SetOutputNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="b8930-207">Il metodo [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) connette l'output di una trasformazione all'output dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-207">The [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) method connects a transform's output to the effect's output.</span></span> <span data-ttu-id="b8930-208">Poiché un effetto ha un solo output, solo una singola trasformazione può essere designata come ' nodo di output '.</span><span class="sxs-lookup"><span data-stu-id="b8930-208">Because an effect only has one output, only a single transform can be designated as the 'output node'.</span></span>

<span data-ttu-id="b8930-209">Questo codice usa due trasformazioni separate per creare un effetto unificato.</span><span class="sxs-lookup"><span data-stu-id="b8930-209">This code uses two separate transforms to create a unified effect.</span></span> <span data-ttu-id="b8930-210">In questo caso, l'effetto è un'ombreggiatura traslata.</span><span class="sxs-lookup"><span data-stu-id="b8930-210">In this case, the effect is a translated drop shadow.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a><span data-ttu-id="b8930-211">Aggiunta di proprietà personalizzate a un effetto</span><span class="sxs-lookup"><span data-stu-id="b8930-211">Adding custom properties to an effect</span></span>

<span data-ttu-id="b8930-212">Gli effetti possono definire proprietà personalizzate che consentono a un'app di modificare il comportamento dell'effetto durante il Runtime.</span><span class="sxs-lookup"><span data-stu-id="b8930-212">Effects can define custom properties that allow an app to change the effect's behavior during runtime.</span></span> <span data-ttu-id="b8930-213">Per definire una proprietà per un effetto personalizzato, è necessario eseguire tre passaggi:</span><span class="sxs-lookup"><span data-stu-id="b8930-213">There are three steps to define a property for a custom effect:</span></span>

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a><span data-ttu-id="b8930-214">Aggiungere i metadati della proprietà ai dati di registrazione dell'effetto</span><span class="sxs-lookup"><span data-stu-id="b8930-214">Add the property metadata to the effect's registration data</span></span>

### <a name="add-property-to-registration-xml"></a><span data-ttu-id="b8930-215">Aggiungere la proprietà a XML di registrazione</span><span class="sxs-lookup"><span data-stu-id="b8930-215">Add property to registration XML</span></span>

<span data-ttu-id="b8930-216">È necessario definire le proprietà di un effetto personalizzato durante la registrazione iniziale dell'effetto con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b8930-216">You must define a custom effect's properties during the effect's initial registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="b8930-217">In primo luogo, è necessario aggiornare il codice XML di registrazione dell'effetto nel metodo di registrazione pubblico con la nuova proprietà:</span><span class="sxs-lookup"><span data-stu-id="b8930-217">First, you must update the effect's registration XML in its public registration method with the new property:</span></span>


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



<span data-ttu-id="b8930-218">Quando si definisce una proprietà Effect in XML, è necessario un nome, un tipo e un nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="b8930-218">When you define an effect property in XML, it needs a name, a type, and a display name.</span></span> <span data-ttu-id="b8930-219">Il nome visualizzato di una proprietà, oltre ai valori di categoria, autore e Descrizione dell'effetto globale, può e deve essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="b8930-219">A property's display name, as well as the overall effect's category, author, and description values can and should be localized.</span></span>

<span data-ttu-id="b8930-220">Per ogni proprietà, un effetto può facoltativamente specificare valori predefiniti, min e max.</span><span class="sxs-lookup"><span data-stu-id="b8930-220">For each property, an effect can optionally specify default, min, and max values.</span></span> <span data-ttu-id="b8930-221">Questi valori sono destinati esclusivamente all'utilizzo informativo.</span><span class="sxs-lookup"><span data-stu-id="b8930-221">These values are for informational use only.</span></span> <span data-ttu-id="b8930-222">Non vengono applicati da [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b8930-222">They are not enforced by [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="b8930-223">È necessario implementare la logica predefinita/min/max specificata nella classe Effect.</span><span class="sxs-lookup"><span data-stu-id="b8930-223">It is up to you to implement any specified default/min/max logic in the effect class yourself.</span></span>

<span data-ttu-id="b8930-224">Il valore del tipo elencato nel codice XML per la proprietà deve corrispondere al tipo di dati corrispondente utilizzato dai metodi getter e setter della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b8930-224">The type value listed in the XML for the property must match the corresponding data type used by the property's getter and setter methods.</span></span> <span data-ttu-id="b8930-225">In questa tabella vengono visualizzati i valori XML corrispondenti per ogni tipo di dati:</span><span class="sxs-lookup"><span data-stu-id="b8930-225">Corresponding XML values for each data type are shown in this table:</span></span>



| <span data-ttu-id="b8930-226">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b8930-226">Data type</span></span>                                                                                                                              | <span data-ttu-id="b8930-227">Valore XML corrispondente</span><span class="sxs-lookup"><span data-stu-id="b8930-227">Corresponding XML value</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="b8930-228">PWSTR</span><span class="sxs-lookup"><span data-stu-id="b8930-228">PWSTR</span></span>                                                                                                                                  | <span data-ttu-id="b8930-229">string</span><span class="sxs-lookup"><span data-stu-id="b8930-229">string</span></span>                  |
| <span data-ttu-id="b8930-230">BOOL</span><span class="sxs-lookup"><span data-stu-id="b8930-230">BOOL</span></span>                                                                                                                                   | <span data-ttu-id="b8930-231">bool</span><span class="sxs-lookup"><span data-stu-id="b8930-231">bool</span></span>                    |
| <span data-ttu-id="b8930-232">UINT</span><span class="sxs-lookup"><span data-stu-id="b8930-232">UINT</span></span>                                                                                                                                   | <span data-ttu-id="b8930-233">uint32</span><span class="sxs-lookup"><span data-stu-id="b8930-233">uint32</span></span>                  |
| <span data-ttu-id="b8930-234">INT</span><span class="sxs-lookup"><span data-stu-id="b8930-234">INT</span></span>                                                                                                                                    | <span data-ttu-id="b8930-235">int32</span><span class="sxs-lookup"><span data-stu-id="b8930-235">int32</span></span>                   |
| <span data-ttu-id="b8930-236">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b8930-236">FLOAT</span></span>                                                                                                                                  | <span data-ttu-id="b8930-237">float</span><span class="sxs-lookup"><span data-stu-id="b8930-237">float</span></span>                   |
| [<span data-ttu-id="b8930-238">**D2D \_ vector \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="b8930-238">**D2D\_VECTOR\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | <span data-ttu-id="b8930-239">Vector2</span><span class="sxs-lookup"><span data-stu-id="b8930-239">vector2</span></span>                 |
| [<span data-ttu-id="b8930-240">**\_Vettore D2D \_ 3F**</span><span class="sxs-lookup"><span data-stu-id="b8930-240">**D2D\_VECTOR\_3F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | <span data-ttu-id="b8930-241">Vector3</span><span class="sxs-lookup"><span data-stu-id="b8930-241">vector3</span></span>                 |
| [<span data-ttu-id="b8930-242">**D2D \_ vector \_ 4F**</span><span class="sxs-lookup"><span data-stu-id="b8930-242">**D2D\_VECTOR\_4F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | <span data-ttu-id="b8930-243">Vector4</span><span class="sxs-lookup"><span data-stu-id="b8930-243">vector4</span></span>                 |
| <span data-ttu-id="b8930-244">[**\_Matrice D2D \_ 3x2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span><span class="sxs-lookup"><span data-stu-id="b8930-244">[**D2D\_MATRIX\_3X2\_F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span></span> | <span data-ttu-id="b8930-245">matrix3x2</span><span class="sxs-lookup"><span data-stu-id="b8930-245">matrix3x2</span></span>               |
| [<span data-ttu-id="b8930-246">**\_Matrice D2D \_ 4x3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="b8930-246">**D2D\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | <span data-ttu-id="b8930-247">matrix4x3</span><span class="sxs-lookup"><span data-stu-id="b8930-247">matrix4x3</span></span>               |
| [<span data-ttu-id="b8930-248">**D2D \_ Matrix \_ 4x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="b8930-248">**D2D\_MATRIX\_4X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | <span data-ttu-id="b8930-249">matrix4x4</span><span class="sxs-lookup"><span data-stu-id="b8930-249">matrix4x4</span></span>               |
| [<span data-ttu-id="b8930-250">**\_Matrice D2D \_ 5x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="b8930-250">**D2D\_MATRIX\_5X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | <span data-ttu-id="b8930-251">matrix5x4</span><span class="sxs-lookup"><span data-stu-id="b8930-251">matrix5x4</span></span>               |
| <span data-ttu-id="b8930-252">BYTE\[\]</span><span class="sxs-lookup"><span data-stu-id="b8930-252">BYTE\[\]</span></span>                                                                                                                               | <span data-ttu-id="b8930-253">blob</span><span class="sxs-lookup"><span data-stu-id="b8930-253">blob</span></span>                    |
| <span data-ttu-id="b8930-254">IUnknown\*</span><span class="sxs-lookup"><span data-stu-id="b8930-254">IUnknown\*</span></span>                                                                                                                             | <span data-ttu-id="b8930-255">IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8930-255">iunknown</span></span>                |
| <span data-ttu-id="b8930-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span><span class="sxs-lookup"><span data-stu-id="b8930-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span></span>                                                                                       | <span data-ttu-id="b8930-257">ColorContext</span><span class="sxs-lookup"><span data-stu-id="b8930-257">colorcontext</span></span>            |
| <span data-ttu-id="b8930-258">CLSID</span><span class="sxs-lookup"><span data-stu-id="b8930-258">CLSID</span></span>                                                                                                                                  | <span data-ttu-id="b8930-259">clsid</span><span class="sxs-lookup"><span data-stu-id="b8930-259">clsid</span></span>                   |
| <span data-ttu-id="b8930-260">Enumerazione ([**\_ \_ modalità di interpolazione d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode)e così via)</span><span class="sxs-lookup"><span data-stu-id="b8930-260">Enumeration ([**D2D1\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span></span>                                                | <span data-ttu-id="b8930-261">enum</span><span class="sxs-lookup"><span data-stu-id="b8930-261">enum</span></span>                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a><span data-ttu-id="b8930-262">Mappare la nuova proprietà ai metodi getter e setter</span><span class="sxs-lookup"><span data-stu-id="b8930-262">Map the new property to getter and setter methods</span></span>

<span data-ttu-id="b8930-263">Successivamente, l'effetto deve eseguire il mapping di questa nuova proprietà ai metodi getter e setter.</span><span class="sxs-lookup"><span data-stu-id="b8930-263">Next, the effect must map this new property to getter and setter methods.</span></span> <span data-ttu-id="b8930-264">Questa operazione viene eseguita tramite la matrice di [**\_ \_ associazione della proprietà d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) passata al metodo [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .</span><span class="sxs-lookup"><span data-stu-id="b8930-264">This is done through the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array that is passed into the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method.</span></span>

<span data-ttu-id="b8930-265">La matrice di [**\_ \_ associazione della proprietà d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b8930-265">The [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array looks like this:</span></span>


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



<span data-ttu-id="b8930-266">Dopo aver creato la matrice XML e bindings, passarli nel metodo [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :</span><span class="sxs-lookup"><span data-stu-id="b8930-266">Once you create the XML and bindings array, pass them into the [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method:</span></span>


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



<span data-ttu-id="b8930-267">Per la \_ \_ macro di associazione del tipo di valore d2d1 è \_ necessario che la classe Effect erediti da [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) prima di qualsiasi altra interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b8930-267">The D2D1\_VALUE\_TYPE\_BINDING macro requires the effect class to inherit from [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) before any other interface.</span></span>

<span data-ttu-id="b8930-268">Le proprietà personalizzate per un effetto vengono indicizzate nell'ordine in cui sono dichiarate nel codice XML e, una volta create, è possibile accedervi tramite l'app usando i metodi [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) e [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) .</span><span class="sxs-lookup"><span data-stu-id="b8930-268">Custom properties for an effect are indexed in the order they are declared in the XML, and once created can be accessed by the app using the [**ID2D1Properties::SetValue**](id2d1properties-setvalue-overload.md) and [**ID2D1Properties::GetValue**](id2d1properties-getvalue-overload.md) methods.</span></span> <span data-ttu-id="b8930-269">Per praticità, è possibile creare un'enumerazione pubblica che elenca ogni proprietà nel file di intestazione dell'effetto:</span><span class="sxs-lookup"><span data-stu-id="b8930-269">For convenience, you can create a public enumeration that lists each property in the effect's header file:</span></span>


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a><span data-ttu-id="b8930-270">Creare i metodi getter e setter per la proprietà</span><span class="sxs-lookup"><span data-stu-id="b8930-270">Create the getter and setter methods for the property</span></span>

<span data-ttu-id="b8930-271">Il passaggio successivo consiste nel creare i metodi getter e setter per la nuova proprietà.</span><span class="sxs-lookup"><span data-stu-id="b8930-271">The next step is to create the getter and setter methods for the new property.</span></span> <span data-ttu-id="b8930-272">I nomi dei metodi devono corrispondere a quelli specificati nella matrice di [**\_ \_ associazione della proprietà d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) .</span><span class="sxs-lookup"><span data-stu-id="b8930-272">The names of the methods must match the ones specified in the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array.</span></span> <span data-ttu-id="b8930-273">Inoltre, il tipo di proprietà specificato nel codice XML dell'effetto deve corrispondere al tipo del parametro del metodo di impostazione e al valore restituito del metodo Get.</span><span class="sxs-lookup"><span data-stu-id="b8930-273">In addition, the property type specified in the effect's XML must match the type of the setter method's parameter and the getter method's return value.</span></span>


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a><span data-ttu-id="b8930-274">Trasformazioni dell'effetto aggiornamento in risposta alla modifica di una proprietà</span><span class="sxs-lookup"><span data-stu-id="b8930-274">Update effect's transforms in response to property change</span></span>

<span data-ttu-id="b8930-275">Per aggiornare effettivamente l'output di un'immagine di un effetto in risposta a una modifica di proprietà, l'effetto deve modificare le trasformazioni sottostanti.</span><span class="sxs-lookup"><span data-stu-id="b8930-275">To actually update an effect's image output in response to a property change, the effect needs to change its underlying transforms.</span></span> <span data-ttu-id="b8930-276">Questa operazione viene in genere eseguita nel metodo [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) dell'effetto che [Direct2D](./direct2d-portal.md) chiama automaticamente quando una delle proprietà di un effetto è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="b8930-276">This is typically done in the effect's [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method which [Direct2D](./direct2d-portal.md) automatically calls when one of an effect's properties has been changed.</span></span> <span data-ttu-id="b8930-277">Tuttavia, le trasformazioni possono essere aggiornate in qualsiasi metodo dell'effetto, ad esempio Initialize o i metodi di impostazione delle proprietà dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-277">However, transforms can be updated in any of the effect's methods: such as Initialize or the effect's property setter methods.</span></span>

<span data-ttu-id="b8930-278">Ad esempio, se un effetto contiene un [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) e si vuole modificare il valore di offset in risposta alla proprietà offset dell'effetto da modificare, il codice seguente verrà aggiunto in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span><span class="sxs-lookup"><span data-stu-id="b8930-278">For example, if an effect contained an [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) and wanted to modify its offset value in response to the effect's Offset property being changed, it would add the following code in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span></span>


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a><span data-ttu-id="b8930-279">Creazione di una trasformazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b8930-279">Creating a custom transform</span></span>

<span data-ttu-id="b8930-280">Per implementare le operazioni sulle immagini oltre a quelle fornite in [Direct2D](./direct2d-portal.md), è necessario implementare trasformazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="b8930-280">To implement image operations beyond what is provided in [Direct2D](./direct2d-portal.md), you must implement custom transforms.</span></span> <span data-ttu-id="b8930-281">Le trasformazioni personalizzate possono modificare arbitrariamente un'immagine di input tramite l'uso di shader HLSL personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b8930-281">Custom transforms can arbitrarily change an input image through the use of custom HLSL shaders.</span></span>

<span data-ttu-id="b8930-282">Le trasformazioni implementano una di due diverse interfacce a seconda dei tipi di shader utilizzati.</span><span class="sxs-lookup"><span data-stu-id="b8930-282">Transforms implement one of two different interfaces depending on the types of shaders they use.</span></span> <span data-ttu-id="b8930-283">Le trasformazioni che usano pixel e/o vertex shader devono implementare [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), mentre le trasformazioni che usano compute shader devono implementare [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span><span class="sxs-lookup"><span data-stu-id="b8930-283">Transforms using pixel and/or vertex shaders must implement [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), while transforms using compute shaders must implement [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span></span> <span data-ttu-id="b8930-284">Entrambe le interfacce ereditano da [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="b8930-284">These interfaces both inherit from [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span> <span data-ttu-id="b8930-285">Questa sezione è incentrata sull'implementazione della funzionalità comune a entrambe.</span><span class="sxs-lookup"><span data-stu-id="b8930-285">This section focuses on implementing the functionality that is common to both.</span></span>

<span data-ttu-id="b8930-286">L'interfaccia [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) dispone di quattro metodi per implementare:</span><span class="sxs-lookup"><span data-stu-id="b8930-286">The [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface has four methods to implement:</span></span>

### <a name="getinputcount"></a><span data-ttu-id="b8930-287">GetInputCount</span><span class="sxs-lookup"><span data-stu-id="b8930-287">GetInputCount</span></span>

<span data-ttu-id="b8930-288">Questo metodo restituisce un Integer che rappresenta il numero di input per la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-288">This method returns an integer representing the input count for the transform.</span></span>


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a><span data-ttu-id="b8930-289">MapInputRectsToOutputRect</span><span class="sxs-lookup"><span data-stu-id="b8930-289">MapInputRectsToOutputRect</span></span>

<span data-ttu-id="b8930-290">[Direct2D](./direct2d-portal.md) chiama il metodo [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) ogni volta che viene eseguito il rendering della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-290">[Direct2D](./direct2d-portal.md) calls the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) method each time the transform is rendered.</span></span> <span data-ttu-id="b8930-291">Direct2D passa un rettangolo che rappresenta i limiti di ogni input alla trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-291">Direct2D passes a rectangle representing the bounds of each of the inputs to the transform.</span></span> <span data-ttu-id="b8930-292">La trasformazione è quindi responsabile del calcolo dei limiti dell'immagine di output.</span><span class="sxs-lookup"><span data-stu-id="b8930-292">The transform is then responsible for calculating the bounds of the output image.</span></span> <span data-ttu-id="b8930-293">Le dimensioni dei rettangoli per tutti i metodi in questa interfaccia ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) sono definite in pixel, non in DIP.</span><span class="sxs-lookup"><span data-stu-id="b8930-293">The size of the rectangles for all the methods on this interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) are defined in pixels, not DIPs.</span></span>

<span data-ttu-id="b8930-294">Questo metodo è anche responsabile del calcolo dell'area dell'output che è opaca in base alla logica dello shader e alle aree opache di ogni input.</span><span class="sxs-lookup"><span data-stu-id="b8930-294">This method is also responsible for calculating the region of the output that is opaque based on the logic of its shader and the opaque regions of each input.</span></span> <span data-ttu-id="b8930-295">Un'area opaca di un'immagine è definita come quella in cui il canale alfa è' 1' per l'intero rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b8930-295">An opaque region of an image is defined as that where the alpha channel is '1' for the entirety of the rectangle.</span></span> <span data-ttu-id="b8930-296">Se non è chiaro se l'output di una trasformazione è opaco, il rettangolo di output opaco deve essere impostato su (0, 0, 0, 0) come valore sicuro.</span><span class="sxs-lookup"><span data-stu-id="b8930-296">If it is unclear whether a transform's output is opaque, the output opaque rectangle should be set to (0, 0, 0, 0) as a safe value.</span></span> <span data-ttu-id="b8930-297">[Direct2D](./direct2d-portal.md) utilizza queste informazioni per eseguire le ottimizzazioni del rendering con contenuto "opaco garantito".</span><span class="sxs-lookup"><span data-stu-id="b8930-297">[Direct2D](./direct2d-portal.md) uses this info to perform rendering optimizations with 'guaranteed opaque' content.</span></span> <span data-ttu-id="b8930-298">Se questo valore non è accurato, può causare il rendering errato.</span><span class="sxs-lookup"><span data-stu-id="b8930-298">If this value is inaccurate, it can result in incorrect rendering.</span></span>

<span data-ttu-id="b8930-299">È possibile modificare il comportamento di rendering della trasformazione (come definito nelle sezioni da 6 a 8) durante questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b8930-299">The you can modify the transform's rendering behavior (as defined in sections 6 through 8) during this method.</span></span> <span data-ttu-id="b8930-300">Tuttavia, non è possibile modificare altre trasformazioni nel grafico di trasformazione o il layout del grafico qui.</span><span class="sxs-lookup"><span data-stu-id="b8930-300">However, the you can't modify other transforms in the transform graph, or the graph layout itself here.</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



<span data-ttu-id="b8930-301">Per un esempio più complesso, prendere in considerazione la modalità di rappresentazione di una semplice operazione di sfocatura:</span><span class="sxs-lookup"><span data-stu-id="b8930-301">For a more complex example, consider how a simple blur operation would be represented:</span></span>

<span data-ttu-id="b8930-302">Se un'operazione di sfocatura usa un raggio di 5 pixel, le dimensioni del rettangolo di output devono espandersi di 5 pixel, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b8930-302">If a blur operation uses a 5 pixel radius, the size of the output rectangle must expand by 5 pixels, as shown below.</span></span> <span data-ttu-id="b8930-303">Quando si modificano le coordinate del rettangolo, una trasformazione deve garantire che la logica non causi alcun overflow nelle coordinate del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b8930-303">When modifying rectangle coordinates, a transform must ensure that its logic does not cause any over/underflows in the rectangle coordinates.</span></span>


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



<span data-ttu-id="b8930-304">Poiché l'immagine è sfocata, un'area dell'immagine opaca potrebbe ora essere parzialmente trasparente.</span><span class="sxs-lookup"><span data-stu-id="b8930-304">Because the image is blurred, a region of the image which was opaque may now be partially transparent.</span></span> <span data-ttu-id="b8930-305">Ciò è dovuto al fatto che l'area al di fuori dell'immagine viene impostata sul nero trasparente e tale trasparenza verrà mescolata nell'immagine intorno ai bordi.</span><span class="sxs-lookup"><span data-stu-id="b8930-305">This is because the area outside the image defaults to transparent black and this transparency will be blended into the image around the edges.</span></span> <span data-ttu-id="b8930-306">La trasformazione deve riflettere questa operazione nei calcoli dei rettangoli opachi di output:</span><span class="sxs-lookup"><span data-stu-id="b8930-306">The transform must reflect this in its output opaque rectangle calculations:</span></span>


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



<span data-ttu-id="b8930-307">Questi calcoli vengono visualizzati qui:</span><span class="sxs-lookup"><span data-stu-id="b8930-307">These calculations are visualized here:</span></span>

![illustrazione del calcolo del rettangolo.](images/custom-effects2.png)

<span data-ttu-id="b8930-309">Per ulteriori informazioni su questo metodo, vedere la pagina di riferimento di [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .</span><span class="sxs-lookup"><span data-stu-id="b8930-309">For more info about this method, see the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) reference page.</span></span>

### <a name="mapoutputrecttoinputrects"></a><span data-ttu-id="b8930-310">MapOutputRectToInputRects</span><span class="sxs-lookup"><span data-stu-id="b8930-310">MapOutputRectToInputRects</span></span>

<span data-ttu-id="b8930-311">[Direct2D](./direct2d-portal.md) chiama il metodo [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) dopo [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="b8930-311">[Direct2D](./direct2d-portal.md) calls the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) method after [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="b8930-312">La trasformazione deve calcolare la porzione dell'immagine da leggere per eseguire correttamente il rendering dell'area di output richiesta.</span><span class="sxs-lookup"><span data-stu-id="b8930-312">The transform must calculate what portion of the image it needs to read from in order to correctly render the requested output region.</span></span>

<span data-ttu-id="b8930-313">Come prima, se un effetto esegue esclusivamente il mapping dei pixel 1-1, può passare il rettangolo di output al rettangolo di input:</span><span class="sxs-lookup"><span data-stu-id="b8930-313">As before, if an effect strictly maps pixels 1-1, it can pass the output rectangle through to the input rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



<span data-ttu-id="b8930-314">Analogamente, se una trasformazione compatta o espande un'immagine, come nell'esempio di sfocatura, i pixel utilizzano spesso i pixel circostanti per calcolare il relativo valore.</span><span class="sxs-lookup"><span data-stu-id="b8930-314">Likewise, if a transform shrinks or expands an image (like the blur example here), pixels often use surrounding pixels to calculate their value.</span></span> <span data-ttu-id="b8930-315">Con una sfocatura, viene calcolata la media di un pixel con i pixel circostanti, anche se si trovano all'esterno dei limiti dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="b8930-315">With a blur, a pixel is averaged with its surrounding pixels, even if they are outside of the bounds of the input image.</span></span> <span data-ttu-id="b8930-316">Questo comportamento si riflette nel calcolo.</span><span class="sxs-lookup"><span data-stu-id="b8930-316">This behavior is reflected in the calculation.</span></span> <span data-ttu-id="b8930-317">Come prima, la trasformazione controlla gli overflow quando si espandono le coordinate di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b8930-317">As before, the transform checks for overflows when expanding a rectangle's coordinates.</span></span>


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



<span data-ttu-id="b8930-318">Questa figura Visualizza il calcolo.</span><span class="sxs-lookup"><span data-stu-id="b8930-318">This figure visualizes the calculation.</span></span> <span data-ttu-id="b8930-319">[Direct2D](./direct2d-portal.md) esegue automaticamente il campionamento di pixel neri trasparenti in cui l'immagine di input non esiste, consentendo la fusione graduale della sfocatura con il contenuto esistente sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="b8930-319">[Direct2D](./direct2d-portal.md) automatically samples transparent black pixels where the input image doesn't exist, allowing the blur to be blended gradually with the existing content on the screen.</span></span>

![illustrazione di un campionamento di effetto di pixel neri trasparenti all'esterno di un rettangolo.](images/custom-effects3.png)

<span data-ttu-id="b8930-321">Se il mapping non è semplice, questo metodo deve impostare il rettangolo di input sull'area massima per garantire i risultati corretti.</span><span class="sxs-lookup"><span data-stu-id="b8930-321">If the mapping is non-trivial, then this method should set the input rectangle to the maximum area to guarantee correct results.</span></span> <span data-ttu-id="b8930-322">A tale scopo, impostare i bordi sinistro e superiore su INT \_ min e i bordi destro e inferiore su int \_ max.</span><span class="sxs-lookup"><span data-stu-id="b8930-322">To do this, set the left and top edges to INT\_MIN, and the right and bottom edges to INT\_MAX.</span></span>

<span data-ttu-id="b8930-323">Per ulteriori informazioni su questo metodo, vedere l'argomento [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .</span><span class="sxs-lookup"><span data-stu-id="b8930-323">For more info about this method, see the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) topic.</span></span>

### <a name="mapinvalidrect"></a><span data-ttu-id="b8930-324">MapInvalidRect</span><span class="sxs-lookup"><span data-stu-id="b8930-324">MapInvalidRect</span></span>

<span data-ttu-id="b8930-325">[Direct2D](./direct2d-portal.md) chiama anche il metodo [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="b8930-325">[Direct2D](./direct2d-portal.md) also calls the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) method.</span></span> <span data-ttu-id="b8930-326">Tuttavia, a differenza dei metodi [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) e [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) Direct2D, non è garantito che lo chiami in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="b8930-326">However, unlike the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) and [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) methods Direct2D is not guaranteed to call it at any particular time.</span></span> <span data-ttu-id="b8930-327">Questo metodo stabilisce concettualmente quale parte dell'output di una trasformazione deve essere di nuovo sottoposta a rendering in risposta a una parte o a tutte le modifiche apportate all'input.</span><span class="sxs-lookup"><span data-stu-id="b8930-327">This method conceptually decides what part of a transform's output needs to be re-rendered in response to part or all of its input changing.</span></span> <span data-ttu-id="b8930-328">Esistono tre scenari diversi per i quali calcolare un oggetto Rect non valido della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-328">There are three different scenarios for which to calculate a transform's invalid rect.</span></span>

### <a name="transforms-with-one-to-one-pixel-mapping"></a><span data-ttu-id="b8930-329">Trasformazioni con mapping di pixel uno-a-uno</span><span class="sxs-lookup"><span data-stu-id="b8930-329">Transforms with one-to-one pixel mapping</span></span>

<span data-ttu-id="b8930-330">Per le trasformazioni che mappano i pixel 1-1, passare semplicemente il rettangolo di input non valido al rettangolo di output non valido:</span><span class="sxs-lookup"><span data-stu-id="b8930-330">For transforms that map pixels 1-1, simply pass the invalid input rectangle through to the invalid output rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a><span data-ttu-id="b8930-331">Trasformazioni con mapping di pixel molti-a-molti</span><span class="sxs-lookup"><span data-stu-id="b8930-331">Transforms with many-to-many pixel mapping</span></span>

<span data-ttu-id="b8930-332">Quando i pixel di output di una trasformazione dipendono dall'area circostante, il rettangolo di input non valido deve essere espanso.</span><span class="sxs-lookup"><span data-stu-id="b8930-332">When a transform's output pixels are dependent on their surrounding area, the invalid input rectangle must correspondingly be expanded.</span></span> <span data-ttu-id="b8930-333">In questo modo si riflette che i pixel che racchiudono il rettangolo di input non valido saranno interessati e diventeranno non validi.</span><span class="sxs-lookup"><span data-stu-id="b8930-333">This is to reflect that pixels surrounding the invalid input rectangle will also be affected and become invalid.</span></span> <span data-ttu-id="b8930-334">Ad esempio, una sfocatura di cinque pixel usa il calcolo seguente:</span><span class="sxs-lookup"><span data-stu-id="b8930-334">For example, a five pixel blur uses the following calculation:</span></span>


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a><span data-ttu-id="b8930-335">Trasformazioni con mapping di pixel complessi</span><span class="sxs-lookup"><span data-stu-id="b8930-335">Transforms with complex pixel mapping</span></span>

<span data-ttu-id="b8930-336">Per le trasformazioni in cui i pixel di input e di output non dispongono di un mapping semplice, l'intero output può essere contrassegnato come non valido.</span><span class="sxs-lookup"><span data-stu-id="b8930-336">For transforms where input and output pixels do not have a simple mapping, the entire output can be marked as invalid.</span></span> <span data-ttu-id="b8930-337">Se, ad esempio, una trasformazione restituisce semplicemente il colore medio dell'input, viene modificato l'intero output della trasformazione se viene modificata anche una piccola parte dell'input.</span><span class="sxs-lookup"><span data-stu-id="b8930-337">For example, if a transform simply outputs the average color of the input, the entire output of the transform changes if even a small part of the input is changed.</span></span> <span data-ttu-id="b8930-338">In questo caso, il rettangolo di output non valido deve essere impostato su un rettangolo logicamente infinito (mostrato di seguito).</span><span class="sxs-lookup"><span data-stu-id="b8930-338">In this case, the invalid output rectangle should be set to a logically infinite rectangle (shown below).</span></span> <span data-ttu-id="b8930-339">[Direct2D](./direct2d-portal.md) lo blocca automaticamente ai limiti dell'output.</span><span class="sxs-lookup"><span data-stu-id="b8930-339">[Direct2D](./direct2d-portal.md) automatically clamps this to the bounds of the output.</span></span>


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



<span data-ttu-id="b8930-340">Per ulteriori informazioni su questo metodo, vedere l'argomento [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="b8930-340">For more info about this method, see the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) topic.</span></span>

<span data-ttu-id="b8930-341">Una volta implementati questi metodi, l'intestazione della trasformazione conterrà quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b8930-341">Once these methods have been implemented, your transform's header will contain the following:</span></span>


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a><span data-ttu-id="b8930-342">Aggiunta di un pixel shader a una trasformazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b8930-342">Adding a pixel shader to a custom transform</span></span>

<span data-ttu-id="b8930-343">Una volta creata, una trasformazione deve fornire uno shader che modifichi i pixel dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8930-343">Once a transform has been created, it needs to provide a shader that will manipulate the image pixels.</span></span> <span data-ttu-id="b8930-344">In questa sezione vengono illustrati i passaggi per l'utilizzo di un pixel shader con una trasformazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="b8930-344">This section covers the steps to using a pixel shader with a custom transform.</span></span>

### <a name="implementing-id2d1drawtransform"></a><span data-ttu-id="b8930-345">Implementazione di ID2D1DrawTransform</span><span class="sxs-lookup"><span data-stu-id="b8930-345">Implementing ID2D1DrawTransform</span></span>

<span data-ttu-id="b8930-346">Per usare un pixel shader, la trasformazione deve implementare l'interfaccia [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , che eredita dall'interfaccia [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) descritta nella sezione 5.</span><span class="sxs-lookup"><span data-stu-id="b8930-346">To use a pixel shader, the transform must implement the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, which inherits from the [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface described in section 5.</span></span> <span data-ttu-id="b8930-347">Questa interfaccia contiene un nuovo metodo da implementare:</span><span class="sxs-lookup"><span data-stu-id="b8930-347">This interface contains one new method to implement:</span></span>

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a><span data-ttu-id="b8930-348">SetDrawInfo (ID2D1DrawInfo \* pDrawInfo)</span><span class="sxs-lookup"><span data-stu-id="b8930-348">SetDrawInfo(ID2D1DrawInfo \*pDrawInfo)</span></span>

<span data-ttu-id="b8930-349">[Direct2D](./direct2d-portal.md) chiama il metodo [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) quando la trasformazione viene aggiunta per la prima volta al grafico di trasformazione di un effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-349">[Direct2D](./direct2d-portal.md) calls the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="b8930-350">Questo metodo fornisce un parametro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) che controlla il modo in cui viene eseguito il rendering della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-350">This method provides an [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="b8930-351">Vedere l'argomento **ID2D1DrawInfo** per i metodi disponibili qui.</span><span class="sxs-lookup"><span data-stu-id="b8930-351">See the **ID2D1DrawInfo** topic for the methods available here.</span></span>

<span data-ttu-id="b8930-352">Se la trasformazione sceglie di archiviare questo parametro come variabile membro della classe, è possibile accedere all'oggetto *drawInfo* e modificarlo da altri metodi, ad esempio setter di proprietà o [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="b8930-352">If the transform chooses to store this parameter as a class member variable, the *drawInfo* object can be accessed and changed from other methods such as property setters or [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="b8930-353">In particolare, non è possibile chiamare i metodi [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) o [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) in [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="b8930-353">Notably, it cannot be called from the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) or [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods on [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span>

### <a name="creating-a-guid-for-the-pixel-shader"></a><span data-ttu-id="b8930-354">Creazione di un GUID per la pixel shader</span><span class="sxs-lookup"><span data-stu-id="b8930-354">Creating a GUID for the pixel shader</span></span>

<span data-ttu-id="b8930-355">Successivamente, la trasformazione deve definire un GUID univoco per il pixel shader stesso.</span><span class="sxs-lookup"><span data-stu-id="b8930-355">Next, the transform must define a unique GUID for the pixel shader itself.</span></span> <span data-ttu-id="b8930-356">Questa operazione viene utilizzata quando [Direct2D](./direct2d-portal.md) carica lo shader in memoria, così come quando la trasformazione sceglie quali pixel shader utilizzare per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b8930-356">This is used when [Direct2D](./direct2d-portal.md) loads the shader into memory, as well as when the transform chooses which pixel shader to use for execution.</span></span> <span data-ttu-id="b8930-357">Per generare un GUID casuale, è possibile usare strumenti come guidgen.exe, incluso in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b8930-357">Tools such as guidgen.exe, which is included with Visual Studio, can be used to generate a random GUID.</span></span>


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a><span data-ttu-id="b8930-358">Caricamento della pixel shader con Direct2D</span><span class="sxs-lookup"><span data-stu-id="b8930-358">Loading the pixel shader with Direct2D</span></span>

<span data-ttu-id="b8930-359">Prima di poter utilizzare la trasformazione, è necessario che un pixel shader venga caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="b8930-359">A pixel shader must be loaded into memory before it can be used by the transform.</span></span>

<span data-ttu-id="b8930-360">Per caricare il pixel shader in memoria, la trasformazione deve leggere il codice byte compilato dello shader da. File CSO generato da Visual Studio (per informazioni dettagliate, vedere la documentazione di [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ) in una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="b8930-360">To load the pixel shader into memory, the transform should read the compiled shader byte code from the .CSO file generated by Visual Studio (see [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details) into a byte array.</span></span> <span data-ttu-id="b8930-361">Questa tecnica è illustrata in dettaglio nell' [esempio SDK D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="b8930-361">This technique is demonstrated in detail in the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="b8930-362">Una volta che i dati dello shader sono stati caricati in una matrice di byte, chiamare il metodo [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) sull'oggetto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-362">Once the shader data has been loaded into a byte array, call the [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) method on the effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object.</span></span> <span data-ttu-id="b8930-363">[Direct2D](./direct2d-portal.md) ignora le chiamate a **LoadPixelShader** quando uno shader con lo stesso GUID è già stato caricato.</span><span class="sxs-lookup"><span data-stu-id="b8930-363">[Direct2D](./direct2d-portal.md) ignores calls to **LoadPixelShader** when a shader with the same GUID has already been loaded.</span></span>

<span data-ttu-id="b8930-364">Dopo che un pixel shader è stato caricato in memoria, la trasformazione deve selezionarla per l'esecuzione passando il relativo GUID al metodo [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) sul parametro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fornito durante il metodo [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) .</span><span class="sxs-lookup"><span data-stu-id="b8930-364">After a pixel shader has been loaded into memory, the transform needs to select it for execution by passing its GUID to the [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided during the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="b8930-365">Il pixel shader deve essere già caricato in memoria prima di essere selezionato per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b8930-365">The pixel shader must be already loaded into memory before being selected for execution.</span></span>

### <a name="changing-shader-operation-with-constant-buffers"></a><span data-ttu-id="b8930-366">Modifica dell'operazione dello shader con i buffer costanti</span><span class="sxs-lookup"><span data-stu-id="b8930-366">Changing shader operation with constant buffers</span></span>

<span data-ttu-id="b8930-367">Per modificare la modalità di esecuzione di uno shader, una trasformazione può passare un buffer costante al pixel shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-367">To change how a shader executes, a transform may pass a constant buffer to the pixel shader.</span></span> <span data-ttu-id="b8930-368">A tale scopo, una trasformazione definisce uno struct che contiene le variabili desiderate nell'intestazione della classe:</span><span class="sxs-lookup"><span data-stu-id="b8930-368">To do so, a transform defines a struct that contains the desired variables in the class header:</span></span>


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



<span data-ttu-id="b8930-369">La trasformazione chiama quindi il metodo [**ID2D1DrawInfo:: SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) sul parametro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fornito nel metodo [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) per passare questo buffer allo shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-369">The transform then calls the [**ID2D1DrawInfo::SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided in the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method to pass this buffer to the shader.</span></span>

<span data-ttu-id="b8930-370">Il [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) deve anche definire uno struct corrispondente che rappresenta il buffer costante.</span><span class="sxs-lookup"><span data-stu-id="b8930-370">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) also needs to define a corresponding struct that represents the constant buffer.</span></span> <span data-ttu-id="b8930-371">Le variabili contenute nello struct dello shader devono corrispondere a quelle nello struct della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-371">The variables contained in the shader's struct must match those in the transform's struct.</span></span>


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



<span data-ttu-id="b8930-372">Una volta definito il buffer, i valori contenuti in possono essere letti da qualsiasi posizione all'interno del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-372">Once the buffer has been defined, the values contained within can be read from anywhere within the pixel shader.</span></span>

### <a name="writing-a-pixel-shader-for-direct2d"></a><span data-ttu-id="b8930-373">Scrittura di un pixel shader per Direct2D</span><span class="sxs-lookup"><span data-stu-id="b8930-373">Writing a pixel shader for Direct2D</span></span>

<span data-ttu-id="b8930-374">Le trasformazioni [Direct2D](./direct2d-portal.md) usano gli shader creati usando [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)standard.</span><span class="sxs-lookup"><span data-stu-id="b8930-374">[Direct2D](./direct2d-portal.md) transforms use shaders authored using standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="b8930-375">Tuttavia, esistono alcuni concetti chiave per la scrittura di una pixel shader eseguita dal contesto di una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-375">However, there are a few key concepts to writing a pixel shader that executes from the context of a transform.</span></span> <span data-ttu-id="b8930-376">Per un esempio completo di pixel shader completamente funzionale, vedere l'esempio [D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="b8930-376">For a completed example of a fully functionally pixel shader, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="b8930-377">[Direct2D](./direct2d-portal.md) esegue automaticamente il mapping degli input di una trasformazione agli oggetti [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) in HLSL.</span><span class="sxs-lookup"><span data-stu-id="b8930-377">[Direct2D](./direct2d-portal.md) automatically maps a transform's inputs to [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) objects in the HLSL.</span></span> <span data-ttu-id="b8930-378">Il primo **Texture2D** si trova in Register T0 e il primo **SamplerState** si trova in Register S0.</span><span class="sxs-lookup"><span data-stu-id="b8930-378">The first **Texture2D** is located at register t0, and the first **SamplerState** is located at register s0.</span></span> <span data-ttu-id="b8930-379">Ogni input aggiuntivo si trova nei registri corrispondenti successivi (ad esempio T1 e S1).</span><span class="sxs-lookup"><span data-stu-id="b8930-379">Each additional input is located at the next corresponding registers (t1 and s1 for example).</span></span> <span data-ttu-id="b8930-380">È possibile campionare i dati dei pixel per un particolare input chiamando Sample nell'oggetto **Texture2D** e passando l'oggetto **SamplerState** corrispondente e le coordinate Texel.</span><span class="sxs-lookup"><span data-stu-id="b8930-380">Pixel data for a particular input can be sampled by calling Sample on the **Texture2D** object and passing in the corresponding **SamplerState** object and the texel coordinates.</span></span>

<span data-ttu-id="b8930-381">Una pixel shader personalizzata viene eseguita una volta per ogni pixel di cui viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="b8930-381">A custom pixel shader is run once for each pixel that is rendered.</span></span> <span data-ttu-id="b8930-382">Ogni volta che viene eseguito lo shader, [Direct2D](./direct2d-portal.md) fornisce automaticamente tre parametri che ne identificano la posizione di esecuzione corrente:</span><span class="sxs-lookup"><span data-stu-id="b8930-382">Each time the shader is run, [Direct2D](./direct2d-portal.md) automatically provides three parameters that identify its current execution position:</span></span>

-   <span data-ttu-id="b8930-383">Scena-output dello spazio: questo parametro rappresenta la posizione di esecuzione corrente in termini di superficie di destinazione complessiva.</span><span class="sxs-lookup"><span data-stu-id="b8930-383">Scene-space output: This parameter represents the current execution position in terms of the overall target surface.</span></span> <span data-ttu-id="b8930-384">Viene definito in pixel e i relativi valori min/max corrispondono ai limiti del rettangolo restituito da [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="b8930-384">It is defined in pixels and its min/max values correspond to the bounds of the rectangle returned by [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span>
-   <span data-ttu-id="b8930-385">Clip-spazio output: questo parametro viene usato da Direct3D e non deve essere usato nel pixel shader di una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-385">Clip-space output: This parameter is used by Direct3D, and is must not be used in a transform's pixel shader.</span></span>
-   <span data-ttu-id="b8930-386">Texel-input di spazio: questo parametro rappresenta la posizione di esecuzione corrente in una particolare trama di input.</span><span class="sxs-lookup"><span data-stu-id="b8930-386">Texel-space input: This parameter represents the current execution position in a particular input texture.</span></span> <span data-ttu-id="b8930-387">Uno shader non deve prendere alcuna dipendenza dal modo in cui questo valore viene calcolato.</span><span class="sxs-lookup"><span data-stu-id="b8930-387">A shader should not take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="b8930-388">Deve essere usato solo per campionare l'input del pixel shader, come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="b8930-388">It should only use it to sample the pixel shader's input, as shown in the code below:</span></span>


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a><span data-ttu-id="b8930-389">Aggiunta di un vertex shader a una trasformazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b8930-389">Adding a vertex shader to a custom transform</span></span>

<span data-ttu-id="b8930-390">È possibile utilizzare vertex shader per eseguire scenari di imaging diversi rispetto ai pixel shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-390">You can use vertex shaders to accomplish different imaging scenarios than pixel shaders.</span></span> <span data-ttu-id="b8930-391">In particolare, i vertex shader possono eseguire gli effetti di un'immagine basata sulla geometria trasformando i vertici che costituiscono un'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8930-391">In particular, vertex shaders can perform geometry-based image effects by transforming vertices that comprise an image.</span></span> <span data-ttu-id="b8930-392">I vertex shader possono essere usati indipendentemente da o insieme ai pixel shader specificati dalla trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-392">Vertex shaders can be used independently of or in conjunction with transform-specified pixel shaders.</span></span> <span data-ttu-id="b8930-393">Se non si specifica un vertex shader, il [Direct2D](./direct2d-portal.md) sostituisce in un vertex shader predefinito per l'uso con la pixel shader personalizzata.</span><span class="sxs-lookup"><span data-stu-id="b8930-393">If a vertex shader is not specified, [Direct2D](./direct2d-portal.md) substitutes in a default vertex shader for use with the custom pixel shader.</span></span>

<span data-ttu-id="b8930-394">Il processo per l'aggiunta di un vertex shader a una trasformazione personalizzata è simile a quello di un pixel shader: la trasformazione implementa l'interfaccia [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , crea un GUID e (facoltativamente) passa buffer costanti allo shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-394">The process for adding a vertex shader to a custom transform is similar to that of a pixel shader – the transform implements the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, creates a GUID, and (optionally) passes constant buffers to the shader.</span></span> <span data-ttu-id="b8930-395">Tuttavia, esistono alcuni passaggi chiave aggiuntivi che sono univoci per i vertex shader:</span><span class="sxs-lookup"><span data-stu-id="b8930-395">However, there are a few key additional steps that are unique to vertex shaders:</span></span>

### <a name="creating-a-vertex-buffer"></a><span data-ttu-id="b8930-396">Creazione di un buffer vertici</span><span class="sxs-lookup"><span data-stu-id="b8930-396">Creating a vertex buffer</span></span>

<span data-ttu-id="b8930-397">Un vertex shader per definizione viene eseguito sui vertici passati, non sui singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="b8930-397">A vertex shader by definition executes on vertices passed to it, not individual pixels.</span></span> <span data-ttu-id="b8930-398">Per specificare i vertici per l'esecuzione dello shader, una trasformazione crea un buffer del vertice da passare allo shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-398">To specify the vertices for the shader to execute on, a transform creates a vertex buffer to pass to the shader.</span></span> <span data-ttu-id="b8930-399">Il layout dei buffer dei vertici esula dall'ambito di questo documento.</span><span class="sxs-lookup"><span data-stu-id="b8930-399">The layout of vertex buffers is beyond the scope of this document.</span></span> <span data-ttu-id="b8930-400">Per informazioni dettagliate, vedere il [riferimento a Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o l' [esempio SDK D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) per un'implementazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="b8930-400">Please see the [Direct3D reference](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) for details, or the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="b8930-401">Dopo la creazione di un buffer vertex in memoria, la trasformazione usa il metodo [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) sull'oggetto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) dell'effetto contenitore per passare i dati alla GPU.</span><span class="sxs-lookup"><span data-stu-id="b8930-401">After creating a vertex buffer in memory, the transform uses the [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) method on the containing effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object to pass that data to the GPU.</span></span> <span data-ttu-id="b8930-402">Per un'implementazione di esempio, vedere l' [esempio D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) .</span><span class="sxs-lookup"><span data-stu-id="b8930-402">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="b8930-403">Se non viene specificato alcun vertex buffer dalla trasformazione, [Direct2D](./direct2d-portal.md) passa un buffer dei vertici predefinito che rappresenta la posizione dell'immagine rettangolare.</span><span class="sxs-lookup"><span data-stu-id="b8930-403">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) passes a default vertex buffer representing the rectangular image location.</span></span>

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a><span data-ttu-id="b8930-404">Modifica di SetDrawInfo per utilizzare un vertex shader</span><span class="sxs-lookup"><span data-stu-id="b8930-404">Changing SetDrawInfo to utilize a vertex shader</span></span>

<span data-ttu-id="b8930-405">Analogamente a quanto avviene con i pixel shader, la trasformazione deve caricare e selezionare un vertex shader per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b8930-405">Like with pixel shaders, the transform must load and select a vertex shader for execution.</span></span> <span data-ttu-id="b8930-406">Per caricare il vertex shader, chiama il metodo [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) sul metodo [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) ricevuto nel metodo Initialize dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-406">To load the vertex shader, it calls the [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) method on the [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) method received in the effect's Initialize method.</span></span> <span data-ttu-id="b8930-407">Per selezionare il vertex shader per l'esecuzione, chiama [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) sul parametro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) ricevuto nel metodo [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-407">To select the vertex shader for execution, it calls [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter received in the transform's [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="b8930-408">Questo metodo accetta un GUID per un vertex shader caricato in precedenza e, facoltativamente, un buffer di vertici creato in precedenza per l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-408">This method accepts a GUID for a previously-loaded vertex shader as well as (optionally) a previously-created vertex buffer for the shader to execute on.</span></span>

### <a name="implementing-a-direct2d-vertex-shader"></a><span data-ttu-id="b8930-409">Implementazione di un vertex shader Direct2D</span><span class="sxs-lookup"><span data-stu-id="b8930-409">Implementing a Direct2D vertex shader</span></span>

<span data-ttu-id="b8930-410">Una trasformazione di estrazione può contenere sia un pixel shader che un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-410">A draw transform can contain both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="b8930-411">Se una trasformazione definisce sia un pixel shader che un vertex shader, l'output del vertex shader viene fornito direttamente al pixel shader: l'app può personalizzare la firma di ritorno del vertex shader/i parametri del pixel shader purché siano coerenti.</span><span class="sxs-lookup"><span data-stu-id="b8930-411">If a transform defines both a pixel shader and a vertex shader, then the output from the vertex shader is given directly to the pixel shader: the app can customize the return signature of the vertex shader / the parameters of the pixel shader as long as they are consistent.</span></span>

<span data-ttu-id="b8930-412">D'altra parte, se una trasformazione contiene solo un vertex shader e si basa sulla pixel shader pass-through predefinita di [Direct2D](./direct2d-portal.md), deve restituire l'output predefinito seguente:</span><span class="sxs-lookup"><span data-stu-id="b8930-412">On the other hand, if a transform only contains a vertex shader, and relies on [Direct2D](./direct2d-portal.md)'s default pass-through pixel shader, it must return the following default output:</span></span>


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="b8930-413">Un vertex shader archivia il risultato delle trasformazioni dei vertici nella variabile di output dello spazio della scena dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-413">A vertex shader stores the result of its vertex transformations in the shader's Scene-space output variable.</span></span> <span data-ttu-id="b8930-414">Per calcolare l'output dello spazio di ritaglio e le variabili di input dello spazio Texel, [Direct2D](./direct2d-portal.md) fornisce automaticamente matrici di conversione in un buffer costante:</span><span class="sxs-lookup"><span data-stu-id="b8930-414">To compute the Clip-space output and the Texel-space input variables, [Direct2D](./direct2d-portal.md) automatically provides conversion matrices in a constant buffer:</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



<span data-ttu-id="b8930-415">Il codice vertex shader di esempio è riportato di seguito che usa le matrici di conversione per calcolare gli spazi di ritaglio e di Texel corretti previsti da [Direct2D](./direct2d-portal.md):</span><span class="sxs-lookup"><span data-stu-id="b8930-415">Sample vertex shader code can be found below that uses the conversion matrices to calculate the correct clip and texel spaces expected by [Direct2D](./direct2d-portal.md):</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



<span data-ttu-id="b8930-416">Il codice precedente può essere usato come punto di partenza per un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-416">The above code can be used as a starting point for a vertex shader.</span></span> <span data-ttu-id="b8930-417">Passa semplicemente attraverso l'immagine di input senza eseguire alcuna trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-417">It merely passes through the input image without performing any transforms.</span></span> <span data-ttu-id="b8930-418">Anche in questo caso, vedere l' [esempio D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) per una trasformazione basata su vertex shader completamente implementata.</span><span class="sxs-lookup"><span data-stu-id="b8930-418">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a fully-implemented vertex shader-based transform.</span></span>

<span data-ttu-id="b8930-419">Se non viene specificato alcun vertex buffer dalla trasformazione, [Direct2D](./direct2d-portal.md) sostituisce un buffer di vertici predefinito che rappresenta la posizione dell'immagine rettangolare.</span><span class="sxs-lookup"><span data-stu-id="b8930-419">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) substitutes in a default vertex buffer representing the rectangular image location.</span></span> <span data-ttu-id="b8930-420">I parametri del vertex shader vengono modificati in quelli dell'output dello shader predefinito:</span><span class="sxs-lookup"><span data-stu-id="b8930-420">The parameters to the vertex shader are changed to those of the default shader output:</span></span>


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="b8930-421">Il vertex shader non può modificare i parametri *sceneSpaceOutput* e *clipSpaceOutput* .</span><span class="sxs-lookup"><span data-stu-id="b8930-421">The vertex shader may not modify its *sceneSpaceOutput* and *clipSpaceOutput* parameters.</span></span> <span data-ttu-id="b8930-422">Deve restituirle invariate.</span><span class="sxs-lookup"><span data-stu-id="b8930-422">It must return them unchanged.</span></span> <span data-ttu-id="b8930-423">Potrebbe tuttavia modificare i parametri di *texelSpaceInput* per ogni immagine di input.</span><span class="sxs-lookup"><span data-stu-id="b8930-423">It may however modify the *texelSpaceInput* parameter(s) for each input image.</span></span> <span data-ttu-id="b8930-424">Se la trasformazione contiene anche un pixel shader personalizzato, il vertex shader è ancora in grado di passare parametri personalizzati aggiuntivi direttamente al pixel shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-424">If the transform also contains a custom pixel shader, the vertex shader is still able to pass additional custom parameters directly to the pixel shader.</span></span> <span data-ttu-id="b8930-425">Inoltre, il buffer personalizzato (B0) delle matrici di conversione *sceneSpace* non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b8930-425">Additionally, the *sceneSpace* conversion matrices custom buffer (b0) is no longer provided.</span></span>

## <a name="adding-a-compute-shader-to-a-custom-transform"></a><span data-ttu-id="b8930-426">Aggiunta di un compute shader a una trasformazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b8930-426">Adding a compute shader to a custom transform</span></span>

<span data-ttu-id="b8930-427">Infine, le trasformazioni personalizzate possono utilizzare i compute shader per determinati scenari di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-427">Finally, custom transforms may utilize compute shaders for certain targeted scenarios.</span></span> <span data-ttu-id="b8930-428">Compute Shaders può essere usato per implementare effetti di immagini complessi che richiedono l'accesso arbitrario ai buffer dell'immagine di input e di output.</span><span class="sxs-lookup"><span data-stu-id="b8930-428">Compute shaders can be used to implement complex image effects that require arbitrary access to input and output image buffers.</span></span> <span data-ttu-id="b8930-429">Un algoritmo istogramma di base, ad esempio, non può essere implementato con una pixel shader a causa di limitazioni relative all'accesso alla memoria.</span><span class="sxs-lookup"><span data-stu-id="b8930-429">For example, a basic histogram algorithm cannot be implemented with a pixel shader due to limitations on memory access.</span></span>

<span data-ttu-id="b8930-430">Poiché i compute shader hanno requisiti di livello di funzionalità hardware più elevati rispetto ai pixel shader, è consigliabile usare i pixel shader quando possibile per implementare un dato effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-430">Because compute shaders have higher hardware feature level requirements than pixel shaders, pixel shaders should be used when possible to implement a given effect.</span></span> <span data-ttu-id="b8930-431">In particolare, i compute shader vengono eseguiti solo sulla maggior parte delle schede di livello DirectX 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b8930-431">Specifically, compute shaders only run on most DirectX 10 level cards and higher.</span></span> <span data-ttu-id="b8930-432">Se una trasformazione sceglie di usare un compute shader, deve verificare il supporto hardware appropriato durante la creazione dell'istanza oltre all'implementazione dell'interfaccia [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .</span><span class="sxs-lookup"><span data-stu-id="b8930-432">If a transform chooses to use a compute shader, it must check for the appropriate hardware support during instantiation in addition to implementing the [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) interface.</span></span>

### <a name="checking-for-compute-shader-support"></a><span data-ttu-id="b8930-433">Verifica del supporto di Compute Shader</span><span class="sxs-lookup"><span data-stu-id="b8930-433">Checking for Compute Shader support</span></span>

<span data-ttu-id="b8930-434">Se un effetto usa un compute shader, deve verificare il supporto compute shader durante la creazione usando il metodo [**ID2D1EffectContext:: CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="b8930-434">If an effect uses a compute shader, it must check for compute shader support during its creation using the [**ID2D1EffectContext::CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) method.</span></span> <span data-ttu-id="b8930-435">Se la GPU non supporta Compute Shaders, l'effetto deve restituire le [**funzionalità del \_ \_ dispositivo D2DERR \_ insufficienti**](direct2d-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b8930-435">If the GPU does not support compute shaders, the effect must return [**D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES**](direct2d-error-codes.md).</span></span>

<span data-ttu-id="b8930-436">Sono disponibili due tipi diversi di compute shader che possono essere usati da una trasformazione: Shader Model 4 (DirectX 10) e Shader Model 5 (DirectX 11).</span><span class="sxs-lookup"><span data-stu-id="b8930-436">There are two different types of compute shaders that a transform can use: Shader Model 4 (DirectX 10) and Shader Model 5 (DirectX 11).</span></span> <span data-ttu-id="b8930-437">Esistono alcune limitazioni per gli shader del modello Shader 4.</span><span class="sxs-lookup"><span data-stu-id="b8930-437">There are certain limitations to Shader Model 4 shaders.</span></span> <span data-ttu-id="b8930-438">Per informazioni dettagliate, vedere la documentazione di [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) .</span><span class="sxs-lookup"><span data-stu-id="b8930-438">See the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details.</span></span> <span data-ttu-id="b8930-439">Le trasformazioni possono contenere entrambi i tipi di shader e possono eseguire il fallback al modello Shader 4 quando necessario: vedere l' [esempio D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) per un'implementazione di questo.</span><span class="sxs-lookup"><span data-stu-id="b8930-439">Transforms can contain both types of shaders, and can fall back to Shader Model 4 when required: see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for an implementation of this.</span></span>

### <a name="implement-id2d1computetransform"></a><span data-ttu-id="b8930-440">Implementare ID2D1ComputeTransform</span><span class="sxs-lookup"><span data-stu-id="b8930-440">Implement ID2D1ComputeTransform</span></span>

<span data-ttu-id="b8930-441">Questa interfaccia contiene due nuovi metodi da implementare, oltre a quelli in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="b8930-441">This interface contains two new methods to implement in addition to the ones in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span></span>

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a><span data-ttu-id="b8930-442">SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo)</span><span class="sxs-lookup"><span data-stu-id="b8930-442">SetComputeInfo(ID2D1ComputeInfo \*pComputeInfo)</span></span>

<span data-ttu-id="b8930-443">Come per i pixel e i vertex shader, [Direct2D](./direct2d-portal.md) chiama il metodo [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) quando la trasformazione viene aggiunta per la prima volta al grafico di trasformazione di un effetto.</span><span class="sxs-lookup"><span data-stu-id="b8930-443">Like with pixel and vertex shaders, [Direct2D](./direct2d-portal.md) calls the [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="b8930-444">Questo metodo fornisce un parametro [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) che controlla il modo in cui viene eseguito il rendering della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b8930-444">This method provides an [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="b8930-445">Ciò include la scelta del compute shader da eseguire tramite il metodo [**ID2D1ComputeInfo:: SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) .</span><span class="sxs-lookup"><span data-stu-id="b8930-445">This includes choosing the compute shader to execute through the [**ID2D1ComputeInfo::SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) method.</span></span> <span data-ttu-id="b8930-446">Se la trasformazione sceglie di archiviare questo parametro come variabile membro della classe, è possibile accedervi e modificarli da qualsiasi metodo Transform o Effect, fatta eccezione per i metodi [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) e [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="b8930-446">If the transform chooses to store this parameter as a class member variable, it can be accessed and changed from any transform or effect method with the exception of the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) and [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods.</span></span> <span data-ttu-id="b8930-447">Vedere l'argomento **ID2D1ComputeInfo** per altri metodi disponibili qui.</span><span class="sxs-lookup"><span data-stu-id="b8930-447">See the **ID2D1ComputeInfo** topic for other methods available here.</span></span>

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a><span data-ttu-id="b8930-448">CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect, UInt32 \* PDIMENSIONX, UInt32 \* pDimensionY, UInt32 \* pDimensionZ)</span><span class="sxs-lookup"><span data-stu-id="b8930-448">CalculateThreadgroups(ID2D1ComputeInfo \*pOutputRect, UINT32 \*pDimensionX, UINT32 \*pDimensionY, UINT32 \*pDimensionZ)</span></span>

<span data-ttu-id="b8930-449">Mentre i pixel shader vengono eseguiti in base ai singoli pixel e i vertex shader vengono eseguiti in base ai singoli vertici, i compute shader vengono eseguiti in base a 'threadgroup.</span><span class="sxs-lookup"><span data-stu-id="b8930-449">Whereas pixel shaders are executed on a per-pixel basis and vertex shaders are executed on a per-vertex basis, compute shaders are executed on a per-'threadgroup' basis.</span></span> <span data-ttu-id="b8930-450">Un ThreadGroup rappresenta un numero di thread eseguiti contemporaneamente nella GPU.</span><span class="sxs-lookup"><span data-stu-id="b8930-450">A threadgroup represents a number of threads that execute concurrently on the GPU.</span></span> <span data-ttu-id="b8930-451">Il codice HLSL di Compute Shader decide il numero di thread da eseguire per ogni ThreadGroup.</span><span class="sxs-lookup"><span data-stu-id="b8930-451">The compute shader HLSL code decides how many threads should be executed per threadgroup.</span></span> <span data-ttu-id="b8930-452">L'effetto ridimensiona il numero di threadgroups in modo che lo shader esegua il numero di volte desiderato, a seconda della logica dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-452">The effect scales the number of threadgroups so that the shader executes the desired number of times, depending on the shader's logic.</span></span>

<span data-ttu-id="b8930-453">Il metodo [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) consente alla trasformazione di informare [Direct2D](./direct2d-portal.md) il numero di gruppi di thread necessari, in base alla dimensione dell'immagine e alla conoscenza della trasformazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-453">The [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) method allows the transform to inform [Direct2D](./direct2d-portal.md) how many thread groups are required, based on the size of the image and the transform's own knowledge of the shader.</span></span>

<span data-ttu-id="b8930-454">Il numero di esecuzioni del compute shader è un prodotto dei conteggi ThreadGroup specificati qui e l'annotazione ' numThreads ' in compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span><span class="sxs-lookup"><span data-stu-id="b8930-454">The number of times the compute shader is executed is a product of the threadgroup counts specified here and the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="b8930-455">Se, ad esempio, la trasformazione imposta le dimensioni ThreadGroup su (2, 2, 1), lo shader specifica (3, 3, 1) thread per ogni ThreadGroup, quindi verranno eseguiti 4 threadgroups, ognuno con 9 thread, per un totale di 36 istanze di thread.</span><span class="sxs-lookup"><span data-stu-id="b8930-455">For example, if the transform sets the threadgroup dimensions to be (2,2,1) the shader specifies (3,3,1) threads per threadgroup, then 4 threadgroups will be executed, each with 9 threads in them, for a total of 36 thread instances.</span></span>

<span data-ttu-id="b8930-456">Uno scenario comune consiste nell'elaborare un pixel di output per ogni istanza del compute shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-456">A common scenario is to process one output pixel for each instance of the compute shader.</span></span> <span data-ttu-id="b8930-457">Per calcolare il numero di gruppi di thread per questo scenario, la trasformazione divide la larghezza e l'altezza dell'immagine in base alle rispettive dimensioni x e y dell'annotazione ' numThreads ' nel [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)compute shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-457">To calculate the number of thread groups for this scenario, the transform divides the width and height of the image by the respective x and y dimensions of the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span>

<span data-ttu-id="b8930-458">In particolare, se viene eseguita questa divisione, il numero di gruppi di thread richiesti deve essere sempre arrotondato per eccesso all'intero più vicino. in caso contrario, i pixel "resto" non verranno eseguiti su.</span><span class="sxs-lookup"><span data-stu-id="b8930-458">Importantly, if this division is performed, then the number of thread groups requested must always be rounded up to the nearest integer, otherwise the 'remainder' pixels will not be executed upon.</span></span> <span data-ttu-id="b8930-459">Se uno shader, ad esempio, calcola un singolo pixel con ogni thread, il codice del metodo verrebbe visualizzato come segue.</span><span class="sxs-lookup"><span data-stu-id="b8930-459">If a shader (for example) computes a single pixel with each thread, the method's code would appear as follows.</span></span>


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



<span data-ttu-id="b8930-460">[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) usa il codice seguente per specificare il numero di thread in ogni gruppo di thread:</span><span class="sxs-lookup"><span data-stu-id="b8930-460">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) uses the following code to specify the number of threads in each thread group:</span></span>


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



<span data-ttu-id="b8930-461">Durante l'esecuzione, il ThreadGroup corrente e l'indice del thread corrente vengono passati come parametri al metodo shader:</span><span class="sxs-lookup"><span data-stu-id="b8930-461">During execution, the current threadgroup and current thread index are passed as parameters to the shader method:</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a><span data-ttu-id="b8930-462">Lettura dei dati dell'immagine</span><span class="sxs-lookup"><span data-stu-id="b8930-462">Reading image data</span></span>

<span data-ttu-id="b8930-463">Compute Shaders accede all'immagine di input della trasformazione come una singola trama bidimensionale:</span><span class="sxs-lookup"><span data-stu-id="b8930-463">Compute shaders access the transform's input image as a single two-dimensional texture:</span></span>


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



<span data-ttu-id="b8930-464">Tuttavia, come i pixel shader, non è garantito che i dati dell'immagine inizino da (0, 0) sulla trama.</span><span class="sxs-lookup"><span data-stu-id="b8930-464">However, like pixel shaders, the image's data is not guaranteed to begin at (0, 0) on the texture.</span></span> <span data-ttu-id="b8930-465">Al contrario, [Direct2D](./direct2d-portal.md) fornisce costanti di sistema che consentono agli shader di compensare qualsiasi offset:</span><span class="sxs-lookup"><span data-stu-id="b8930-465">Instead, [Direct2D](./direct2d-portal.md) provides system constants that allow shaders to compensate for any offset:</span></span>


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



<span data-ttu-id="b8930-466">Quando sono stati definiti il metodo di supporto e il buffer costanti sopra indicati, lo shader può campionare i dati dell'immagine usando quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b8930-466">Once the above constant buffer and helper method have been defined, the shader can sample image data using the following:</span></span>


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a><span data-ttu-id="b8930-467">Scrittura di dati immagine</span><span class="sxs-lookup"><span data-stu-id="b8930-467">Writing image data</span></span>

<span data-ttu-id="b8930-468">[Direct2D](./direct2d-portal.md) prevede che uno shader definisca un buffer di output per l'immagine risultante da inserire.</span><span class="sxs-lookup"><span data-stu-id="b8930-468">[Direct2D](./direct2d-portal.md) expects a shader to define an output buffer for the resulting image to be placed.</span></span> <span data-ttu-id="b8930-469">In Shader Model 4 (DirectX 10), deve trattarsi di un buffer unidimensionale a causa di vincoli di funzionalità:</span><span class="sxs-lookup"><span data-stu-id="b8930-469">In Shader Model 4 (DirectX 10), this must be a single-dimensional buffer due to feature constraints:</span></span>


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



<span data-ttu-id="b8930-470">La trama di output è indicizzata Row-First per consentire l'archiviazione dell'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="b8930-470">The output texture is indexed row-first to allow the entire image to be stored.</span></span>


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



<span data-ttu-id="b8930-471">D'altra parte, Shader Model 5 (DirectX 11) shaders può usare trame di output bidimensionali:</span><span class="sxs-lookup"><span data-stu-id="b8930-471">On the other hand, Shader Model 5 (DirectX 11) shaders can use two-dimensional output textures:</span></span>


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



<span data-ttu-id="b8930-472">Con Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) fornisce un parametro ' outputOffset ' aggiuntivo nel buffer costante.</span><span class="sxs-lookup"><span data-stu-id="b8930-472">With Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) provides an additional 'outputOffset' parameter in the constant buffer.</span></span> <span data-ttu-id="b8930-473">L'output dello shader deve essere offsetted in base a questo importo:</span><span class="sxs-lookup"><span data-stu-id="b8930-473">The shader's output should be offsetted by this amount:</span></span>


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="b8930-474">Di seguito è riportato uno shader di tipo pass-through con il modello 5 compute shader completato.</span><span class="sxs-lookup"><span data-stu-id="b8930-474">A completed pass-through Shader Model 5 compute shader is shown below.</span></span> <span data-ttu-id="b8930-475">Ogni thread compute shader legge e scrive un singolo pixel dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="b8930-475">In it, each of the compute shader threads reads and writes a single pixel of the input image.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="b8930-476">Il codice riportato di seguito mostra la versione equivalente di Shader Model 4 dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8930-476">The code below shows the equivalent Shader Model 4 version of the shader.</span></span> <span data-ttu-id="b8930-477">Si noti che ora viene eseguito il rendering dello shader in un buffer di output unidimensionale.</span><span class="sxs-lookup"><span data-stu-id="b8930-477">Notice that the shader now renders into a single-dimensional output buffer.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a><span data-ttu-id="b8930-478">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8930-478">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8930-479">Esempio di SDK D2DCustomEffects</span><span class="sxs-lookup"><span data-stu-id="b8930-479">D2DCustomEffects SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 