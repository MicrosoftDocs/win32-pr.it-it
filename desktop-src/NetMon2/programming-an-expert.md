---
description: Il Network Monitor SDK include le funzioni e il codice di esempio necessari per compilare esperti. Tuttavia, è anche possibile usare gli strumenti esistenti, incluso un editor di finestre.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programmazione di un esperto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131462"
---
# <a name="programming-an-expert"></a>Programmazione di un esperto

Il Network Monitor SDK include le funzioni e il codice di esempio necessari per compilare esperti. Tuttavia, è anche possibile usare gli strumenti esistenti, incluso un editor di finestre.

## <a name="minimum-requirements-to-run-an-expert"></a>Requisiti minimi per l'esecuzione di un esperto

Nella tabella seguente sono elencati i punti di ingresso della DLL e le funzioni esperte che è necessario utilizzare per compilare un esperto.



| Nome                                                 | Type               | Obbligatorio?                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [**DllMain**](dllmain-expert.md)                    | Funzione voce DLL | Sì                                             |
| [**Registra esperto**](register-expert.md)           | Funzione voce DLL | Sì                                             |
| [**Correre**](run.md)                                   | Funzione voce DLL | Sì                                             |
| [**Configurare**](configure.md)                       | Funzione voce DLL | Solo se l'esperto fornisce la configurazione utente. |
| [**ExpertIndicateStatus**](expertindicatestatus.md) | Funzione Expert    | Sì                                             |
| [**ExpertSubmitEvent**](expertsubmitevent.md)       | Funzione Expert    | Sì                                             |



 

Esaminare gli argomenti di riferimento per esperti e parser nell'SDK di Network Monitor per aggiornare il codice sorgente e quindi usare il codice di esempio e le procedure fornite negli argomenti seguenti:

-   [Creazione di un esperto](building-an-expert.md)
-   [Installazione di un esperto](installing-an-expert-to-network-monitor-2-1.md)
-   [Debug di un esperto](debugging-an-expert.md)

Per le DLL di esperti è richiesta la convenzione di chiamata C, non C++, perché le funzioni vengono chiamate tramite puntatori a funzione tramite un overlay. Tramite un set di funzioni esperte specializzate, l'esperto può accedere ai frame nell'acquisizione. L'esperto può utilizzare la maggior parte delle Network Monitor API per modificare i dati restituiti. Quando un esperto trova le informazioni da inviare all'utente, le informazioni vengono composte in una struttura di dati degli eventi e inviate a Network Monitor, che quindi Visualizza le informazioni in una finestra di output esperta. L'esperto deve aggiornare periodicamente Network Monitor con informazioni sullo stato di completamento percentuale, fornito dalla funzione [**ExpertIndicateStatus**](expertindicatestatus.md) .

Le funzioni esportate dell'esperto vengono chiamate come segue:

-   Quando Network Monitor crea l'elenco di esperti da presentare all'utente, Network Monitor chiama la funzione [**Register Expert**](register-expert.md) .
-   Dopo la chiamata a **Register**, se l'esperto è configurabile, Network Monitor chiama la funzione [**Configure**](configure.md) .
-   Quando l'utente Network Monitor fa clic su **Esegui esperto**, Network Monitor chiama la funzione [**Run**](run.md) .

Quando gli esperti analizzano i frame richiesti e individuano un problema, usano [**ExpertSubmitEvent**](expertsubmitevent.md) per inviare un evento che contiene informazioni sul problema. Network Monitor distribuisce l'evento al Visualizzatore eventi standard (condiviso) o (se l'esperto esegue la registrazione) a una Visualizzatore eventi privata.

 

 



