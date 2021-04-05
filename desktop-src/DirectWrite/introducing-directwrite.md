---
title: Introduzione a DirectWrite
description: Le persone comunicano con il testo sempre nella loro vita quotidiana.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, informazioni
- DirectWrite, funzionalità tipografiche
- tipografia
- DirectWrite, testo internazionale
- DirectWrite, tipi di carattere OpenType
- Tipi di carattere OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, panoramica delle API
- DirectWrite, IDWriteFontFace
- IDWriteFontFace
- DirectWrite, rendering del testo
- DirectWrite, modalità di rendering
- DirectWrite, interoperatività GDI
- DirectWrite, interoperabilità
- interoperabilità, DirectWrite
- interoperabilità, Graphics Device Interface (GDI)
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872906"
---
# <a name="introducing-directwrite"></a>Introduzione a DirectWrite

Le persone comunicano con il testo sempre nella loro vita quotidiana. È il modo principale in cui le persone utilizzano un volume di informazioni sempre maggiore. In passato, veniva usato per stampare contenuto, principalmente documenti, giornali, libri e così via. Sempre più, si tratta di contenuto online nel proprio PC Windows. Un tipico utente di Windows dedica molto tempo alla lettura dallo schermo del computer. Potrebbero navigare sul Web, analizzare la posta elettronica, comporre un report, compilare un foglio di calcolo o scrivere software, ma ciò che realmente stanno leggendo. Anche se il testo e i tipi di carattere comportano quasi tutte le parti dell'esperienza utente in Windows, per la maggior parte degli utenti la lettura sullo schermo non è piacevole come la lettura dell'output stampato.

Per gli sviluppatori di applicazioni Windows la scrittura di codice di gestione del testo è una sfida a causa dei maggiori requisiti per una migliore leggibilità, una formattazione sofisticata e un controllo del layout e il supporto per più linguaggi che l'applicazione deve visualizzare. Anche il sistema di gestione del testo più semplice deve consentire l'input di testo, il layout, la visualizzazione, la modifica e la copia e incolla. Gli utenti di Windows in genere prevedono ancora più di queste funzionalità di base, richiedendo anche semplici editor per supportare più tipi di carattere, diversi stili di paragrafo, immagini incorporate, controllo ortografico e altre funzionalità. La moderna progettazione dell'interfaccia utente non è più conforme al formato singolo, al testo normale, ma deve presentare un'esperienza migliore con i tipi di carattere e i layout di testo avanzati.

Questa è un'introduzione al modo in cui [DirectWrite](direct-write-portal.md) consente alle applicazioni Windows di migliorare l'esperienza di testo per l'interfaccia utente e i documenti.

## <a name="improving-the-text-experience"></a>Miglioramento dell'esperienza di testo

Le applicazioni Windows moderne hanno requisiti sofisticati per il testo nell'interfaccia utente e nei documenti. Sono incluse una migliore leggibilità, il supporto per una vasta gamma di linguaggi e script e prestazioni di rendering superiori. Inoltre, la maggior parte delle applicazioni esistenti richiede un modo per portare avanti gli investimenti esistenti nella codebase di WindowsWin32.

[DirectWrite](direct-write-portal.md) fornisce le tre funzionalità seguenti che consentono agli sviluppatori di applicazioni Windows di migliorare l'esperienza di testo all'interno delle applicazioni: indipendenza dal sistema di rendering, tipografia di alta qualità e più livelli di funzionalità.

## <a name="rendering-system-independence"></a>Indipendenza Rendering-System

[DirectWrite](direct-write-portal.md) è indipendente da qualsiasi tecnologia grafica specifica. Le applicazioni sono gratuite per l'utilizzo della tecnologia di rendering più adatta alle proprie esigenze. Ciò offre alle applicazioni la flessibilità di continuare a eseguire il rendering di alcune parti dell'applicazione tramite GDI e altre parti tramite Direct3D o [Direct2D](../direct2d/direct2d-portal.md). Infatti, un'applicazione può scegliere di eseguire il rendering di DirectWrite tramite uno stack di rendering proprietario.

## <a name="high-quality-typography"></a>Tipografia High-Quality

[DirectWrite](direct-write-portal.md) sfrutta i vantaggi offerti dalla tecnologia dei tipi di carattere [OpenType](../intl/opentype-font-format.md) per abilitare la tipografia di qualità elevata in un'applicazione Windows. Il sistema dei tipi di carattere DirectWrite fornisce servizi per la gestione dell'enumerazione dei tipi di carattere, del fallback del tipo di carattere e della memorizzazione nella cache del tipo di carattere, tutti necessari per le applicazioni per la gestione di

Il supporto [OpenType](../intl/opentype-font-format.md) fornito da [DirectWrite](direct-write-portal.md) consente agli sviluppatori di aggiungere alle proprie applicazioni funzionalità tipografiche avanzate e supporto per testo internazionale.

## <a name="support-for-advanced-typographic-features"></a>Supporto per funzionalità tipografiche avanzate

[DirectWrite](direct-write-portal.md) consente agli sviluppatori di applicazioni di sbloccare le funzionalità dei tipi di carattere OpenType che non possono essere utilizzati in WINFORMS o GDI. L'oggetto DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) espone molte delle funzionalità avanzate dei tipi di carattere OpenType, ad esempio alternative stilistiche e ornati. Microsoft Windows Software Development Kit (SDK) fornisce un set di tipi di carattere [OpenType](../intl/opentype-font-format.md) di esempio progettati con funzionalità avanzate, ad esempio i tipi di carattere Pericle e Pescadero. Per ulteriori informazioni sulle funzionalità OpenType, vedere [funzionalità dei tipi di carattere OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).

## <a name="support-for-international-text"></a>Supporto per testo internazionale

[DirectWrite](direct-write-portal.md) utilizza i tipi di carattere [OpenType](../intl/opentype-font-format.md) per consentire un ampio supporto per il testo internazionale. Sono supportate funzionalità Unicode quali surrogati, BIDI, interruzioni di riga e UV. La creazione di elementi, la sostituzione e la definizione di un glifo di script basati sul linguaggio garantiscono che il layout e il rendering del testo in qualsiasi script siano corretti.

Sono attualmente supportati gli script seguenti:

> [!Note]  
> Per gli script contrassegnati con un \* , non sono disponibili tipi di carattere di sistema predefiniti. Le applicazioni devono installare i tipi di carattere che supportano questi script.

 

-   Arabo
-   Armeno
-   Bengala
-   Bopomofo
-   Braille\*
-   Sillabico aborigeno canadese
-   Cherokee
-   Cinese (semplificato & tradizionale)
-   Cirillico
-   Copto\*
-   Devanagari
-   Etiope
-   Georgiano
-   Glagolitico\*
-   Greco
-   Gujarati
-   Gurmukhi
-   Ebraico
-   Giapponese
-   Kannada
-   Khmer
-   Coreano
-   Lao
-   Latino
-   Malayalam
-   Mongolo
-   Myanmar
-   Nuovo tai lue
-   Ogamico\*
-   Odia
-   ' Carattere phags-pa
-   Runico\*
-   Singalese
-   Siriaco
-   Tai le
-   Tamil
-   Telugu
-   Thaana
-   Thai
-   Tibetano
-   Yi

## <a name="multiple-layers-of-functionality"></a>Più livelli di funzionalità

[DirectWrite](direct-write-portal.md) fornisce livelli di funzionalità con factoring, in cui ogni livello interagisce senza interruzioni con il successivo. Il progetto API offre agli sviluppatori di applicazioni la libertà e la flessibilità di adottare singoli livelli, a seconda delle esigenze e della pianificazione. Nel diagramma seguente viene illustrata la relazione tra questi livelli.

![diagramma dei livelli DirectWrite e del modo in cui comunicano con un'applicazione o un Framework dell'interfaccia utente e l'API grafica](images/intro-01.png)

L'API di layout del testo fornisce la funzionalità di livello più alto disponibile in [DirectWrite](direct-write-portal.md). Fornisce servizi per l'applicazione per misurare, visualizzare e interagire con stringhe di testo formattate in modo completo. Questa API di testo può essere usata nelle applicazioni che attualmente usano Win32 DrawText per creare un'interfaccia utente moderna con testo formattato in modo completo.

Le applicazioni con utilizzo intensivo del testo che implementano il proprio motore di layout possono utilizzare il livello successivo, ovvero il processore di script. Il processore di script suddivide un blocco di testo in blocchi di script e gestisce il mapping tra le rappresentazioni Unicode e la rappresentazione del glifo appropriata nel tipo di carattere, in modo che il testo dello script possa essere visualizzato correttamente nella lingua corretta. Il sistema di layout utilizzato dal livello API del layout del testo è basato sul sistema di elaborazione di tipi di carattere e script.

Il livello di rendering del glifo è il livello più basso di funzionalità e fornisce funzionalità di rendering dei glifi per le applicazioni che implementano il proprio motore di layout di testo. Il livello di rendering del glifo è utile anche per le applicazioni che implementano un renderer personalizzato per modificare il comportamento di disegno del glifo tramite la funzione di callback nell'API di formattazione del testo [DirectWrite](direct-write-portal.md) .

Il sistema dei tipi di carattere [DirectWrite](direct-write-portal.md) è disponibile per tutti i livelli funzionali di DirectWrite e consente a un'applicazione di accedere alle informazioni sul tipo di carattere e sul glifo. È progettato per gestire le tecnologie dei tipi di carattere e i formati di dati comuni. Il modello di tipo di carattere DirectWrite segue la pratica tipografica comune di supportare un numero qualsiasi di pesi, stili e estendezioni nella stessa famiglia di caratteri. Questo modello, lo stesso modello seguito da WPF e CSS, specifica che i tipi di carattere che differiscono solo per il peso (grassetto, chiaro e così via), lo stile (verticale, corsivo o obliquo) o l'estensione (stretta, ridotta, ampia e così via) vengono considerati membri di una singola famiglia di caratteri.

### <a name="improved-text-rendering-with-cleartype"></a>Rendering del testo migliorato con ClearType

Migliorare la leggibilità sullo schermo è un requisito fondamentale per tutte le applicazioni Windows. L'evidenza della ricerca nella psicologia cognitiva indica che è necessario essere in grado di riconoscere accuratamente ogni lettera e che la spaziatura tra le lettere è fondamentale per l'elaborazione rapida. Le lettere e le parole che non sono simmetriche vengono percepite come orribili e peggiorano l'esperienza di lettura. Kevin Larson, Microsoft Advanced Reading Technologies Group, ha scritto un articolo sull'argomento pubblicato in Spectrum IEEE. L'articolo è denominato "tecnologia del testo" ( https://www.spectrum.ieee.org/print/5049) .

Il rendering del testo in [DirectWrite](direct-write-portal.md) viene eseguito utilizzando Microsoft ClearType, che migliora la chiarezza e la leggibilità del testo. ClearType sfrutta il fatto che gli schermi LCD moderni hanno striping RGB per ogni pixel che possono essere controllati singolarmente. DirectWrite utilizza i miglioramenti più recenti per ClearType, incluso prima con Windows Vista con Windows Presentation Foundation, che consente di valutare non solo le singole lettere, ma anche la spaziatura tra le lettere. Prima di questi miglioramenti di ClearType, il testo con una dimensione di "lettura" di 10 o 12 punti era difficile da visualizzare: è possibile posizionare un pixel tra le lettere, che era spesso troppo piccolo o 2 pixel, che era spesso troppo grande. L'uso della risoluzione aggiuntiva nei subpixel fornisce la spaziatura frazionaria, che migliora l'uniformità e la simmetria dell'intera pagina.

Nell'illustrazione seguente viene illustrato il modo in cui i glifi possono iniziare su qualsiasi limite dei sottopixel quando si utilizza il posizionamento dei sottopixel.

Viene eseguito il rendering della figura seguente utilizzando la versione GDI del renderer ClearType, che non utilizza il posizionamento dei subpixel.

![illustrazione della "tecnologia" di cui è stato eseguito il rendering senza posizionamento dei subpixel](images/intro-03.png)

Viene eseguito il rendering della figura seguente usando la versione [DirectWrite](direct-write-portal.md) del renderer ClearType, che usa il posizionamento dei subpixel.

![illustrazione della "tecnologia" di cui è stato eseguito il rendering con il posizionamento dei subpixel](images/intro-04.png)

Si noti che la spaziatura tra le lettere h e n è più uniforme nella seconda immagine e la lettera o è distanziata ulteriormente dalla lettera n, più anche con la lettera l. Si noti inoltre che le steli sulle lettere l sono più naturali.

Il posizionamento ClearType del sottopixel offre la spaziatura più accurata dei caratteri sullo schermo, soprattutto in dimensioni ridotte, in cui la differenza tra un subpixel e un pixel intero rappresenta una percentuale significativa della larghezza del glifo. Consente di misurare il testo in uno spazio di risoluzione ideale e di eseguirne il rendering in corrispondenza della relativa posizione naturale, con la granularità del sottopixel. Il testo misurato e sottoposto a rendering mediante questa tecnologia è, per definizione, indipendente dalla risoluzione, vale a dire che lo stesso layout del testo viene effettuato attraverso la gamma di diverse risoluzioni di visualizzazione.

A differenza di entrambi i tipi di rendering GDI ClearType, il sottopixel ClearType offre la larghezza più accurata dei caratteri.

Per impostazione predefinita, l'API della stringa di testo adotta il rendering del testo dei sottopixel, il che significa che il testo viene misurato in base alla risoluzione ideale indipendentemente dalla risoluzione dello schermo corrente e produce il risultato del posizionamento del glifo in base alle larghezze di avanzamento e al posizionamento dei glifi effettivamente ridimensionati.

Per il testo di grandi dimensioni, [DirectWrite](direct-write-portal.md) Abilita anche l'anti-aliasing lungo l'asse y per rendere i bordi più uniformi ed eseguire il rendering delle lettere come la finestra di progettazione del tipo di carattere. La figura seguente mostra l'anti-aliasing della direzione y.

![illustrazione di "ClearType" di cui è stato eseguito il rendering come testo GDI e come testo DirectWrite con l'anti-aliasing della direzione y](images/intro-05.png)

Sebbene il testo di [DirectWrite](direct-write-portal.md) sia posizionato e sottoposto a rendering utilizzando il sottopixel ClearType per impostazione predefinita, sono disponibili altre opzioni di rendering. Molte applicazioni esistenti utilizzano GDI per eseguire il rendering della maggior parte dell'interfaccia utente e alcune applicazioni utilizzano i controlli di modifica del sistema che continuano a utilizzare GDI per il rendering del testo. Quando si aggiunge il testo di DirectWrite a queste applicazioni, potrebbe essere necessario sacrificare i miglioramenti dell'esperienza di lettura forniti da ClearType in subpixel, in modo che il testo abbia un aspetto coerente all'interno dell'applicazione.

Per soddisfare questi requisiti, [DirectWrite](direct-write-portal.md) supporta anche le seguenti opzioni di rendering:

-   ClearType del sottopixel (impostazione predefinita).
-   ClearType dei sottopixel con anti-aliasing in dimensioni orizzontali e verticali.
-   Testo con alias.
-   GDI naturale a larghezza (usato da Microsoft Word visualizzazione di lettura, ad esempio).
-   Compatibile con GDI: larghezza (inclusa la bitmap incorporata dell'Asia orientale).

Ognuna di queste modalità di rendering può essere ottimizzata tramite l'API DirectWrite e tramite il nuovo sintonizzatore ClearType della posta in arrivo di Windows 7.

> [!Note]  
> A partire da Windows 8, è consigliabile usare l'anti-aliasing del testo in scala di grigi nella maggior parte dei casi. Per altre informazioni, vedere la sezione seguente.

 

### <a name="support-for-natural-layout"></a>Supporto per il layout naturale

Il layout naturale è indipendente dalla risoluzione, quindi la spaziatura dei caratteri non cambia quando si esegue lo zoom avanti o indietro o a seconda del valore DPI dello schermo. Un vantaggio secondario è che la spaziatura è vera per la progettazione del tipo di carattere. Il layout naturale è reso possibile dal supporto di DirectWrite per il rendering naturale, il che significa che i singoli glifi possono essere posizionati in una frazione di pixel.

Sebbene il layout naturale sia quello predefinito, alcune applicazioni devono eseguire il rendering del testo con la stessa spaziatura e l'aspetto di GDI. Per tali applicazioni, DirectWrite fornisce le modalità di misurazione naturale GDI classico e GDI e le modalità di rendering corrispondenti.

Una delle modalità di rendering sopra elencate può essere combinata con una delle due modalità di anti-aliasing: ClearType o scala di grigi. L'anti-aliasing ClearType simula una risoluzione più elevata modificando singolarmente i valori di colore rosso, verde e blu di ogni pixel. L'anti-aliasing in scala di grigi calcola un solo valore di code coverage (o Alpha) per ogni pixel. ClearType è l'impostazione predefinita, ma l'anti-aliasing in scala di grigi è consigliato per le app di Windows Store perché è più veloce ed è compatibile con l'anti-aliasing standard, pur continuando a essere estremamente leggibile.

## <a name="api-overview"></a>Panoramica API

L'interfaccia [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) è il punto di partenza per l'uso della funzionalità DirectWrite. La Factory è l'oggetto radice che crea un set di oggetti che possono essere usati insieme.

L'operazione di formattazione e layout è un prerequisito per le operazioni, in quanto il testo deve essere formattato correttamente e disposto a un set di vincoli specificato prima di poter essere disegnato o sottoposto a hit test. Due oggetti chiave che è possibile creare con un [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) a questo scopo sono [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). Un oggetto **IDWriteTextFormat** rappresenta le informazioni di formattazione per un paragrafo di testo. La funzione [**IDWriteFactory archiviata nei:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) accetta la stringa di input, i vincoli associati, ad esempio la dimensione dello spazio da compilare e l'oggetto **IDWriteTextFormat** , e inserisce il risultato completamente analizzato e formattato in **IDWriteTextLayout** da usare nelle operazioni successive.

L'applicazione può quindi eseguire il rendering del testo utilizzando la funzione [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) fornita da [Direct2D](../direct2d/direct2d-portal.md) o implementando una funzione di callback che può utilizzare GDI, Direct2D o altri sistemi grafici per eseguire il rendering dei glifi. Per un singolo testo di formato, la funzione [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) su Direct2D fornisce un modo più semplice per creare testo senza dover prima creare un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a>Formattazione e disegno di "Hello World" con DirectWrite

Nell'esempio di codice riportato di seguito viene illustrato come un'applicazione può formattare un singolo paragrafo utilizzando [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e come utilizzarla per creare la funzione di [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [Direct2D](../direct2d/direct2d-portal.md).


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a>Accesso al sistema di tipi di carattere

Oltre a specificare un nome della famiglia di caratteri per la stringa di testo usando l'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) nell'esempio precedente, [DirectWrite](direct-write-portal.md) offre alle applicazioni un maggiore controllo sulla selezione dei tipi di carattere tramite l'enumerazione dei tipi di carattere e la possibilità di creare una raccolta di tipi di carattere personalizzata basata su tipi di carattere incorporati.

L'oggetto [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) è una raccolta di famiglie di caratteri. DirectWrite consente di accedere al set di tipi di carattere installati nel sistema tramite una raccolta di tipi di carattere speciale denominata raccolta di tipi di carattere di sistema. Questa operazione viene ottenuta chiamando il metodo [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) dell'oggetto [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) . Un'applicazione può inoltre creare una raccolta di tipi di carattere personalizzata da un set di tipi di carattere enumerati da un callback definito dall'applicazione, ovvero tipi di carattere privati installati da un'applicazione o tipi di carattere incorporati in un documento.

L'applicazione può quindi chiamare [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) per ottenere un oggetto FontFamily specifico all'interno della raccolta e quindi chiamare [**IDWriteFontFamily:: GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) per ottenere un oggetto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) specifico. L'oggetto **IDWriteFont** rappresenta un tipo di carattere in una raccolta di tipi di carattere ed espone le proprietà e alcune metriche dei tipi di carattere di base.

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) è un altro oggetto che rappresenta un tipo di carattere ed espone un set completo di metriche su un tipo di carattere. **IDWriteFontFace** può essere creato direttamente da un nome di tipo di carattere; per accedere a un'applicazione non è necessario ottenere una raccolta di tipi di carattere. È utile per un'applicazione di layout di testo, ad esempio Microsoft Word, che deve eseguire una query sui dettagli per un tipo di carattere specifico.

Nel diagramma seguente viene illustrata la relazione tra questi oggetti.

![diagramma della relazione tra una raccolta di tipi di carattere, una famiglia di caratteri e un tipo di carattere](images/fontcollection.png)

### <a name="idwritefontface"></a>IDWriteFontFace

L'oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) rappresenta un tipo di carattere e fornisce informazioni più dettagliate sul tipo di carattere rispetto all'oggetto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) . Le metriche relative al tipo di carattere e al glifo della **IDWriteFontFace** sono utili per le applicazioni che implementano il layout del testo.

La maggior parte delle applicazioni mainstream non utilizzerà queste API direttamente e utilizzerà invece [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) o specifica direttamente il nome della famiglia di caratteri.

Nella tabella seguente sono riepilogati gli scenari di utilizzo per i due oggetti.



| Category                                                                                                         | [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| API per supportare l'interazione dell'utente, ad esempio un'interfaccia utente di selezione dei tipi di carattere: Descrizione e altre API informative | Sì                                        | No                                                 |
| API per supportare il mapping dei tipi di carattere: famiglia, stile, peso, estensione, code coverage dei caratteri                                 | Sì                                        | No                                                 |
| API DrawText                                                                                                     | Sì                                        | No                                                 |
| API usate per il rendering                                                                                          | No                                         | Sì                                                |
| API usate per il layout del testo: metriche del glifo e così via                                                              | No                                         | Sì                                                |
| API per il controllo dell'interfaccia utente e il layout del testo: metriche a livello di carattere                                                           | Sì                                        | Sì                                                |



 

Di seguito è riportato un esempio di applicazione che enumera i tipi di carattere nella raccolta di tipi di carattere di sistema.


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a>Rendering del testo

Le API per il rendering del testo consentono di eseguire il rendering dei glifi in un tipo di carattere [DirectWrite](direct-write-portal.md) in una superficie [Direct2D](../direct2d/direct2d-portal.md) o in una bitmap indipendente dal dispositivo GDI oppure di essere convertiti in strutture o bitmap. Il rendering ClearType in DirectWrite supporta il posizionamento dei subpixel con maggiore nitidezza e contrasto rispetto alle implementazioni precedenti di Windows. DirectWrite supporta anche testo in bianco e nero con alias per supportare scenari che coinvolgono caratteri asiatici orientali con bitmap incorporate o in cui l'utente ha disabilitato la smussatura dei caratteri di qualsiasi tipo.

Tutte le opzioni sono regolabili da tutte le manopole ClearType disponibili accessibili tramite le API [DirectWrite](direct-write-portal.md) ed esposte anche tramite la nuova applet del pannello di controllo del sintonizzatore ClearType di Windows 7.

Sono disponibili due API per il rendering dei glifi, una che fornisce il rendering con accelerazione hardware tramite [Direct2D](../direct2d/direct2d-portal.md) e l'altra che fornisce il rendering del software a una bitmap GDI. Un'applicazione che usa [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e l'implementazione del callback [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) può chiamare una di queste funzioni in risposta a un callback [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) . Inoltre, le applicazioni che implementano il proprio layout o gestiscono i dati a livello di glifo possono usare queste API.

1.  [**ID2DRenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    Le applicazioni possono usare l'API [Direct2D](../direct2d/direct2d-portal.md) [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) per fornire l'accelerazione hardware per il rendering del testo con la GPU. L'accelerazione hardware ha effetto su tutte le fasi della pipeline di rendering del testo, dall'Unione di glifi alle esecuzioni di glifi e dall'applicazione di filtri alla bitmap di esecuzione del glifo, all'applicazione dell'algoritmo di Blend ClearType all'output visualizzato finale. Si tratta dell'API consigliata per ottenere le migliori prestazioni di rendering.

2.  [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    Le applicazioni possono usare il metodo [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per eseguire il rendering del software di un'esecuzione di glifi in una bitmap da 32 BPP. L'oggetto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) incapsula una bitmap e un contesto di dispositivo di memoria che può essere usato per il rendering dei glifi. Questa API è utile se si desidera rimanere con GDI perché si dispone di una codebase esistente che esegue il rendering in GDI.

Se si dispone di un'applicazione che dispone di codice di layout di testo che utilizza GDI e si desidera mantenere il codice di layout esistente ma si utilizza [DirectWrite](direct-write-portal.md) solo per il passaggio finale dei glifi di rendering, [**IDWriteGdiInterop:: CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) fornisce il Bridge tra le due API. Prima di chiamare questa funzione, l'applicazione userà la funzione **IDWriteGdiInterop:: CreateFontFaceFromHdc** per ottenere un riferimento del tipo di carattere da un contesto di dispositivo.

> [!Note]  
> Per la maggior parte degli scenari, è possibile che le applicazioni non debbano usare queste API per il rendering di glifi. Dopo che un'applicazione ha creato un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , può usare il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) per eseguire il rendering del testo.

 

## <a name="custom-rendering-modes"></a>Modalità di rendering personalizzate

Un numero di parametri influisce sul rendering del testo, ad esempio gamma, livello ClearType, geometria pixel e contrasto migliorato. I parametri di rendering sono incapsulati da un oggetto che implementa l'interfaccia [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) pubblica. L'oggetto parametri di rendering viene inizializzato automaticamente in base alle proprietà hardware e/o alle preferenze utente specificate tramite l'applet del pannello di controllo ClearType in Windows 7. In genere, se un client usa l'API di layout [DirectWrite](direct-write-portal.md) , DirectWrite seleziona automaticamente una modalità di rendering che corrisponde alla modalità di misurazione specificata.

Le applicazioni che vogliono un maggiore controllo possono usare [**IDWriteFactory archiviata nei:: CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) per implementare le diverse opzioni di rendering. Questa funzione può essere usata anche per impostare la gamma, la geometria dei pixel e il contrasto migliorato.

Di seguito sono riportate le varie opzioni di rendering disponibili:

-   Anti-aliasing sub-pixel

    L'applicazione imposta il parametro *renderingMode* sulla \_ modalità di rendering DWrite \_ \_ Natural per specificare il rendering con anti-aliasing solo nella dimensione orizzontale.

-   Anti-aliasing di sottopixel in dimensioni orizzontali e verticali.

    L'applicazione imposta il parametro *renderingMode* sulla \_ modalità di rendering DWrite \_ \_ Natural \_ simmetrica per specificare il rendering con anti-aliasing nelle dimensioni orizzontale e verticale. In questo modo, le curve e le linee diagonali sembrano più smussate a scapito della morbidezza e vengono in genere usate in dimensioni superiori a 16 ppem.

-   Testo con alias

    L'applicazione imposta il parametro *renderingMode* su \_ modalità di rendering DWrite \_ \_ con alias per specificare il testo con alias.

-   Testo in scala di grigi

    L'applicazione imposta il parametro *pixelGeometry* su DWrite \_ pixel \_ Geometry \_ flat per specificare il testo in scala di grigi.

-   Compatibile con GDI: larghezza (inclusa la bitmap incorporata dell'Asia orientale)

    L'applicazione imposta il parametro *renderingMode* sulla \_ modalità di rendering DWrite \_ \_ GDI \_ classico per specificare l'anti-aliasing a larghezza compatibile con GDI.

-   GDI naturale-larghezza

    L'applicazione imposta il parametro *renderingMode* sulla \_ modalità di rendering DWrite \_ \_ GDI \_ Natural per specificare l'anti-aliasing compatibile con larghezza naturale GDI.

-   Testo struttura

    Per il rendering di grandi dimensioni, uno sviluppatore di applicazioni potrebbe preferire il rendering usando il contorno dei tipi di carattere anziché eseguendo la rasterizzazione in una bitmap. L'applicazione imposta il parametro *renderingMode* sulla **\_ \_ \_ struttura della modalità di rendering DWrite** per specificare che il rendering deve ignorare il rasterizzatore e utilizzare direttamente le strutture.

## <a name="gdi-interoperability"></a>Interoperabilità GDI

L'interfaccia [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) fornisce l'interoperabilità con GDI. Questo consente alle applicazioni di continuare l'investimento esistente nelle basi di codice GDI e di usare selettivamente [DirectWrite](direct-write-portal.md) per il rendering o il layout.

Di seguito sono riportate le API che consentono a un'applicazione di eseguire la migrazione da o verso il sistema di tipi di carattere GDI:

-   [**CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    Crea un oggetto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) che corrisponde alle proprietà specificate dalla struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

-   [**ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    Inizializza una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basata sulle proprietà compatibili con GDI del [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)specificato.

-   [**ConvertFontFaceToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    Inizializza una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basata sulle proprietà compatibili con GDI del [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)specificato.

-   [**CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    Crea un oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) che corrisponde al **Hfont** attualmente selezionato.

## <a name="conclusion"></a>Conclusione

Il miglioramento dell'esperienza di lettura è di grande importanza per gli utenti che si trovino sullo schermo o su carta. [DirectWrite](direct-write-portal.md) offre la facilità d'uso e il modello di programmazione a più livelli per gli sviluppatori di applicazioni per migliorare l'esperienza di testo per le applicazioni Windows. Le applicazioni possono usare DirectWrite per eseguire il rendering del testo formattato in modo RTF per l'interfaccia utente e i documenti con l'API layout. Per scenari più complessi, un'applicazione può lavorare direttamente con glifi, accedere a tipi di carattere e così via e sfruttare la potenza di DirectWrite per offrire funzionalità tipografiche di alta qualità.

Le funzionalità di interoperabilità di [DirectWrite](direct-write-portal.md) consentono agli sviluppatori di applicazioni di portare avanti le codebase Win32 esistenti e di adottare DirectWrite in modo selettivo all'interno delle applicazioni.

 

 