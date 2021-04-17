---
title: API grafiche in Windows
description: In questo articolo vengono illustrate le funzionalità e le API di Windows graphics.
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543ee7c5e3cdbfb022cc9299dd5ddd3cdd36981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399575"
---
# <a name="graphics-apis-in-windows"></a>API grafiche in Windows

Windows Vista include il supporto per un modello di driver di visualizzazione completamente nuovo che rappresenta una revisione principale nella progettazione di driver video a partire dall'introduzione del Windows Driver Model (WDM) per Windows 98. Questo modello riprogettato riflette l'evoluzione dell'hardware video dal mondo delle operazioni raster 2D e delle applicazioni GDI a quello dei giochi 3D con hardware grafico a funzione fissa e infine a quello della moderna unità di elaborazione grafica (GPU) programmabile che supporta una vasta gamma di applicazioni grafiche a prestazioni elevate. Windows 7 e Windows 8 si basano sull'infrastruttura grafica di Windows Vista fornendo funzionalità grafiche e API aggiuntive. In questo articolo vengono illustrate le funzionalità e le API di Windows graphics.

-   [Background](#background)
-   [Direct3D 9](#direct3d-9)
-   [9Ex Direct3D](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10,1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11,1](#direct3d-111)
-   [OpenGL](#opengl)
-   [Compatibilità delle applicazioni, GDI e versioni precedenti di Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [Indicazioni](#recommendations)

## <a name="background"></a>Sfondo

L'API principale per la programmazione di elementi grafici dal primo giorno di Windows è stata l'interfaccia GDI (Graphical Device Interface). Questa API è stata progettata per gestire numerosi dispositivi di output 2D e costituisce la base per l'esperienza dell'interfaccia utente di Windows. DirectDraw e Direct3D sono stati introdotti come API alternative per supportare giochi a schermo intero e rendering 3D come estensioni per l'hardware esistente del tempo. Le interazioni con GDI erano complesse. La combinazione efficace di elementi GDI tradizionali con elementi Direct3D è stata limitata da questa progettazione. La versione di WDM di Windows XP, nota come XPDM, riflette la natura affiancata di GDI e Direct3D (vedere la figura 1).

**Figura 1. API grafiche in Windows XP**

![XPDM](images/graphics-apis-in-windows-xp.gif)

Nel corso degli anni, la potenza delle schede video 3D è cresciuta notevolmente fino al punto in cui la maggior parte dell'hardware è dedicata a questa funzione. Un nuovo modello di driver, Windows Display Driver Model (WDDM), porta la GPU e Direct3D a Forefront, consentendo la creazione di un'esperienza completamente nuova, il desktop 3D, che fonde perfettamente il mondo 2D di GDI con la potenza di GPU programmabili moderne. Con WDDM, l'hardware video è interamente guidato da Direct3D e tutte le altre interfacce grafiche comunicano con l'hardware video tramite il nuovo modello di driver basato su Direct3D (vedere la figura 2).

**Figura 2. API grafiche in Windows Vista**

![WDDM](images/graphics-apis-in-windows-vista.gif)

Per ulteriori informazioni su WDDM, vedere la [Guida alla progettazione di Windows Vista Display Driver Model (WDDM)](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) in MSDN.

## <a name="direct3d-9"></a>Direct3D 9

La versione 9 di DirectX è stata rilasciata per la prima volta per Windows in 2002, con aggiornamenti successivi in 2003 e 2004. Questa API rappresenta un decennio di evoluzione delle tecnologie DirectX, l'introduzione di modelli di programmazione shader più potenti per Direct3D e una maturità supportata da migliaia di titoli di spedizione. Direct3D 9 è l'interfaccia grafica principale di Windows Vista. Rimane l'API ideale da usare per la scrittura di giochi 3D e applicazioni che devono essere eseguite in un'ampia gamma di versioni hardware e Windows esistenti. I dettagli del nuovo modello di driver sono nascosti per le applicazioni che usano le interfacce Direct3D 9, ma dietro le quinte il sistema operativo sta sfruttando tutte le nuove funzionalità per offrire un vero multitasking della GPU, una gestione delle risorse più efficiente e prestazioni affidabili.

Per garantire la compatibilità completa con le versioni precedenti di Windows, è necessario emulare alcune peculiarità del vecchio modello di driver anche con il nuovo modello di driver di visualizzazione di Windows Vista. Ad esempio, quando un'applicazione a schermo intero perde lo stato attivo, deve presupporre che abbia perso tutte le risorse nella memoria video (VRAM) e ricaricare quelle create come risorse non gestite, anche se il nuovo modello di driver gestisce le risorse in modo trasparente senza rimuoverle dal contesto di dispositivo. Anche il concetto di un tipo di risorsa gestito rispetto a quello predefinito è specifico per il vecchio modello di driver. Un altro esempio è l'aspettativa di errore durante l'allocazione di risorse non gestite (pool predefinito) in eccesso rispetto alla quantità di VRAM disponibile, anche se il nuovo modello di driver è in grado di fornire una quantità quasi illimitata di memoria video virtuale. A causa di questi requisiti, le applicazioni Direct3D in esecuzione in Windows Vista continueranno a ricevere le condizioni di errore. Pertanto, sono limitati alla possibilità di usare le interfacce Direct3D 9 di base per usare completamente alcune funzionalità del nuovo modello di driver.

Sebbene i nuovi sistemi distribuiti con Windows Vista includano schede video con driver WDDM e i nuovi driver per alcune schede video più diffuse sono inclusi nella finestra di dialogo, Windows Vista continua a supportare la possibilità di usare i driver XPDM meno recenti per gli aggiornamenti e le edizioni aziendali. Nei sistemi che usano il vecchio modello di driver, è necessario usare Direct3D 9 e le interfacce precedenti e il funzionamento del sistema grafico è molto simile a quello di Windows XP (Figura 1). WDDM è necessario per le applicazioni per l'uso di Direct3D 9Ex, Direct3D 10 e versioni successive.

## <a name="direct3d-9ex"></a>9Ex Direct3D

L'interfaccia Direct3D 9Ex fornisce l'accesso a una lieve estensione dell'API Direct3D 9 standard che espone l'allocazione delle risorse virtualizzata, la nuova semantica dei dispositivi perduti e altre nuove funzionalità disponibili in Windows Vista. Con la creazione di questo oggetto esteso, l'API Direct3D 9 utilizza la nuova semantica e pertanto richiede che l'applicazione usi logica diversa (e quindi percorsi di codice diversi) per la creazione, la gestione e la gestione degli errori per i nuovi tipi di condizioni. Questa API è disponibile solo in Windows Vista e richiede driver WDDM. Poiché Direct3D 9Ex usa un percorso di codice API e driver separato rispetto a Direct3D 9, il supporto di questa API richiede test case aggiuntivi per l'applicazione.

Il motivo principale per cui si crea la nuova API Direct3D 9Ex è stato quello di consentire l'accesso completo alle nuove funzionalità di WDDM mantenendo la compatibilità per le applicazioni Direct3D esistenti. Il nuovo desktop 3D e molte applicazioni specifiche di Windows Vista usano questa versione di Direct3D 9, ma non sono funzionali quando sono in esecuzione su driver XPDM precedenti. Poiché l'API Direct3D 9Ex non verrà mai visualizzata nelle versioni precedenti di Windows a causa della mancanza di supporto per WDDM, le interfacce standard Direct3D 9 coprono un set di sistemi molto più ampio. Per le applicazioni a prestazioni elevate che possono sfruttare i vantaggi della prossima generazione di hardware video, la versione 10 di Direct3D completamente nuova offre molte nuove funzionalità non esposte da Direct3D 9Ex. Di conseguenza, per i giochi e la maggior parte delle applicazioni, Direct3D 9 o Direct3D 10 è l'API consigliata.

> [!Note]  
> DirectX SDK non fornisce esempi, intestazioni o librerie per l'interfaccia 9Ex di Direct3D. MSDN Library e Windows SDK (noto in precedenza come Platform SDK) contengono la documentazione, le intestazioni e le librerie disponibili.

 

Per ulteriori informazioni su Direct3D 9Ex, vedere la pagina relativa a [DirectX per Windows Vista](/previous-versions//ms681824(v=vs.85)) in MDSN.

## <a name="direct3d-10"></a>Direct3D 10

Per sfruttare al massimo il potenziale del nuovo modello di driver di Windows Vista e dell'hardware di prossima generazione, è stata creata una versione completamente nuova dell'API Direct3D. Sebbene WDDM elimini alcune delle limitazioni sulle prestazioni nel sistema grafico esistente, Direct3D 10 consente di rimuovere i colli di bottiglia di progettazione nell'API Direct3D esistente e semplifica notevolmente l'attività di programmazione della GPU.

La nuova API Elimina completamente tutti gli aspetti a funzione fissa, sostituendo questi ultimi con costrutti programmabili e semplificando notevolmente l'implementazione interna. Centinaia di bit per le funzionalità nelle versioni precedenti di Direct3D sono stati completamente eliminati e sostituiti con un set di funzionalità ben definito e inclusivo che include solo alcuni scenari di utilizzo facoltativi per formati di risorse specifici. La creazione e la convalida di risorse con utilizzo intensivo della CPU ora hanno una semantica esplicita nella nuova API. In questo modo è possibile ottenere un comportamento molto più prevedibile delle prestazioni e ridurre notevolmente il sovraccarico per singolo progetto. Le risorse possono essere riconfigurate in più formati per consentire un uso efficiente in varie fasi e il set di funzionalità impone un numero molto inferiore di restrizioni sugli scenari di utilizzo per i formati. Sono disponibili anche nuovi formati di trama con mapping normale con compressione a blocchi.

Nella nuova API, le costanti dello shader e lo stato del dispositivo sono risorse esplicite, consentendo un caching molto più efficiente sull'hardware e la convalida dei driver molto semplificata. Il modello di shader programmabile è stato unificato tra Vertex e pixel shader e reso più espressivo con un modello di calcolo e un set di operatori ben definiti. È stata inoltre aggiunta una nuova fase geometry shader per operare sulle primitive dopo la fase vertex shader. I risultati delle operazioni della GPU nelle fasi Vertex e geometry shader della pipeline possono essere trasmessi alla RAM video per il riutilizzo, consentendo la possibilità di eseguire operazioni GPU a più passaggi estremamente complesse con un'interazione minima della CPU.

Tutti questi miglioramenti abilitano la tecnologia grafica di nuova generazione ed espandono la capacità delle applicazioni di non caricare il lavoro nella GPU. L'offload consente la personalizzazione di caratteri più complessi basata su GPU, tecniche di morphing accelerate, generazione di volumi shadow ed estrusione, sistemi particellari e fisici che sono interamente basati su GPU, materiali più complessi combinati in batch di grandi dimensioni, in cui vengono illustrate le procedure dettagliate, il mapping di spostamento con traccia in tempo reale, la generazione di un cubo a passaggio singolo e molte altre tecniche, il tutto senza perdere risorse della CPU per applicazioni più complesse

Per offrire questo livello di innovazione in Direct3D 10, l'hardware precedente non può essere espresso come un'implementazione parziale di una nuova interfaccia. Una scheda video è in grado di supportare tutte le nuove funzionalità o non è una scheda con supporto per Direct3D 10. Di conseguenza, sebbene Direct3D 9 possa guidare l'hardware DirectX7 con molti bit di funzionalità e limitazioni di utilizzo mancanti, Direct3D 10 funziona solo con una nuova generazione di schede video. Per supportare l'hardware video precedente, un'applicazione deve supportare anche le interfacce Direct3D 9. Le versioni future di Direct3D si basano sulla versione 10, che lo estendono alle nuove versioni dell'API garantendo un superset rigoroso della funzionalità Direct3D 10.

Per ulteriori informazioni su Direct3D 10, vedere [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="direct3d-101"></a>Direct3D 10,1

Windows Vista Service Pack 1 estende l'API Direct3D 10 con Direct3D 10,1, che aggiunge interfacce opzionali e un modello shader aggiuntivo per supportare le nuove funzionalità hardware delle schede video che supportano Direct3D 10,1. Tutto l'hardware in grado di supportare Direct3D 10,1 supporta completamente tutte le funzionalità di Direct3D 10 e gli sviluppatori di giochi possono usare le funzionalità aggiuntive di Direct3D 10,1, quando disponibili.

> [!Note]  
> Direct3D 10,1 è l'API grafica utilizzata dal desktop di Windows 7.

 

> [!Note]  
> Windows 7 e l'aggiornamento di Windows Vista ([KB 971644](https://support.microsoft.com/kb/971644)) aggiungono il supporto per DXGI 1,1, i livelli di funzionalità 10level9 e il dispositivo WARP10 all'API Direct3D 10,1 esistente.

 

## <a name="direct3d-11"></a>Direct3D 11

Windows 7 supporta una nuova revisione di Direct3D, Direct3D 11, basata sulla progettazione dell'API Direct3D 10,1. Le nuove funzionalità dell'API includono il rendering multithreading e la creazione di risorse, compute shader, il supporto per i livelli di funzionalità 10level9 e il dispositivo di rendering del software WARP10 e le nuove funzionalità hardware della classe Direct3D 11, ad esempio la suddivisione a mosaico con Hull & Domain shader, i formati di compressione della trama BC6H e BC7, il modello di shader 5,0 e il collegamento Dynamic shader. La nuova API può usare schede video esistenti Direct3D 10 e 10,1, alcune schede Direct3D 9 attraverso i livelli di funzionalità di 10level9 con supporto limitato per le funzionalità e la generazione più recente di schede video di Direct3D 11.

Oltre all'API Direct3D 11, Windows 7 include DXGI 1,1, Direct2D, DirectWrite e il supporto per i driver WDDM 1,1.

> [!Note]  
> Direct3D 11 e le API correlate sono disponibili anche come aggiornamento a Windows Vista (vedere [KB 971644](https://support.microsoft.com/kb/971644)).

 

## <a name="direct3d-111"></a>Direct3D 11,1

Windows 8 estende l' [API Direct3D 11](#direct3d-11) con Direct3D 11,1. Direct3D 11,1 supporta tutti i componenti hardware esistenti con supporto per i [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11, 10 \_ x e 9 \_ x, oltre a un nuovo livello di funzionalità di 11 \_ 1.

Oltre all' [API Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features), Windows 8 include [DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), i [contesti di dispositivo Direct2D](/windows/desktop/Direct2D/devices-and-device-contexts)e il supporto per i driver WDDM 1,2.

> [!Note]  
> Se si vuole che le app di Windows Store programmino grafica 3D con DirectX, è possibile usare l'API Direct3D 11,1. Per altre informazioni sulla programmazione di grafica 3D con DirectX, vedere [Introduzione alla grafica 3D con DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).

 

**Aggiornamento della piattaforma per Windows 7:** È disponibile il supporto parziale per l' [API Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features) in Windows 7 o windows Server 2008 R2 con l' [aggiornamento della piattaforma per Windows 7](https://support.microsoft.com/kb/2670838) installato. Per ulteriori informazioni sull'aggiornamento della piattaforma per Windows 7, vedere [aggiornamento della piattaforma per Windows 7](platform-update-for-windows-7.md).

## <a name="opengl"></a>OpenGL

Windows Vista, Windows 7 e Windows 8 forniscono lo stesso supporto di Windows XP per OpenGL, che consente ai produttori di schede video di fornire un driver client installabile (ICD) per OpenGL che fornisce supporto con accelerazione hardware. Si noti che le versioni più recenti di tali ICD sono necessarie per supportare completamente Windows Vista, Windows 7 o Windows 8. Se non è installato alcun ICD, il sistema esegue il fallback al livello software OpenGL v 1.1 nella maggior parte dei casi.

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>Compatibilità delle applicazioni, GDI e versioni precedenti di Direct3D

I sistemi grafici Windows Vista, Windows 7 e Windows 8 sono progettati per supportare un'ampia gamma di scenari hardware e di utilizzo per consentire una nuova tecnologia, continuando a supportare i sistemi esistenti. Le interfacce grafiche esistenti, ad esempio GDI, GDI+ e le versioni precedenti di Direct3D, continuano a funzionare in Windows Vista e Windows 7, ma sono rimappate internamente laddove possibile. Ciò significa che la maggior parte delle applicazioni Windows esistenti continuerà a funzionare.

Windows Vista, Windows 7 e Windows 8 continuano a supportare le stesse interfacce Direct3D e DirectDraw di Windows XP, tornando alla versione 3 di DirectX (ad eccezione della modalità Direct3D's mantenuta, che è stata rimossa). Analogamente a Windows XP Professional x64 Edition, le applicazioni native a 64 bit nelle versioni più recenti di Windows sono limitate alle interfacce Direct3D9, DirectDraw7 o più recenti. Le applicazioni ad alte prestazioni devono usare Direct3D 9 o versione successiva per assicurarsi che abbiano la corrispondenza più vicina alle funzionalità hardware.

## <a name="recommendations"></a>Consigli

Quando si seleziona un'API per l'applicazione grafica, tenere presenti le raccomandazioni seguenti:

-   Usare Direct3D 9 se l'applicazione deve supportare Windows XP o una versione precedente di Windows.
-   Utilizzare Direct3D 9 Se si desidera supportare Windows Vista o Windows 7 in esecuzione con i driver XPDM. Per i sistemi Windows Vista o Windows 7 che non dispongono di Direct3D 10 o un migliore hardware video, è possibile scegliere di utilizzare il percorso di codice di Windows XP Direct3D 9 esistente o utilizzare i livelli di funzionalità di 10level9 tramite l'API Direct3D 10,1 o Direct3D 11.
-   Usare Direct3D 11 per sfruttare i vantaggi della nuova generazione di hardware video in Windows Vista, Windows 7 e Windows 8. Le app di Windows Store devono usare Direct3D 11 o versione successiva.

 

 