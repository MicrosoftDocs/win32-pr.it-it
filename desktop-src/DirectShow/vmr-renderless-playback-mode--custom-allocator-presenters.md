---
description: Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757667"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a>Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)

In modalità di riproduzione senza rendering, VMR non esegue il rendering. USA invece un allocatore-Presenter personalizzato fornito dall'applicazione. Questa modalità è utile per giochi e altri tipi di applicazioni con effetti video avanzati. La modalità di riproduzione con rendering consente alle applicazioni di creare e controllare la propria superficie DirectDraw (VMR-7) o la superficie Direct3D (VMR-9) e di accedere ai bit video in fase di presentazione.

In modalità senza rendering, VMR-9 non carica automaticamente il componente mixer.

In modalità di riproduzione senza rendering, l'applicazione esegue le attività seguenti:

-   Gestisce la finestra di riproduzione.
-   Alloca l'oggetto DirectDraw o Direct3D e il buffer del frame finale.
-   Notifica al resto del sistema di riproduzione l'oggetto in uso.
-   Visualizza il buffer dei frame all'ora corretta.
-   Gestisce tutte le modifiche in modalità di risoluzione, monitora le modifiche e le perdite di superficie. Deve consigliare il resto del sistema di riproduzione di questi eventi.

VMR esegue le operazioni seguenti:

-   Gestisce tutte le tempistiche correlate alla presentazione del fotogramma video.
-   Fornisce informazioni sul controllo di qualità per l'applicazione e il resto del sistema di riproduzione.
-   Presenta un'interfaccia coerente con i componenti upstream del sistema di riproduzione, che non sono consapevoli del fatto che l'applicazione fornisce l'allocazione del buffer di frame e l'esecuzione del rendering.
-   Fornisce qualsiasi combinazione di flussi video che potrebbero essere necessari prima del rendering.

Poiché il deinterlacciamento viene eseguito dal mixer, Allocator-Presenter riceve sempre i frame deinterlacciati. Per ulteriori informazioni, vedere [impostazione delle preferenze di deinterlacciamento](setting-deinterlace-preferences.md).

Per ulteriori informazioni sulla specifica di un allocatore-Presenter personalizzato, vedere gli argomenti seguenti:

-   [Specifica di un Allocator-Presenter personalizzato per VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [Specifica di un Allocator-Presenter personalizzato per VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [Sincronizzazione di VMR alla frequenza di aggiornamento del monitoraggio](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



