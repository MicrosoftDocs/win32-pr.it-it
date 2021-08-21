---
title: API di grafica in Windows
description: Questo articolo illustra le Windows grafica e le API.
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848f24c42aa98c6d27a0873ab07c389dea24826d880188837536d83bd87549b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987161"
---
# <a name="graphics-apis-in-windows"></a>API di grafica in Windows

Windows Vista include il supporto per un modello di driver video completamente nuovo che rappresenta una revisione importante nella progettazione dei driver video dopo l'introduzione del modello di driver Windows (WDM) per Windows 98. Questo modello riprogettato riflette l'evoluzione dell'hardware video dal mondo delle operazioni raster 2D e delle applicazioni GDI a quello dei giochi 3D con hardware grafico a funzione fissa e infine a quello della moderna GPU (Programmable Graphics Processing Unit) che supporta un'ampia gamma di applicazioni grafiche ad alte prestazioni. Windows 7 e Windows 8 si basano sull'infrastruttura grafica Windows Vista fornendo api e funzionalità grafiche aggiuntive. Questo articolo illustra le Windows grafica e le API.

-   [Background](#background)
-   [Direct3D 9](#direct3d-9)
-   [Direct3D 9Ex](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10.1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11.1](#direct3d-111)
-   [Opengl](#opengl)
-   [Compatibilità delle applicazioni, GDI e versioni precedenti di Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [Indicazioni](#recommendations)

## <a name="background"></a>Sfondo

L'API principale per la programmazione della grafica fin dai primi Windows è stata l'interfaccia GDI (Graphical Device Interface). Questa API è stata progettata per gestire numerosi dispositivi di output 2D e ha costituito la base per l'esperienza Windows'interfaccia utente. DirectDraw e Direct3D sono stati introdotti come API alternative per supportare giochi a schermo intero e rendering 3D come estensioni all'hardware esistente del tempo. Le interazioni con GDI erano complesse. L'intermixing efficace degli elementi GDI tradizionali con gli elementi Direct3D è stato limitato da questa progettazione. La Windows XP di WDM, nota come XPDM, riflette la natura affiancata di GDI e Direct3D (vedere la figura 1).

**Figura 1. API di grafica in Windows XP**

![xpdm](images/graphics-apis-in-windows-xp.gif)

Nel corso degli anni, la potenza delle schede video 3D è aumentata notevolmente fino al punto in cui la maggior parte dell'hardware è dedicata a questa funzione. Un nuovo modello di driver, Windows Display Driver Model (WDDM), porta all'avanguardia la GPU e Direct3D, consentendo la creazione di un'esperienza completamente nuova, il desktop 3D, che combina perfettamente il mondo 2D di GDI con la potenza delle MODERNE GPU programmabili. Con WDDM, l'hardware video è interamente basato su Direct3D e tutte le altre interfacce grafiche comunicano con l'hardware video tramite il nuovo modello di driver incentrato su Direct3D (vedere la figura 2).

**Figura 2. API di grafica in Windows Vista**

![Wddm](images/graphics-apis-in-windows-vista.gif)

Per altre informazioni su WDDM, vedere guida Windows progettazione di [Vista Display Driver Model (WDDM)](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) su MSDN.

## <a name="direct3d-9"></a>Direct3D 9

La versione 9 di DirectX è stata rilasciata per la Windows nel 2002, con gli aggiornamenti successivi nel 2003 e nel 2004. Questa API rappresenta un decennio di evoluzione delle tecnologie DirectX, l'introduzione di modelli di programmazione shader più potenti per Direct3D e una maturità supportata da migliaia di titoli di spedizione. Direct3D 9 è l'interfaccia grafica principale in Windows Vista. Rimane l'API ideale da usare per la scrittura di giochi e applicazioni 3D che devono essere eseguiti nell'ampia gamma di hardware e versioni Windows esistenti. I dettagli del nuovo modello di driver sono nascosti alle applicazioni che usano le interfacce Direct3D 9, ma dietro le quinte il sistema operativo sfrutta appieno le nuove funzionalità per offrire un vero multitasking della GPU, una gestione delle risorse più efficiente e prestazioni affidabili.

Per garantire la compatibilità completa con le versioni precedenti di Windows, è necessario emulare alcune funzionalità del modello di driver precedente anche con il nuovo modello di driver video Windows Vista. Ad esempio, quando un'applicazione a schermo intero perde lo stato attivo, deve presupporre che abbia perso tutte le risorse nella memoria video (VRAM) e ricaricare quelle create come risorse non gestite anche se il nuovo modello di driver gestisce le risorse in modo trasparente senza che siano state rimosso dal contesto di dispositivo. Anche il concetto di tipo di risorsa gestito e predefinito è specifico per il modello di driver precedente. Un altro esempio è la previsione di errore quando si allocano risorse non gestite (pool predefinito) oltre la quantità di VRAM disponibile, anche se il nuovo modello di driver può fornire una quantità quasi illimitata di memoria video virtuale. A causa di questi requisiti, le applicazioni Direct3D in esecuzione Windows Vista riceveranno comunque queste condizioni di errore. Di conseguenza, sono limitati nella possibilità di usare le interfacce Direct3D 9 di base per usare completamente alcune funzionalità del nuovo modello di driver.

Mentre i nuovi sistemi distribuiti con Windows Vista includono schede video con driver WDDM e nella casella sono inclusi nuovi driver per una serie di schede video più diffusi, Windows Vista continua a supportare la possibilità di usare driver XPDM meno recenti per gli aggiornamenti e le edizioni aziendali. Nei sistemi che usano il modello di driver precedente è necessario usare Direct3D 9 e le interfacce precedenti e il funzionamento del sistema di grafica è molto simile a quello di Windows XP (Figura 1). WDDM è necessario per le applicazioni per usare Direct3D 9Ex, Direct3D 10 e versioni successive.

## <a name="direct3d-9ex"></a>Direct3D 9Ex

L'interfaccia Direct3D 9Ex consente di accedere a una leggera estensione dell'API Direct3D 9 standard che espone l'allocazione di risorse virtualizzate, la nuova semantica del dispositivo persa e altre nuove funzionalità disponibili durante l'esecuzione in Windows Vista. Creando questo oggetto esteso, l'API Direct3D 9 usa la nuova semantica e pertanto richiede all'applicazione di usare logica diversa (e quindi percorsi di codice diversi) per la creazione delle risorse, la gestione e la gestione degli errori per nuovi tipi di condizioni. Questa API è disponibile solo in Windows Vista e richiede driver WDDM. Poiché Direct3D 9Ex usa un'API separata e un percorso del codice del driver rispetto a Direct3D 9, il supporto di questa API richiede test case aggiuntivi per l'applicazione.

Il motivo principale per la creazione della nuova API Direct3D 9Ex è stato consentire l'accesso completo alle nuove funzionalità di WDDM mantenendo la compatibilità per le applicazioni Direct3D esistenti. Il nuovo desktop 3D e molte applicazioni specifiche di Windows Vista usano questa versione di Direct3D 9, ma non sono funzionali quando vengono eseguite in driver XPDM meno recenti. Poiché l'API Direct3D 9Ex non verrà mai visualizzata nelle versioni precedenti di Windows a causa della mancanza di supporto per WDDM, le interfacce Standard Direct3D 9 coprono un set di sistemi molto più ampio. Per le applicazioni ad alte prestazioni che possono sfruttare la nuova generazione di hardware video, la versione 10 di Direct3D completamente nuova offre molte nuove funzionalità non esposte da Direct3D 9Ex. Di conseguenza, per i giochi e la maggior parte delle altre applicazioni, Direct3D 9 o Direct3D 10 è l'API consigliata.

> [!Note]  
> DirectX SDK non fornisce esempi, intestazioni o librerie per l'interfaccia Direct3D 9Ex. MSDN Library e Windows SDK (noto in precedenza come Platform SDK) contengono la documentazione, le intestazioni e le librerie disponibili.

 

Per altre informazioni su Direct3D 9Ex, vedere [DirectX per](/previous-versions//ms681824(v=vs.85)) Windows Vista in MDSN.

## <a name="direct3d-10"></a>Direct3D 10

Per realizzare appieno il potenziale del nuovo modello di driver Windows Vista e dell'hardware di nuova generazione, è stata creata una versione completamente nuova dell'API Direct3D. Sebbene WDDM elimini alcune delle limitazioni relative alle prestazioni nel sistema grafico esistente, Direct3D 10 va oltre rimuovendo i colli di bottiglia di progettazione nell'API Direct3D esistente e semplifica notevolmente l'attività di programmazione della GPU.

La nuova API elimina completamente tutti gli aspetti a funzione fissa, sostituendoli con costrutti programmabili e semplificando notevolmente l'implementazione interna. Le centinaia di bit di funzionalità nelle versioni precedenti di Direct3D sono state completamente eliminate e sostituite con un set di funzionalità ben definito e inclusivo che include solo alcuni scenari di utilizzo facoltativi per formati di risorse specifici. La creazione e la convalida di risorse a elevato utilizzo di CPU hanno ora una semantica esplicita nella nuova API. Ciò consente un comportamento delle prestazioni molto più prevedibile e riduce notevolmente il sovraccarico per disegno. Le risorse possono essere riconfigurate in più forme per consentire un uso efficiente in varie fasi e il set di funzionalità impone molte meno restrizioni sugli scenari di utilizzo per i formati. Sono disponibili anche nuovi formati di trama mappa normale compressa a blocchi.

Nella nuova API le costanti shader e lo stato del dispositivo sono risorse esplicite, consentendo una memorizzazione nella cache molto più efficiente nell'hardware e semplificando notevolmente la convalida dei driver. Il modello di shader programmabile è stato unificato in vertici e pixel shader e reso più espressivo con un modello di calcolo ben definito e un set di operatori. Inoltre, è stata aggiunta una nuova fase geometry shader per operare sulle primitive dopo la fase vertex shader. I risultati del lavoro della GPU nelle fasi vertex e geometry shader della pipeline possono essere trasmessi alla RAM video per il riutilizzo, consentendo la possibilità di operazioni GPU multipass estremamente complesse con interazione minima con la CPU.

Tutti questi miglioramenti abilitano la tecnologia grafica di nuova generazione ed espandono la capacità delle applicazioni di eseguire l'off-load del lavoro nella GPU. L'offload consente un'interfaccia dei caratteri basata su GPU più complessa, tecniche di morphing accelerato, generazione ed estrusione di volumi ombreggiati, sistemi di particelle e fisica interamente basati su GPU, materiali più complessi combinati in batch efficienti di grandi dimensioni, dettagli procedurali, mapping dello spostamento tracciato da raggi in tempo reale, generazione di mappe cubi a passaggio singolo e molte altre tecniche, il tutto liberando le risorse della CPU per applicazioni più complesse.

Per fornire questo livello di innovazione in Direct3D 10, l'hardware meno recente non può essere espresso come implementazione parziale di una nuova interfaccia. Una scheda video è in grado di supportare tutte le nuove funzionalità o non è una scheda che supporta Direct3D 10. Pertanto, mentre Direct3D 9 può essere utilizzato per l'hardware dell'era DirectX7 con molti bit di funzionalità mancanti e limitazioni di utilizzo, Direct3D 10 funziona solo su una nuova generazione di schede video. Per supportare hardware video meno recente, un'applicazione deve supportare anche le interfacce Direct3D 9. Le versioni future di Direct3D si baseranno sulla versione 10, estenderla alle nuove versioni dell'API garantendo al tempo stesso un superset rigoroso della funzionalità Direct3D 10.

Per altre informazioni su Direct3D 10, vedere [Direct3D 10.](/windows/desktop/direct3d10/d3d10-graphics)

## <a name="direct3d-101"></a>Direct3D 10.1

Windows Vista Service Pack 1 estende l'API Direct3D 10 con Direct3D 10.1, che aggiunge interfacce facoltative e un modello di shader aggiuntivo per supportare le nuove funzionalità hardware delle schede video che supportano Direct3D 10.1. Tutto l'hardware in grado di supportare Direct3D 10.1 supporta completamente anche tutte le funzionalità di Direct3D 10 e gli sviluppatori di giochi possono usare le funzionalità aggiuntive di Direct3D 10.1, se disponibili.

> [!Note]  
> Direct3D 10.1 è l'API grafica usata dal desktop Windows 7.

 

> [!Note]  
> Windows 7 e l'aggiornamento di Windows Vista ([KB 971644](https://support.microsoft.com/kb/971644)) aggiungono il supporto per i livelli di funzionalità DXGI 1.1, 10level9 e il dispositivo WARP10 all'API Direct3D 10.1 esistente.

 

## <a name="direct3d-11"></a>Direct3D 11

Windows 7 supporta una nuova revisione di Direct3D, Direct3D 11, compilata sulla progettazione dell'API Direct3D 10.1. Le nuove funzionalità dell'API includono il rendering multithreading e la creazione di risorse, Compute Shader, il supporto per i livelli di funzionalità 10level9 e il dispositivo di rendering software WARP10 e le nuove funzionalità hardware di classe Direct3D 11, ad esempio la sfasatura tramite shader di dominio di tipo hull &, i formati di compressione delle trame BC6H e BC7, il modello shader 5.0 e il collegamento dinamico dello shader. La nuova API può usare le schede video di classe Direct3D 10 e 10.1 esistenti, alcune schede Direct3D 9 fino ai livelli di funzionalità 10level9 con supporto limitato delle funzionalità e le schede video di classe Direct3D 11 di ultima generazione.

Oltre all'API Direct3D 11, Windows 7 include DXGI 1.1, Direct2D, DirectWrite e il supporto per i driver WDDM 1.1.

> [!Note]  
> Direct3D 11 e le API correlate sono disponibili anche come aggiornamento di Windows Vista (vedere [kb 971644](https://support.microsoft.com/kb/971644)).

 

## <a name="direct3d-111"></a>Direct3D 11.1

Windows 8 estende [l'API Direct3D 11](#direct3d-11) con Direct3D 11.1. Direct3D 11.1 supporta tutto l'hardware esistente che supporta i livelli [di](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) funzionalità 11, 10 x e 9 x, nonché un nuovo livello di funzionalità \_ \_ 11 \_ 1.

Oltre [all'API Direct3D 11.1,](/windows/desktop/direct3d11/direct3d-11-1-features)Windows 8 include [DXGI 1.2,](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)contesti di dispositivo [Direct2D](/windows/desktop/Direct2D/devices-and-device-contexts)e il supporto per i driver WDDM 1.2.

> [!Note]  
> Se si vuole che le app Windows Store programmino grafica 3D con DirectX, è possibile usare l'API Direct3D 11.1. Per altre informazioni sulla programmazione della grafica 3D con DirectX, vedere Introduzione alla grafica [3D con DirectX.](/previous-versions/windows/apps/hh465137(v=win.10))

 

**Aggiornamento della piattaforma per Windows 7:** Il supporto parziale è disponibile per [l'API Direct3D 11.1](/windows/desktop/direct3d11/direct3d-11-1-features) in Windows 7 o Windows Server 2008 R2 con l'aggiornamento della piattaforma [per Windows 7 installato.](https://support.microsoft.com/kb/2670838) Per altre informazioni sull'aggiornamento della piattaforma per Windows 7, vedi [Aggiornamento della piattaforma per Windows 7.](platform-update-for-windows-7.md)

## <a name="opengl"></a>Opengl

Windows Vista, Windows 7 e Windows 8 offrono lo stesso supporto di Windows XP per OpenGL, che consente ai produttori di schede video di fornire un driver client installabile (ICD) per OpenGL che fornisce supporto accelerato hardware. Si noti che le versioni più recenti di tali ICD sono necessarie per supportare completamente Windows Vista o Windows 7 o Windows 8. Se non è installato alcun ICD, nella maggior parte dei casi il sistema verrà nuovamente installato al livello software OpenGL v1.1.

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>Compatibilità delle applicazioni, GDI e versioni precedenti di Direct3D

I Windows di grafica Windows Vista, Windows 7 e Windows 8 sono progettati per supportare un'ampia gamma di scenari hardware e di utilizzo per abilitare nuove tecnologie continuando a supportare i sistemi esistenti. Le interfacce grafiche esistenti, ad esempio GDI, GDI+ e le versioni precedenti di Direct3D, continuano a funzionare in Windows Vista e Windows 7, ma vengono mappate internamente laddove possibile. Ciò significa che la maggior parte delle applicazioni Windows esistenti continuerà a funzionare.

Windows Vista, Windows 7 e Windows 8 continuano a supportare le stesse interfacce Direct3D e DirectDraw di Windows XP, fino alla versione 3 di DirectX (ad eccezione della modalità mantenuta di Direct3D, che è stata rimossa). Come per Windows XP Professional x64 Edition, le applicazioni native a 64 bit nelle versioni più recenti di Windows sono limitate alle interfacce Direct3D9, DirectDraw7 o più recenti. Le applicazioni ad alte prestazioni devono usare Direct3D 9 o versioni successive per assicurarsi di avere la corrispondenza più vicina alle funzionalità hardware.

## <a name="recommendations"></a>Consigli

Quando si seleziona un'API per l'applicazione grafica, tenere presenti le raccomandazioni seguenti:

-   Usare Direct3D 9 se l'applicazione deve supportare Windows XP o una versione precedente di Windows.
-   Usare Direct3D 9 se si vuole supportare Windows Vista o Windows 7 in esecuzione con driver XPDM. Per i sistemi Windows Vista o Windows 7 che non dispongono di hardware video Direct3D 10 o superiore, è possibile scegliere di usare il percorso del codice Windows XP Direct3D 9 esistente o usare i livelli di funzionalità 10level9 tramite l'API Direct3D 10.1 o Direct3D 11.
-   Usare Direct3D 11 per sfruttare la nuova generazione di hardware video in Windows Vista, Windows 7 e Windows 8. Windows Le app dello Store devono usare Direct3D 11 o versione successiva.

 

 