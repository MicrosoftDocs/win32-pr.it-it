---
description: Questa esercitazione illustra come riprodurre file multimediali usando l'oggetto Sessione multimediale.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Come riprodurre file multimediali con Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ba44212227be87e78d29c60a76bc3acdc2b1483b1029c62dd288bb7434b2a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878861"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>Come riprodurre file multimediali con Media Foundation

Questa esercitazione illustra come riprodurre file multimediali usando [l'oggetto Sessione](media-session.md) multimediale.

## <a name="prerequisites"></a>Prerequisiti

Prima di leggere questo argomento, è necessario avere familiarità con i concetti Media Foundation seguenti:

-   [Sessione multimediale](media-session.md)
-   [Resolver di origine](source-resolver.md)
-   [Topologie](topologies.md)
-   [Generatori di eventi multimediali](media-event-generators.md)
-   [Descrittori di presentazione](presentation-descriptors.md)

> [!Note]  
> In questo argomento non viene descritto come riprodurre file protetti da DRM (Digital Rights Management). Per informazioni su DRM in Microsoft Media Foundation, vedere [Come riprodurre file multimediali protetti.](how-to-play-protected-media-files.md)

 

## <a name="overview"></a>Panoramica

Gli oggetti seguenti vengono usati per riprodurre un file multimediale con la sessione multimediale:

-   *Un'origine multimediale* è un oggetto che analizza un file multimediale o un'altra origine di dati multimediali. L'origine *multimediale crea* oggetti flusso per ogni flusso audio o video nel file. *I decodificatori* convertono i dati multimediali codificati in video e audio non compressi.
-   Il *sistema di risoluzione dell'origine* crea un'origine multimediale da un URL.
-   EVR [(Enhanced Video Renderer)](enhanced-video-renderer.md) esegue il rendering del video sullo schermo.
-   Il [renderer audio di streaming](streaming-audio-renderer.md) (SAR) esegue il rendering dell'audio in un altoparlante o in un altro dispositivo di output audio.
-   Una *topologia definisce* il flusso di dati dall'origine multimediale all'EVR e alla SAR.
-   La *sessione multimediale* controlla il flusso di dati e invia eventi di stato all'applicazione. La figura seguente illustra questo processo.

![Diagramma che mostra la riproduzione tramite la sessione multimediale](images/session-playback.gif)

Di seguito è riportata una descrizione generale dei passaggi necessari per riprodurre un file multimediale usando la sessione multimediale:

1.  Chiamare la [**funzione MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare la Media Foundation piattaforma.
2.  Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare una nuova istanza della sessione multimediale.
3.  Usare il sistema di risoluzione di origine per creare un'origine multimediale. Per altre informazioni, vedere [Uso del resolver di origine](using-the-source-resolver.md).
4.  Creare una topologia che connette l'origine multimediale all'EVR e alla SAR. In questo passaggio l'applicazione crea *una* topologia parziale che non include i decodificatori. Per altre informazioni, vedere [Creazione di topologie di riproduzione](creating-playback-topologies.md).
5.  Chiamare [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.
6.  Usare [**l'interfaccia IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) per ottenere eventi dalla sessione multimediale.
7.  Chiamare [**IMFMediaSession::Start per**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) avviare la riproduzione. Dopo l'avvio della riproduzione, è possibile sospenderla chiamando [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)o arrestarla chiamando [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
8.  Quando l'applicazione viene chiusa, rilasciare le risorse:

    1.  Chiamare [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la sessione multimediale. Questo metodo è asincrono. Al termine, la sessione multimediale invia un [evento MESessionClosed.](mesessionclosed.md) È quindi possibile eseguire i passaggi rimanenti.
    2.  Chiamare [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) per arrestare l'origine multimediale.
    3.  Chiamare [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) per arrestare la sessione multimediale.
    4.  Chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare la Media Foundation piattaforma.

Le sezioni seguenti illustrano un esempio di codice completo:

-   [Passaggio 1: Dichiarare la classe CPlayer](step-1--declare-the-cplayer-class.md)
-   [Passaggio 2: Creare l'oggetto CPlayer](step-2--create-the-cplayer-object.md)
-   [Passaggio 3: Aprire un file multimediale](step-3--open-a-media-file.md)
-   [Passaggio 4: Creare la sessione multimediale](step-4--create-the-media-session.md)
-   [Passaggio 5: Gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md)
-   [Passaggio 6: Controllare la riproduzione](step-6--control-playback.md)
-   [Passaggio 7: Arrestare la sessione multimediale](step-7--shut-down-the-media-session.md)
-   [Esempio di riproduzione di sessioni multimediali](media-session-playback-example.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> </dl>

 

 



