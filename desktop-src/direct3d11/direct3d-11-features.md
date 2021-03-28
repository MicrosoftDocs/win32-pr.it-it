---
title: Funzionalità di Direct3D 11
description: La guida alla programmazione contiene informazioni su come usare la pipeline programmabile Direct3D 11 per creare grafica 3D in tempo reale per giochi e per applicazioni scientifiche e desktop.
ms.assetid: ee4dae04-1a52-4587-87c1-006abb687a91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b6ec64e315275ca6faaf513d04f996609615a2
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047571"
---
# <a name="direct3d-11-features"></a>Funzionalità di Direct3D 11

La guida alla programmazione contiene informazioni su come usare la pipeline programmabile Direct3D 11 per creare grafica 3D in tempo reale per giochi e per applicazioni scientifiche e desktop.

-   [Compute Shader](#compute-shader)
-   [Collegamento dinamico dello shader](#dynamic-shader-linking)
-   [Multithreading](#multithreading)
-   [Tassellatura](#tessellation)
-   [Elenco completo delle funzionalità](#full-listing-of-features)
-   [Funzionalità aggiunte nelle versioni precedenti](#features-added-in-previous-releases)
-   [Argomenti correlati](#related-topics)

## <a name="compute-shader"></a>Compute Shader

Un compute shader è uno shader programmabile progettato per l'elaborazione parallela dei dati per utilizzo generico. In altre parole, Compute Shaders consente di usare una GPU come processore parallelo per utilizzo generico. Compute shader è simile agli altri shader della pipeline programmabile (ad esempio vertex, pixel, Geometry) nel modo in cui accede a input e output. La tecnologia compute shader è nota anche come tecnologia DirectCompute. Un compute shader è integrato in Direct3D ed è accessibile tramite un dispositivo Direct3D. Può condividere direttamente le risorse di memoria con gli shader grafici usando il dispositivo Direct3D. Tuttavia, non è direttamente connesso ad altre fasi dello shader.

Un compute shader è progettato per le applicazioni di mercato di massa che eseguono calcoli a frequenze interattive, quando il costo della transizione tra l'API (e lo stack software associato) e una CPU comporta un sovraccarico eccessivo.

Un compute shader ha un proprio set di Stati. Un compute shader non ha necessariamente un mapping forzato di 1-1 a record di input (ad esempio, un vertex shader) o a record di output (ad esempio, il pixel shader). Alcune funzionalità dello shader Graphics sono supportate, mentre altre sono state rimosse, in modo da poter aggiungere nuove funzionalità specifiche di compute shader.

Per supportare le funzionalità specifiche di compute shader, sono ora disponibili diversi nuovi tipi di risorse, ad esempio buffer di lettura/scrittura, trame e buffer strutturati.

Per ulteriori informazioni, vedere [Panoramica di Compute Shader](direct3d-11-advanced-stages-compute-shader.md) .

## <a name="dynamic-shader-linking"></a>Collegamento dinamico dello shader

I sistemi di rendering devono gestire una complessità significativa quando gestiscono gli shader, offrendo allo stesso tempo la possibilità di ottimizzare il codice dello shader. Si tratta di una sfida ancora maggiore perché gli shader devono supportare una varietà di materiali diversi in una scena di cui è stato eseguito il rendering in varie configurazioni hardware. Per risolvere questo problema, gli sviluppatori dello shader hanno spesso ricorreto a uno dei due approcci generali. Sono stati creati shader completi di grandi dimensioni, che possono essere usati da un'ampia gamma di elementi della scena, che comportano una certa flessibilità o creano singoli shader per ogni flusso geometrico, tipo di materiale o combinazione di tipi di luce necessaria.

Questi grandi shader per scopi generali gestiscono questo problema ricompilando lo stesso shader con definizioni del preprocessore diverse e il secondo metodo usa la potenza dello sviluppatore di forza bruta per ottenere lo stesso risultato. L'esplosione della permutazione dello shader è stata spesso un problema per gli sviluppatori che ora devono gestire migliaia di permutazioni dello shader diverse all'interno della pipeline di gioco e di asset.

Direct3D 11 e Shader Model 5 introducono costrutti di linguaggio orientato a oggetti e forniscono il supporto di runtime per il collegamento dello shader per aiutare gli sviluppatori a programmare gli shader.

Per ulteriori informazioni, vedere [Dynamic Linking](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) .

## <a name="multithreading"></a>Multithreading

Molte applicazioni grafiche sono associate alla CPU a causa di attività costose quali attraversamento del grafico della scena, ordinamento degli oggetti e simulazioni fisiche. Poiché i sistemi multicore sono sempre più disponibili, Direct3D 11 ha migliorato il supporto per il multithreading per consentire un'interazione efficace tra più thread CPU e le API grafiche D3D11.

Direct3D 11 consente la funzionalità seguente per supportare il multithreading:

-   Gli oggetti simultanei vengono ora creati in thread distinti, rendendo disponibili funzioni di punto di ingresso che creano oggetti a thread libero, in modo che molti thread creino oggetti simultaneamente. Ad esempio, un'applicazione può ora compilare uno shader o caricare una trama in un thread durante il rendering in un altro.
-   Gli elenchi di comandi possono essere creati su più thread: un elenco di comandi è una sequenza registrata di comandi grafici. Con Direct3D 11, è possibile creare elenchi di comandi su più thread CPU, che consente l'attraversamento parallelo del database di scena o l'elaborazione fisica su più thread. Questo consente di liberare il thread di rendering principale per inviare i buffer dei comandi all'hardware.

Per ulteriori informazioni, vedere [multithreading](overviews-direct3d-11-render-multi-thread.md) .

## <a name="tessellation"></a>Suddivisione a mosaico

È possibile utilizzare la suddivisione a mosaico per eseguire il rendering di un singolo modello con diversi livelli di dettaglio. Questo approccio genera un modello più geometricamente accurato che dipende dal livello di dettaglio richiesto per una scena. Utilizzare la suddivisione a mosaico in una scena in cui il livello di dettaglio consente un modello di geometria inferiore, riducendo la richiesta di larghezza di banda di memoria utilizzata durante il rendering.

In Direct3D, la suddivisione a mosaico è implementata nella GPU per calcolare una superficie curva più liscia da una patch di input grossolana (meno dettagliata). Ogni superficie della patch (quad o triangolo) è suddivisa in visi triangolari più piccoli che approssimano meglio la superficie desiderata.

Per informazioni sull'implementazione dello schema a mosaico nella pipeline grafica, vedere [Cenni preliminari sullo schema a mosaico](direct3d-11-advanced-stages-tessellation.md).

## <a name="full-listing-of-features"></a>Elenco completo delle funzionalità

Questo è un elenco completo delle funzionalità di Direct3D 11.

-   È possibile eseguire Direct3D 11 su [hardware](overviews-direct3d-11-devices-downlevel.md) di livello inferiore specificando un [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) quando si crea un dispositivo.
-   È possibile eseguire la suddivisione a mosaico (vedere [Cenni preliminari sulla suddivisione a mosaico](direct3d-11-advanced-stages-tessellation.md)) usando i tipi di shader seguenti:

    -   Hull shader
    -   Domain shader

-   Direct3D 11 supporta il multithreading (vedere [multithreading](overviews-direct3d-11-render-multi-thread.md))

    -   Creazione di una risorsa/shader/oggetto multithread
    -   Creazione dell'elenco di visualizzazione multithread

-   Direct3D 11 espande gli shader con le funzionalità seguenti (vedere il [modello di shader 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl))

    -   Risorse indirizzabili: trame, buffer costanti e Samplers
    -   Tipi di risorse aggiuntivi, ad esempio buffer di lettura/scrittura e trame (vedere [nuovi tipi di risorse](direct3d-11-advanced-stages-cs-resources.md)).
    -   Subroutine
    -   Compute shader (vedere Panoramica di [compute shader](direct3d-11-advanced-stages-compute-shader.md)): uno shader che consente di velocizzare i calcoli dividendo lo spazio dei problemi tra diversi thread software o gruppi di thread e condividendo i dati tra i registri dello shader per ridurre significativamente la quantità di dati necessari per l'input in uno shader. Gli algoritmi che il compute shader può migliorare significativamente includono l'elaborazione post, l'animazione, la fisica e l'intelligenza artificiale.
    -   Geometry shader (vedere le [funzionalità geometry shader](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features))

        -   Creazione di istanze: consente a geometry shader di restituire un massimo di 1024 vertici o qualsiasi combinazione di istanze e vertici fino a 1024 (al massimo 32 istanze di vertici di 32).

    -   Pixel shader

        -   Copertura come input PS
        -   Interpolazione programmabile degli input: il pixel shader può valutare gli attributi all'interno del pixel, in qualsiasi punto della griglia multisample
        -   Il campionamento centrale degli attributi deve rispettare le regole seguenti:

            -   Se vengono analizzati tutti gli esempi della primitiva, l'attributo viene valutato in corrispondenza del pixel Center, indipendentemente dal fatto che il modello di esempio disponga di una posizione di esempio nel centro pixel.
            -   In caso contrario, l'attributo viene valutato in corrispondenza del primo campione trattato, ovvero l'esempio con l'indice più basso tra tutti gli indici di esempio. In questa situazione, il code coverage di esempio viene determinato dopo l'applicazione dell'operazione AND logica alla copertura e allo stato di rasterizzazione della maschera di esempio.
            -   Se non viene analizzato alcun campione, ad esempio su pixel helper che vengono eseguiti fuori dai limiti di una primitiva per riempire gli indicatori di pixel 2x2, l'attributo viene valutato in uno dei modi seguenti:

                -   Se lo stato di rasterizzazione maschera di esempio è un subset degli esempi nel pixel, il primo campione incluso nello stato di rasterizzazione maschera di esempio è il punto di valutazione.
                -   In caso contrario, nella condizione di esempio-maschera completa, il centro pixel è il punto di valutazione.

-   Direct3D 11 espande le trame (vedere [Panoramica delle trame](overviews-direct3d-11-resources-textures.md)) con le funzionalità seguenti

    -   Gather4

        -   Supporto per le trame multicomponente: specificare un canale da cui caricare
        -   Supporto per gli offset programmabili

    -   Streaming

        -   Clamp di trama per limitare il precaricamento di WDDM

    -   limiti di trama 16K
    -   Richiedi la precisione a 8 bit di sottotexel e secondaria al filtro della trama
    -   Nuovi formati di compressione delle trame (1 nuovo formato LDR e 1 nuovo formato HDR)

-   Direct3D 11 supporta la oDepth conservativa: questo algoritmo consente a un pixel shader di confrontare il valore di profondità per pixel della pixel shader con quello nell'rasterizzatore. Il risultato Abilita le operazioni di abbattimento precoce della profondità mantenendo la possibilità di restituire oDepth da un pixel shader.
-   Direct3D 11 supporta memoria di grandi dimensioni

    -   Consenti risorse > 4 GB
    -   Mantieni gli indici delle risorse a 32 bit, ma la risorsa è più grande

-   Direct3D 11 supporta i miglioramenti dell'output di flusso

    -   Output flusso indirizzabile
    -   Aumentare il numero di output del flusso a 4
    -   Modificare tutti i buffer di output del flusso in più elementi

-   Direct3D 11 supporta il modello di shader 5 (vedere il [modello di shader 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5))

    -   Raddoppia con le denormazioni
    -   Istruzione set count BITS
    -   Trova istruzione set di primo bit
    -   Gestione di porta/overflow
    -   Istruzioni di inversione di bit per FFT
    -   Intrinseco scambio condizionale
    -   ResInfo nei buffer
    -   Reciproco a precisione ridotta
    -   Istruzioni di conversione shader-FP16 in FP32 e viceversa
    -   Buffer strutturato, che è un nuovo tipo di buffer contenente elementi strutturati.

-   Direct3D 11 supporta le visualizzazioni di profondità o stencil di sola lettura

    -   Disabilita le Scritture nella parte di sola lettura, consente di usare la trama come input e per l'abbattimento della profondità

-   Direct3D 11 supporta il progetto indirect-Direct3D 10 implementa DrawAuto, che accetta il contenuto (generato dalla GPU) e ne esegue il rendering (sulla GPU). Direct3D 11 generalizza DrawAuto in modo che possa essere chiamato da un compute shader mediante DrawInstanced e DrawIndexedInstanced.
-   Direct3D 11 supporta funzionalità varie

    -   Viewport a virgola mobile
    -   Clamping mipmap per risorsa
    -   Distorsione profondità: questo algoritmo aggiorna il comportamento della distorsione della profondità, usando lo stato di rasterizzazione. Il risultato Elimina gli scenari in cui la distorsione calcolata potrebbe essere NaN.
    -   Limiti delle risorse: gli indici di risorse devono essere ancora <= 32 bit, ma le risorse possono avere dimensioni maggiori di 4 GB.
    -   Precisione del rasterizzatore
    -   Requisiti di MSAA
    -   Contatori ridotti
    -   Formato a 1 bit e filtro del testo rimossi

## <a name="features-added-in-previous-releases"></a>Funzionalità aggiunte nelle versioni precedenti

Per l'elenco delle funzionalità aggiunte nelle versioni precedenti, vedere gli argomenti seguenti:

-   [Novità dell'SDK di agosto 2009 per Windows 7/Direct3D 11](dx11-whats-new.md)
-   [Novità della versione Technical Preview di novembre 2008 Direct3D 11](dx11-08nov-whats-new.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 