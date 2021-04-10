---
description: Informazioni sulla sessione multimediale
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Informazioni sulla sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968846"
---
# <a name="about-the-media-session"></a>Informazioni sulla sessione multimediale

La sessione multimediale espone l'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) . Esistono due modi per creare la sessione multimediale, a seconda che l'applicazione supporti il contenuto protetto:

-   Se l'applicazione non supporta il contenuto protetto, è possibile creare la sessione multimediale chiamando [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession). Questa funzione crea la sessione multimediale all'interno del processo dell'applicazione.
-   Per supportare il contenuto protetto, creare la sessione multimediale chiamando [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Questa funzione crea la sessione multimediale all'interno del processo del percorso multimediale protetto (PMP). L'applicazione riceve un puntatore a un oggetto proxy che effettua il marshalling delle chiamate al metodo attraverso il limite di processo. Si noti che la sessione multimediale PMP può essere usata per riprodurre contenuto non crittografato, nonché per contenuti protetti.

Tutte le applicazioni che usano la sessione multimediale seguiranno i passaggi generali seguenti:

1.  Creare una topologia.
2.  Accodare la topologia nella sessione multimediale chiamando [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).
3.  Controllare il flusso di dati chiamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)o [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
4.  Prima di uscire dall'applicazione, chiamare [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la sessione multimediale.
5.  Arrestare le origini multimediali create dall'applicazione, chiamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
6.  Arrestare la sessione multimediale chiamando [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

Quando si usa la sessione multimediale, l'applicazione non deve avviare, sospendere o arrestare direttamente l'origine del supporto. Tutte le modifiche di stato devono essere avviate chiamando i metodi [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) . Le modifiche di stato nell'origine supporto vengono gestite dalla sessione multimediale.

Molti altri dettagli dipendono dalla funzionalità specifica dell'applicazione.

## <a name="protected-content"></a>Contenuto protetto

Per riprodurre contenuti protetti, è necessario creare la sessione multimediale all'interno del percorso multimediale protetto (PMP), chiamando [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Questa funzione crea un'istanza della sessione multimediale all'interno di PMP e restituisce un puntatore a un oggetto proxy che effettua il marshalling delle interfacce attraverso il limite del processo.

Nella maggior parte dei casi, l'uso della sessione multimediale all'interno del PMP è trasparente per l'applicazione. Tuttavia, l'applicazione potrebbe dover richiamare determinate azioni che consentono all'utente di riprodurre il contenuto. È ad esempio possibile che l'utente debba ottenere una licenza DRM. Media Foundation definisce un meccanismo generico per queste azioni usando l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .

Per altre informazioni, vedere i seguenti argomenti:

-   [Percorso supporto protetto](protected-media-path.md)
-   [Come riprodurre file multimediali protetti](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>Orologio di presentazione

La sessione multimediale gestisce tutti gli aspetti del clock di presentazione:

-   Creazione del clock di presentazione.

-   Selezione dell'origine dell'ora.

-   Notifica dei sink di supporto sull'orologio

-   Avvio, arresto e sospensione dell'orologio secondo necessità.

-   Chiusura dell'orologio.

Per ottenere un puntatore al clock di presentazione, chiamare [**IMFMediaSession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) nella sessione multimediale. Il clock di presentazione non restituisce un tempo valido fino a quando la sessione multimediale non invia l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag MF TOPOSTATUS \_ Ready. Fino ad allora, **getclock** restituisce MF \_ E \_ clock \_ No \_ time \_ source.

Un'applicazione che usa la sessione multimediale non deve mai avviare, arrestare o sospendere il clock di presentazione; modificare la frequenza di clock; o arrestare l'orologio.

Quando l'applicazione chiama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), la sessione multimediale avvia il clock di presentazione con un'ora di inizio uguale alla posizione iniziale specificata nel metodo **Start** . Per ulteriori informazioni sulla sessione multimediale, vedere [media session](media-session.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 



