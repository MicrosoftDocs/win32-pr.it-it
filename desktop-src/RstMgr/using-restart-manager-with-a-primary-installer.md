---
title: Uso di gestione riavvio con un programma di installazione primario
description: Nella procedura seguente viene descritto come utilizzare Gestione riavvio per arrestare e riavviare le applicazioni e i servizi. Quando si usa Gestione riavvio con un unico programma di installazione, questo programma di installazione è anche il programma di installazione principale che controlla l'interfaccia utente.
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38956ee8d04bc377809e93579080d9b767c3da3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955296"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>Uso di gestione riavvio con un programma di installazione primario

Nella procedura seguente viene descritto come utilizzare Gestione riavvio per arrestare e riavviare le applicazioni e i servizi. Quando si usa Gestione riavvio con un unico programma di installazione, questo programma di installazione è anche il programma di installazione principale che controlla l'interfaccia utente.

**Per usare Gestione riavvio con un programma di installazione primario**

1.  Il programma di installazione chiama la funzione [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) per avviare la sessione di gestione riavvio e ottenere un handle di sessione e una chiave.
2.  Il programma di installazione chiama la funzione [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) per registrare le risorse. Gestione riavvio può utilizzare solo le risorse registrate per determinare quali applicazioni e servizi devono essere arrestati e riavviati. Tutte le risorse che possono essere interessate dall'installazione devono essere registrate con la sessione. Le risorse possono essere identificate in base al nome file, al nome breve del servizio o a una struttura di [**\_ \_ processo univoca RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) .
3.  Il programma di installazione chiama la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) per ottenere una matrice di strutture di [**\_ \_ informazioni del processo RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) che elenca tutte le applicazioni e i servizi che devono essere arrestati e riavviati.

    Se il valore del parametro *lpdwRebootReason* restituito dalla funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) è diverso da zero, gestione riavvio non è in grado di liberare una risorsa registrata dalla chiusura di un'applicazione o di un servizio. In questo caso, è necessario arrestare e riavviare il sistema per continuare l'installazione. Il programma di installazione deve richiedere all'utente un'azione, arrestare programmi o servizi oppure pianificare un arresto e un riavvio del sistema.

    Se il valore del parametro *lpdwRebootReason* restituito dalla funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) è zero, il programma di installazione deve chiamare la funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) . Questa operazione arresta i servizi e le applicazioni che usano risorse registrate. Il programma di installazione deve quindi eseguire le modifiche di sistema necessarie per completare l'installazione. Infine, il programma di installazione deve chiamare la funzione [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) in modo che la gestione riavvio possa riavviare le applicazioni arrestate e registrate per il riavvio.

4.  Il programma di installazione può utilizzare la funzione [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) per impedire che le applicazioni e i servizi specificati vengano arrestati o riavviati dalle operazioni di gestione riavvio. La funzione [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist) restituisce un elenco di applicazioni e servizi da filtrare dall'arresto e dal riavvio. La funzione [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter) rimuove un filtro.
5.  Il programma di installazione chiama la funzione [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) per chiudere la sessione di gestione riavvio.

Per un frammento di codice di esempio che mostra l'avvio e l'uso di una sessione di gestione riavvio usando un programma di installazione primario e quindi aggiungendo un programma di installazione secondario alla sessione esistente, vedere [uso di gestione riavvio con un programma di installazione secondario](using-restart-manager-with-a-secondary-installer.md).

 

 




