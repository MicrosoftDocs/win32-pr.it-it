---
description: Informazioni sulle WINDOWS Core Audio
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Informazioni sulle WINDOWS Core Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07d5336522a681fc5f2d6e8ee5db0c17eacccfa46ea4cc4559bf00e6ea629031
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018549"
---
# <a name="about-the-windows-core-audio-apis"></a>Informazioni sulle WINDOWS Core Audio

Questa documentazione fornisce informazioni sulle API audio di base per la famiglia di Windows microsoft.

Le API core audio sono state introdotte in Windows Vista. Si tratta di un nuovo set di componenti audio in modalità utente che offre alle applicazioni client funzionalità audio migliorate. Queste funzionalità includono:

-   Streaming audio a bassa latenza e resiliente agli anomali.
-   Maggiore affidabilità (molte funzioni audio sono state spostate dalla modalità kernel alla modalità utente).
-   Sicurezza migliorata (l'elaborazione del contenuto audio protetto avviene in un processo sicuro con privilegi inferiori).
-   Assegnazione di ruoli specifici a livello di sistema (console, contenuti multimediali e comunicazioni) a singoli dispositivi audio.
-   Astrazione software dei dispositivi endpoint audio (ad esempio, altoparlanti, cuffia e microfoni) che l'utente manipola direttamente.

Le API core audio sono state migliorate in Windows 7. Per altre informazioni sui miglioramenti e sulle nuove funzionalità aggiunte, vedere Novità delle API audio core [in Windows 7.](what-s-new-for-core-audio-apis-in-windows-7.md)

Questa documentazione descrive le API audio di base. Queste API fungono da base per le API di livello superiore seguenti:

-   Directsound
-   Directmusic
-   Windows funzioni **waveXxx e** **mixerXxx multimediali**
-   Media Foundation

Queste API di livello superiore usano le API Audio core per condividere l'accesso ai dispositivi audio. Media Foundation è una novità di Windows Vista, mentre DirectSound, DirectMusic e le funzioni **waveXxx** e **mixerXxx** sono supportati in Windows 98, Windows Millennium Edition e in Windows 2000 e versioni successive.

La maggior parte delle applicazioni audio comunica con le API di livello superiore invece di comunicare direttamente con le API audio di base. Di seguito sono riportati alcuni esempi di applicazioni che usano API di livello superiore:

-   Lettori multimediali
-   Lettori DVD
-   Giochi
-   Applicazioni aziendali, ad esempio Microsoft Office PowerPoint, che riproducino file audio

In genere, queste applicazioni comunicano con le MEDIA FOUNDATION DirectSound.

La comunicazione diretta con le API Core Audio potrebbe non essere adatta per molte applicazioni audio per utilizzo generico. Ad esempio, le API Core Audio richiedono flussi audio per usare i formati di dati nativi di un dispositivo audio. Tuttavia, gli sviluppatori di software di terze parti che sviluppano i tipi di prodotti seguenti potrebbero richiedere le funzionalità speciali delle API audio di base:

-   Professional applicazioni audio "pro audio"
-   Applicazioni di comunicazione in tempo reale
-   API audio di terze parti

Un'applicazione "audio pro" o RTC potrebbe richiedere l'accesso diretto alle funzionalità di basso livello delle API audio core per ottenere la latenza minima ottenendo l'accesso esclusivo all'hardware audio. Un'API audio di terze parti potrebbe richiedere l'accesso diretto alle API audio core per implementare un set di funzionalità che potrebbero non essere completamente supportate da una singola API audio di alto livello fornita con Windows.

Un'applicazione che usa un'API audio legacy per riprodurre o registrare audio potrebbe richiedere funzionalità aggiuntive non supportate dall'API audio legacy, ma supportate dalle API audio core. In molti casi, l'applicazione può accedere a queste funzionalità direttamente tramite le API audio core, che possono essere usate insieme all'API audio legacy.

Le API audio di base sono:

-   [API Dispositivo multimediale (MMDevice).](mmdevice-api.md) I client usano questa API per enumerare i dispositivi endpoint audio nel sistema.
-   [Windows API (Audio Session API)](wasapi.md). I client usano questa API per creare e gestire flussi audio da e verso dispositivi endpoint audio.
-   [API DeviceTopology](devicetopology-api.md). I client usano questa API per accedere direttamente alle funzionalità topologiche (ad esempio, i controlli del volume e i multiplexer) che si trovano lungo i percorsi dei dati all'interno dei dispositivi hardware nelle schede audio.
-   [API EndpointVolume](endpointvolume-api.md). I client usano questa API per accedere direttamente ai controlli del volume nei dispositivi endpoint audio. Questa API viene usata principalmente dalle applicazioni che gestiscono flussi audio in modalità esclusiva.

Queste API supportano la nozione semplice di dispositivo endpoint, descritta in [Dispositivi endpoint audio.](audio-endpoint-devices.md)

Microsoft non prevede di rendere disponibili le API core audio descritte qui per l'uso con le versioni precedenti di Windows, tra cui Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 e Windows 98.

Questa panoramica contiene gli argomenti seguenti.



| **Argomento**                                                                                      | **Descrizione**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Novità delle API core audio in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Riepiloga le nuove funzionalità e i miglioramenti apportati alle API audio core                   |
| [File di intestazione e componenti di sistema](header-files-and-system-components.md)                   | Descrive i file di intestazione e i componenti di sistema per le API core audio.                 |
| [Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)       | Elenca gli esempi in Windows SDK che usano le API audio core.                        |




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API audio di base](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



