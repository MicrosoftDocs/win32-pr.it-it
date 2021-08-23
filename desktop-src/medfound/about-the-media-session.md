---
description: Informazioni sulla sessione multimediale
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Informazioni sulla sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68816f4c9b9468de2e687a7d00087c5232cc5d24509c9166c5f04c7c0370f6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035639"
---
# <a name="about-the-media-session"></a>Informazioni sulla sessione multimediale

La sessione multimediale espone [**l'interfaccia IMFMediaSession.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) Esistono due modi per creare la sessione multimediale, a seconda che l'applicazione supporti il contenuto protetto:

-   Se l'applicazione non supporta contenuto protetto, è possibile creare la sessione multimediale chiamando [**MFCreateMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) Questa funzione crea la sessione multimediale all'interno del processo dell'applicazione.
-   Per supportare il contenuto protetto, creare la sessione multimediale chiamando [**MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) Questa funzione crea la sessione multimediale all'interno del processo PMP (Protected Media Path). L'applicazione riceve un puntatore a un oggetto proxy che effettua il marshalling delle chiamate al metodo attraverso il limite del processo. Si noti che la sessione multimediale PMP può essere usata per riprodurre contenuto non crittografato, nonché contenuto protetto.

Qualsiasi applicazione che usa la sessione multimediale seguirà questi passaggi generali:

1.  Creare una topologia.
2.  Accodare la topologia nella sessione multimediale chiamando [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).
3.  Controllare il flusso di dati chiamando [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)o [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
4.  Prima della chiusura dell'applicazione, chiamare [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la sessione multimediale.
5.  Arrestare tutte le origini multimediali create dall'applicazione chiamando [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
6.  Arrestare la sessione multimediale chiamando [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

Quando si usa la sessione multimediale, l'applicazione non deve avviare, sospendere o arrestare direttamente l'origine multimediale. Tutte le modifiche di stato devono essere avviate chiamando [**i metodi IMFMediaSession.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) Le modifiche di stato nell'origine multimediale vengono gestite dalla sessione multimediale.

Molti altri dettagli dipenderanno dalla funzionalità specifica dell'applicazione.

## <a name="protected-content"></a>Contenuto protetto

Per riprodurre contenuto protetto, è necessario creare la sessione multimediale all'interno del percorso del supporto protetto (PMP) chiamando [**MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) Questa funzione crea un'istanza della sessione multimediale all'interno del PMP e restituisce un puntatore a un oggetto proxy che effettua il marshalling delle interfacce attraverso il limite del processo.

Per la maggior parte dei casi, l'uso della sessione multimediale all'interno del PMP è trasparente per l'applicazione. Tuttavia, l'applicazione potrebbe dover richiamare determinate azioni che consentono all'utente di riprodurre il contenuto. Ad esempio, l'utente potrebbe dover ottenere una licenza DRM. Media Foundation definisce un meccanismo generico per queste azioni usando [**l'interfaccia IMFContentEnabler.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)

Per altre informazioni, vedere i seguenti argomenti:

-   [Percorso del supporto protetto](protected-media-path.md)
-   [Come riprodurre file multimediali protetti](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>Orologio di presentazione

La sessione multimediale gestisce tutti gli aspetti dell'orologio di presentazione:

-   Creazione dell'orologio di presentazione.

-   Selezione dell'origine ora.

-   Notifica dell'orologio ai sink multimediali

-   Avvio, arresto e sospensione dell'orologio in base alle esigenze.

-   Arresto dell'orologio.

Per ottenere un puntatore all'orologio della presentazione, chiamare [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) nella sessione multimediale. L'orologio di presentazione non restituisce un'ora valida fino a quando la sessione multimediale non invia [l'evento MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag MF TOPOSTATUS \_ READY. Fino ad allora, **GetClock** restituisce MF \_ E CLOCK NO TIME \_ \_ \_ \_ SOURCE.

Un'applicazione che usa la sessione multimediale non deve mai avviare, arrestare o sospendere l'orologio della presentazione; modificare la frequenza di clock; o arrestare l'orologio.

Quando l'applicazione chiama [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), la sessione multimediale avvia l'orologio della presentazione con un'ora di inizio uguale alla posizione iniziale specificata nel **metodo Start.** Per altre informazioni sulla sessione multimediale, vedere [Sessione multimediale.](media-session.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 



