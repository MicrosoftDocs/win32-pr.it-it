---
title: Roadmap per app DirectX desktop
description: Di seguito sono disponibili risorse chiave che consentono di iniziare a usare DirectX e C++ per sviluppare app desktop a elevato utilizzo di grafica, ad esempio i giochi.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5940e775de65d6d22a9b244d1bd0b881240cf296b740c9a0be9c38f3ab0725a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983891"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Roadmap per app DirectX desktop

Di seguito sono disponibili risorse chiave che consentono di iniziare a usare DirectX e C++ per sviluppare app desktop a elevato utilizzo di grafica, ad esempio giochi. Questo non è un elenco completo di tutte le funzionalità o le risorse disponibili.

## <a name="get-started"></a>Introduzione

Ecco alcuni argomenti chiave. Configurazione del progetto DirectX, attribuzione di Windows applicazioni di esempio.

| Argomento | Descrizione |
|-|-|
| [Creare la prima app Windows con DirectX](building-your-first-directx-app.md) | Usare questa esercitazione di base per iniziare a usare lo sviluppo di app DirectX, quindi usare la roadmap per continuare a esplorare DirectX. |
| [Introduzione a DirectX per Windows](getting-started-with-a-directx-game.md) | Esaminare i passaggi da eseguire per iniziare a sviluppare un gioco con DirectX e C++. |
| [Codice completo per un framework DirectX](complete-code-sample-for-using-a-corewindow-with-directx.md) | Ottenere il codice per un framework di rendering DirectX di base. |
| [Come usare Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | Questa sezione illustra come usare l'API Microsoft Direct3D 11 per eseguire diverse attività comuni. |
| [Guida alla programmazione per Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews) | La guida per programmatori contiene informazioni su come usare la pipeline programmabile Microsoft Direct3D 11 per creare grafica 3D in tempo reale per applicazioni desktop. |
| [Strumenti per la grafica DirectX](/windows/desktop/direct3dtools/dx-graphics-tools) | Documentazione per gli strumenti usati per supportare lo sviluppo DirectX. |
| [Novità di Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Scomposizione di tutte le funzionalità aggiunte nelle versioni più recenti di DirectX e Direct3D (attualmente 11.2). |
| [Scaricare Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | È necessario avere Visual Studio Express 2013 per Windows Desktop creare giochi Windows Store. Per una presentazione delle Visual Studio, vedere [Sviluppare app Windows Store usando Visual Studio 2012.](/previous-versions/windows/apps/br211384(v=win.10)) Per informazioni sulle nuove funzionalità di Visual Studio, vedere [Product Highlights for Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [Dov'è DirectX SDK?](../directx-sdk--august-2009-.md) | Contiene indicazioni per gli sviluppatori che vogliono portare i propri progetti DirectX in Microsoft Visual Studio. |

## <a name="sample-applications"></a>Applicazioni di esempio

| Argomento | Descrizione |
|-|-|
| [Esempio Win32 dell'esercitazione su Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Esempio di esercitazione su Direct3D desktop di base. |
| [Esempio di rendering video DirectX](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Esempio che illustra il rendering video personalizzato con Direct3D. |

## <a name="review-key-direct3d-11-concepts"></a>Esaminare i concetti chiave di Direct3D 11

| Argomento | Descrizione |
|-|-|
| [Pipeline grafica](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Illustra la pipeline grafica Direct3D 11 di base. |
| [Rendering](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Illustra i modelli di rendering Direct3D, i componenti, gli shader e il flusso delle chiamate API. |
| [Risorse](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Vengono illustrate le "risorse" Direct3D, ad esempio buffer e altri tipi di risorse GPU. |
| [Effetti](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Illustra le istanze e gli effetti multi shader Direct3D.  |
| [Procedura: Creare una catena di scambio](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Come creare la catena di scambio usata per disegnare pixel in un'area dello schermo. |
| [Procedura: Creare un dispositivo e un contesto immediato](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Come creare un'astrazione di dispositivo Direct3D e un contesto immediato per il disegno. |
| [Procedura: Creare un vertex buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Come creare un elenco semplice di vertici mesh per l'elaborazione da parte della GPU. |
| [Procedura: Creare un buffer di indice](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Come creare un index buffer che consenta al vertex shader di eseguire l'ordine dei vertici in una mesh. |
| [Procedura: Creare un buffer costante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Come passare dati costanti (uniformi) tra la CPU e la GPU durante il rendering. |
| [Procedura: Creare una trama](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Come creare una trama o un'altra risorsa buffer che può essere campionata dalla GPU. |
| [Procedura: Inizializzare una trama da un file](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Come caricare una trama da un file ed elaborarla per l'uso da parte della pipeline shader. |
| [Procedura: Compilare uno shader](../direct3d11/how-to--compile-a-shader.md) | Come compilare uno shader da usare nell'applicazione grafica. |

## <a name="graphics-apis"></a>API grafiche

| Argomento | Descrizione |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Documentazione delle API di base per la virtualizzazione della GPU e delle relative risorse e per il disegno di grafica usando un modello shader unificato. |
| [Direct3D HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Documentazione di riferimento High-Level shader, la sintassi e le regole usate per definire i programmi shader eseguiti come parte della pipeline grafica in un modello shader unificato. |
| [Interfaccia grafica DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Documentazione delle API di basso livello usate per acquisire l'interfaccia GPU e le risorse di sistema. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Documentazione per le API Direct2D, che supportano il disegno di primitive 2D. In genere, Direct2D viene usato per interfacce utente personalizzate, elaborazione di immagini e invio in batch e giochi semplici. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Documentazione per le API DirectWrite, che supportano il rendering e il ridimensionamento dei caratteri personalizzati. |
| [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api) | Documentazione per le API WIC, usate per la lettura e la gestione di formati di immagine bitmap diversi. |
| [Superfici DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) per trame | Documentazione per le API DDS, usate per la compressione e la decompressione delle trame 2D in combinazione con le API WIC. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Documentazione per le API DirectXMath, che supportano Direct3D con un set di tipi e funzioni adatti per lo sviluppo di grafica in tempo reale 3D. (in precedenza XNAMath). |
| [DirectCompute](https://walbourn.github.io/) | Documentazione per le API DirectCompute, usate per la funzionalità shader di calcolo o per uso generico. |

## <a name="audio-media-and-input-apis"></a>API audio, multimediali e di input

| Argomento | Descrizione |
|-|-|
| [Guida alla programmazione di XAudio2](/windows/desktop/xaudio2/programming-guide) | Nodo di primo livello per la documentazione concettuale dell'API audio XAudio2. |
| [Guida di riferimento alla programmazione di XAudio2](/windows/desktop/xaudio2/programming-reference) | Nodo di primo livello per la documentazione di riferimento dell'API audio XAudio2. |
| [Guida per programmatori XInput](/windows/desktop/xinput/programming-guide) | Nodo di primo livello per la documentazione concettuale dell'API controller XInput. |
| [Informazioni di riferimento sulla programmazione XInput](/windows/desktop/xinput/programming-reference) | Nodo di primo livello per la documentazione di riferimento sull'API controller XInput. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Nodo di primo livello per la documentazione dell'API di riproduzione multimediale (audio/video) Media Foundation (MF). In genere, MF viene usato nei giochi per la riproduzione in riproduzione, mentre XAudio2 viene usato per l'audio dinamico. |

## <a name="port-to-directx-11"></a>Porta a DirectX 11

| Argomento | Descrizione |
|-|-|
| [Migrazione a Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Linee guida di base per lo spostamento della codebase DirectX 9 in DirectX 11. |
| [Tecniche di codifica a doppio uso per i giochi](https://walbourn.github.io/) | Post di blog dettagliato sullo sviluppo per i livelli di funzionalità DirectX 9 e \_ \* DirectX 11 \_ \* in una singola applicazione. |
| [Implementazione di buffer shadow per il livello di funzionalità Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)) | Linee guida per l'implementazione delle mappe shadow nel livello di funzionalità DirectX \_ \* 9. |

## <a name="work-with-c"></a>Usare C++

Se si ha una vecchia mano con C++ in Windows, le cose potrebbero essere leggermente diverse. Di seguito sono riportati alcuni puntatori agli argomenti che consentono di ottenere un punto di controllo sulla differenza.

> [!NOTE]
> Alcuni di questi argomenti consentono di gestire l'applicazione C++/CX. È tuttavia consigliabile usare [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) per le nuove applicazioni. C++/WinRT è una proiezione del linguaggio C++ 17 interamente standard e moderna per le API di Windows Runtime (WinRT), implementata come libreria basata su file di intestazione e progettata per fornirti accesso privilegiato alla moderna API di Windows.

| Argomento | Descrizione |
|-|-|
| [**Visual C++ di riferimento al linguaggio (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Pagina di alto livello che collega al contenuto correlato a C++. |
| [**Riferimento rapido (Windows Runtime e Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Tabella che fornisce informazioni rapide sulle parole Visual C++ e sulle parole chiave delle estensioni dei componenti (C++/CX). |
| [**Sistema di tipi (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Contenuto di riferimento per i tipi supportati da C++/CX. |
| [**Spazi dei nomi (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | Contenuto di riferimento per gli spazi dei nomi che contengono tipi specifici di C++ che possono essere usati nelle Windows Store. |

| Argomento | Descrizione |
|-|-|
| [Programmazione asincrona (DirectX e C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Informazioni sulla programmazione asincrona e multithreading per app e giochi DirectX. |
| [Programmazione asincrona in C++](/previous-versions/windows/apps/hh780559(v=win.10)) | Vengono descritti i modi di base per usare la classe di attività per Windows metodi asincroni di Runtime. |
| [**Classe task (runtime di concorrenza)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Documentazione di riferimento per la classe task. |
| [Parallelismo delle attività (runtime di concorrenza)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Discussione approfondita sulla classe di attività e su come usarla. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>Librerie aggiuntive utili per Windows C++

| Argomento | Descrizione |
|-|-|
| [Libreria di modelli standard C++](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows I tipi di runtime sono molto validi con i tipi della libreria di modelli standard. La maggior parte delle app Windows Store C++ usa raccolte e algoritmi della libreria di modelli standard, ad eccezione del limite ABI. |
| [Parallel Patterns Library](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | PPL fornisce algoritmi e tipi che semplificano il parallelismo delle attività e il parallelismo dei dati nella CPU.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP l'accesso alla GPU per il parallelismo dei dati per utilizzo generico nelle schede video che supportano DirectX 11. |

## <a name="blogs-and-other-resources"></a>Blog e altre risorse

| Argomento | Descrizione |
|-|-|
| [Blog sui giochi Windows e DirectX](https://walbourn.github.io/) | Blog aggiornato regolarmente da un collaboratore di sviluppo DirectX chiave e un'ottima risorsa per gli sviluppatori DirectX. |
| [Windows Blog per sviluppatori DirectX](https://devblogs.microsoft.com/directx/) | Blog ufficiale Windows DirectX. |
| [Blog di DirectX di Michaeln Hargreave](https://www.shawnhargreaves.com/blogindex.html)) | Blog per sviluppatori di un altro collaboratore di sviluppo di DirectX Windows rispettato. |
| [DirectX Tool Kit](https://directxtk.codeplex.com/) | Sito CodePlex per DirectX Tool Kit (DxTK), che contiene una serie di UTILI API di supporto per il caricamento di mesh, la riproduzione di suoni e altri comportamenti comuni. |
| [Libreria di elaborazione delle trame DirectXTex](https://directxtex.codeplex.com/) | Sito di plex di codice per DirectX Texture Processing Library (DxTEX), che contiene le API di supporto per l'elaborazione delle trame e la compressione/decompressione. |