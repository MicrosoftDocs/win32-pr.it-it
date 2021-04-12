---
description: Le tabelle del gruppo procedura di installazione controllano le attività eseguite durante l'installazione mediante azioni standard e azioni personalizzate.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Gruppo tabelle procedure di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349756"
---
# <a name="installation-procedure-tables-group"></a>Gruppo tabelle procedure di installazione

Le tabelle del gruppo procedura di installazione controllano le attività eseguite durante l'installazione mediante [azioni standard](standard-actions.md) e [azioni personalizzate](custom-actions.md).

Alcune tabelle in questo gruppo controllano un'azione di alto livello fornendo una sequenza di azioni. Ognuna delle tabelle di sequenza seguenti controlla una parte di un'azione di alto livello.

-   [Tabella InstallUISequence](installuisequence-table.md)
-   [Tabella InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabella AdminUISequence](adminuisequence-table.md)
-   [Tabella AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabella AdvtUISequence](advtuisequence-table.md)
-   [Tabella AdvtExecuteSequence](advtexecutesequence-table.md)

In alcune situazioni è necessario che un'installazione esegua operazioni che non è possibile utilizzare solo le [azioni standard](standard-actions.md). Per fornire il massimo livello di flessibilità, il programma di installazione fornisce agli autori di installazione la possibilità di creare azioni personalizzate. Se si dispone di azioni personalizzate, è necessario registrarle con il programma di installazione popolando la tabella CustomAction.

La [tabella CustomAction](customaction-table.md) fornisce i mezzi per integrare il codice personalizzato e i dati nel processo di installazione. Il codice eseguito può essere un flusso contenuto all'interno del database, un file installato di recente o un eseguibile esistente.

Le tabelle seguenti estendono le funzionalità del programma di installazione per modificare file e cartelle durante l'installazione.

-   La [tabella RemoveFile](removefile-table.md) contiene un elenco di file che vengono rimossi durante l'installazione.
-   La [tabella RemoveIniFile](removeinifile-table.md) contiene le informazioni che un'applicazione deve rimuovere dai file ini.
-   La [tabella RemoveRegistry](removeregistry-table.md) contiene le informazioni che vengono eliminate dal registro di sistema quando viene selezionato il componente corrispondente da installare.
-   La [tabella CreateFolder](createfolder-table.md) elenca le cartelle che devono essere create durante l'installazione. Sebbene il programma di installazione crei le cartelle non appena sono necessarie, queste vengono rimosse non appena sono vuote. L'elenco di cartelle nella tabella CreateFolder non viene eliminato fino a quando il componente non viene disinstallato.
-   La [tabella MoveFile](movefile-table.md) contiene un elenco di file da spostare o copiare da una directory di origine specificata nel computer dell'utente in una directory di destinazione. Non è necessario usare la tabella MoveFile per descrivere i file associati ai componenti da installare.

Per configurare le condizioni necessarie che devono essere soddisfatte per avviare l'installazione, popolare la tabella LaunchCondition.

La [tabella LaunchCondition](launchcondition-table.md) contiene un elenco di condizioni che devono essere soddisfatte affinché l'azione abbia esito positivo.

 

 



