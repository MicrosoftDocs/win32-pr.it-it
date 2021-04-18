---
description: Questa esercitazione illustra come riprodurre file multimediali usando l'oggetto della sessione multimediale.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Come riprodurre file multimediali con Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104561899"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>Come riprodurre file multimediali con Media Foundation

Questa esercitazione illustra come riprodurre file multimediali usando l'oggetto della [sessione multimediale](media-session.md) .

## <a name="prerequisites"></a>Prerequisiti

Prima di leggere questo argomento, è necessario avere familiarità con i concetti Media Foundation seguenti:

-   [Sessione multimediale](media-session.md)
-   [Resolver di origine](source-resolver.md)
-   [Topologie](topologies.md)
-   [Generatori di eventi multimediali](media-event-generators.md)
-   [Descrittori di presentazione](presentation-descriptors.md)

> [!Note]  
> In questo argomento non viene descritto come riprodurre file protetti da Digital Rights Management (DRM). Per informazioni su DRM in Microsoft Media Foundation, vedere [How to Play Protected Media Files](how-to-play-protected-media-files.md).

 

## <a name="overview"></a>Panoramica

Gli oggetti seguenti vengono usati per riprodurre un file multimediale con la sessione multimediale:

-   Un' *origine multimediale* è un oggetto che analizza un file multimediale o un'altra origine dei dati multimediali. L'origine multimediale crea oggetti *flusso* per ogni flusso audio o video del file. I *decodificatori* convertono i dati multimediali codificati in audio e video non compressi.
-   Il *resolver di origine* crea un'origine multimediale da un URL.
-   Il [renderer video migliorato](enhanced-video-renderer.md) (EVR) esegue il rendering dei video sullo schermo.
-   Il [renderer di streaming audio](streaming-audio-renderer.md) (SAR) esegue il rendering dell'audio in un altoparlante o in un altro dispositivo di output audio.
-   Una *topologia* definisce il flusso dei dati dall'origine multimediale a EVR e SAR.
-   La *sessione multimediale* controlla il flusso di dati e invia eventi di stato all'applicazione. La figura seguente illustra questo processo.

![diagramma che mostra la riproduzione mediante la sessione multimediale](images/session-playback.gif)

Di seguito è riportata una descrizione generale dei passaggi necessari per riprodurre un file multimediale tramite la sessione multimediale:

1.  Chiamare la funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare la piattaforma Media Foundation.
2.  Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare una nuova istanza della sessione multimediale.
3.  Usare il resolver di origine per creare un'origine multimediale. Per ulteriori informazioni, vedere [using the source resolver](using-the-source-resolver.md).
4.  Creare una topologia che connette l'origine multimediale a EVR e SAR. In questo passaggio, l'applicazione crea una topologia *parziale* che non include i decodificatori. Per ulteriori informazioni, vedere [creazione di topologie di riproduzione](creating-playback-topologies.md).
5.  Chiamare [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.
6.  Usare l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) per ottenere gli eventi dalla sessione multimediale.
7.  Chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per avviare la riproduzione. Una volta avviata la riproduzione, è possibile sospenderla chiamando [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)o arrestarla chiamando [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
8.  Quando l'applicazione viene chiusa, rilasciare le risorse:

    1.  Chiamare [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la sessione multimediale. Questo metodo è asincrono. Al termine, la sessione multimediale Invia un evento [MESessionClosed](mesessionclosed.md) . Quindi, è possibile eseguire i passaggi rimanenti.
    2.  Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) per arrestare l'origine del supporto.
    3.  Chiamare [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) per arrestare la sessione multimediale.
    4.  Chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare la piattaforma Media Foundation.

Le sezioni seguenti mostrano un esempio di codice completo:

-   [Passaggio 1: dichiarare la classe CPlayer](step-1--declare-the-cplayer-class.md)
-   [Passaggio 2: creare l'oggetto CPlayer](step-2--create-the-cplayer-object.md)
-   [Passaggio 3: aprire un file multimediale](step-3--open-a-media-file.md)
-   [Passaggio 4: creare la sessione multimediale](step-4--create-the-media-session.md)
-   [Passaggio 5: gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md)
-   [Passaggio 6: controllare la riproduzione](step-6--control-playback.md)
-   [Passaggio 7: arrestare la sessione multimediale](step-7--shut-down-the-media-session.md)
-   [Esempio di riproduzione della sessione multimediale](media-session-playback-example.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> </dl>

 

 



