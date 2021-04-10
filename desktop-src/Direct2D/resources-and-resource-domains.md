---
title: Panoramica delle risorse
description: Descrive le risorse Direct2D e il modo in cui possono essere condivise.
ms.assetid: afd308a7-9524-4436-9a0e-8575383d96fa
keywords:
- Direct2D, risorse
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bf4eb807a25b592e32a2d83436532af17462d70c
ms.sourcegitcommit: 7d0cc7eb398fee8f5be55cd654a12d29937d643c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/08/2021
ms.locfileid: "104351001"
---
# <a name="resources-overview"></a>Panoramica delle risorse

Una risorsa Direct2D è un oggetto usato per il disegno ed è rappresentato da un'interfaccia Direct2D, ad esempio [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) o [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). In questo argomento vengono descritti i tipi di risorse Direct2D e il modo in cui possono essere condivisi.

In questo argomento sono incluse le sezioni seguenti:

-   [Informazioni sulle risorse Direct2D](#about-direct2d-resources)
-   [Risorse indipendenti dal dispositivo](#device-independent-resources)
-   [Risorse dipendenti dal dispositivo](#device-dependent-resources)
-   [Condivisione delle risorse di fabbrica](#sharing-factory-resources)
-   [Condivisione delle risorse di destinazione di rendering](#sharing-render-target-resources)
    -   [Destinazioni di rendering hardware](#hardware-render-targets)
    -   [Destinazioni di rendering della superficie di DXGI](#dxgi-surface-render-targets)
    -   [Destinazioni di rendering compatibili e bitmap condivise](#compatible-render-targets-and-shared-bitmaps)

## <a name="about-direct2d-resources"></a>Informazioni sulle risorse Direct2D

Molte API 2D con accelerazione hardware sono progettate per un modello di risorse basato sulla CPU e un set di operazioni di rendering che funzionano bene con le CPU. successivamente, alcune parti dell'API sono con accelerazione hardware. Per l'implementazione di queste API è necessario un gestore di risorse per il mapping delle risorse della CPU alle risorse nella GPU. A causa delle limitazioni della GPU, alcune operazioni potrebbero non essere più accelerate in ogni circostanza. In questi casi, Resource Manager deve comunicare tra la CPU e la GPU (costosa) in modo da poter passare al rendering della CPU. In alcuni casi è possibile che il rendering venga forzato in modo imprevedibile per eseguire il fallback completo alla CPU. Inoltre, le operazioni di rendering che risultano semplici potrebbero richiedere passaggi di rendering intermedi temporanei che non sono esposti nell'API e che richiedono risorse GPU aggiuntive.

Direct2D fornisce un mapping più diretto per l'uso completo della GPU. Fornisce due categorie di risorse: indipendenti dal dispositivo e dipendenti dal dispositivo.

-   Le risorse indipendenti dal dispositivo, ad esempio [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), vengono mantenute sulla CPU.
-   Le risorse dipendenti dal dispositivo, ad esempio [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), vengono mappate direttamente alle risorse sulla GPU (quando è disponibile l'accelerazione hardware). Le chiamate di rendering vengono eseguite combinando informazioni sui vertici e sul code coverage da una geometria con informazioni di texturing prodotte dalle risorse dipendenti dal dispositivo.

Quando si creano risorse dipendenti dal dispositivo, le risorse di sistema (GPU, se disponibile o CPU) vengono allocate quando il dispositivo viene creato e non cambiano da un'operazione di rendering a un'altra. Questa situazione Elimina la necessità di un gestore di risorse. Oltre ai miglioramenti delle prestazioni generali forniti dall'eliminazione di un gestore di risorse, questo modello consente di controllare direttamente qualsiasi rendering intermedio.

Poiché Direct2D fornisce un controllo così elevato sulle risorse, è necessario comprendere i diversi tipi di risorse e quando è possibile utilizzarli insieme.

## <a name="device-independent-resources"></a>Risorse Device-Independent

Come descritto nella sezione precedente, le risorse indipendenti dal dispositivo si trovano sempre nella CPU e non sono mai associate a un dispositivo di rendering hardware. Di seguito sono riportate risorse indipendenti dal dispositivo:

-   [**ID2D1DrawingStateBlock**](/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock)
-   [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
-   [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) e le interfacce che ereditano da esso.
-   [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) e [ **ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
-   [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)

Usare un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), una risorsa indipendente dal dispositivo, per creare risorse indipendenti dal dispositivo. Per creare una factory, usare la funzione [**CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .

Ad eccezione delle destinazioni di rendering, tutte le risorse create da una factory sono indipendenti dal dispositivo. Una destinazione di rendering è una risorsa dipendente dal dispositivo.

## <a name="device-dependent-resources"></a>Risorse Device-Dependent

Qualsiasi risorsa non denominata nell'elenco precedente è una risorsa dipendente dal dispositivo. Le risorse dipendenti dal dispositivo sono associate a un particolare dispositivo di rendering. Quando è disponibile l'accelerazione hardware, il dispositivo è la GPU. In altri casi, si tratta della CPU.

Per creare la maggior parte delle risorse dipendenti dal dispositivo, usare una destinazione di rendering. Nella maggior parte dei casi, utilizzare una factory per creare una destinazione di rendering.

Di seguito sono riportati alcuni esempi di risorse dipendenti dal dispositivo:

-   [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) e le interfacce che ereditano da esso. Usare una destinazione di rendering per creare pennelli.
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer). Usare una destinazione di rendering per creare i livelli.
-   [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e le interfacce che ereditano da esso. Per creare una destinazione di rendering, utilizzare una factory o un'altra destinazione di rendering.

> [!Note]  
> A partire da Windows 8 sono disponibili nuove interfacce che creano risorse dipendenti dal dispositivo. Un [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) e un [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) possono condividere una risorsa se il contesto di dispositivo e la risorsa vengono creati dallo stesso **ID2D1Device**.

 

Le risorse dipendenti dal dispositivo diventano inutilizzabili quando i dispositivi di rendering associati diventano non disponibili. Ciò significa che quando si riceve l'errore di [**\_ \_ destinazione D2DERR ricrea**](direct2d-error-codes.md) per una destinazione di rendering, è necessario ricreare la destinazione di rendering e tutte le relative risorse.

## <a name="sharing-factory-resources"></a>Condivisione delle risorse di fabbrica

È possibile condividere tutte le risorse indipendenti dal dispositivo create da una factory con tutte le altre risorse (indipendenti dal dispositivo o dipendenti dal dispositivo) create dalla stessa factory. Ad esempio, è possibile usare due oggetti [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) per creare lo stesso [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) se entrambi gli oggetti **ID2D1RenderTarget** sono stati creati dalla stessa factory.

Le interfacce di sink ([**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink), [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)e [**ID2D1TessellationSink**](/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink)) possono essere condivise con le risorse create da qualsiasi Factory. A differenza di altre interfacce in Direct2D, è possibile usare qualsiasi implementazione di un'interfaccia sink. Ad esempio, è possibile usare la propria implementazione di **ID2D1SimplifiedGeometrySink**.

## <a name="sharing-render-target-resources"></a>Condivisione delle risorse di destinazione di rendering

La possibilità di condividere le risorse create da una destinazione di rendering dipende dal tipo di destinazione di rendering. Quando si crea una destinazione di rendering di tipo d2d1 per il [**\_ tipo di \_ destinazione di \_ \_ rendering**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type), le risorse create da tale destinazione di rendering possono essere utilizzate solo da tale destinazione di rendering, a meno che la destinazione di rendering non sia inserita in una delle categorie descritte nelle sezioni seguenti. Questo problema si verifica perché non si conosce il dispositivo che verrà utilizzato dalla destinazione di rendering, che potrebbe essere il rendering nell'hardware locale, nel software o nell'hardware di un client remoto. Ad esempio, è possibile scrivere un programma che smette di funzionare quando viene visualizzato in remoto o quando la destinazione di rendering viene aumentata di dimensione oltre le dimensioni massime supportate dall'hardware di rendering.

Le sezioni seguenti descrivono le circostanze in cui una risorsa creata da una destinazione di rendering può essere condivisa con un'altra destinazione di rendering.

### <a name="hardware-render-targets"></a>Destinazioni di rendering hardware

È possibile condividere le risorse tra qualsiasi destinazione di rendering che usi in modo esplicito l'hardware, purché la modalità remota sia compatibile. La modalità di comunicazione remota è garantita solo quando entrambe le destinazioni di rendering utilizzano il flag di utilizzo della destinazione di rendering d2d1 o della **destinazione di \_ rendering della \_ destinazione \_ \_ \_** di rendering d2d1, oppure se non viene specificato alcun flag. [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) Queste impostazioni garantiscono che le risorse si trovino sempre nello stesso computer. Per specificare una modalità di utilizzo, impostare il campo **Usage** della struttura delle [**proprietà della \_ destinazione di rendering \_ \_ d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) utilizzata per creare la destinazione di rendering con uno o più flag di **utilizzo della \_ \_ destinazione \_ di rendering d2d1** .

Per creare una destinazione di rendering che utilizza in modo esplicito il rendering hardware, impostare il campo **tipo** della struttura delle [**proprietà di \_ \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) utilizzata per creare la destinazione di rendering per l'hardware del tipo di [**destinazione di \_ rendering \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="dxgi-surface-render-targets"></a>Destinazioni di rendering della superficie di DXGI

È possibile condividere le risorse create da una destinazione di rendering della superficie DXGI con qualsiasi altra destinazione di rendering della superficie DXGI che usa lo stesso dispositivo Direct3D sottostante.

### <a name="compatible-render-targets-and-shared-bitmaps"></a>Destinazioni di rendering compatibili e bitmap condivise

È possibile condividere le risorse tra una destinazione di rendering e destinazioni di rendering compatibili create da tale destinazione di rendering. Per creare una destinazione di rendering compatibile, usare il metodo [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) .

È possibile usare il metodo [**ID2D1RenderTarget:: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) che può essere condiviso tra le due destinazioni di rendering specificate nella chiamata al metodo, se il metodo ha esito positivo. Questo metodo avrà esito positivo fino a quando le due destinazioni di rendering utilizzeranno lo stesso dispositivo sottostante per il rendering.

 

 
