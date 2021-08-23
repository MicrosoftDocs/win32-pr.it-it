---
description: Le annotazioni e la semantica standard (DXSAS) forniscono un metodo di uso degli shader in modo standard che consente l'uso degli shader con strumenti, applicazioni e motori di gioco.
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: Riferimenti alle annotazioni e alla semantica standard DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6da1489f92fce16e4717d501a64ab862fb9292c271397aa4a77e00e74c2e7952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373636"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>Riferimenti alle annotazioni e alla semantica standard DirectX

Le annotazioni e la semantica standard (DXSAS) forniscono un metodo di uso degli shader in modo standard che consente l'uso degli shader con strumenti, applicazioni e motori di gioco. DXSAS definisce un set di semantica e annotazioni associate ai valori dell'applicazione host e ai parametri degli effetti allo scopo di condividere gli effetti. Per poter essere utili, queste annotazioni e semantiche devono essere implementate sia nell'applicazione host che nel file degli effetti. Questo documento descrive lo standard DXSAS che sfrutta la potenza di DirectX Effect Framework per consentire alle applicazioni e agli strumenti host di condividere effetti DirectX (file con estensione fx) a livello di codice, nonché di progettare l'interazione con l'interfaccia utente.

## <a name="background-information"></a>Informazioni di base

Le annotazioni standard e la semantica sono progettate per associare i parametri effect e X-file ai valori dell'applicazione host. D3DX Effect Framework (o effetti) incapsula lo stato di rendering. Incapsulando lo stato di rendering (inclusi vertice, trama e stato di elaborazione pixel) in un effetto, è possibile creare una libreria di effetti che copre un'ampia gamma di opzioni di rendering. Possono essere incluse opzioni come il rendering in diversi tipi di hardware o il rendering con fusione a passaggio singolo o multipass. Per altre informazioni sul framework degli effetti, vedere Informazioni [di riferimento sugli effetti](dx9-graphics-reference-effects.md). DXSAS si basa su questo framework, consentendo un'esperienza più coerente per gli sviluppatori. Dopo che la configurazione del rendering è stata incapsulata in un effetto, lo standard DXSAS consente allo sviluppatore dell'effetto di esporre la finalità dei parametri dell'effetto tramite annotazioni. Queste annotazioni possono quindi essere lette da qualsiasi applicazione o strumento host (non solo quello progettato per l'uso dell'effetto) conforme allo standard, che comprenderà come usare l'effetto nel modo in cui è stato progettato.

La standardizzazione del set di semantica degli effetti e delle annotazioni supportate dalle applicazioni host consente agli autori di effetti di creare effetti che possono essere usati in più progetti e quindi promuovere una community più ampia di utenti con effetti. Lo standard DXSAS rende i file leggibili dagli sviluppatori, scambiabili tra gli strumenti e consente agli sviluppatori di sfruttare gli strumenti di terze parti per la creazione di effetti per la pipeline.

Questo documento descrive lo standard DXSAS che usa le annotazioni per esprimere la finalità dei parametri di effetto, nonché la definizione di una raccolta di valori dell'applicazione host che le applicazioni host accettano di rendere disponibili per un effetto.

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>Creazione di effetti con annotazioni standard e semantica

Come si può vedere dal diagramma seguente, lo standard DXSAS richiede annotazioni in un file degli effetti, nonché un'applicazione host che segue le linee guida descritte qui per lavorare con il file.

![Diagramma dello standard dxsas per le applicazioni host e i file degli effetti](images/sas-2.png)

L'applicazione host deve implementare la logica dell'interfaccia utente e l'ambiente host. Per implementare effetti conformi a DXSAS, leggere gli argomenti seguenti:

-   Il [parametro globale](global-parameter.md) definisce le informazioni pertinenti all'effetto, ad esempio la versione o l'autore dell'effetto.
-   [Data Binding](data-binding.md) definisce la raccolta di parametri (nonché il tipo e la struttura) che possono essere usati da un effetto che può essere impostato dall'applicazione host esposta agli effetti.
-   Per associare un controllo dell'interfaccia utente a un parametro dell'effetto, usare un'annotazione [dell'interfaccia utente](ui-annotation.md). Queste annotazioni includono: [SasUiMax](ui-annotation.md), [SasUiMin](ui-annotation.md), [SasUiSteps](ui-annotation.md), [SasUiStepsPower](ui-annotation.md)e [SasUiStride](ui-annotation.md).
-   Per inizializzare un parametro dell'effetto con i dati contenuti in un file esterno, usare un'annotazione [di inizializzazione del parametro](parameter-initialization-annotation.md).
-   Quando i dati vengono trasferiti tra l'applicazione host e un effetto (o viceversa), il cast e la [conversione](casting-and-conversion.md) si verificheranno quando i tipi non corrispondono esattamente. Questa sezione specifica la modalità di scrittura dei dati quando i tipi di origine e di destinazione differiscono. Usare inoltre [ParameterValueModifiers](casting-and-conversion.md) per modificare il modo in cui l'applicazione host deve interpretare i dati letti dal parametro effect. Queste annotazioni includono: [SasNormalize](casting-and-conversion.md) e [SasUnits](casting-and-conversion.md).

## <a name="case-sensitivity"></a>Maiuscole/minuscole

Per tutti gli identificatori, la semantica e i valori di annotazione non viene fatto distinzione tra maiuscole e minuscole. Per i nomi delle annotazioni (non i valori) viene fatto distinzione tra maiuscole e minuscole. I nomi delle annotazioni vengono riconosciuti dal sistema di effetti D3DX e pertanto anche i nomi delle annotazioni saS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'effetto](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



