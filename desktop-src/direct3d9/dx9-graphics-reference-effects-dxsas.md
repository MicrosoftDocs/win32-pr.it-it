---
description: Le annotazioni e la semantica standard (DXSAS) forniscono un metodo per usare gli shader in modo standard che consente di usare gli shader con strumenti, applicazioni e motori di gioco.
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: Informazioni di riferimento sulla semantica e le annotazioni standard DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c989f4aed7c01c62d6133e01fe035223b74c8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481693"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>Informazioni di riferimento sulla semantica e le annotazioni standard DirectX

Le annotazioni e la semantica standard (DXSAS) forniscono un metodo per usare gli shader in modo standard che consente di usare gli shader con strumenti, applicazioni e motori di gioco. DXSAS definisce un set di semantiche e annotazioni associate ai valori dell'applicazione host e ai parametri di effetto allo scopo di condividere gli effetti. Affinché le annotazioni e la semantica siano utili, è necessario implementarle sia nell'applicazione host che nel file di effetti. Questo documento descrive lo standard DXSAS che sfrutta la potenza del Framework degli effetti DirectX per consentire alle applicazioni e agli strumenti host di condividere gli effetti DirectX (file con estensione FX) a livello di codice, nonché di progettare interazioni con l'interfaccia utente.

## <a name="background-information"></a>Informazioni di base

Le annotazioni e la semantica standard sono progettate per associare i parametri Effect e X-file ai valori dell'applicazione host. Il Framework D3DX Effect (o Effects) incapsula lo stato di rendering. Incapsulando lo stato di rendering (incluso lo stato di elaborazione di vertici, trame e pixel) in un effetto, è possibile creare una libreria di effetti che copra un'ampia gamma di opzioni di rendering. Questo potrebbe includere opzioni come il rendering su diversi tipi di hardware o il rendering con la combinazione di una o più pass. Per altre informazioni sul Framework degli effetti, vedere [riferimento a effetti](dx9-graphics-reference-effects.md). DXSAS si basa su questo Framework, consentendo un'esperienza più coerente per gli sviluppatori. Una volta che l'installazione del rendering è incapsulata in un effetto, lo standard DXSAS consente all'autore dell'effetto di esporre lo scopo dei parametri di effetto tramite le annotazioni. Queste annotazioni possono essere lette da qualsiasi applicazione o strumento host (non solo quello progettato per utilizzare l'effetto), che è conforme allo standard, comprenderà come utilizzare l'effetto nel modo in cui è stato progettato.

La standardizzazione della semantica degli effetti e delle annotazioni che ospitano le applicazioni supporta gli autori degli effetti che consentono di creare effetti che possono essere utilizzati in più progetti e quindi di promuovere una community più ampia di utenti effetti. Lo standard DXSAS rende i file leggibili dagli sviluppatori, scambiabili tra gli strumenti e consente agli sviluppatori di sfruttare gli strumenti di terze parti per la creazione di effetti per la loro pipeline.

Questo documento descrive lo standard DXSAS che usa le annotazioni per esprimere lo scopo dei parametri di effetto, nonché definire una raccolta di valori dell'applicazione host che le applicazioni host accettano di rendere disponibile a un effetto.

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>Creazione di effetti con le annotazioni e la semantica standard

Come si può notare dal diagramma seguente, lo standard DXSAS richiede le annotazioni in un file degli effetti, oltre a un'applicazione host che segue le linee guida descritte qui per lavorare con il file.

![diagramma dello standard dxsas per le applicazioni host e i file degli effetti](images/sas-2.png)

L'applicazione host deve implementare la logica dell'interfaccia utente e l'ambiente host. Per implementare gli effetti conformi a DXSAS, leggere gli argomenti seguenti:

-   Il [parametro globale](global-parameter.md) definisce le informazioni pertinenti all'effetto, ad esempio la versione, o l'autore dell'effetto.
-   Il [Data Binding](data-binding.md) definisce la raccolta di parametri (così come il tipo e la struttura) che può essere utilizzata da un effetto che può essere impostato dall'applicazione host esposta agli effetti.
-   Per associare un controllo dell'interfaccia utente a un parametro Effect, usare un' [annotazione dell'](ui-annotation.md)interfaccia utente. Queste annotazioni includono: [SasUiMax](ui-annotation.md), [SasUiMin](ui-annotation.md), [SasUiSteps](ui-annotation.md), [SasUiStepsPower](ui-annotation.md)e [SasUiStride](ui-annotation.md).
-   Per inizializzare un parametro Effect con i dati contenuti in un file esterno, usare un' [annotazione di inizializzazione del parametro](parameter-initialization-annotation.md).
-   Quando i dati vengono trasferiti tra l'applicazione host e un effetto (o viceversa), il [cast e la conversione](casting-and-conversion.md) si verificheranno quando i tipi non corrispondono esattamente. In questa sezione viene specificato come vengono scritti i dati quando i tipi di origine e di destinazione sono diversi. Inoltre, utilizzare [ParameterValueModifiers](casting-and-conversion.md) per modificare il modo in cui l'applicazione host deve interpretare i dati letti dal parametro Effect. Queste annotazioni includono: [SasNormalize](casting-and-conversion.md) e [SasUnits](casting-and-conversion.md).

## <a name="case-sensitivity"></a>Maiuscole/minuscole

Per tutti gli identificatori, la semantica e i valori di annotazione non viene fatta distinzione tra maiuscole I nomi di annotazioni (non i valori) fanno distinzione tra maiuscole e I nomi delle annotazioni vengono riconosciuti dal sistema D3DX Effects e pertanto sono anche nomi di annotazioni SAS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a effetti](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



