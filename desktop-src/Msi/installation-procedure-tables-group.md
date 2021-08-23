---
description: Le tabelle del gruppo Procedura di installazione controllano le attività eseguite durante l'installazione da azioni standard e azioni personalizzate.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Gruppo tabelle procedura di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c66cc377fdf36969699f0e150fc30a02363ed24aa1848c4492917bffda7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633586"
---
# <a name="installation-procedure-tables-group"></a>Gruppo tabelle procedura di installazione

Le tabelle del gruppo Procedura di installazione controllano le attività eseguite durante [l'installazione](standard-actions.md) da azioni standard e [azioni personalizzate](custom-actions.md).

Alcune tabelle di questo gruppo controllano un'azione di alto livello fornendo una sequenza di azioni. Ognuna delle tabelle di sequenza seguenti controlla una parte di un'azione di alto livello.

-   [Tabella InstallUISequence](installuisequence-table.md)
-   [Tabella InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabella AdminUISequence](adminuisequence-table.md)
-   [Tabella AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabella AdvtUISequence](advtuisequence-table.md)
-   [Tabella AdvtExecuteSequence](advtexecutesequence-table.md)

Possono verificarsi situazioni in cui un'installazione deve eseguire operazioni che non sono possibili usando solo [azioni standard.](standard-actions.md) Per offrire il massimo grado di flessibilità, il programma di installazione offre agli autori del programma di installazione la possibilità di creare azioni personalizzate. Se sono presenti azioni personalizzate, è necessario registrarle con il programma di installazione popolando la tabella CustomAction.

La [tabella CustomAction consente](customaction-table.md) di integrare codice e dati personalizzati nel processo di installazione. Il codice eseguito può essere un flusso contenuto nel database, un file installato di recente o un eseguibile esistente.

Le tabelle seguenti estendono le funzionalità del programma di installazione per modificare file e cartelle durante l'installazione.

-   La [tabella RemoveFile](removefile-table.md) contiene un elenco di file che vengono rimossi durante l'installazione.
-   La [tabella RemoveIniFile](removeinifile-table.md) contiene le informazioni che un'applicazione deve rimuovere .ini file.
-   La [tabella RemoveRegistry contiene](removeregistry-table.md) le informazioni che vengono eliminate dal Registro di sistema quando si seleziona il componente corrispondente per l'installazione.
-   La [tabella CreateFolder elenca](createfolder-table.md) le cartelle che devono essere create durante l'installazione. Anche se il programma di installazione crea le cartelle in base alle esigenze, queste vengono rimosse non appena sono vuote. L'elenco cartelle nella tabella CreateFolder non viene eliminato fino a quando il componente non viene disinstallato.
-   La [tabella MoveFile](movefile-table.md) contiene un elenco di file da spostare o copiare da una directory di origine specificata nel computer dell'utente a una directory di destinazione. Non è necessario usare la tabella MoveFile per descrivere i file associati ai componenti da installare.

Per impostare le condizioni necessarie che devono essere soddisfatte per avviare l'installazione, popolare la tabella LaunchCondition.

La [tabella LaunchCondition](launchcondition-table.md) contiene un elenco di condizioni, che devono essere tutte soddisfatte per l'esito positivo dell'azione.

 

 



