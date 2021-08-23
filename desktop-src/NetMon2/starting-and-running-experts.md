---
description: Facendo clic su Esegui esperti nella finestra Esperti dell'interfaccia utente Network Monitor vengono avviati gli esperti selezionati per il file di acquisizione e viene chiamata la funzione Esegui. All'avvio, l'esperto analizza il file di acquisizione usando diverse funzioni frame di esperti.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Esperti di avvio ed esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc85ba39c393ac253ca688a826bc77747c8d17bea29b089250a63f6f833066c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555323"
---
# <a name="starting-and-running-experts"></a>Esperti di avvio ed esecuzione

Facendo **clic su Esegui esperti** nella finestra Esperti dell'interfaccia utente Network Monitor vengono avviati gli esperti selezionati per il file di acquisizione e viene chiamata la [**funzione**](run.md) Esegui. All'avvio, l'esperto analizza il file di acquisizione usando diverse funzioni frame di esperti.

La [**funzione ExpertIndicateStatus**](expertindicatestatus.md) fornisce informazioni sullo stato dell'esperto. Quando si esegue un esperto con Network Monitor, nella finestra Visualizzazione stato esperto vengono visualizzate informazioni sullo stato aggiornate periodicamente (dal completamento da 0 a 100%).

![Finestra di visualizzazione dello stato dell'esperto](images/exview.png)

L'esperto è attivo fino a quando i dati non completano il passaggio del file di acquisizione. Al termine del passaggio, viene visualizzata Visualizzatore eventi finestra di dialogo. Le informazioni in questa finestra dipendono dal tipo di esperto che ha analizzato i dati. La figura seguente mostra una visualizzazione Esperto di distribuzione delle proprietà, che riepiloga i dati del frame analizzati dall'esperto.

![visualizzazione esperta della distribuzione delle proprietà](images/exview1.png)

Un secondo report (non visualizzato) riepiloga i risultati dell'esperto di Transmission Control Protocol (TCP) Retransmit.

È anche possibile:

-   Creare una voce per una pagina di riferimento eventi (ERP) che consiglia all'utente di problemi o condizioni rilevate (come illustrato nella finestra Analisi).
-   Creare voci per correzioni suggerite o dati esplicativi che forniscono informazioni aggiuntive (come illustrato nella finestra Risoluzione).

Dopo che l'esperto ha completato l'attività, Network Monitor l'esperto dalla memoria attiva. Gli esperti devono usare le funzioni di memoria protetta incluse in Platform Software Development Kit (SDK); queste funzioni puliscono la memoria se gli esperti hanno esito negativo in fase di esecuzione.

 

 



