---
description: In questa sezione viene descritto come stampare da un programma Windows nativo.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Procedura: Stampare da un programma Windows dati'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999f112285dfff389583b15f7c7c2913a3e125bc58713e2ba5f18973aa6e1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971340"
---
# <a name="how-to-print-from-a-windows-program"></a>Procedura: Stampare da un programma Windows dati

In questa sezione viene descritto come stampare da un programma Windows nativo.

## <a name="overview"></a>Panoramica

La stampa è in genere parte integrante di un programma Windows nativo. Pertanto, non è una funzionalità che è possibile aggiungere facilmente dopo aver scritto il programma. Detto questo, se il programma è progettato per l'uso di documenti XPS, non sarà necessario molto, se presente, codice aggiuntivo per eseguire il rendering del contenuto del documento per la stampa. I documenti XPS dell'applicazione possono essere inviati direttamente a una stampante con un driver della stampante XPSDrv.

Usare [l'API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) per creare il contenuto del documento e l'API di stampa [XPS](xps-printing.md) per inviare il contenuto del documento alla stampante. L'API di stampa XPS elabora il contenuto del documento per la stampante di destinazione. Se la stampante selezionata dispone di un driver della stampante XPSDrv, il documento verrà inviato alla stampante senza alcuna conversione aggiuntiva. Se la stampante selezionata dispone di un driver della stampante basato su GDI, il programma può anche inviare il contenuto alla stampante e l'API di stampa XPS converte il contenuto del documento in modo che sia compatibile con il driver della stampante basato su GDI. In entrambi i casi, l'elaborazione eseguita dall'applicazione è la stessa.

## <a name="printing-tasks"></a>Attività di stampa

Negli argomenti seguenti vengono descritti i passaggi di base per la stampa del contenuto del programma.

1.  **Raccogliere informazioni sul processo di stampa dall'utente.**

    In genere, un utente avvia un processo di stampa quando seleziona l'opzione di stampa da un menu e il programma visualizza una finestra di dialogo di stampa per raccogliere i dettagli del processo di stampa. L'utente seleziona in genere la stampante, il numero di copie e i dettagli di configurazione della stampante, ad esempio stampa fronte retro e graffatura.

    Per informazioni su come eseguire questa operazione, vedere Procedura: Raccogliere [informazioni sui processi di stampa dall'utente.](preparing-to-print.md)

2.  **Indicatore di stato di creazione.**

    Un indicatore di stato fornisce all'utente commenti e suggerimenti sull'avanzamento del processo di stampa. L'indicatore di stato può essere un indicatore di  stato che fa parte di una finestra di dialogo che include il pulsante Annulla per il processo oppure un indicatore di stato nella barra di stato nella parte inferiore della finestra principale.

    Per informazioni sul funzionamento dell'indicatore di stato, [vedere Procedura: Visualizzare lo stato del processo di stampa.](cancel-dialog-box.md)

    Per altre idee su come visualizzare lo stato di avanzamento [](/windows/desktop/windows-application-ui-development) del processo di stampa, vedere le informazioni nelle linee guida per lo sviluppo dell'interfaccia utente Windows'applicazione.

3.  **Avviare il thread di stampa.**

    Dopo che il programma ha raccolto le informazioni sul processo di stampa dall'utente, può avviare il thread di stampa per eseguire l'elaborazione effettiva del documento per la stampa.

    Per informazioni sul thread di stampa, vedere [Procedura: Avviare e arrestare un thread di stampa.](how-to--start-and-stop-a-printing-thread.md)

4.  **Eseguire il rendering dei dati del processo di stampa.**

    Il thread di stampa esegue il rendering dei dati del documento per la stampa. È consigliabile suddividere questa elaborazione in passaggi di elaborazione discreti in modo che l'utente possa interrompere l'elaborazione e annullare il processo, nonché non consentire al thread di elaborazione di bloccare altri thread e processi.

    Per informazioni sul rendering dei dati del processo di stampa, vedere [Procedura: Eseguire il rendering dei dati del processo di stampa.](how-to--render-the-print-job-data.md)

5.  **Monitorare lo stato del processo di stampa.**

    Quando viene eseguito ogni passaggio di elaborazione, aggiornare l'indicatore di stato per informare l'uso. Calcolare i passaggi di elaborazione per completare il processo richiesto e quindi aggiornare l'indicatore di stato durante l'esecuzione di tali passaggi.

6.  **Chiudere il processo di stampa e terminare il thread di stampa.**

    Dopo che il programma ha inviato il processo di stampa alla stampante o se l'utente ha annullato il processo di stampa, è necessario chiudere il processo di stampa e rilasciare le risorse utilizzate dal processo di stampa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura: Raccogliere informazioni sul processo di stampa dall'utente](preparing-to-print.md)
</dt> </dl>

 

 
