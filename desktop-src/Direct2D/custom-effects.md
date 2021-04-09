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
# <a name="custom-effects"></a>Effetti personalizzati

[Direct2D](./direct2d-portal.md) viene fornito con una raccolta di effetti che eseguono una serie di operazioni di immagine comuni. Per l'elenco completo degli effetti, vedere l'argomento relativo agli [effetti predefiniti](built-in-effects.md) . Per le funzionalità che non possono essere ottenute con gli effetti predefiniti, Direct2D consente di scrivere effetti personalizzati usando [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)standard. È possibile utilizzare questi effetti personalizzati insieme agli effetti predefiniti forniti con Direct2D.

Per visualizzare esempi di un effetto completo su pixel, vertex e compute shader, vedere l' [esempio D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

In questo argomento vengono illustrati i passaggi e i concetti necessari per progettare e creare un effetto personalizzato con funzionalità complete.

## <a name="introduction-what-is-inside-an-effect"></a>Introduzione: che cosa si trova all'interno di un effetto?

![diagramma effetto ombreggiatura.](images/custom-effects1.png)

A livello concettuale, un effetto [Direct2D](./direct2d-portal.md) esegue un'attività di creazione dell'immagine, ad esempio la modifica della luminosità, la desaturazione di un'immagine o, come illustrato in precedenza, la creazione di un'ombreggiatura. All'app sono semplici. Possono accettare zero o più immagini di input, esporre più proprietà che controllano l'operazione e generare un'unica immagine di output.

Sono disponibili quattro parti diverse di un effetto personalizzato di cui l'autore di un effetto è responsabile:

1.  Interfaccia Effect: l'interfaccia Effect definisce concettualmente il modo in cui un'app interagisce con un effetto personalizzato, ad esempio il numero di input accettati dall'effetto e le proprietà disponibili. L'interfaccia Effect gestisce un grafico di trasformazione, che contiene le operazioni di creazione di immagini effettive.
2.  Transform Graph: ogni effetto crea un grafico di trasformazione interno costituito da singole trasformazioni. Ogni trasformazione rappresenta una singola operazione di immagine. L'effetto è responsabile del collegamento di queste trasformazioni in un grafico per l'esecuzione dell'effetto della creazione di immagini desiderato. Un effetto può aggiungere, rimuovere, modificare e riordinare le trasformazioni in risposta alle modifiche apportate alle proprietà esterne dell'effetto.
3.  Transform: una trasformazione rappresenta una singola operazione di immagine. Lo scopo principale è quello di ospitare gli shader eseguiti per ogni pixel di output. A tal fine, è responsabile del calcolo delle nuove dimensioni dell'immagine di output in base alla logica nei relativi shader. Deve inoltre calcolare l'area dell'immagine di input da cui gli shader devono leggere per eseguire il rendering dell'area di output richiesta.
4.  Shader: uno shader viene eseguito sull'input della trasformazione sulla GPU (o CPU se viene specificato il rendering del software quando l'app crea il dispositivo Direct3D). Gli shader degli effetti sono scritti in[HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)(High Level Shading Language) e vengono compilati in codice byte durante la compilazione dell'effetto, che viene quindi caricato dall'effetto in fase di esecuzione. In questo documento di riferimento viene descritto come scrivere HLSL conformi a [Direct2D](./direct2d-portal.md). La documentazione di Direct3D contiene una panoramica di base di HLSL.

## <a name="creating-an-effect-interface"></a>Creazione di un'interfaccia di effetto

L'interfaccia Effect definisce il modo in cui un'app interagisce con l'effetto personalizzato. Per creare un'interfaccia effetto, una classe deve implementare ID2D1EffectImpl, definire i metadati che descrivono l'effetto, ad esempio il nome, il numero di input e le proprietà, e creare metodi che registrano l'effetto personalizzato per l'uso con [Direct2D](./direct2d-portal.md).

Una volta implementati tutti i componenti per un'interfaccia di effetto, l'intestazione della classe sarà simile alla seguente:


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



### <a name="implement-id2d1effectimpl"></a>Implementare ID2D1EffectImpl

L'interfaccia [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) contiene tre metodi che è necessario implementare:

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a>Initialize (ID2D1EffectContext \* pContextInternal, ID2D1TransformGraph \* pTransformGraph)

[Direct2D](./direct2d-portal.md) chiama il metodo [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) dopo che il metodo [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) è stato chiamato dall'app. È possibile utilizzare questo metodo per eseguire l'inizializzazione interna o qualsiasi altra operazione necessaria per l'effetto. Inoltre, è possibile usarlo per creare il grafico di trasformazione iniziale dell'effetto.

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a>Segraph (ID2D1TransformGraph \* pTransformGraph)

[Direct2D](./direct2d-portal.md) chiama il metodo [**segraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) quando viene modificato il numero di input per l'effetto. Mentre la maggior parte degli effetti ha un numero costante di input, altri come l' [effetto composito](composite.md) supportano un numero variabile di input. Questo metodo consente a questi effetti di aggiornare il grafico di trasformazione in risposta a un conteggio di input modificabile. Se un effetto non supporta un numero di input variabile, questo metodo può semplicemente restituire E \_ NOTIMPL.

### <a name="prepareforrender-d2d1_change_type-changetype"></a>PrepareForRender ( \_ tipo di modifica d2d1 \_ ChangeType)

Il metodo [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) consente agli effetti di eseguire qualsiasi operazione in risposta a modifiche esterne. [Direct2D](./direct2d-portal.md) chiama questo metodo appena prima di eseguire il rendering di un effetto se almeno una di queste condizioni è vera:

-   L'effetto è stato inizializzato in precedenza ma non ancora creato.
-   Una proprietà Effect è stata modificata dopo l'ultima chiamata di progetto.
-   Lo stato del contesto [Direct2D](./direct2d-portal.md) chiamante (ad esempio dpi) è stato modificato dopo l'ultima chiamata di progetto.

### <a name="implement-the-effect-registration-and-callback-methods"></a>Implementare i metodi di registrazione e callback degli effetti

È necessario che le app registrino gli effetti con [Direct2D](./direct2d-portal.md) prima di crearne un'istanza. Questa registrazione ha come ambito un'istanza di una factory Direct2D e deve essere ripetuta ogni volta che l'app viene eseguita. Per abilitare questa registrazione, un effetto personalizzato definisce un GUID univoco, un metodo pubblico che registra l'effetto e un metodo di callback privato che restituisce un'istanza dell'effetto.

### <a name="define-a-guid"></a>Definire un GUID

È necessario definire un GUID che identifichi in modo univoco l'effetto per la registrazione con [Direct2D](./direct2d-portal.md). L'app usa lo stesso per identificare l'effetto quando chiama [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).

Questo codice illustra la definizione di un GUID di questo tipo per un effetto. È necessario creare un proprio GUID univoco usando uno strumento di generazione GUID, ad esempio guidgen.exe.


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a>Definire un metodo di registrazione pubblico

Definire quindi un metodo pubblico che l'app deve chiamare per registrare l'effetto con [Direct2D](./direct2d-portal.md). Poiché la registrazione degli effetti è specifica di un'istanza di una factory Direct2D, il metodo accetta un'interfaccia [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) come parametro. Per registrare l'effetto, il metodo chiama quindi l'API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) sul parametro **ID2D1Factory1** .

Questa API accetta una stringa XML che descrive i metadati, gli input e le proprietà dell'effetto. I metadati per un effetto sono solo a scopo informativo e possono essere sottoposti a query dall'app tramite l'interfaccia [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) . I dati di input e delle proprietà, d'altra parte, vengono usati da [Direct2D](./direct2d-portal.md) e rappresentano la funzionalità dell'effetto.

Di seguito è riportata una stringa XML per un effetto di esempio minimo. L'aggiunta di proprietà personalizzate al codice XML viene analizzata nella sezione aggiunta di proprietà personalizzate a un effetto.


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



### <a name="define-an-effect-factory-callback-method"></a>Definire un metodo di callback Factory degli effetti

L'effetto deve inoltre fornire un metodo di callback privato che restituisca un'istanza dell'effetto tramite un singolo \* \* parametro IUnknown. Un puntatore a questo metodo viene fornito a [Direct2D](./direct2d-portal.md) quando l'effetto viene registrato tramite l'API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) tramite il [**parametro \_ \_ Factory Effect PD2D1**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .


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



### <a name="implement-the-iunknown-interface"></a>Implementare l'interfaccia IUnknown

Infine, l'effetto deve implementare l'interfaccia IUnknown per la compatibilità con COM.

## <a name="creating-the-effects-transform-graph"></a>Creazione del grafico di trasformazione dell'effetto

Un effetto può utilizzare diverse trasformazioni (singole operazioni di immagine) per creare l'effetto di imaging desiderato. Per controllare l'ordine in cui queste trasformazioni vengono applicate all'immagine di input, l'effetto li dispone in un grafico di trasformazione. Un grafico di trasformazione può usare gli effetti e le trasformazioni inclusi in [Direct2D](./direct2d-portal.md) , nonché le trasformazioni personalizzate create dall'autore dell'effetto.

### <a name="using-transforms-included-with-direct2d"></a>Uso delle trasformazioni incluse con Direct2D

Queste sono le trasformazioni usate più di frequente fornite con [Direct2D](./direct2d-portal.md).

-   [**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): questa trasformazione unisce un numero arbitrario di input in base a una descrizione di Blend, vedere l'argomento della [**\_ \_ Descrizione di d2d1 Blend**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) e l' [esempio di modalità effetto composito Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) per esempi di Blend. Questa trasformazione viene restituita dal metodo [**ID2D1EffectContext:: CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .
-   [**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): questa trasformazione espande le dimensioni di output di un'immagine in base [**alla \_ \_ modalità di estensione d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specificata. Questa trasformazione viene restituita dal metodo [**ID2D1EffectContext:: CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .
-   [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): questa trasformazione compensa (converte) l'input in base a un numero intero di pixel. Questa trasformazione viene restituita dal metodo [**ID2D1EffectContext:: CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .
-   Qualsiasi effetto esistente può essere trattato come una trasformazione allo scopo di trasformare la creazione di grafici tramite il metodo [**ID2D1EffectContext:: CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .

### <a name="creating-a-single-node-transform-graph"></a>Creazione di un grafico di trasformazione a nodo singolo

Dopo aver creato una trasformazione, l'input dell'effetto deve essere connesso all'input della trasformazione e l'output della trasformazione deve essere connesso all'output dell'effetto. Quando un effetto contiene una sola trasformazione, è possibile usare il metodo [**ID2D1TransformGraph:: SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) per eseguire facilmente questa operazione.

È possibile creare o modificare una trasformazione nei metodi [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) o [**segraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) dell'effetto usando il parametro ID2D1TransformGraph specificato. Se un effetto deve apportare modifiche al grafico di trasformazione in un altro metodo in cui questo parametro non è disponibile, l'effetto può salvare il parametro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) come variabile membro della classe e accedervi altrove, ad esempio [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) o un metodo di callback di proprietà personalizzato.

Di seguito è riportato un esempio di metodo [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) . Questo metodo crea un grafico di trasformazione a nodo singolo che compensa l'immagine di 100 pixel in ogni asse.


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



### <a name="creating-a-multi-node-transform-graph"></a>Creazione di un grafico di trasformazione a più nodi

L'aggiunta di più trasformazioni al grafico di trasformazione di un effetto consente agli effetti di eseguire internamente più operazioni di immagine presentate a un'app come singolo effetto unificato.

Come indicato in precedenza, il grafico di trasformazione dell'effetto può essere modificato in qualsiasi metodo di effetto usando il parametro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) ricevuto nel metodo [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) dell'effetto. Le API seguenti su tale interfaccia possono essere utilizzate per creare o modificare il grafico di trasformazione di un effetto:

### <a name="addnodeid2d1transformnode-pnode"></a>AddNode (ID2D1TransformNode \* pNode)

Il metodo [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , in pratica,' Registra ' la trasformazione con l'effetto e deve essere chiamato prima che la trasformazione possa essere usata con qualsiasi altro metodo di trasformazione Graph.

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a>ConnectToEffectInput (UINT32 toEffectInputIndex, ID2D1TransformNode \* pNode, UInt32 toNodeInputIndex)

Il metodo [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) connette l'input dell'immagine dell'effetto all'input di una trasformazione. Lo stesso input di effetto può essere connesso a più trasformazioni.

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a>ConnectNode (ID2D1TransformNode \* pFromNode, ID2D1TransformNode \* PTONODE, UInt32 toNodeInputIndex)

Il metodo [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) connette l'output di una trasformazione a un altro input della trasformazione. Un output di trasformazione può essere connesso a più trasformazioni.

### <a name="setoutputnodeid2d1transformnode-pnode"></a>SetOutputNode (ID2D1TransformNode \* pNode)

Il metodo [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) connette l'output di una trasformazione all'output dell'effetto. Poiché un effetto ha un solo output, solo una singola trasformazione può essere designata come ' nodo di output '.

Questo codice usa due trasformazioni separate per creare un effetto unificato. In questo caso, l'effetto è un'ombreggiatura traslata.


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



## <a name="adding-custom-properties-to-an-effect"></a>Aggiunta di proprietà personalizzate a un effetto

Gli effetti possono definire proprietà personalizzate che consentono a un'app di modificare il comportamento dell'effetto durante il Runtime. Per definire una proprietà per un effetto personalizzato, è necessario eseguire tre passaggi:

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a>Aggiungere i metadati della proprietà ai dati di registrazione dell'effetto

### <a name="add-property-to-registration-xml"></a>Aggiungere la proprietà a XML di registrazione

È necessario definire le proprietà di un effetto personalizzato durante la registrazione iniziale dell'effetto con [Direct2D](./direct2d-portal.md). In primo luogo, è necessario aggiornare il codice XML di registrazione dell'effetto nel metodo di registrazione pubblico con la nuova proprietà:


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



Quando si definisce una proprietà Effect in XML, è necessario un nome, un tipo e un nome visualizzato. Il nome visualizzato di una proprietà, oltre ai valori di categoria, autore e Descrizione dell'effetto globale, può e deve essere localizzato.

Per ogni proprietà, un effetto può facoltativamente specificare valori predefiniti, min e max. Questi valori sono destinati esclusivamente all'utilizzo informativo. Non vengono applicati da [Direct2D](./direct2d-portal.md). È necessario implementare la logica predefinita/min/max specificata nella classe Effect.

Il valore del tipo elencato nel codice XML per la proprietà deve corrispondere al tipo di dati corrispondente utilizzato dai metodi getter e setter della proprietà. In questa tabella vengono visualizzati i valori XML corrispondenti per ogni tipo di dati:



| Tipo di dati                                                                                                                              | Valore XML corrispondente |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| PWSTR                                                                                                                                  | string                  |
| BOOL                                                                                                                                   | bool                    |
| UINT                                                                                                                                   | uint32                  |
| INT                                                                                                                                    | int32                   |
| FLOAT                                                                                                                                  | float                   |
| [**D2D \_ vector \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | Vector2                 |
| [**\_Vettore D2D \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | Vector3                 |
| [**D2D \_ vector \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | Vector4                 |
| [**\_Matrice D2D \_ 3x2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool)) | matrix3x2               |
| [**\_Matrice D2D \_ 4x3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | matrix4x3               |
| [**D2D \_ Matrix \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | matrix4x4               |
| [**\_Matrice D2D \_ 5x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | matrix5x4               |
| BYTE\[\]                                                                                                                               | blob                    |
| IUnknown\*                                                                                                                             | IUnknown                |
| [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*                                                                                       | ColorContext            |
| CLSID                                                                                                                                  | clsid                   |
| Enumerazione ([**\_ \_ modalità di interpolazione d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode)e così via)                                                | enum                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a>Mappare la nuova proprietà ai metodi getter e setter

Successivamente, l'effetto deve eseguire il mapping di questa nuova proprietà ai metodi getter e setter. Questa operazione viene eseguita tramite la matrice di [**\_ \_ associazione della proprietà d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) passata al metodo [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .

La matrice di [**\_ \_ associazione della proprietà d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) ha un aspetto simile al seguente:


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



Dopo aver creato la matrice XML e bindings, passarli nel metodo [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



Per la \_ \_ macro di associazione del tipo di valore d2d1 è \_ necessario che la classe Effect erediti da [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) prima di qualsiasi altra interfaccia.

Le proprietà personalizzate per un effetto vengono indicizzate nell'ordine in cui sono dichiarate nel codice XML e, una volta create, è possibile accedervi tramite l'app usando i metodi [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) e [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) . Per praticità, è possibile creare un'enumerazione pubblica che elenca ogni proprietà nel file di intestazione dell'effetto:


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a>Creare i metodi getter e setter per la proprietà

Il passaggio successivo consiste nel creare i metodi getter e setter per la nuova proprietà. I nomi dei metodi devono corrispondere a quelli specificati nella matrice di [**\_ \_ associazione della proprietà d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) . Inoltre, il tipo di proprietà specificato nel codice XML dell'effetto deve corrispondere al tipo del parametro del metodo di impostazione e al valore restituito del metodo Get.


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



### <a name="update-effects-transforms-in-response-to-property-change"></a>Trasformazioni dell'effetto aggiornamento in risposta alla modifica di una proprietà

Per aggiornare effettivamente l'output di un'immagine di un effetto in risposta a una modifica di proprietà, l'effetto deve modificare le trasformazioni sottostanti. Questa operazione viene in genere eseguita nel metodo [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) dell'effetto che [Direct2D](./direct2d-portal.md) chiama automaticamente quando una delle proprietà di un effetto è stata modificata. Tuttavia, le trasformazioni possono essere aggiornate in qualsiasi metodo dell'effetto, ad esempio Initialize o i metodi di impostazione delle proprietà dell'effetto.

Ad esempio, se un effetto contiene un [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) e si vuole modificare il valore di offset in risposta alla proprietà offset dell'effetto da modificare, il codice seguente verrà aggiunto in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):


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



## <a name="creating-a-custom-transform"></a>Creazione di una trasformazione personalizzata

Per implementare le operazioni sulle immagini oltre a quelle fornite in [Direct2D](./direct2d-portal.md), è necessario implementare trasformazioni personalizzate. Le trasformazioni personalizzate possono modificare arbitrariamente un'immagine di input tramite l'uso di shader HLSL personalizzati.

Le trasformazioni implementano una di due diverse interfacce a seconda dei tipi di shader utilizzati. Le trasformazioni che usano pixel e/o vertex shader devono implementare [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), mentre le trasformazioni che usano compute shader devono implementare [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform). Entrambe le interfacce ereditano da [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform). Questa sezione è incentrata sull'implementazione della funzionalità comune a entrambe.

L'interfaccia [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) dispone di quattro metodi per implementare:

### <a name="getinputcount"></a>GetInputCount

Questo metodo restituisce un Integer che rappresenta il numero di input per la trasformazione.


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a>MapInputRectsToOutputRect

[Direct2D](./direct2d-portal.md) chiama il metodo [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) ogni volta che viene eseguito il rendering della trasformazione. Direct2D passa un rettangolo che rappresenta i limiti di ogni input alla trasformazione. La trasformazione è quindi responsabile del calcolo dei limiti dell'immagine di output. Le dimensioni dei rettangoli per tutti i metodi in questa interfaccia ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) sono definite in pixel, non in DIP.

Questo metodo è anche responsabile del calcolo dell'area dell'output che è opaca in base alla logica dello shader e alle aree opache di ogni input. Un'area opaca di un'immagine è definita come quella in cui il canale alfa è' 1' per l'intero rettangolo. Se non è chiaro se l'output di una trasformazione è opaco, il rettangolo di output opaco deve essere impostato su (0, 0, 0, 0) come valore sicuro. [Direct2D](./direct2d-portal.md) utilizza queste informazioni per eseguire le ottimizzazioni del rendering con contenuto "opaco garantito". Se questo valore non è accurato, può causare il rendering errato.

È possibile modificare il comportamento di rendering della trasformazione (come definito nelle sezioni da 6 a 8) durante questo metodo. Tuttavia, non è possibile modificare altre trasformazioni nel grafico di trasformazione o il layout del grafico qui.


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



Per un esempio più complesso, prendere in considerazione la modalità di rappresentazione di una semplice operazione di sfocatura:

Se un'operazione di sfocatura usa un raggio di 5 pixel, le dimensioni del rettangolo di output devono espandersi di 5 pixel, come illustrato di seguito. Quando si modificano le coordinate del rettangolo, una trasformazione deve garantire che la logica non causi alcun overflow nelle coordinate del rettangolo.


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



Poiché l'immagine è sfocata, un'area dell'immagine opaca potrebbe ora essere parzialmente trasparente. Ciò è dovuto al fatto che l'area al di fuori dell'immagine viene impostata sul nero trasparente e tale trasparenza verrà mescolata nell'immagine intorno ai bordi. La trasformazione deve riflettere questa operazione nei calcoli dei rettangoli opachi di output:


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



Questi calcoli vengono visualizzati qui:

![illustrazione del calcolo del rettangolo.](images/custom-effects2.png)

Per ulteriori informazioni su questo metodo, vedere la pagina di riferimento di [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .

### <a name="mapoutputrecttoinputrects"></a>MapOutputRectToInputRects

[Direct2D](./direct2d-portal.md) chiama il metodo [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) dopo [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). La trasformazione deve calcolare la porzione dell'immagine da leggere per eseguire correttamente il rendering dell'area di output richiesta.

Come prima, se un effetto esegue esclusivamente il mapping dei pixel 1-1, può passare il rettangolo di output al rettangolo di input:


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



Analogamente, se una trasformazione compatta o espande un'immagine, come nell'esempio di sfocatura, i pixel utilizzano spesso i pixel circostanti per calcolare il relativo valore. Con una sfocatura, viene calcolata la media di un pixel con i pixel circostanti, anche se si trovano all'esterno dei limiti dell'immagine di input. Questo comportamento si riflette nel calcolo. Come prima, la trasformazione controlla gli overflow quando si espandono le coordinate di un rettangolo.


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



Questa figura Visualizza il calcolo. [Direct2D](./direct2d-portal.md) esegue automaticamente il campionamento di pixel neri trasparenti in cui l'immagine di input non esiste, consentendo la fusione graduale della sfocatura con il contenuto esistente sullo schermo.

![illustrazione di un campionamento di effetto di pixel neri trasparenti all'esterno di un rettangolo.](images/custom-effects3.png)

Se il mapping non è semplice, questo metodo deve impostare il rettangolo di input sull'area massima per garantire i risultati corretti. A tale scopo, impostare i bordi sinistro e superiore su INT \_ min e i bordi destro e inferiore su int \_ max.

Per ulteriori informazioni su questo metodo, vedere l'argomento [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .

### <a name="mapinvalidrect"></a>MapInvalidRect

[Direct2D](./direct2d-portal.md) chiama anche il metodo [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Tuttavia, a differenza dei metodi [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) e [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) Direct2D, non è garantito che lo chiami in un momento specifico. Questo metodo stabilisce concettualmente quale parte dell'output di una trasformazione deve essere di nuovo sottoposta a rendering in risposta a una parte o a tutte le modifiche apportate all'input. Esistono tre scenari diversi per i quali calcolare un oggetto Rect non valido della trasformazione.

### <a name="transforms-with-one-to-one-pixel-mapping"></a>Trasformazioni con mapping di pixel uno-a-uno

Per le trasformazioni che mappano i pixel 1-1, passare semplicemente il rettangolo di input non valido al rettangolo di output non valido:


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



### <a name="transforms-with-many-to-many-pixel-mapping"></a>Trasformazioni con mapping di pixel molti-a-molti

Quando i pixel di output di una trasformazione dipendono dall'area circostante, il rettangolo di input non valido deve essere espanso. In questo modo si riflette che i pixel che racchiudono il rettangolo di input non valido saranno interessati e diventeranno non validi. Ad esempio, una sfocatura di cinque pixel usa il calcolo seguente:


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a>Trasformazioni con mapping di pixel complessi

Per le trasformazioni in cui i pixel di input e di output non dispongono di un mapping semplice, l'intero output può essere contrassegnato come non valido. Se, ad esempio, una trasformazione restituisce semplicemente il colore medio dell'input, viene modificato l'intero output della trasformazione se viene modificata anche una piccola parte dell'input. In questo caso, il rettangolo di output non valido deve essere impostato su un rettangolo logicamente infinito (mostrato di seguito). [Direct2D](./direct2d-portal.md) lo blocca automaticamente ai limiti dell'output.


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



Per ulteriori informazioni su questo metodo, vedere l'argomento [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .

Una volta implementati questi metodi, l'intestazione della trasformazione conterrà quanto segue:


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



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a>Aggiunta di un pixel shader a una trasformazione personalizzata

Una volta creata, una trasformazione deve fornire uno shader che modifichi i pixel dell'immagine. In questa sezione vengono illustrati i passaggi per l'utilizzo di un pixel shader con una trasformazione personalizzata.

### <a name="implementing-id2d1drawtransform"></a>Implementazione di ID2D1DrawTransform

Per usare un pixel shader, la trasformazione deve implementare l'interfaccia [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , che eredita dall'interfaccia [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) descritta nella sezione 5. Questa interfaccia contiene un nuovo metodo da implementare:

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a>SetDrawInfo (ID2D1DrawInfo \* pDrawInfo)

[Direct2D](./direct2d-portal.md) chiama il metodo [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) quando la trasformazione viene aggiunta per la prima volta al grafico di trasformazione di un effetto. Questo metodo fornisce un parametro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) che controlla il modo in cui viene eseguito il rendering della trasformazione. Vedere l'argomento **ID2D1DrawInfo** per i metodi disponibili qui.

Se la trasformazione sceglie di archiviare questo parametro come variabile membro della classe, è possibile accedere all'oggetto *drawInfo* e modificarlo da altri metodi, ad esempio setter di proprietà o [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). In particolare, non è possibile chiamare i metodi [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) o [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) in [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).

### <a name="creating-a-guid-for-the-pixel-shader"></a>Creazione di un GUID per la pixel shader

Successivamente, la trasformazione deve definire un GUID univoco per il pixel shader stesso. Questa operazione viene utilizzata quando [Direct2D](./direct2d-portal.md) carica lo shader in memoria, così come quando la trasformazione sceglie quali pixel shader utilizzare per l'esecuzione. Per generare un GUID casuale, è possibile usare strumenti come guidgen.exe, incluso in Visual Studio.


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a>Caricamento della pixel shader con Direct2D

Prima di poter utilizzare la trasformazione, è necessario che un pixel shader venga caricato in memoria.

Per caricare il pixel shader in memoria, la trasformazione deve leggere il codice byte compilato dello shader da. File CSO generato da Visual Studio (per informazioni dettagliate, vedere la documentazione di [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ) in una matrice di byte. Questa tecnica è illustrata in dettaglio nell' [esempio SDK D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

Una volta che i dati dello shader sono stati caricati in una matrice di byte, chiamare il metodo [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) sull'oggetto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) dell'effetto. [Direct2D](./direct2d-portal.md) ignora le chiamate a **LoadPixelShader** quando uno shader con lo stesso GUID è già stato caricato.

Dopo che un pixel shader è stato caricato in memoria, la trasformazione deve selezionarla per l'esecuzione passando il relativo GUID al metodo [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) sul parametro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fornito durante il metodo [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) . Il pixel shader deve essere già caricato in memoria prima di essere selezionato per l'esecuzione.

### <a name="changing-shader-operation-with-constant-buffers"></a>Modifica dell'operazione dello shader con i buffer costanti

Per modificare la modalità di esecuzione di uno shader, una trasformazione può passare un buffer costante al pixel shader. A tale scopo, una trasformazione definisce uno struct che contiene le variabili desiderate nell'intestazione della classe:


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



La trasformazione chiama quindi il metodo [**ID2D1DrawInfo:: SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) sul parametro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fornito nel metodo [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) per passare questo buffer allo shader.

Il [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) deve anche definire uno struct corrispondente che rappresenta il buffer costante. Le variabili contenute nello struct dello shader devono corrispondere a quelle nello struct della trasformazione.


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



Una volta definito il buffer, i valori contenuti in possono essere letti da qualsiasi posizione all'interno del pixel shader.

### <a name="writing-a-pixel-shader-for-direct2d"></a>Scrittura di un pixel shader per Direct2D

Le trasformazioni [Direct2D](./direct2d-portal.md) usano gli shader creati usando [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)standard. Tuttavia, esistono alcuni concetti chiave per la scrittura di una pixel shader eseguita dal contesto di una trasformazione. Per un esempio completo di pixel shader completamente funzionale, vedere l'esempio [D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

[Direct2D](./direct2d-portal.md) esegue automaticamente il mapping degli input di una trasformazione agli oggetti [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) in HLSL. Il primo **Texture2D** si trova in Register T0 e il primo **SamplerState** si trova in Register S0. Ogni input aggiuntivo si trova nei registri corrispondenti successivi (ad esempio T1 e S1). È possibile campionare i dati dei pixel per un particolare input chiamando Sample nell'oggetto **Texture2D** e passando l'oggetto **SamplerState** corrispondente e le coordinate Texel.

Una pixel shader personalizzata viene eseguita una volta per ogni pixel di cui viene eseguito il rendering. Ogni volta che viene eseguito lo shader, [Direct2D](./direct2d-portal.md) fornisce automaticamente tre parametri che ne identificano la posizione di esecuzione corrente:

-   Scena-output dello spazio: questo parametro rappresenta la posizione di esecuzione corrente in termini di superficie di destinazione complessiva. Viene definito in pixel e i relativi valori min/max corrispondono ai limiti del rettangolo restituito da [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).
-   Clip-spazio output: questo parametro viene usato da Direct3D e non deve essere usato nel pixel shader di una trasformazione.
-   Texel-input di spazio: questo parametro rappresenta la posizione di esecuzione corrente in una particolare trama di input. Uno shader non deve prendere alcuna dipendenza dal modo in cui questo valore viene calcolato. Deve essere usato solo per campionare l'input del pixel shader, come illustrato nel codice seguente:


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



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a>Aggiunta di un vertex shader a una trasformazione personalizzata

È possibile utilizzare vertex shader per eseguire scenari di imaging diversi rispetto ai pixel shader. In particolare, i vertex shader possono eseguire gli effetti di un'immagine basata sulla geometria trasformando i vertici che costituiscono un'immagine. I vertex shader possono essere usati indipendentemente da o insieme ai pixel shader specificati dalla trasformazione. Se non si specifica un vertex shader, il [Direct2D](./direct2d-portal.md) sostituisce in un vertex shader predefinito per l'uso con la pixel shader personalizzata.

Il processo per l'aggiunta di un vertex shader a una trasformazione personalizzata è simile a quello di un pixel shader: la trasformazione implementa l'interfaccia [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , crea un GUID e (facoltativamente) passa buffer costanti allo shader. Tuttavia, esistono alcuni passaggi chiave aggiuntivi che sono univoci per i vertex shader:

### <a name="creating-a-vertex-buffer"></a>Creazione di un buffer vertici

Un vertex shader per definizione viene eseguito sui vertici passati, non sui singoli pixel. Per specificare i vertici per l'esecuzione dello shader, una trasformazione crea un buffer del vertice da passare allo shader. Il layout dei buffer dei vertici esula dall'ambito di questo documento. Per informazioni dettagliate, vedere il [riferimento a Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o l' [esempio SDK D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) per un'implementazione di esempio.

Dopo la creazione di un buffer vertex in memoria, la trasformazione usa il metodo [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) sull'oggetto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) dell'effetto contenitore per passare i dati alla GPU. Per un'implementazione di esempio, vedere l' [esempio D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) .

Se non viene specificato alcun vertex buffer dalla trasformazione, [Direct2D](./direct2d-portal.md) passa un buffer dei vertici predefinito che rappresenta la posizione dell'immagine rettangolare.

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a>Modifica di SetDrawInfo per utilizzare un vertex shader

Analogamente a quanto avviene con i pixel shader, la trasformazione deve caricare e selezionare un vertex shader per l'esecuzione. Per caricare il vertex shader, chiama il metodo [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) sul metodo [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) ricevuto nel metodo Initialize dell'effetto. Per selezionare il vertex shader per l'esecuzione, chiama [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) sul parametro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) ricevuto nel metodo [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) della trasformazione. Questo metodo accetta un GUID per un vertex shader caricato in precedenza e, facoltativamente, un buffer di vertici creato in precedenza per l'esecuzione dello shader.

### <a name="implementing-a-direct2d-vertex-shader"></a>Implementazione di un vertex shader Direct2D

Una trasformazione di estrazione può contenere sia un pixel shader che un vertex shader. Se una trasformazione definisce sia un pixel shader che un vertex shader, l'output del vertex shader viene fornito direttamente al pixel shader: l'app può personalizzare la firma di ritorno del vertex shader/i parametri del pixel shader purché siano coerenti.

D'altra parte, se una trasformazione contiene solo un vertex shader e si basa sulla pixel shader pass-through predefinita di [Direct2D](./direct2d-portal.md), deve restituire l'output predefinito seguente:


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Un vertex shader archivia il risultato delle trasformazioni dei vertici nella variabile di output dello spazio della scena dello shader. Per calcolare l'output dello spazio di ritaglio e le variabili di input dello spazio Texel, [Direct2D](./direct2d-portal.md) fornisce automaticamente matrici di conversione in un buffer costante:


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



Il codice vertex shader di esempio è riportato di seguito che usa le matrici di conversione per calcolare gli spazi di ritaglio e di Texel corretti previsti da [Direct2D](./direct2d-portal.md):


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



Il codice precedente può essere usato come punto di partenza per un vertex shader. Passa semplicemente attraverso l'immagine di input senza eseguire alcuna trasformazione. Anche in questo caso, vedere l' [esempio D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) per una trasformazione basata su vertex shader completamente implementata.

Se non viene specificato alcun vertex buffer dalla trasformazione, [Direct2D](./direct2d-portal.md) sostituisce un buffer di vertici predefinito che rappresenta la posizione dell'immagine rettangolare. I parametri del vertex shader vengono modificati in quelli dell'output dello shader predefinito:


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Il vertex shader non può modificare i parametri *sceneSpaceOutput* e *clipSpaceOutput* . Deve restituirle invariate. Potrebbe tuttavia modificare i parametri di *texelSpaceInput* per ogni immagine di input. Se la trasformazione contiene anche un pixel shader personalizzato, il vertex shader è ancora in grado di passare parametri personalizzati aggiuntivi direttamente al pixel shader. Inoltre, il buffer personalizzato (B0) delle matrici di conversione *sceneSpace* non è più disponibile.

## <a name="adding-a-compute-shader-to-a-custom-transform"></a>Aggiunta di un compute shader a una trasformazione personalizzata

Infine, le trasformazioni personalizzate possono utilizzare i compute shader per determinati scenari di destinazione. Compute Shaders può essere usato per implementare effetti di immagini complessi che richiedono l'accesso arbitrario ai buffer dell'immagine di input e di output. Un algoritmo istogramma di base, ad esempio, non può essere implementato con una pixel shader a causa di limitazioni relative all'accesso alla memoria.

Poiché i compute shader hanno requisiti di livello di funzionalità hardware più elevati rispetto ai pixel shader, è consigliabile usare i pixel shader quando possibile per implementare un dato effetto. In particolare, i compute shader vengono eseguiti solo sulla maggior parte delle schede di livello DirectX 10 e versioni successive. Se una trasformazione sceglie di usare un compute shader, deve verificare il supporto hardware appropriato durante la creazione dell'istanza oltre all'implementazione dell'interfaccia [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .

### <a name="checking-for-compute-shader-support"></a>Verifica del supporto di Compute Shader

Se un effetto usa un compute shader, deve verificare il supporto compute shader durante la creazione usando il metodo [**ID2D1EffectContext:: CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) . Se la GPU non supporta Compute Shaders, l'effetto deve restituire le [**funzionalità del \_ \_ dispositivo D2DERR \_ insufficienti**](direct2d-error-codes.md).

Sono disponibili due tipi diversi di compute shader che possono essere usati da una trasformazione: Shader Model 4 (DirectX 10) e Shader Model 5 (DirectX 11). Esistono alcune limitazioni per gli shader del modello Shader 4. Per informazioni dettagliate, vedere la documentazione di [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) . Le trasformazioni possono contenere entrambi i tipi di shader e possono eseguire il fallback al modello Shader 4 quando necessario: vedere l' [esempio D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) per un'implementazione di questo.

### <a name="implement-id2d1computetransform"></a>Implementare ID2D1ComputeTransform

Questa interfaccia contiene due nuovi metodi da implementare, oltre a quelli in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a>SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo)

Come per i pixel e i vertex shader, [Direct2D](./direct2d-portal.md) chiama il metodo [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) quando la trasformazione viene aggiunta per la prima volta al grafico di trasformazione di un effetto. Questo metodo fornisce un parametro [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) che controlla il modo in cui viene eseguito il rendering della trasformazione. Ciò include la scelta del compute shader da eseguire tramite il metodo [**ID2D1ComputeInfo:: SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) . Se la trasformazione sceglie di archiviare questo parametro come variabile membro della classe, è possibile accedervi e modificarli da qualsiasi metodo Transform o Effect, fatta eccezione per i metodi [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) e [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Vedere l'argomento **ID2D1ComputeInfo** per altri metodi disponibili qui.

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a>CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect, UInt32 \* PDIMENSIONX, UInt32 \* pDimensionY, UInt32 \* pDimensionZ)

Mentre i pixel shader vengono eseguiti in base ai singoli pixel e i vertex shader vengono eseguiti in base ai singoli vertici, i compute shader vengono eseguiti in base a 'threadgroup. Un ThreadGroup rappresenta un numero di thread eseguiti contemporaneamente nella GPU. Il codice HLSL di Compute Shader decide il numero di thread da eseguire per ogni ThreadGroup. L'effetto ridimensiona il numero di threadgroups in modo che lo shader esegua il numero di volte desiderato, a seconda della logica dello shader.

Il metodo [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) consente alla trasformazione di informare [Direct2D](./direct2d-portal.md) il numero di gruppi di thread necessari, in base alla dimensione dell'immagine e alla conoscenza della trasformazione dello shader.

Il numero di esecuzioni del compute shader è un prodotto dei conteggi ThreadGroup specificati qui e l'annotazione ' numThreads ' in compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl). Se, ad esempio, la trasformazione imposta le dimensioni ThreadGroup su (2, 2, 1), lo shader specifica (3, 3, 1) thread per ogni ThreadGroup, quindi verranno eseguiti 4 threadgroups, ognuno con 9 thread, per un totale di 36 istanze di thread.

Uno scenario comune consiste nell'elaborare un pixel di output per ogni istanza del compute shader. Per calcolare il numero di gruppi di thread per questo scenario, la trasformazione divide la larghezza e l'altezza dell'immagine in base alle rispettive dimensioni x e y dell'annotazione ' numThreads ' nel [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)compute shader.

In particolare, se viene eseguita questa divisione, il numero di gruppi di thread richiesti deve essere sempre arrotondato per eccesso all'intero più vicino. in caso contrario, i pixel "resto" non verranno eseguiti su. Se uno shader, ad esempio, calcola un singolo pixel con ogni thread, il codice del metodo verrebbe visualizzato come segue.


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



[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) usa il codice seguente per specificare il numero di thread in ogni gruppo di thread:


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



Durante l'esecuzione, il ThreadGroup corrente e l'indice del thread corrente vengono passati come parametri al metodo shader:


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



### <a name="reading-image-data"></a>Lettura dei dati dell'immagine

Compute Shaders accede all'immagine di input della trasformazione come una singola trama bidimensionale:


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



Tuttavia, come i pixel shader, non è garantito che i dati dell'immagine inizino da (0, 0) sulla trama. Al contrario, [Direct2D](./direct2d-portal.md) fornisce costanti di sistema che consentono agli shader di compensare qualsiasi offset:


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



Quando sono stati definiti il metodo di supporto e il buffer costanti sopra indicati, lo shader può campionare i dati dell'immagine usando quanto segue:


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



### <a name="writing-image-data"></a>Scrittura di dati immagine

[Direct2D](./direct2d-portal.md) prevede che uno shader definisca un buffer di output per l'immagine risultante da inserire. In Shader Model 4 (DirectX 10), deve trattarsi di un buffer unidimensionale a causa di vincoli di funzionalità:


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



La trama di output è indicizzata Row-First per consentire l'archiviazione dell'intera immagine.


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



D'altra parte, Shader Model 5 (DirectX 11) shaders può usare trame di output bidimensionali:


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



Con Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) fornisce un parametro ' outputOffset ' aggiuntivo nel buffer costante. L'output dello shader deve essere offsetted in base a questo importo:


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



Di seguito è riportato uno shader di tipo pass-through con il modello 5 compute shader completato. Ogni thread compute shader legge e scrive un singolo pixel dell'immagine di input.


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



Il codice riportato di seguito mostra la versione equivalente di Shader Model 4 dello shader. Si noti che ora viene eseguito il rendering dello shader in un buffer di output unidimensionale.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di SDK D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 