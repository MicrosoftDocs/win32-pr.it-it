---
description: In questo argomento viene descritto come visualizzare l'avanzamento del processo di stampa per l'utente e assegnare loro l'opzione per annullare un processo di stampa attualmente in corso.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Procedura: visualizzare lo stato di avanzamento del processo di stampa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311834"
---
# <a name="how-to-display-the-print-job-progress"></a>Procedura: visualizzare lo stato di avanzamento del processo di stampa

In questo argomento viene descritto come visualizzare l'avanzamento del processo di stampa per l'utente e assegnare loro l'opzione per annullare un processo di stampa attualmente in corso.

## <a name="overview"></a>Panoramica

Una routine della finestra di dialogo stato di stampa esegue in genere le funzioni seguenti.

-   Visualizza lo stato del processo di stampa per l'utente.
-   Avviare il thread di elaborazione stampa.
-   Consente di visualizzare un pulsante **Annulla** per consentire all'utente di arrestare un processo di stampa prima del completamento.

In modo rigoroso, l'unica cosa che la routine della finestra di dialogo stato di stampa deve eseguire è visualizzare l'avanzamento del processo di stampa. Tuttavia, poiché le altre due funzioni nell'elenco precedente sono strettamente correlate, sono state incluse anche in questo modulo.

## <a name="displaying-print-job-progress"></a>Visualizzazione dello stato del processo di stampa

Una procedura di stampa dello stato di avanzamento della finestra di dialogo gestisce i messaggi della finestra seguenti.

-   **\_INITDIALOG WM**

    Inizializza i controlli utilizzati dalla finestra di dialogo.

-   **\_cursore WM**

    Imposta il cursore su un puntatore quando l'utente è in grado di annullare un processo di stampa e al cursore di attesa quando il processo di stampa si trova in un punto in cui non può essere annullato.

-   **stampa \_ \_ inizio stampa \_ utente**

    Imposta i parametri dell'indicatore di stato per il processo di stampa e crea il thread di stampa per avviare l'elaborazione del processo di stampa.

    Si tratta di un messaggio di finestra specifico dell'applicazione.

-   **\_comando WM-IDCANCEL**

    Imposta l'evento Cancel per indicare al thread di elaborazione della stampa di annullare il processo di stampa.

-   **\_ \_ aggiornamento dello stato di stampa dell'utente \_**

    Aggiorna l'indicatore di stato e il testo dello stato per visualizzare lo stato corrente del processo di stampa.

    Si tratta di un messaggio di finestra specifico dell'applicazione.

-   **\_chiusura stampa \_ utente**

    Imposta il testo dello stato di chiusura nella finestra di dialogo stato per indicare che il processo di stampa è in fase di chiusura.

    Si tratta di un messaggio di finestra specifico dell'applicazione.

-   **\_stampa utente \_ completata**

    Visualizza il messaggio "stampa processo completato" per l'utente e rilascia handle ed eventi utilizzati in questo processo di stampa.

    Si tratta di un messaggio di finestra specifico dell'applicazione.

 

 



