---
title: Uso di Gestione riavvio con un programma di installazione primario
description: La procedura seguente descrive come usare Gestione riavvio per arrestare e riavviare applicazioni e servizi. Quando si usa Gestione riavvio con un singolo programma di installazione, questo programma di installazione è anche il programma di installazione principale che controlla l'interfaccia utente.
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764086166fc895d44f1a555f453d2941487c5d999adfa8d38581a12f07c9c45c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010009"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>Uso di Gestione riavvio con un programma di installazione primario

La procedura seguente descrive come usare Gestione riavvio per arrestare e riavviare applicazioni e servizi. Quando si usa Gestione riavvio con un singolo programma di installazione, questo programma di installazione è anche il programma di installazione principale che controlla l'interfaccia utente.

**Per usare Gestione riavvio con un programma di installazione primario**

1.  Il programma di installazione chiama [**la funzione RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) per avviare la sessione di Gestione riavvio e ottenere un handle di sessione e una chiave.
2.  Il programma di installazione chiama [**la funzione RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) per registrare le risorse. Gestione riavvio può usare solo le risorse registrate per determinare quali applicazioni e servizi devono essere arrestati e riavviati. Tutte le risorse che possono essere interessate dall'installazione devono essere registrate con la sessione. Le risorse possono essere identificate in base al nome file, al nome breve del servizio o a una [**struttura RM \_ UNIQUE \_ PROCESS.**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process)
3.  Il programma di installazione chiama la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) per ottenere una matrice di strutture [**RM \_ PROCESS \_ INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) che elenca tutte le applicazioni e i servizi che devono essere arrestati e riavviati.

    Se il valore del *parametro lpdwRebootReason* restituito dalla funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) è diverso da zero, Gestione riavvio non è in grado di liberare una risorsa registrata dall'arresto di un'applicazione o di un servizio. In questo caso, è necessario un arresto e un riavvio del sistema per continuare l'installazione. Il programma di installazione deve richiedere all'utente un'azione, arrestare programmi o servizi o pianificare l'arresto e il riavvio del sistema.

    Se il valore del *parametro lpdwRebootReason* restituito dalla funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) è zero, il programma di installazione deve chiamare la [**funzione RmShutdown.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) In questo modo vengono arrestati i servizi e le applicazioni che usano risorse registrate. Il programma di installazione deve quindi eseguire le modifiche di sistema necessarie per completare l'installazione. Infine, il programma di installazione deve chiamare la funzione [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) in modo che Gestione riavvio possa riavviare le applicazioni arrestate e registrate per un riavvio.

4.  Il programma di installazione può usare [**la funzione RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) per impedire l'arresto o il riavvio di applicazioni e servizi specificati da parte delle operazioni di Gestione riavvio. La [**funzione RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist) restituisce un elenco delle applicazioni e dei servizi da filtrare dall'arresto e dal riavvio. La [**funzione RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter) rimuove un filtro.
5.  Il programma di installazione chiama [**la funzione RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) per chiudere la sessione di Gestione riavvio.

Per un frammento di codice di esempio che illustra l'avvio e l'uso di una sessione di Gestione riavvio con un programma di installazione primario e quindi l'aggiunta di un programma di installazione secondario alla sessione esistente, vedere Uso di Gestione riavvio con un programma di installazione [secondario.](using-restart-manager-with-a-secondary-installer.md)

 

 




