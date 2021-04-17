---
title: Uso di DirectX con schermi HDR e colori avanzati
description: In questo argomento viene fornita una panoramica tecnica sul rendering di contenuti High Dynamic Range Direct3D 11 e Direct3D 12 in una visualizzazione HDR10 con il supporto dei colori avanzati di Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104566148"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a>Uso di DirectX con schermi di intervallo dinamici elevati e colori avanzati

In questo argomento viene fornita una panoramica tecnica sull'output di contenuto Direct3D 11 e Direct3D 11 (HDR) a una visualizzazione HDR10 con il supporto di colori avanzati di Windows 10. Vengono riepilogate alcune delle principali differenze concettuali tra l'output e la visualizzazione di HDR10 rispetto alle visualizzazioni standard tradizionali (SDR, Dynamic Range) standard. Vengono inoltre illustrati i principali requisiti tecnici che consentono all'app di supportare correttamente Windows Advanced Color, oltre a raccomandazioni e procedure consigliate.

## <a name="introduction"></a>Introduzione

Windows 10 supporta le visualizzazioni HDR e altri colori avanzati, che offrono una fedeltà dei colori significativamente superiore rispetto alla visualizzazione SDR tradizionale. È possibile usare Direct3D, Direct2D e altre API grafiche per eseguire il rendering del contenuto HDR in una visualizzazione idonea.

Windows Advanced Color si riferisce a diverse tecnologie correlate, introdotte per la prima volta con Windows 10 versione 1703, che forniscono il supporto per le visualizzazioni che superano le funzionalità di colore di standard standard (SDR) tradizionale. Le tre principali funzionalità estese sono descritte di seguito. Il tipo più comune di visualizzazione dei colori avanzata, HDR10, supporta tutte e tre le funzionalità estese.

### <a name="high-dynamic-range"></a>Intervallo dinamico elevato

L'intervallo dinamico si riferisce alla differenza tra la luminosità massima e minima in una scena. Questa operazione viene spesso misurata in nit (candela per centimetro quadrato). Le scene reali, ad esempio questo tramonto, presentano spesso intervalli dinamici di 10 ordini di grandezza della luminanza; l'occhio umano può discernere un intervallo ancora maggiore dopo l'adattamento.

![immagine di un tramonto con luminosità e punti più bui nella scena con etichetta](images/HDR-HDR.jpg)

Da Direct3D 9, i motori grafici sono stati in grado di eseguire internamente il rendering delle scene con questo livello di fedeltà fisicamente accurata. Tuttavia, un tipico display con intervalli dinamici standard è in grado di riprodurre solo più di 3 ordini di grandezza della luminanza e pertanto qualsiasi contenuto con rendering HDR doveva essere Tonemapped (compresso) nell'intervallo limitato dello schermo. Le nuove visualizzazioni HDR, incluse quelle conformi allo standard HDR10 (BT. 2100), interrompono questa limitazione.

### <a name="wide-color-gamut-with-automatic-system-color-management"></a>Ampia gamma di colori con gestione automatica dei colori del sistema

Il gamut dei colori si riferisce all'intervallo e alla saturazione dei colori che possono essere riprodotti da una visualizzazione. Il colore naturale più saturo che l'occhio umano può percepire è pura, luce monocromatica, ad esempio ciò che è prodotto da un laser. Tuttavia, le visualizzazioni dei consumer mainstream possono spesso riprodurre colori solo all'interno della gamut sRGB, che rappresenta solo il 35% di tutti i colori percepibili. Il diagramma seguente è una rappresentazione del "locus spettrale" umano o di tutti i colori percepibili (a un determinato livello di luminanza), in cui il triangolo più piccolo è la gamut di sRGB.

![diagramma del locus e della gamut dello spettro umano](images/HDR-WCG.jpg)

Gli schermi High end e Professional PC presentano gamme di colori supportate a lungo, significativamente più larghe rispetto a sRGB, ad esempio Adobe RGB e D65-P3. E questo ampio numero di visualizzazioni è sempre più comune. Tuttavia, prima del colore avanzato, Windows non ha eseguito alcuna gestione dei colori a livello di sistema per le applicazioni. Ciò significava che se un'app DirectX veniva sottoposta a rendering, ad esempio, un rosso o RGB (1.0, 0,0, 0,0) alla catena di scambio, Windows analizzava semplicemente il rosso più saturo che la visualizzazione poteva riprodurre, indipendentemente dalla gamma di colori effettiva dello schermo.

Le app che necessitavano di un'accuratezza dei colori elevata potevano eseguire query sulle funzionalità cromatiche dello schermo (ad esempio, usando i profili ICC) ed eseguire la gestione dei colori in-process per individuare correttamente la gamma di colori della visualizzazione. Tuttavia, la maggior parte delle app e del contenuto visivo presuppone che la visualizzazione sia sRGB e che si basino sul sistema operativo per soddisfare questo presupposto.

Windows Advanced Color consente la gestione automatica dei colori a livello di sistema. Il Gestione finestre desktop (DWM) è il compositor di Windows. Quando è abilitata la funzionalità colore avanzato, DWM esegue una conversione esplicita dei colori dallo spazio dei colori del contenuto visivo dell'app allo spazio colore della composizione canonica, che è scRGB. Windows quindi color: converte il contenuto del framebuffer composto nello spazio colore nativo della visualizzazione. In questo modo, il contenuto sRGB tradizionale ottiene automaticamente un comportamento accurato per il colore, mentre le app compatibili con i colori avanzate possono sfruttare le funzionalità di colore complete dello schermo.

### <a name="deep-precisionbit-depth"></a>Precisione profonda/profondità bit

La precisione numerica, o la profondità del bit, si riferisce a rappresentare o distinguere colori simili ma distinti senza bande né artefatti. Il PC mainstream Visualizza il supporto di 8 bit per canale di colore, mentre l'occhio umano richiede almeno 10-12 bit di precisione per evitare distorsioni percepibili, senza ricorrere a tecniche come la dithering o a seconda delle condizioni di visualizzazione.

![immagine di turbine a 2 bit simulati per canale di colore rispetto a 8 bit per canale](images/HDR-bitdepth.jpg)

Prima del colore avanzato, le app con finestra con restrizioni di DWM potevano inviare il contenuto solo a 8 bit per canale di colore, anche se la visualizzazione supportava una profondità di bit superiore. Quando il colore avanzato è abilitato, DWM ne esegue la composizione usando il punto a virgola mobile a metà precisione IEEE (FP16), eliminando eventuali colli di bottiglia e consentendo l'uso della precisione completa dello schermo.

## <a name="system-requirements"></a>Requisiti di sistema

### <a name="operating-system-os"></a>Sistema operativo

Il supporto dei colori avanzati è stato prima fornito con Windows 10, versione 1703, ed è stato notevolmente migliorato a ogni aggiornamento. Questo argomento presuppone che l'applicazione sia destinata a Windows 10, versione 1903 o successiva.

### <a name="display"></a>Visualizza

Per sfruttare i vantaggi di un intervallo dinamico elevato, è necessario disporre di una visualizzazione che supporti lo standard HDR10. Windows funziona al meglio con le visualizzazioni con [certificazione VESA DisplayHDR](https://displayhdr.org/).

### <a name="graphics-processor-gpu"></a>Processore grafico (GPU)

È necessaria una GPU recente. Per supportare le visualizzazioni HDR10, Windows 10 richiede uno dei seguenti elementi.

* NVIDIA GeForce 1000 Series (Pascal) o versione successiva
* Serie AMD Radeon RX 400 (Polaris) o versione successiva
* Serie Intel Core 7 selezionata (KABY Lake) o versione successiva

Si noti che i requisiti hardware aggiuntivi si applicano a seconda degli scenari, tra cui l'accelerazione del codec hardware (HEVC a 10 bit, VP9 a 10 bit e così via) e il supporto PlayReady (SL3000). Per informazioni più specifiche, contattare il fornitore della GPU.

### <a name="graphics-driver-wddm"></a>Driver Graphics (WDDM)

Il driver di grafica disponibile più recente è fortemente consigliato, da Windows Update o dal sito Web del fornitore della GPU o del produttore del computer. Per Windows 10, versione 1903 e versioni successive, è consigliabile che i driver supportino almeno Windows Display Driver Model (WDDM) versione 2,6.

## <a name="supported-rendering-apis"></a>API di rendering supportate

Windows 10 supporta un'ampia gamma di Framework e API per il rendering. Il supporto dei colori avanzati si basa fondamentalmente sull'app per poter eseguire una presentazione moderna usando DXGI o le API del livello visivo.

* [Infrastruttura grafica DirectX (DXGI)](../direct3ddxgi/dx-graphics-dxgi.md)
* [Livello visivo (Windows. UI. Composition)](/windows/uwp/composition/visual-layer)

Pertanto, qualsiasi API di rendering che può restituire uno di questi metodi di presentazione può supportare il colore avanzato. Questo include, ma non è limitato a questi.

* [Direct3D 11](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [Direct3D 12](../direct3d12/direct3d-12-graphics.md)
* [Direct2D](../direct2d/direct2d-portal.md)
* [Win2D](https://github.com/Microsoft/Win2D)
  * Richiede l'uso delle API **CanvasSwapChain** o **CanvasSwapChainPanel** di livello inferiore.
* [**Windows.UI.Input.Inking**](/uwp/api/Windows.UI.Input.Inking)
  * Supporta il rendering dell'input penna personalizzato con DirectX.
* [XAML](/windows/uwp/xaml-platform/)
  * Supporta la riproduzione di video HDR usando **mediaplayerelement**.
  * Supporta la decodifica di immagini JPEG XR usando l'elemento **Image** .
  * Supporta l'interoperabilità DirectX con **SwapChainPanel**.

## <a name="handling-dynamic-display-capabilities"></a>Gestione delle funzionalità di visualizzazione dinamiche

Windows 10 supporta un'ampia gamma di schermi avanzati che supportano i colori, da pannelli integrati con efficienza energetica ai monitor e ai televisori di giochi high-end. Gli utenti di Windows si aspettano che l'app gestisca facilmente tutte queste varianti, incluse le visualizzazioni SDR esistenti.

Windows 10 offre agli utenti il controllo delle funzionalità di colore HDR e avanzate. L'app deve rilevare la configurazione della visualizzazione corrente e rispondere in modo dinamico alle modifiche della funzionalità. Questo problema può verificarsi per diversi motivi, ad esempio perché l'utente ha abilitato o disabilitato una funzionalità o ha spostato l'app tra diversi schermi oppure lo stato di alimentazione del sistema è cambiato.

### <a name="universal-windows-platform-uwp-apps"></a>App piattaforma UWP (Universal Windows Platform) (UWP)

Se si sta scrivendo un'app UWP, indipendentemente dall'API di rendering grafica in uso, usare [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) per ottenere le funzionalità di visualizzazione. Ottenere un'istanza di **AdvancedColorInfo** da [**DisplayInformation:: GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).

Per verificare il tipo di colore avanzato attualmente attivo, utilizzare la proprietà [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) . In Windows 10, versione 1903 e versioni successive, restituisce uno dei tre valori possibili: **SDR**, **WCG** o **HDR**. Si tratta della proprietà più importante da controllare ed è necessario configurare la pipeline di rendering e presentazione in risposta al tipo attivo.

Per verificare quali tipi di colore avanzati sono supportati, ma non necessariamente attivi, chiamare [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable). Queste informazioni possono essere usate, ad esempio, per richiedere all'utente di passare all'app impostazioni di Windows in modo da abilitare l'abilitazione di HDR o WCG.

Gli altri membri di **AdvancedColorInfo** forniscono informazioni quantitative sul volume di colori fisico del pannello (luminanza e cromatura), corrispondenti ai metadati HDR statici di SMPTE St. 2086. Usare queste informazioni per configurare il mapping di tonemapping e gamut di HDR dell'app.

Per gestire le modifiche apportate alle funzionalità avanzate dei colori, effettuare la registrazione per l'evento [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) . Questo evento viene generato se per qualsiasi motivo viene modificato un parametro delle funzionalità di colore avanzate della visualizzazione.

Gestire questo evento ottenendo una nuova istanza di **AdvancedColorInfo** e controllando quali valori sono stati modificati.

### <a name="desktop-win32-directx-apps"></a>App DirectX desktop (Win32)

Se si sta scrivendo un'app Win32 e si usa DirectX per eseguire il rendering, usare [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) per ottenere le funzionalità di visualizzazione. Ottenere un'istanza di questo struct tramite [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).

Per verificare il tipo di colore avanzato attualmente attivo, utilizzare la proprietà dello **spazio** dei colori, che è di tipo [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), e contiene uno dei valori seguenti:

* **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR
* **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR

> [!Note]
> Altri tipi di colori avanzati, ad esempio WCG, vengono considerati come DSP da DXGI. Non è possibile usare DXGI per identificare una visualizzazione WCG.

> [!Note]
> DXGI non consente di controllare quali tipi di colore avanzati sono supportati ma non attivi al momento.

La maggior parte degli altri membri di **DXGI_OUTPUT_DESC1** fornisce informazioni quantitative sul volume di colori fisico (luminanza e cromatura) del pannello, corrispondenti ai metadati HDR statici di SMPTE St. 2086. Usare queste informazioni per configurare il mapping di tonemapping e gamut di HDR dell'app.

Le app Win32 non hanno un meccanismo nativo per rispondere alle modifiche avanzate della funzionalità colore. Se invece l'app usa un ciclo di rendering, è necessario eseguire una query su [**IDXGIFactory1:: uncurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) con ogni frame. Se viene segnalato **false**, è necessario ottenere un nuovo **DXGI_OUTPUT_DESC1** e verificare quali valori sono stati modificati.

Inoltre, il message pump Win32 deve gestire il messaggio di [**WM_SIZE**](../winmsg/wm-size.md) , che indica che è possibile che l'applicazione sia stata spostata tra diverse visualizzazioni.

> [!Note]
> Per ottenere un nuovo **DXGI_OUTPUT_DESC1**, è necessario ottenere la visualizzazione corrente. Tuttavia, non è necessario chiamare **IDXGISwapChain:: GetContainingOutput**. Ciò è dovuto al fatto che le catene di scambio restituiranno un output DXGI non aggiornato quando **DXGIFactory:: l'oggetto** è false e la ricreazione della catena di scambio per ottenere un output corrente genera una schermata nera temporanea. È invece consigliabile enumerare i limiti di tutti gli output di DXGI e determinare quale è la più grande intersezione con i limiti della finestra dell'app.

L'esempio di codice seguente deriva dal [repository DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a>Configurazione della catena di scambio DirectX

Una volta stabilito che la visualizzazione supporta attualmente le funzionalità di colore avanzate, configurare la catena di scambio come indicato di seguito.

### <a name="use-a-flip-presentation-model-effect"></a>Usare un effetto del modello Flip Presentation

Quando si crea la catena di scambio usando **CreateSwapChainFor [HWND | Composizione | CoreWindow]** metodi, è necessario usare il modello DXGI Flip selezionando l'opzione **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** o **DXGI_SWAP_EFFECT_FLIP_DISCARD** , che rende la catena di scambio idonea per l'elaborazione dei colori avanzata da DWM e varie ottimizzazioni a schermo intero. Per ulteriori informazioni, vedere l'argomento [per ottenere prestazioni ottimali, utilizzare DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a>Opzione 1. Usare il formato pixel FP16 e lo spazio colore scRGB

Windows 10 supporta due combinazioni principali di formato pixel e spazio colore per i colori avanzati. Selezionarne uno in base ai requisiti specifici dell'app.

Per le app per utilizzo generico, quando si crea una catena di scambio è consigliabile specificare [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Questo è noto anche come *FP16* nel [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). Per impostazione predefinita, una catena di scambio creata con un formato pixel a virgola mobile viene considerata come se utilizzasse lo spazio colore [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , noto anche come *ScRGB*.

Questa combinazione fornisce l'intervallo numerico e la precisione per specificare quasi tutti i colori fisicamente possibili ed eseguire l'elaborazione arbitraria, inclusa la fusione. Inoltre, se si usa Direct2D, Win2D o Windows. UI. Composition, questa è l'unica combinazione supportata per qualsiasi catena di scambio o destinazione intermedia che contiene contenuto colore avanzato. 

Il compromesso principale di questa opzione è che utilizza 64 bit per pixel, che raddoppiano l'utilizzo della larghezza di banda e della memoria GPU rispetto ai formati di pixel UINT8 SDR tradizionali. Inoltre, scRGB utilizza valori numerici che non rientrano nell'intervallo normalizzato [0,1] per rappresentare i colori che non rientrano nel gamut di sRGB e/o superiori a 80 nit di luminanza. Ad esempio, scRGB (1,0, 1,0, 1,0) codifica il bianco D65 standard a 80 nit; Tuttavia, scRGB (12,5, 12,5, 12,5) codifica lo stesso D65 bianco a un livello molto più luminoso di 1000 nit. Alcune operazioni grafiche richiedono un intervallo numerico normalizzato ed è necessario modificare l'operazione o rinormalizzare i valori dei colori.

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a>Opzione 2: usare il formato pixel UINT10/RGB10 e lo spazio colore HDR10/BT. 2100

Per le app che usano contenuto con codifica HDR10, ad esempio lettori multimediali o app che dovrebbero essere usate principalmente in scenari a schermo intero, ad esempio giochi, quando si crea la catena di scambio è consigliabile specificare [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). Per impostazione predefinita, questo viene considerato come usando lo spazio dei colori di sRGB; Pertanto, è necessario chiamare in modo esplicito [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)e impostare come spazio colore [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), noto anche come HDR10/BT. 2100.

Questa combinazione presenta restrizioni più restrittive rispetto a FP16. Questa operazione può essere usata solo con Direct3D 11 o Direct3D 12. Inoltre, UINT10/HDR10 presenta limitazioni come formato temporaneo perché usa la funzione ST. 2084 EOTF ("gamma"), che è altamente non lineare, e ottimizzata come formato wire, e perché offre solo 2 bit di alfa.

Questa combinazione può tuttavia offrire potenti ottimizzazioni delle prestazioni quando viene usata nell'output finale dell'app. USA gli stessi 32 bit per pixel dei formati UINT8 SDR pixel tradizionali. Inoltre, in alcuni scenari a schermo intero, il sistema operativo può ottimizzare le prestazioni analizzando direttamente la superficie di HDR10.

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a>Uso di una catena di scambio colori avanzata quando la visualizzazione è in modalità SDR

È possibile usare una catena di scambio dei colori avanzata anche se la visualizzazione non supporta alcune o tutte le funzionalità di colore avanzate richieste dal contenuto. In questi casi, il Gestione finestre desktop (DWM) downconvert il contenuto per adattarlo alle funzionalità della visualizzazione. In Windows 10, versione 1903 e successive, eseguirà il ritaglio numerico; Se, ad esempio, si esegue il rendering in una catena di scambio FP16 scRGB, tutti gli elementi esterni all'intervallo numerico [0, 1] vengono ritagliati.

Questo comportamento Downconversion si verifica anche se la finestra dell'app si trova a due o più schermi con funzionalità di colore avanzate diverse. **AdvancedColorInfo** e **IDXGIOutput6** vengono estratti per segnalare solo le caratteristiche della visualizzazione "principale" (definite come visualizzazione contenente il centro della finestra).

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a>Eseguire correttamente il rendering del contenuto SDR con il livello bianco di riferimento SDR

In molti scenari, l'app vuole eseguire il rendering del contenuto sia di SDR che di HDR; ad esempio, il rendering di sottotitoli o controlli di trasporto su video HDR o sull'interfaccia utente in una scena di gioco. È importante comprendere il concetto di *livello bianco di riferimento SDR* per garantire che il contenuto SDR appaia corretto in una visualizzazione HDR.

Windows considera il contenuto HDR come _riferimento alla scena_, ovvero un particolare valore di colore deve essere visualizzato a un livello di luminanza specifico. ad esempio, scRGB (1,0, 1,0, 1,0) e HDR10 (497, 497, 497) codificano entrambi esattamente D65 bianchi alla luminanza di 80 nit. Nel frattempo, il contenuto SDR è stato tradizionalmente reso di _output_ (o a cui viene fatto riferimento), vale a dire che la luminanza viene lasciata all'utente o al dispositivo. ad esempio, sRGB (1,0, 1,0, 1,0) codifica D65 bianco come negli esempi HDR, ma con qualsiasi luminanza massima per la quale è configurata la visualizzazione. Windows consente all'utente di modificare il _livello di riferimento di DSP_ in base alla preferenza. si tratta della luminanza che Windows eseguirà il rendering di sRGB (1,0, 1,0, 1,0) in. Nei monitoraggi HDR del desktop i livelli bianchi di riferimento SDR sono in genere impostati su circa 200 nit.

> [!Note]
> In una visualizzazione che supporta un controllo della luminosità, ad esempio su un portatile, Windows modificherà anche la luminosità del contenuto HDR (a cui si fa riferimento) in modo che corrisponda al livello di luminosità desiderato dell'utente, ma ciò è invisibile all'app. A meno che non si stia tentando di garantire una riproduzione accurata del segnale HDR, in genere è possibile ignorare questo problema.

Se l'app esegue sempre il rendering di SDR e HDR per separare le superfici e si basa sulla composizione del sistema operativo, Windows eseguirà automaticamente la regolazione corretta per incrementare il contenuto di SDR al livello bianco desiderato. Ad esempio, se l'app usa XAML ed esegue il rendering del contenuto HDR nel proprio **SwapChainPanel**.

Tuttavia, se l'app esegue la propria composizione di DSP e contenuto HDR in un'unica superficie, si è responsabili dell'esecuzione autonoma della regolazione del livello bianco di riferimento SDR. In caso contrario, il contenuto di SDR potrebbe sembrare troppo debole presumendo condizioni di visualizzazione desktop tipiche. Per prima cosa, è necessario ottenere il livello bianco di riferimento SDR corrente, quindi è necessario modificare i valori dei colori di qualsiasi contenuto SDR di cui si sta eseguendo il rendering.

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a>Passaggio 1. Ottenere il livello bianco di riferimento SDR corrente

Attualmente, solo le app UWP possono ottenere il livello bianco di riferimento SDR corrente tramite [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits). Questa API richiede un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

### <a name="step-2-adjust-color-values-of-sdr-content"></a>Passaggio 2: Modificare i valori dei colori del contenuto SDR

Windows definisce il livello del bianco di riferimento nominale o predefinito a 80 pidocchi; Se quindi si esegue il rendering di un bianco standard (1,0, 1,0, 1,0) in una catena di scambio FP16, questo verrà riprodotto alla luminanza di 80 nit. Per corrispondere al livello di riferimento effettivo definito dall'utente, è necessario modificare il contenuto SDR da 80 nit al livello specificato tramite **AdvancedColorInfo. SdrWhiteLevelInNits**.

Se si esegue il rendering usando FP16 e ScRGB o qualsiasi spazio di colore che usa la gamma lineare (1,0), è possibile moltiplicare semplicemente il valore del colore SDR per _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_. Se si usa Direct2D, esiste una costante predefinita [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), che ha un valore di 80.

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

Se si esegue il rendering usando uno spazio di colore gamma non lineare, ad esempio HDR10, l'esecuzione della regolazione del livello bianco di SDR è più complessa. Se si sta scrivendo un pixel shader personalizzato, è consigliabile prendere in considerazione la conversione in gamma lineare per applicare la regolazione.

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a>Adattare il contenuto HDR alle funzionalità dello schermo usando tonemapping

Le visualizzazioni HDR e dei colori avanzati variano significativamente in termini di funzionalità. Ad esempio, la luminanza minima e massima e la gamma di colori che sono in grado di riprodurre. In molti casi, il contenuto HDR conterrà i colori che superano le funzionalità della visualizzazione. Per ottenere la migliore qualità dell'immagine, è importante eseguire tonemapping HDR, comprimendo essenzialmente l'intervallo di colori per adattarlo alla visualizzazione, mantenendo al tempo stesso la finalità visiva del contenuto.

Il più importante parametro singolo per adattarsi a è la luminanza massima, nota anche come MaxCLL (Content Light Level); tonemappers più sofisticate adatteranno anche la luminosità minima (MinCLL) e/o le primarie colore.

### <a name="step-1-get-the-displays-color-volume-capabilities"></a>Passaggio 1. Ottenere le funzionalità del volume di colori della visualizzazione

#### <a name="universal-windows-platform-uwp-apps"></a>App piattaforma UWP (Universal Windows Platform) (UWP)

Usare [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) per ottenere il volume di colori della visualizzazione.

#### <a name="win32-desktop-directx-apps"></a>App DirectX Win32 (desktop)

Usare [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) per ottenere il volume di colori della visualizzazione.

### <a name="step-2-get-the-contents-color-volume-information"></a>Passaggio 2: Ottenere le informazioni sul volume di colori del contenuto

A seconda della provenienza del contenuto HDR, esistono diversi modi possibili per determinare le informazioni relative alla luminanza e al gamut dei colori. Alcuni file di immagine e video HDR contengono metadati SMPTE ST. 2086. Se il rendering del contenuto è stato eseguito in modo dinamico, potrebbe essere possibile estrarre le informazioni sulle scene dalle fasi di rendering interne, ad esempio la fonte di luce più luminosa in una scena.

Una soluzione più generale ma costosa dal punto di vista del calcolo consiste nell'eseguire un istogramma o un altro passaggio di analisi nel frame sottoposto a rendering. L' [esempio di Direct2D Advanced color images SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) illustra come eseguire questa operazione tramite Direct2D; di seguito sono elencati i frammenti di codice più rilevanti:

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a>Passaggio 3. Eseguire l'operazione HDR tonemapping

Tonemapping è intrinsecamente un processo con perdita di perdite e può essere ottimizzato per una serie di metriche percettive o oggettive, quindi non esiste un algoritmo standard. Windows fornisce un [effetto Tonemapper HDR](../direct2d/hdr-tone-map-effect.md) incorporato come parte di Direct2D, oltre che nella pipeline di riproduzione video HDR Media Foundation. Altri algoritmi di uso comune includono le voci ACE filmica, Reinhard e ITU-R BT. 2390-3 EETF (funzione di trasferimento elettrico-elettrico).

Di seguito è illustrato un operatore tonemapper di Reinhard semplificato.

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a>Acquisizione di contenuto HDR e WCG

Le API che supportano la specifica di formati pixel, ad esempio quelle nello spazio dei nomi [**Windows. graphics. Capture**](/uwp/api/windows.graphics.capture) e il metodo [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , offrono la possibilità di acquisire contenuto HDR e WCG senza perdere le informazioni sui pixel. Si noti che dopo aver acquisito i frame di contenuto, è necessaria un'elaborazione aggiuntiva. Ad esempio, il mapping del tono da HDR a SDR (ad esempio, la copia della schermata SDR per Internet Sharing) e il salvataggio del contenuto con il formato appropriato (ad esempio, JPEG XR).

## <a name="additional-resources"></a>Risorse aggiuntive

* *Uso del rendering HDR con DirectX Tool Kit* per DirectX [11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering). Procedura dettagliata su come aggiungere il supporto HDR a un'app DirectX mediante DirectX Tool Kit (DirectXTK).
* [Esempio di Direct2D Advanced color images SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages). Esempio di SDK UWP che implementa un visualizzatore di immagini HDR e WCG con rilevamento del colore avanzato tramite Direct2D. Viene illustrata la gamma completa di procedure consigliate per le app UWP, tra cui la risposta alla visualizzazione delle modifiche alle funzionalità e la regolazione del livello di DSP bianco.
* [Esempio per desktop Direct3D 12 HDR](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR). Esempio di Desktop SDK che implementa una scena Direct3D 12 HDR di base.
* [Esempio Direct3D 12 HDR UWP](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR). UWP equivalente all'esempio precedente.
* [Esempio di SIMPLEHDR PC Xbox ATG](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC). Esempio di Desktop SDK che implementa una scena HDR 11 di base di Direct3D.
