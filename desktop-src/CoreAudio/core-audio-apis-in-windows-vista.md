---
description: API audio Core
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: API audio Core
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 83488233240121ba2edcfd677484df67a452e479
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323875"
---
# <a name="core-audio-apis"></a>API audio Core

> [!NOTE]
> Per esempi di codice, vedere [esempi di SDK che usano le API audio di base](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis).

In questa documentazione vengono fornite informazioni sulle API (Application Programming Interface) di base per la famiglia di sistemi operativi Microsoft Windows. Fornisce le linee guida per gli sviluppatori di software da seguire per lo sviluppo di applicazioni che utilizzano le API audio di base in Windows Vista. Queste API erano nuove in Windows Vista e non sono disponibili nelle versioni precedenti di Windows.

Le API audio principali forniscono i mezzi per le applicazioni audio per accedere ai dispositivi di endpoint audio, ad esempio cuffie e microfoni. Le API audio principali servono come base per le API audio di livello superiore, ad esempio Microsoft DirectSound e le funzioni **waveXxx** di Windows Multimedia. La maggior parte delle applicazioni comunica con le API di livello superiore, ma alcune applicazioni con requisiti speciali potrebbero dover comunicare direttamente con le API di base dell'audio.

A partire da Windows 7, le API esistenti sono state migliorate e sono state aggiunte nuove API per supportare nuovi scenari. Le API di gestione di flussi e sessioni sono state migliorate in modo che l'applicazione sia ora in grado di enumerare e ottenere il controllo esteso della sessione audio. Usando le nuove API, l'applicazione può implementare un'esperienza di attenuazione dei flussi personalizzata. Le nuove API correlate ai dispositivi forniscono l'accesso alle proprietà del driver dei dispositivi endpoint.

Questa documentazione include le sezioni seguenti.

| Sezione                                                                    | Descrizione                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Informazioni sulle API audio di Windows Core](about-the-windows-core-audio-apis.md) | Viene fornita una panoramica delle API audio di Windows Core e vengono descritti i concetti di base. |
| [Guida per programmatori](programming-guide.md)                                 | Vengono descritte le principali funzionalità delle API audio principali e le relative modalità di utilizzo.            |
| [Guida di riferimento alla programmazione](programming-reference.md)                         | Fornisce informazioni di riferimento su C++ per le API audio di base.                       |

## <a name="related-topics"></a>Argomenti correlati

[Tecnologie multimediali per Windows](/previous-versions/bg125389(v=msdn.10))

[Esempi di SDK che usano le API audio principali](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis)
