---
description: Come controllare gli Stati di presentazione
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Come controllare gli Stati di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308765"
---
# <a name="how-to-control-presentation-states"></a>Come controllare gli Stati di presentazione

La sessione multimediale fornisce il controllo del trasporto, ad esempio la modifica degli Stati di presentazione (riproduzione, pausa e arresto in uno scenario di riproduzione in stile playlist). In questo argomento vengono descritti i metodi della sessione multimediale che devono essere chiamati da un'applicazione per modificare lo stato di riproduzione.

Nella tabella seguente vengono illustrate le transizioni di stato di presentazione valide.



| Transizione dello stato | Descrizione                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| Pausa di riproduzione > | Il clock di presentazione si blocca.                                                            |
| Play-> stop  | Il clock di presentazione viene reimpostato.                                                           |
| Pausa-> riproduzione | Il clock di presentazione riprende dal momento in cui si è bloccato durante il ciclo di riproduzione per sospendere la transizione. |
| Sospendi-> arrestare | Il clock di presentazione viene reimpostato.                                                           |
| Stop-> Play  | Il clock di presentazione inizia dall'inizio della presentazione.                      |
| Interrompi-> pausa | Non consentiti.                                                                               |



 

## <a name="to-change-presentation-states"></a>Per modificare gli Stati di presentazione

-   Chiamare il metodo [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) per sospendere la riproduzione.

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    Prima di chiamare questo metodo, l'applicazione deve chiamare il metodo [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) per individuare se l'origine supporto supporta lo stato di sospensione. In caso contrario, questo metodo restituisce **MFSESSIONCAP \_ pause** nel parametro *pdwCaps* .

    Pausa interrompe temporaneamente la sessione multimediale, il clock di presentazione e il sink di flusso per la presentazione corrente. Una volta completata la chiamata, l'applicazione riceve un evento [MESessionPaused](mesessionpaused.md) .

-   Chiamare il metodo [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) per arrestare la riproduzione.

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    Questo metodo arresta la sessione multimediale interrompendo l'origine del supporto, gli orologi corrispondenti e i sink di flusso. Se la sessione multimediale controlla l' [origine del sequencer](sequencer-source.md), le origini native sottostanti vengono arrestate dall'origine del sequencer. Dopo che la sessione multimediale è stata arrestata, l'applicazione riceve un evento [MESessionStopped](mesessionstopped.md) .

-   Chiamare il metodo [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per avviare la riproduzione o cercare una nuova posizione.

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    Questo metodo avvia la sessione multimediale dagli Stati pause e stop. La sessione multimediale è responsabile della configurazione del flusso di dati nella pipeline. Questo metodo indica alla sessione multimediale di avviare il clock di presentazione. Dopo questa chiamata, la sessione multimediale Invia un evento [MESessionStarted](mesessionstarted.md) all'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 



