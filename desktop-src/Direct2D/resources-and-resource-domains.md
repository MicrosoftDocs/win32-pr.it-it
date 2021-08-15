---
title: Panoramica delle risorse
description: Descrive le risorse Direct2D e come possono essere condivise.
ms.assetid: afd308a7-9524-4436-9a0e-8575383d96fa
keywords:
- Direct2D, risorse
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 67dc8c34703c834dbf0f1b651e3c118831d88abe1676feaba68ac53ecb603565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825112"
---
# <a name="resources-overview"></a>Panoramica delle risorse

Una risorsa Direct2D è un oggetto usato per il disegno ed è rappresentato da un'interfaccia Direct2D, ad esempio [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) o [**ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Questo argomento descrive i tipi di risorse Direct2D e come possono essere condivise.

In questo argomento sono incluse le sezioni seguenti:

-   [Informazioni sulle risorse Direct2D](#about-direct2d-resources)
-   [Risorse indipendenti dal dispositivo](#device-independent-resources)
-   [Risorse dipendenti dal dispositivo](#device-dependent-resources)
-   [Condivisione delle risorse di factory](#sharing-factory-resources)
-   [Condivisione delle risorse di destinazione di rendering](#sharing-render-target-resources)
    -   [Destinazioni di rendering hardware](#hardware-render-targets)
    -   [Destinazioni di rendering della superficie DXGI](#dxgi-surface-render-targets)
    -   [Destinazioni di rendering compatibili e bitmap condivise](#compatible-render-targets-and-shared-bitmaps)

## <a name="about-direct2d-resources"></a>Informazioni sulle risorse Direct2D

Molte API 2D con accelerazione hardware sono progettate in base a un modello di risorse incentrato sulla CPU e a un set di operazioni di rendering che funzionano bene sulle CPU. Una parte dell'API è quindi accelerata dall'hardware. L'implementazione di queste API richiede un gestore di risorse per il mapping delle risorse della CPU alle risorse nella GPU. A causa delle limitazioni della GPU, alcune operazioni potrebbero non essere in grado di essere accelerate in ogni circostanza. In questi casi, il gestore di risorse deve comunicare tra la CPU e la GPU (operazione dispendiosa) in modo che possa passare al rendering della CPU. In alcuni casi, potrebbe forzare inconsaamente il rendering a eseguire il fall back completo alla CPU. Inoltre, le operazioni di rendering che sembrano semplici potrebbero richiedere passaggi di rendering intermedi temporanei che non sono esposti nell'API e che richiedono risorse GPU aggiuntive.

Direct2D offre un mapping più diretto per l'uso completo della GPU. Fornisce due categorie di risorse: indipendente dal dispositivo e dipendente dal dispositivo.

-   Le risorse indipendenti dal dispositivo, ad [**esempio ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)vengono mantenute nella CPU.
-   Le risorse dipendenti dal dispositivo, ad esempio [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)vengono mappate direttamente alle risorse nella GPU (quando è disponibile l'accelerazione hardware). Le chiamate di rendering vengono eseguite combinando le informazioni sui vertici e sulla copertura di una geometria con le informazioni di texturing prodotte dalle risorse dipendenti dal dispositivo.

Quando si creano risorse dipendenti dal dispositivo, le risorse di sistema (GPU, se disponibili o CPU) vengono allocate quando il dispositivo viene creato e non cambiano da un'operazione di rendering a un'altra. Questa situazione elimina la necessità di un gestore di risorse. Oltre ai miglioramenti generali delle prestazioni offerti dall'eliminazione di un gestore di risorse, questo modello consente di controllare direttamente qualsiasi rendering intermedio.

Poiché Direct2D offre un controllo così grande sulle risorse, è necessario comprendere i diversi tipi di risorse e quando possono essere usate insieme.

## <a name="device-independent-resources"></a>Device-Independent risorse

Come descritto nella sezione precedente, le risorse indipendenti dal dispositivo risiedono sempre nella CPU e non sono mai associate a un dispositivo di rendering hardware. Di seguito sono riportate le risorse indipendenti dal dispositivo:

-   [**ID2D1DrawingStateBlock**](/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock)
-   [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
-   [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) e le interfacce che ereditano da esso.
-   [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) e [ **ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
-   [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)

Usare [**id2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)una risorsa indipendente dal dispositivo, per creare risorse indipendenti dal dispositivo. Per creare una factory, usare [**la funzione CreateFactory.**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)

Ad eccezione delle destinazioni di rendering, tutte le risorse create da una factory sono indipendenti dal dispositivo. Una destinazione di rendering è una risorsa dipendente dal dispositivo.

## <a name="device-dependent-resources"></a>Device-Dependent risorse

Qualsiasi risorsa non denominata nell'elenco precedente è una risorsa dipendente dal dispositivo. Le risorse dipendenti dal dispositivo sono associate a un particolare dispositivo di rendering. Quando è disponibile l'accelerazione hardware, il dispositivo è la GPU. In altri casi, si tratta della CPU.

Per creare la maggior parte delle risorse dipendenti dal dispositivo, usare una destinazione di rendering. Nella maggior parte dei casi, usare una factory per creare una destinazione di rendering.

Di seguito sono riportati esempi di risorse dipendenti dal dispositivo:

-   [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) e le interfacce che ereditano da esso. Usare una destinazione di rendering per creare pennelli.
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer). Usare una destinazione di rendering per creare livelli.
-   [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e le interfacce che ereditano da esso. Per creare una destinazione di rendering, usare una factory o un'altra destinazione di rendering.

> [!Note]  
> A partire Windows 8, sono disponibili nuove interfacce che creano risorse dipendenti dal dispositivo. [**Id2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) e [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) possono condividere una risorsa se il contesto di dispositivo e la risorsa vengono creati dallo stesso **ID2D1Device**.

 

Le risorse dipendenti dal dispositivo diventano inutilizzabili quando i dispositivi di rendering associati diventano non disponibili. Ciò significa che quando si riceve l'errore [**D2DERR \_ RECREATE \_ TARGET**](direct2d-error-codes.md) per una destinazione di rendering, è necessario ricreare la destinazione di rendering e tutte le relative risorse.

## <a name="sharing-factory-resources"></a>Condivisione delle risorse di factory

È possibile condividere tutte le risorse indipendenti dal dispositivo create da una factory con tutte le altre risorse (indipendenti dal dispositivo o dipendenti dal dispositivo) create dalla stessa factory. Ad esempio, è possibile usare due oggetti [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) per disegnare lo stesso [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) se entrambi gli oggetti **ID2D1RenderTarget** sono stati creati dalla stessa factory.

Le interfacce sink ([**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink), [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)e [**ID2D1TessellationSink**](/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink)) possono essere condivise con le risorse create da qualsiasi factory. A differenza di altre interfacce in Direct2D, è possibile usare qualsiasi implementazione di un'interfaccia sink. Ad esempio, è possibile usare la propria implementazione di **ID2D1SimplifiedGeometrySink**.

## <a name="sharing-render-target-resources"></a>Condivisione delle risorse di destinazione di rendering

La possibilità di condividere le risorse create da una destinazione di rendering dipende dal tipo di destinazione di rendering. Quando si crea una destinazione di rendering di tipo [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT,**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)le risorse create da tale destinazione di rendering possono essere usate solo da tale destinazione di rendering (a meno che la destinazione di rendering non si adatti a una delle categorie descritte nelle sezioni seguenti). Ciò si verifica perché non si conosce il dispositivo che verrà utilizzato dalla destinazione di rendering. Potrebbe essere eseguito il rendering nell'hardware locale, nel software o nell'hardware di un client remoto. Ad esempio, è possibile scrivere un programma che smette di funzionare quando viene visualizzato in remoto o quando le dimensioni della destinazione di rendering superano le dimensioni massime supportate dall'hardware di rendering.

Le sezioni seguenti descrivono le circostanze in cui una risorsa creata da una destinazione di rendering può essere condivisa con un'altra destinazione di rendering.

### <a name="hardware-render-targets"></a>Destinazioni di rendering hardware

È possibile condividere le risorse tra qualsiasi destinazione di rendering che usa in modo esplicito l'hardware, purché la modalità remota sia compatibile. La modalità remota è garantita solo quando entrambe le destinazioni di rendering usano il flag [**D2D1 \_ RENDER TARGET USAGE FORCE BITMAP \_ \_ \_ \_ \_ REMOTING**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) o **D2D1 \_ RENDER TARGET USAGE \_ \_ \_ GDI \_ COMPATIBLE** oppure se non viene specificato alcun flag. Queste impostazioni garantiscono che le risorse si trovino sempre nello stesso computer. Per specificare una modalità  di utilizzo, impostare il campo di utilizzo della struttura [**D2D1 \_ RENDER \_ TARGET \_ PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) usata per creare la destinazione di rendering con uno o più flag **D2D1 \_ RENDER TARGET \_ \_ USAGE.**

Per creare una destinazione di rendering che  usa in modo esplicito il rendering hardware, impostare il campo type della struttura [**D2D1 \_ RENDER \_ TARGET \_ PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) usata per creare la destinazione di rendering su [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ HARDWARE.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)

### <a name="dxgi-surface-render-targets"></a>Destinazioni di rendering della superficie DXGI

È possibile condividere le risorse create da una destinazione di rendering della superficie DXGI con qualsiasi altra destinazione di rendering della superficie DXGI che usa lo stesso dispositivo Direct3D sottostante.

### <a name="compatible-render-targets-and-shared-bitmaps"></a>Destinazioni di rendering compatibili e bitmap condivise

È possibile condividere le risorse tra una destinazione di rendering e destinazioni di rendering compatibili create da tale destinazione di rendering. Per creare una destinazione di rendering compatibile, usare il [**metodo ID2D1RenderTarget::CreateCompatibleRenderTarget.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))

È possibile usare il metodo [**ID2D1RenderTarget::CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) che può essere condiviso tra le due destinazioni di rendering specificate nella chiamata al metodo, se il metodo ha esito positivo. Questo metodo avrà esito positivo purché le due destinazioni di rendering usino lo stesso dispositivo sottostante per il rendering.

 

 
