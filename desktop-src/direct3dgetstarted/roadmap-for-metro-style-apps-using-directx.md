---
title: Roadmap per app DirectX desktop
description: Di seguito sono riportate le risorse principali che consentono di iniziare a usare DirectX e C++ per sviluppare app desktop con utilizzo intensivo di grafica, come i giochi.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca95e1fe281253705620136afdced3cb705fe02
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104047639"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Roadmap per app DirectX desktop

Di seguito sono riportate le risorse principali che consentono di iniziare a usare DirectX e C++ per sviluppare app desktop con utilizzo intensivo di grafica, ad esempio giochi. Non si tratta di un elenco completo di tutte le funzionalità o risorse disponibili.

## <a name="get-started"></a>Introduzione

Ecco alcuni argomenti chiave. Configurare il progetto DirectX, acclimatandosi a Windows e alle applicazioni di esempio.

| Argomento | Descrizione |
|-|-|
| [Creare la prima app di Windows con DirectX](building-your-first-directx-app.md) | Usare questa esercitazione di base per iniziare a sviluppare app DirectX, quindi usare la roadmap per continuare a esplorare DirectX. |
| [Introduzione a DirectX per Windows](getting-started-with-a-directx-game.md) | Esaminare i passaggi da eseguire per iniziare a sviluppare un gioco con DirectX e C++. |
| [Codice completo per un framework DirectX](complete-code-sample-for-using-a-corewindow-with-directx.md) | Ottenere il codice per un Framework di rendering DirectX di base. |
| [Come usare Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | Questa sezione illustra come usare l'API Microsoft Direct3D 11 per eseguire diverse attività comuni. |
| [Guida alla programmazione per Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews) | La guida alla programmazione contiene informazioni su come usare la pipeline programmabile di Microsoft Direct3D 11 per creare grafica 3D in tempo reale per le applicazioni desktop. |
| [Strumenti per la grafica DirectX](/windows/desktop/direct3dtools/dx-graphics-tools) | Documentazione per gli strumenti usati per supportare lo sviluppo DirectX. |
| [Novità di Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Suddivisione di tutte le funzionalità aggiunte nelle versioni più recenti di DirectX e Direct3D (attualmente 11,2). |
| [Scaricare Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | È necessario avere Visual Studio Express 2013 per Windows Desktop per creare giochi di Windows Store. Per una panoramica di Visual Studio, vedere [sviluppare app di Windows Store con Visual studio 2012](/previous-versions/windows/apps/br211384(v=win.10)). Per informazioni sulle nuove funzionalità di Visual Studio, vedere [Highlights for Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [Dov'è DirectX SDK?](../directx-sdk--august-2009-.md) | Contiene informazioni aggiuntive per gli sviluppatori che vogliono portare i progetti DirectX in Microsoft Visual Studio. |

## <a name="sample-applications"></a>Applicazioni di esempio

| Argomento | Descrizione |
|-|-|
| [Esempio di esercitazione su Direct3D Win32](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Esempio di esercitazione Direct3D per desktop di base. |
| [Esempio di rendering video DirectX](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Esempio che illustra il rendering video personalizzato con Direct3D. |

## <a name="review-key-direct3d-11-concepts"></a>Esaminare i concetti chiave di Direct3D 11

| Argomento | Descrizione |
|-|-|
| [Pipeline grafica](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Viene illustrata la pipeline di grafica Direct3D 11 di base. |
| [Rendering](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Vengono illustrati i modelli di rendering Direct3D, i componenti, gli shader e il flusso di chiamate API. |
| [Risorse](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Vengono illustrate le risorse di Direct3D, ad esempio i buffer e altri tipi di risorse GPU. |
| [Effetti](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Vengono illustrati gli effetti e le istanze di Direct3D multishader.  |
| [Procedura: creare una catena di scambio](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Come creare la catena di scambio usata per creare i pixel in un'area dello schermo. |
| [Procedura: creare un dispositivo e un contesto immediato](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Come creare un'astrazione del dispositivo Direct3D e un contesto immediato per il disegno. |
| [Procedura: creare un vertex buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Come creare un semplice elenco di vertici mesh per l'elaborazione da parte della GPU. |
| [Procedura: creare un buffer di indice](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Creazione di un buffer di indice che consente al vertex shader di scorrere l'ordine dei vertici in una mesh. |
| [Procedura: creare un buffer costante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Come passare dati costanti (uniformi) tra la CPU e la GPU durante il rendering. |
| [Procedura: creare una trama](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Come creare una trama o altre risorse di buffer che possono essere campionate dalla GPU. |
| [Procedura: inizializzare una trama da un file](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Come caricare una trama da un file ed elaborarla per l'uso da parte della pipeline dello shader. |
| [Procedura: compilare uno shader](../direct3d11/how-to--compile-a-shader.md) | Come compilare uno shader da usare nell'applicazione grafica. |

## <a name="graphics-apis"></a>API grafiche

| Argomento | Descrizione |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Documentazione delle API principali per la virtualizzazione della GPU e delle relative risorse e per il disegno di immagini con un modello di shader unificato. |
| [HLSL Direct3D](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Documentazione di riferimento per High-Level lingua shader, la sintassi e le regole usate per definire i programmi shader eseguiti come parte della pipeline grafica in un modello di shader unificato. |
| [Interfaccia grafica DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Documentazione delle API di basso livello utilizzate per acquisire l'interfaccia GPU e le risorse di sistema. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Documentazione per le API Direct2D, che supportano il disegno di primitive 2D. In genere, Direct2D viene usato per interfacce utente personalizzate, elaborazione di immagini e batch e giochi semplici. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Documentazione per le API di DirectWrite, che supportano il rendering e il ridimensionamento dei tipi di carattere personalizzati. |
| [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api) | Documentazione per le API WIC, utilizzate per la lettura e la gestione di diversi formati di immagine bitmap. |
| [DirectDraw Surfaces (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) per le trame | Documentazione per le API DDS, che vengono usate per la compressione e la decompressione di trame 2D insieme alle API WIC. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Documentazione per le API DirectXMath, che supportano Direct3D con un set di tipi e funzioni adatti per lo sviluppo di grafica 3D in tempo reale. (In precedenza XNAMath). |
| [DirectCompute](https://walbourn.github.io/) | Documentazione per le API DirectCompute, usate per le funzionalità di calcolo o utilizzo generale dello shader. |

## <a name="audio-media-and-input-apis"></a>API audio, multimediali e di input

| Argomento | Descrizione |
|-|-|
| [Guida alla programmazione di XAudio2](/windows/desktop/xaudio2/programming-guide) | Nodo di primo livello per la documentazione concettuale dell'API audio XAudio2. |
| [Guida di riferimento alla programmazione di XAudio2](/windows/desktop/xaudio2/programming-reference) | Nodo di primo livello per la documentazione di riferimento dell'API audio XAudio2. |
| [Guida alla programmazione di XInput](/windows/desktop/xinput/programming-guide) | Nodo di primo livello per la documentazione concettuale dell'API del controller XInput. |
| [Guida di riferimento alla programmazione XInput](/windows/desktop/xinput/programming-reference) | Nodo di primo livello per la documentazione di riferimento dell'API del controller XInput. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Nodo di livello superiore per la documentazione dell'API di riproduzione (audio/video) del supporto di Media Foundation (MF). In genere, MF viene usato nei giochi per la riproduzione della colonna sonora, mentre XAudio2 viene usato per l'audio dinamico. |

## <a name="port-to-directx-11"></a>Da porta a DirectX 11

| Argomento | Descrizione |
|-|-|
| [Migrazione a Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Linee guida di base per lo trasferimento di codebase DirectX 9 a DirectX 11. |
| [Tecniche di codifica a doppio utilizzo per i giochi](https://walbourn.github.io/) | Post di Blog dettagliato sullo sviluppo per i livelli di funzionalità DirectX 9 \_ \* e DirectX 11 \_ \* in un'unica applicazione. |
| [Implementazione dei buffer shadow per il livello di funzionalità Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)) | Linee guida per l'implementazione di mappe Shadow con il livello di funzionalità DirectX 9 \_ \* . |

## <a name="work-with-c"></a>Usare C++

Se non si ha familiarità con C++ sulle piattaforme Windows, l'aspetto potrebbe essere leggermente diverso. Ecco alcuni puntatori ad argomenti che consentono di ottenere un handle per la differenza.

> [!NOTE]
> Alcuni di questi argomenti sono utili per gestire l'applicazione C++/CX. È tuttavia consigliabile utilizzare [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) per le nuove applicazioni. C++/WinRT è una proiezione del linguaggio C++ 17 interamente standard e moderna per le API di Windows Runtime (WinRT), implementata come libreria basata su file di intestazione e progettata per fornirti accesso privilegiato alla moderna API di Windows.

| Argomento | Descrizione |
|-|-|
| [**Guida di riferimento al linguaggio Visual C++ (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Pagina di alto livello che si collega al contenuto correlato a C++. |
| [**Riferimento rapido (Windows Runtime e Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Tabella che fornisce informazioni rapide sugli operatori e le parole chiave di Visual C++ Component Extensions (C++/CX). |
| [**Sistema di tipi (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Contenuto di riferimento per i tipi supportati da C++/CX. |
| [**Spazi dei nomi (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | Contenuto di riferimento per gli spazi dei nomi che contengono tipi specifici di C++ che possono essere usati nelle app di Windows Store. |

| | |
|-|-|
| [Programmazione asincrona (DirectX e C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Scopri di più sulla programmazione asincrona e multithreading per app e giochi DirectX. |
| [Programmazione asincrona in C++](/previous-versions/windows/apps/hh780559(v=win.10)) | Vengono descritti i modi di base per utilizzare la classe di attività per utilizzare Windows Runtime metodi asincroni. |
| [**Classe Task (runtime di concorrenza)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Documentazione di riferimento per la classe dell'attività. |
| [Parallelismo delle attività (runtime di concorrenza)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Discussione approfondita sulla classe di attività e su come usarla. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>Librerie utili aggiuntive per la programmazione in Windows C++

| | |
|-|-|
| [Libreria di modelli standard C++](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | I tipi di Windows Runtime giocano bene con i tipi di libreria di modelli standard. La maggior parte delle app di Windows Store C++ usa insiemi e algoritmi della libreria di modelli standard, tranne al limite dell'ABI. |
| [Parallel Patterns Library](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | PPL fornisce algoritmi e tipi che semplificano il parallelismo delle attività e il parallelismo dei dati sulla CPU.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP fornisce accesso alla GPU per il parallelismo dei dati per utilizzo generico sulle schede video che supportano DirectX 11. |

## <a name="blogs-and-other-resources"></a>Blog e altre risorse

| Argomento | Descrizione |
|-|-|
| [Blog sui giochi per Windows e DirectX](https://walbourn.github.io/) | Blog aggiornato regolarmente da un collaboratore per sviluppatori DirectX chiave e una risorsa straordinaria per gli sviluppatori DirectX. |
| [Blog per sviluppatori Windows DirectX](https://devblogs.microsoft.com/directx/) | Blog ufficiale di Windows DirectX. |
| [Blog DirectX di Shawn Hargreave](https://www.shawnhargreaves.com/blogindex.html)) | Blog di sviluppo di un altro collaboratore Windows DirectX dev. |
| [DirectX Tool Kit](https://directxtk.codeplex.com/) | Sito CodePlex per DirectX Tool Kit (DxTK), che contiene numerose API di supporto utili per il caricamento di mesh, la riproduzione di suoni e altri comportamenti comuni. |
| [Libreria di elaborazione delle trame DirectXTex](https://directxtex.codeplex.com/) | Sito Plex del codice per DirectX Texture Processing Library (DxTEX), che contiene le API di supporto per l'elaborazione di trame e la compressione/decompressione. |