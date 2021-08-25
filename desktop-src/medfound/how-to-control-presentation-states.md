---
description: Come controllare gli stati di presentazione
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Come controllare gli stati di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2148410527ecf966b10e605bbe4d6beb0ac3d515acd6895e4fc03e73564a72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942421"
---
# <a name="how-to-control-presentation-states"></a>Come controllare gli stati di presentazione

La sessione multimediale fornisce il controllo del trasporto, ad esempio la modifica degli stati di presentazione (Riproduzione, Sospensione e Arresto in uno scenario di riproduzione in stile playlist). Questo argomento descrive i metodi della sessione multimediale che un'applicazione deve chiamare per modificare lo stato di riproduzione.

La tabella seguente illustra le transizioni valide dello stato di presentazione.



| Transizione dello stato | Descrizione                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| Riproduci -> pausa | L'orologio della presentazione si blocca.                                                            |
| Riproduci -> arresta  | L'orologio della presentazione viene reimpostato.                                                           |
| Sospendi -> Riproduzione | L'orologio della presentazione riprende dal momento in cui è stato bloccato durante la transizione Riproduci in pausa. |
| Sospendi -> arresto | L'orologio della presentazione viene reimpostato.                                                           |
| Arresta -> riproduzione  | L'orologio della presentazione inizia dall'inizio della presentazione.                      |
| Arresta -> sospensione | Non consentiti.                                                                               |



 

## <a name="to-change-presentation-states"></a>Per modificare gli stati di presentazione

-   Chiamare il [**metodo IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) per sospendere la riproduzione.

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    Prima di chiamare questo metodo, l'applicazione deve chiamare il [**metodo IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) per determinare se l'origine multimediale supporta lo stato Pause. In caso contrario, questo metodo restituisce **MFSESSIONCAP \_ PAUSE** nel *parametro pdwCaps.*

    Sospendi arresta temporaneamente la sessione multimediale, l'orologio della presentazione e il sink di flusso per la presentazione corrente. Al termine della chiamata, l'applicazione riceve un [evento MESessionPaused.](mesessionpaused.md)

-   Chiamare il [**metodo IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) per arrestare la riproduzione.

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    Questo metodo arresta la sessione multimediale arrestando l'origine multimediale, i clock corrispondenti e i sink di flusso. Se la sessione multimediale controlla l'origine [sequencer,](sequencer-source.md)le origini native sottostanti vengono arrestate dall'origine sequencer. Dopo l'arresto della sessione multimediale, l'applicazione riceve un [evento MESessionStopped.](mesessionstopped.md)

-   Chiamare il [**metodo IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per avviare la riproduzione o cercare una nuova posizione.

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    Questo metodo avvia la sessione multimediale dagli stati Sospendi e Arresta. La sessione multimediale è responsabile della configurazione del flusso di dati nella pipeline. Questo metodo indica alla sessione multimediale di avviare l'orologio della presentazione. Dopo questa chiamata, Media Session invia un [evento MESessionStarted](mesessionstarted.md) all'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 



