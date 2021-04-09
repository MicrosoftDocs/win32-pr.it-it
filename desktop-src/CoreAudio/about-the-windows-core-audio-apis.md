---
description: Informazioni sulle API audio di Windows Core
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Informazioni sulle API audio di Windows Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878338"
---
# <a name="about-the-windows-core-audio-apis"></a>Informazioni sulle API audio di Windows Core

In questa documentazione vengono fornite informazioni sulle API audio principali per la famiglia di sistemi operativi Microsoft Windows.

Le API di base audio sono state introdotte in Windows Vista. Si tratta di un nuovo set di componenti audio in modalità utente che offre applicazioni client con funzionalità audio migliorate. Di seguito sono riportate alcune funzionalità:

-   Streaming audio a bassa latenza e con resilienza.
-   Maggiore affidabilità (molte funzioni audio sono state spostate dalla modalità kernel alla modalità utente).
-   Maggiore sicurezza (l'elaborazione del contenuto audio protetto avviene in un processo sicuro con privilegi inferiori).
-   Assegnazione di particolari ruoli a livello di sistema (console, Multimedia e comunicazioni) a singoli dispositivi audio.
-   Astrazione del software dei dispositivi dell'endpoint audio (ad esempio, altoparlanti, cuffie e microfoni) manipolati direttamente dall'utente.

Le API di base audio sono state migliorate in Windows 7. Per ulteriori informazioni sui miglioramenti e sulle nuove funzionalità aggiunte, vedere [What ' s New for Core Audio API in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).

Questa documentazione descrive le API audio principali. Queste API vengono utilizzate come base per le API di livello superiore seguenti:

-   DirectSound
-   DirectMusic
-   Funzioni **waveXxx** e **mixerXxx** multimediali di Windows
-   Media Foundation

Queste API di livello superiore usano le API audio principali per condividere l'accesso ai dispositivi audio. Media Foundation è una novità di Windows Vista, mentre le funzioni DirectSound, DirectMusic e **waveXxx** e **mixerXxx** sono supportate in Windows 98, Windows Millennium Edition e in Windows 2000 e versioni successive.

La maggior parte delle applicazioni audio comunica con le API di livello superiore anziché comunicare direttamente con le API di base di audio. Di seguito sono riportati alcuni esempi di applicazioni che usano le API di livello superiore:

-   Lettori multimediali
-   Lettori DVD
-   Giochi
-   Applicazioni aziendali, ad esempio Microsoft Office PowerPoint, che riproducono file audio

In genere, queste applicazioni comunicano con le API DirectSound o Media Foundation.

La comunicazione diretta con le API audio di base potrebbe non essere adatta per molte applicazioni audio per utilizzo generico. Ad esempio, le API audio principali richiedono flussi audio per usare i formati di dati nativi di un dispositivo audio. Tuttavia, gli sviluppatori di software di terze parti che sviluppano i tipi di prodotti seguenti potrebbero richiedere le funzionalità speciali delle API audio principali:

-   Applicazioni audio professionali ("Audio Pro")
-   Applicazioni di comunicazione in tempo reale (RTC)
-   API audio di terze parti

Per ottenere una latenza minima, è possibile che un'applicazione "Audio Pro" o un'applicazione RTC debba accedere direttamente alle funzionalità di basso livello delle API audio principali, ottenendo l'accesso esclusivo all'hardware audio. Un'API audio di terze parti potrebbe richiedere l'accesso diretto alle API audio principali per implementare un set di funzionalità che potrebbero non essere supportate interamente da un'unica API audio di alto livello fornita con Windows.

Un'applicazione che usa un'API audio legacy per riprodurre o registrare audio potrebbe richiedere funzionalità aggiuntive non supportate dall'API audio legacy, ma supportate dalle API audio di base. In molti casi, l'applicazione può accedere a queste funzionalità direttamente tramite le API audio principali, che possono essere usate in combinazione con l'API audio legacy.

Le API audio principali sono:

-   [API del dispositivo multimediale (MMDevice)](mmdevice-api.md). I client usano questa API per enumerare i dispositivi dell'endpoint audio nel sistema.
-   [API di sessione audio Windows (WASAPI)](wasapi.md). I client usano questa API per creare e gestire flussi audio da e verso dispositivi endpoint audio.
-   [API DeviceTopology](devicetopology-api.md). I client usano questa API per accedere direttamente alle funzionalità topologiche (ad esempio, i controlli volume e i multiplexer) che si trovano lungo i percorsi dati all'interno dei dispositivi hardware nelle schede audio.
-   [API EndpointVolume](endpointvolume-api.md). I client usano questa API per accedere direttamente ai controlli volume sui dispositivi dell'endpoint audio. Questa API viene usata principalmente dalle applicazioni che gestiscono flussi audio in modalità esclusiva.

Queste API supportano la nozione intuitiva di un dispositivo endpoint, descritto in dispositivi dell' [endpoint audio](audio-endpoint-devices.md).

Microsoft non prevede di creare le API audio principali descritte di seguito disponibili per l'utilizzo con le versioni precedenti di Windows, tra cui Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 e Windows 98.

Questa panoramica include gli argomenti seguenti.



| **Argomento**                                                                                      | **Descrizione**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Novità relative alle API audio di base in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Riepiloga le nuove funzionalità e i miglioramenti apportati alle API audio principali                   |
| [File di intestazione e componenti di sistema](header-files-and-system-components.md)                   | Descrive i file di intestazione e i componenti di sistema per le API audio di base.                 |
| [Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)       | Elenca gli esempi nell'Windows SDK che usano le API di base di audio.                        |




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API audio Core](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



