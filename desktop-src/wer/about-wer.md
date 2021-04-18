---
title: Informazioni su WER
description: Segnalazione errori Windows (WER) è un'infrastruttura di feedback basata su eventi flessibile progettata per raccogliere informazioni sui problemi hardware e software che Windows è in grado di rilevare, segnalare le informazioni a Microsoft e fornire agli utenti le soluzioni disponibili. Per informazioni sui miglioramenti apportati a WER, vedere Novità di WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Segnalazione errori Windows Segnalazione errori Windows, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330903"
---
# <a name="about-wer"></a>Informazioni su WER

Segnalazione errori Windows (WER) è un'infrastruttura di feedback basata su eventi flessibile progettata per raccogliere informazioni sui problemi hardware e software che Windows è in grado di rilevare, segnalare le informazioni a Microsoft e fornire agli utenti le soluzioni disponibili. Per informazioni sui miglioramenti apportati a WER, vedere Novità di [wer](what-s-new-in-wer.md).

A partire da Windows Vista, Windows fornisce un arresto anomalo, nessuna risposta e segnalazione errori del kernel per impostazione predefinita senza richiedere modifiche all'applicazione. Le applicazioni usano invece l'API WER per generare segnalazioni di errori per problemi specifici dell'applicazione che non sono correlati a arresti anomali, non risposte o errori del kernel.

Per generare segnalazioni di errori per problemi specifici dell'applicazione, è necessario che l'applicazione crei una breve descrizione del problema utilizzando alcune informazioni di base denominate *parametri del report*. I parametri del report includono informazioni quali il nome dell'applicazione, la versione dell'applicazione, il nome del modulo, la versione del modulo e il codice di errore. La combinazione di questi parametri del report descrive un problema univoco.

Quando WER verifica la presenza di una soluzione, comunica con il server WER in Microsoft chiedendo prima se il problema è già noto. Il server risponde in uno dei modi seguenti:

-   Se il problema è noto ed è presente una soluzione, il server invia la soluzione al computer client e WER Visualizza le informazioni all'utente.
-   Se il problema viene esaminato, il server può inviare una risposta che indica lo stato. Se lo sviluppatore necessita di ulteriori informazioni per risolvere il problema, il server richiede informazioni aggiuntive da WER e WER chiede all'utente l'autorizzazione per l'invio di queste informazioni.
-   Se il problema non è noto, il server crea un problema affinché uno sviluppatore analizzi e invii una risposta che indica lo stato.

Con questo processo, WER raccoglie ulteriori informazioni, se necessario, o invia una soluzione all'utente, se disponibile. In Windows Vista, l'utente può accedere a **segnalazioni di problemi e soluzioni** in qualsiasi momento per visualizzare le soluzioni disponibili, verificare se sono disponibili nuove soluzioni o gestire le altre impostazioni e report di wer. In Windows 7, le **soluzioni e i report sui problemi** sono ora chiamati **centro operativo**. Fare clic su **Start** e immettere "View" in **Cerca programmi e file** , quindi selezionare **Visualizza tutti i report sui** problemi, **Visualizza cronologia affidabilità** o **Visualizza soluzioni ai problemi**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Segnalazione errori Windows](windows-error-reporting.md)
</dt> </dl>

 

 




