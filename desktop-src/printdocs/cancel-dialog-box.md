---
description: In questo argomento viene descritto come visualizzare lo stato del processo di stampa all'utente e fornire all'utente la possibilità di annullare un processo di stampa attualmente in corso.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Procedura: Visualizzare lo stato del processo di stampa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec61c07844262b258fb052d08d8d20e9285a8f7e9bb83808ea61eddaf32f3a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950611"
---
# <a name="how-to-display-the-print-job-progress"></a>Procedura: Visualizzare lo stato del processo di stampa

In questo argomento viene descritto come visualizzare lo stato del processo di stampa all'utente e fornire all'utente la possibilità di annullare un processo di stampa attualmente in corso.

## <a name="overview"></a>Panoramica

Una procedura della finestra di dialogo dello stato di stampa esegue in genere le funzioni seguenti.

-   Visualizzare lo stato del processo di stampa all'utente.
-   Avviare il thread di elaborazione della stampa.
-   Visualizzare un **pulsante Annulla** in modo che l'utente possa arrestare un processo di stampa prima del completamento.

In senso stretto, l'unica operazione che deve essere eseguita dalla procedura della finestra di dialogo dello stato di stampa è la visualizzazione dello stato del processo di stampa all'utente. Tuttavia, poiché le altre due funzioni nell'elenco precedente sono strettamente correlate, sono state incluse anche in questo modulo.

## <a name="displaying-print-job-progress"></a>Visualizzazione dello stato del processo di stampa

Una routine della finestra di dialogo dello stato di stampa gestisce i messaggi della finestra seguenti.

-   **WM \_ INITDIALOG**

    Inizializza i controlli utilizzati dalla finestra di dialogo.

-   **WM \_ SETCURSOR**

    Imposta il cursore su un puntatore quando l'utente è in grado di annullare un processo di stampa e sul cursore di attesa quando il processo di stampa si trova in un punto in cui non può essere annullato.

-   **AVVIO \_ STAMPA UTENTE \_ \_ STAMPA**

    Imposta i parametri dell'indicatore di stato per il processo di stampa e crea il thread di stampa per avviare l'elaborazione del processo di stampa.

    Si tratta di un messaggio di finestra specifico dell'applicazione.

-   **COMANDO WM \_ - IDCANCEL**

    Imposta l'evento di annullamento per indicare al thread di elaborazione di stampa di annullare il processo di stampa.

-   **AGGIORNAMENTO STATO \_ \_ STAMPA \_ UTENTE**

    Aggiorna l'indicatore di stato e il testo dello stato per mostrare lo stato corrente del processo di stampa.

    Si tratta di un messaggio di finestra specifico dell'applicazione.

-   **CHIUSURA \_ STAMPA \_ UTENTE**

    Imposta il testo dello stato di chiusura nella finestra di dialogo di stato per indicare che il processo di stampa è in chiusura.

    Si tratta di un messaggio di finestra specifico dell'applicazione.

-   **STAMPA \_ UTENTE \_ COMPLETATA**

    Visualizza il messaggio "Processo di stampa completato" all'utente e rilascia gli handle e gli eventi utilizzati in questo processo di stampa.

    Si tratta di un messaggio di finestra specifico dell'applicazione.

 

 



