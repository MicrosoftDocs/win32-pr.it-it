---
title: Funzioni di gestione riavvio
description: L'API di gestione riavvio usa le funzioni identificate nella tabella seguente.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Gestione riavvio riavvio gestione, informazioni di riferimento, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855966"
---
# <a name="restart-manager-functions"></a>Funzioni di gestione riavvio

L'API di gestione riavvio usa le funzioni identificate nella tabella seguente.



| Funzione                                           | Descrizione                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Modifica le azioni di arresto o riavvio.                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Avvia una nuova sessione di gestione riavvio.                                                                                                                                                        |
| [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Consente di unire il processo di un'applicazione a una sessione di gestione riavvio esistente.                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Termina la sessione di gestione riavvio.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Registra le risorse, ad esempio i nomi file, i nomi brevi del servizio o le strutture di [**\_ \_ processo univoche RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , in una sessione di gestione riavvio.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Usato dai programmi di installazione per ottenere un elenco di tutte le applicazioni interessate dalle risorse registrate e dal relativo stato corrente.                                                                              |
| [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Esegue una query sullo stato di arresto e riavvio delle modifiche già applicate.                                                                                                     |
| [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Avvia l'arresto di applicazioni e servizi.                                                                                                                                        |
| [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Rimuove le modifiche di arresto e riavvio che sono già state applicate.                                                                                                                   |
| [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Riavvia le applicazioni e i servizi che sono stati arrestati dalla funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) e che sono stati registrati per il riavvio usando **RegisterApplicationRestart**. |
| [**RmCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Annulla la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) corrente.                                                            |



 

 

 




