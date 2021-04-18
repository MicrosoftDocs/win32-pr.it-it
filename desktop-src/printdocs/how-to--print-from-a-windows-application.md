---
description: In questa sezione viene descritto come stampare da un programma Windows nativo.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Procedura: stampare da un programma Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318378"
---
# <a name="how-to-print-from-a-windows-program"></a>Procedura: stampare da un programma Windows

In questa sezione viene descritto come stampare da un programma Windows nativo.

## <a name="overview"></a>Panoramica

La stampa è in genere parte integrante di un programma Windows nativo. Pertanto, non è una funzionalità che è possibile aggiungere facilmente dopo aver scritto il programma. Detto questo, se il programma è progettato per l'utilizzo di documenti XPS, non sarà necessario molto altro codice aggiuntivo per eseguire il rendering del contenuto del documento per la stampa. I documenti XPS dell'applicazione possono essere inviati direttamente a una stampante che dispone di un driver della stampante XPSDrv.

Utilizzare l' [API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) per creare il contenuto del documento e l' [API di stampa XPS](xps-printing.md) per inviare il contenuto del documento alla stampante. L'API di stampa XPS elabora il contenuto del documento per la stampante di destinazione. Se la stampante selezionata dispone di un driver della stampante XPSDrv, il documento verrà inviato alla stampante senza alcuna conversione aggiuntiva. Se la stampante selezionata dispone di un driver della stampante basato su GDI, il programma può anche inviare il contenuto alla stampante e l'API di stampa XPS converte il contenuto del documento in modo che sia compatibile con il driver della stampante basato su GDI. In entrambi i casi, l'elaborazione eseguita dall'applicazione è la stessa.

## <a name="printing-tasks"></a>Attività di stampa

Negli argomenti seguenti vengono descritti i passaggi di base per la stampa del contenuto del programma.

1.  **Raccoglie le informazioni sul processo di stampa dall'utente.**

    In genere, un utente avvia un processo di stampa quando seleziona l'opzione stampa da un menu e il programma visualizza una finestra di dialogo Stampa per raccogliere i dettagli del processo di stampa. L'utente in genere seleziona la stampante, il numero di copie e i dettagli di configurazione della stampante, ad esempio la stampa su due lati e la graffettatura.

    Per informazioni su come eseguire questa operazione, vedere [procedura: raccogliere informazioni sui processi di stampa dall'utente](preparing-to-print.md).

2.  **Creazione indicatore di stato.**

    Un indicatore di stato consente all'utente di ricevere commenti e suggerimenti sull'avanzamento del processo di stampa. L'indicatore di stato può essere una barra di stato che fa parte di una finestra di dialogo che include il pulsante **Annulla** per il processo oppure un indicatore di stato nella barra di stato nella parte inferiore della finestra principale.

    Per informazioni sul funzionamento dell'indicatore di stato, vedere [procedura: visualizzare lo stato di avanzamento del processo di stampa](cancel-dialog-box.md).

    Per ulteriori informazioni su come visualizzare lo stato di avanzamento del processo di stampa, vedere le informazioni nelle linee guida per [lo sviluppo dell'interfaccia utente delle applicazioni Windows](/windows/desktop/windows-application-ui-development) .

3.  **Avviare il thread di stampa.**

    Dopo che il programma ha raccolto le informazioni sul processo di stampa dall'utente, può avviare il thread di stampa per eseguire l'elaborazione effettiva del documento per la stampa.

    Per informazioni sul thread di stampa, vedere [procedura: avviare e arrestare un thread di stampa](how-to--start-and-stop-a-printing-thread.md).

4.  **Rendering dei dati del processo di stampa.**

    Il thread di stampa esegue il rendering dei dati del documento per la stampa. È consigliabile suddividere questa elaborazione in passaggi di elaborazione discreti in modo che l'utente possa interrompere l'elaborazione e annullare il processo, oltre a non consentire al thread di elaborazione di bloccare altri thread e processi.

    Per informazioni sul rendering dei dati del processo di stampa, vedere [procedura: eseguire il rendering dei dati dei processi di stampa](how-to--render-the-print-job-data.md).

5.  **Monitorare lo stato del processo di stampa.**

    Quando si esegue ogni passaggio di elaborazione, aggiornare l'indicatore di stato per informare l'utilizzo. Calcolare i passaggi di elaborazione per completare il processo richiesto e quindi aggiornare l'indicatore di stato durante l'esecuzione di questi passaggi.

6.  **Chiudere il processo di stampa e terminare il thread di stampa.**

    Dopo che il programma ha inviato il processo di stampa alla stampante o se l'utente ha annullato il processo di stampa, è necessario chiudere il processo di stampa e rilasciare le risorse utilizzate dal processo di stampa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura: raccogliere informazioni sui processi di stampa dall'utente](preparing-to-print.md)
</dt> </dl>

 

 
