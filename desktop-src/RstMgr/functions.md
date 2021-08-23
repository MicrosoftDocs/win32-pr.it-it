---
title: Funzioni di Gestione riavvio
description: L'API Gestione riavvio usa le funzioni identificate nella tabella seguente.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Restart Manager Restart Mgr , reference, functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d628fcd5c1f6488d69152340dd76ae59ac27ea93b2ca157179a052883a26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010199"
---
# <a name="restart-manager-functions"></a>Funzioni di Gestione riavvio

L'API Gestione riavvio usa le funzioni identificate nella tabella seguente.



| Funzione                                           | Descrizione                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Modifica le azioni di arresto o riavvio.                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Avvia una nuova sessione di Gestione riavvio.                                                                                                                                                        |
| [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Aggiunge il processo di un'applicazione a una sessione di Gestione riavvio esistente.                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Termina la sessione di Gestione riavvio.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Registra le risorse, ad esempio nomi di file, nomi brevi del servizio o [**strutture RM \_ UNIQUE \_ PROCESS,**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) in una sessione di Gestione riavvio.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Usato dai programmi di installazione per ottenere un elenco di tutte le applicazioni interessate dalle risorse registrate e il relativo stato corrente.                                                                              |
| [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Esegue una query sullo stato delle modifiche di arresto e riavvio già applicate.                                                                                                     |
| [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Avvia l'arresto di applicazioni e servizi.                                                                                                                                        |
| [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Rimuove le modifiche di arresto e riavvio già applicate.                                                                                                                   |
| [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Riavvia le applicazioni e i servizi che sono stati arrestati dalla funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) e che sono stati registrati per il riavvio tramite **RegisterApplicationRestart**. |
| [**RmCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Annulla la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) corrente.                                                            |



 

 

 




