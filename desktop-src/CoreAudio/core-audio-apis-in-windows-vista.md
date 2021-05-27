---
description: API audio di base
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: API audio di base
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 2cabb462d13786c874401394fa814484f79b0e3b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548956"
---
# <a name="core-audio-apis"></a>API audio di base

> [!NOTE]
> Per esempi di codice, vedere [esempi di SDK che usano le API audio di base.](./sdk-samples-that-use-the-core-audio-apis.md)

Questa documentazione fornisce informazioni sulle API (Application Programming Interface) audio di base per la famiglia di sistemi operativi Microsoft Windows. Fornisce linee guida che gli sviluppatori di software possono seguire per lo sviluppo di applicazioni che usano le API audio di base in Windows Vista. Queste API sono nuove in Windows Vista e non sono disponibili nelle versioni precedenti di Windows.

Le API audio di base consentono alle applicazioni audio di accedere ai dispositivi endpoint audio, ad esempio le cuffi e i microfoni. Le API audio principali fungono da base per le API audio di livello superiore, ad esempio Microsoft DirectSound e le funzioni **waveXxx** multimediali di Windows. La maggior parte delle applicazioni comunica con le API di livello superiore, ma alcune applicazioni con requisiti speciali potrebbero dover comunicare direttamente con le API audio di base.

A partire da Windows 7, le API esistenti sono state migliorate e sono state aggiunte nuove API per supportare nuovi scenari. Le API di gestione del flusso e della sessione sono state migliorate in modo che l'applicazione possa ora enumerare e ottenere il controllo esteso sulla sessione audio. Usando le nuove API, l'applicazione può implementare un'esperienza di attenuazione del flusso personalizzata. Le nuove API correlate al dispositivo forniscono l'accesso alle proprietà del driver dei dispositivi endpoint.

Questa documentazione include le sezioni seguenti.

| Sezione                                                                    | Descrizione                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Informazioni sulle API audio di Windows Core](about-the-windows-core-audio-apis.md) | Fornisce una panoramica delle API audio principali di Windows e descrive i concetti di base. |
| [Guida per programmatori](programming-guide.md)                                 | Descrive le funzionalità principali delle API audio principali e come usarle.            |
| [Guida di riferimento alla programmazione](programming-reference.md)                         | Fornisce informazioni di riferimento su C++ per le API audio principali.                       |

## <a name="related-topics"></a>Argomenti correlati

[Tecnologie multimediali per Windows](/previous-versions/bg125389(v=msdn.10))

[Esempi di SDK che usano le API audio di base](./sdk-samples-that-use-the-core-audio-apis.md)