---
description: Facendo clic su Esegui esperti dalla finestra Experts dell'interfaccia utente di Network Monitor, vengono avviati gli esperti selezionati per il file di acquisizione e viene chiamata la funzione Run. Quando viene avviato, l'esperto analizza il file di acquisizione usando diverse funzioni di frame di esperti.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Avvio ed esecuzione di esperti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318966"
---
# <a name="starting-and-running-experts"></a>Avvio ed esecuzione di esperti

Facendo clic su **Esegui esperti** dalla finestra Experts dell'interfaccia utente di Network Monitor, vengono avviati gli esperti selezionati per il file di acquisizione e viene chiamata la funzione [**Run**](run.md) . Quando viene avviato, l'esperto analizza il file di acquisizione usando diverse funzioni di frame di esperti.

La funzione [**ExpertIndicateStatus**](expertindicatestatus.md) fornisce informazioni sullo stato dell'esperto. Quando si esegue un esperto con Network Monitor, nella finestra di visualizzazione stato esperto vengono visualizzate le informazioni aggiornate sullo stato aggiornate (dal 0 al 100% di completamento).

![finestra di visualizzazione stato esperto](images/exview.png)

L'esperto è attivo fino al completamento del passaggio dei dati tramite il file di acquisizione. Al termine del passaggio, viene visualizzata una finestra Visualizzatore eventi. Le informazioni contenute in questa finestra dipendono dal tipo di esperto che ha analizzato i dati. Nella figura seguente è illustrata una visualizzazione di esperti di distribuzione delle proprietà, che riepiloga i dati del frame analizzati dall'esperto.

![visualizzazione esperto distribuzione proprietà](images/exview1.png)

Un secondo report (non visualizzato) riepiloga i risultati dell'esperto di ritrasmissione del Transmission Control Protocol (TCP).

È anche possibile:

-   Creare una voce per una pagina di riferimento evento (ERP) che informa l'utente di condizioni o problemi rilevati (come illustrato nella finestra di analisi).
-   Creare voci per le correzioni suggerite o i dati esplicativi che forniscono informazioni aggiuntive (come illustrato nella finestra di risoluzione).

Dopo che l'esperto ha completato l'attività, Network Monitor rimuove l'esperto dalla memoria attiva. Gli esperti devono usare le funzioni di memoria protette incluse nel Software Development Kit (SDK) della piattaforma; Queste funzioni ripuliscono la memoria se gli esperti hanno esito negativo in fase di esecuzione.

 

 



