---
title: Invio di lavoro in Direct3D 12
description: Per migliorare l'efficienza della CPU delle app Direct3D, Direct3D 12 non supporta più un contesto immediato associato a un dispositivo.
ms.assetid: BE2F46EA-D4A9-47F7-A2D1-6A486DD4DC1A
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: aa852fc82280b14b0270a7c4a4c40cfe441803b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103736"
---
# <a name="work-submission-in-direct3d-12"></a>Invio di lavoro in Direct3D 12

Per migliorare l'efficienza della CPU delle app Direct3D, a partire dalla versione 12, Direct3D non supporta più un contesto immediato associato a un dispositivo. Al contrario, l'applicazione registra e quindi invia gli *elenchi di comandi*, che contengono chiamate di gestione delle risorse e di disegno. È possibile inviare gli elenchi di comandi da più thread a una o più code di comandi, che gestiscono l'esecuzione dei comandi. Questa modifica fondamentale aumenta l'efficienza a thread singolo consentendo all'applicazione di pre-calcolare il lavoro di rendering per riutilizzarlo in un secondo momento, sfruttando i sistemi multicore distribuendo il lavoro di rendering tra più thread.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Filosofia di progettazione delle code dei comandi e degli elenchi di comandi](design-philosophy-of-command-queues-and-command-lists.md) | Gli obiettivi dell'abilitazione del riutilizzo del rendering del lavoro e del ridimensionamento multithreading richiedono modifiche fondamentali al modo in cui le app Direct3D inviano il lavoro di rendering alla GPU. |
| [Creazione e registrazione di elenchi di comandi e bundle](recording-command-lists-and-bundles.md) | Questo argomento descrive la registrazione di elenchi di comandi e bundle nelle app Direct3D 12. Gli elenchi di comandi e i bundle consentono alle app di registrare le chiamate di disegno o modifica dello stato per un'esecuzione successiva sull'unità di elaborazione grafica (GPU). |
| [Esecuzione e sincronizzazione degli elenchi di comandi](executing-and-synchronizing-command-lists.md) | In Microsoft Direct3D 12 la modalità immediata delle versioni precedenti non è più presente. Al contrario, le app creano elenchi di comandi e bundle, quindi registrano set di comandi GPU. Le code di comando vengono usate per inviare elenchi di comandi da eseguire. Questo modello consente agli sviluppatori di avere un maggiore controllo sull'utilizzo efficiente di GPU e CPU. |
| [Gestione dello stato della pipeline grafica in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md) | Questo argomento descrive come viene impostato lo stato della pipeline grafica in Direct3D 12. |
| [Uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md) | Per ridurre l'utilizzo complessivo della CPU e consentire il multithreading e la pre-elaborazione dei driver, Direct3D 12 sposta la responsabilità della gestione dello stato per ogni risorsa dal driver di grafica all'applicazione. |
| [Pipeline e shader con Direct3D 12](pipelines-and-shaders-with-directx-12.md) | La pipeline programmabile di Direct3D 12 aumenta significativamente le prestazioni di rendering rispetto alle interfacce di programmazione grafica di generazione precedente. |
| [Ombreggiatura a frequenza variabile (VRS)](vrs.md) | L' &mdash; ombreggiatura a frequenza variabile o l'ombreggiatura di pixel grossolani &mdash; è un meccanismo che consente di allocare prestazioni/potenza di rendering a frequenze che variano in base all'immagine sottoposta a rendering. |
| [Passaggi di rendering](direct3d-12-render-passes.md) | La funzionalità di rendering passa consente al renderer di migliorare l'efficienza della GPU riducendo il traffico di memoria alla/dalla memoria fuori chip; Questa operazione consente all'applicazione di identificare meglio i requisiti di ordinamento per il rendering delle risorse e le dipendenze dei dati. |

## <a name="related-topics"></a>Argomenti correlati

* [Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
