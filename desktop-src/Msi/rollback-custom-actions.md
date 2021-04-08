---
description: Quando il programma di installazione elabora lo script di installazione, genera contemporaneamente uno script di rollback.
ms.assetid: 5b9bfc5a-6a78-4b0e-aed8-f25aba089af1
title: Rollback delle azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c4ad91f8f94145399d51ed2ef53999ab0a91d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880185"
---
# <a name="rollback-custom-actions"></a>Rollback delle azioni personalizzate

Quando il programma di installazione elabora lo script di installazione, genera contemporaneamente uno script di rollback. Oltre allo script di rollback, il programma di installazione salva una copia di tutti i file eliminati durante l'installazione. Questi file vengono conservati in una directory di sistema nascosta. Al termine dell'installazione, vengono eliminati lo script di rollback e i file salvati. Se un'installazione ha esito negativo, il programma di installazione tenterà di eseguire il rollback delle modifiche apportate durante l'installazione e di ripristinare lo stato originale del computer.

Sebbene le azioni personalizzate che pianificano le operazioni di sistema inserendo righe nella tabella di database siano invertite da un rollback dell'installazione, le azioni personalizzate che modificano direttamente il sistema o che inviano comandi ad altri servizi di sistema non possono essere sempre invertite da un rollback. Un'azione di rollback personalizzata è un'azione eseguita dal programma di installazione solo durante il rollback dell'installazione e il suo scopo è invertire un'azione personalizzata che ha apportato modifiche al sistema.

Un'azione di rollback personalizzata è un tipo di [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md), perché la sua esecuzione viene posticipata quando viene richiamata durante la sequenza di installazione. Si differenzia da una normale azione personalizzata posticipata in quanto viene eseguita solo durante un rollback. Un'azione di rollback personalizzata deve sempre precedere l'azione personalizzata rinviata che esegue il rollback nella sequenza di azione. Un'azione di rollback personalizzata deve anche gestire il caso in cui l'azione personalizzata rinviata viene interrotta durante l'esecuzione. Ad esempio, se l'utente preme il pulsante Annulla durante l'esecuzione dell'azione personalizzata.

Si noti che le azioni di rollback personalizzate non possono essere eseguite in modo asincrono. Vedere [azioni personalizzate sincrone e asincrone](synchronous-and-asynchronous-custom-actions.md).

Il complemento a un'azione di rollback personalizzata è un' [azione personalizzata di commit](commit-custom-actions.md). Il programma di installazione esegue un'azione personalizzata di commit durante la sequenza di installazione, copia l'azione personalizzata nello script di rollback, ma non esegue l'azione durante il rollback.

Si noti che un'azione di rollback personalizzata potrebbe non essere in grado di rimuovere tutte le modifiche apportate dalle azioni personalizzate di commit. Sebbene il programma di installazione scriva le azioni personalizzate rollback e commit nello script rollback, le azioni personalizzate di commit vengono eseguite solo dopo che il programma di installazione ha elaborato correttamente lo script di installazione. Le azioni personalizzate di commit sono le prime azioni da eseguire nello script di rollback. Se un'azione personalizzata di commit ha esito negativo, il programma di installazione avvia il rollback ma può solo eseguire il rollback delle operazioni già scritte nello script di rollback. Ciò significa che, a seconda dell'azione personalizzata commit, un rollback potrebbe non essere in grado di annullare le modifiche apportate dall'azione. È possibile ignorare gli errori nelle azioni personalizzate di commit creando l'azione personalizzata per ignorare i codici restituiti.

Quando il programma di installazione esegue un'azione di rollback personalizzata, l'unico parametro di modalità che verrà impostato è MSIRUNMODE \_ rollback. Per una descrizione dei parametri della modalità di esecuzione, vedere [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .

È possibile specificare un'azione di rollback personalizzata aggiungendo un flag di opzione al campo Type della [tabella CustomAction](customaction-table.md). Vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md) per il flag di opzione che designa un'azione personalizzata di rollback.

Le azioni personalizzate rollback e commit non vengono eseguite quando il rollback è disabilitato. Se l'autore di un pacchetto richiede questi tipi di azioni personalizzate per l'installazione corretta, è consigliabile usare la proprietà [**RollbackDisabled**](rollbackdisabled.md) in una condizione che impedisce che l'installazione continui quando il rollback è disabilitato. Per informazioni su come disabilitare il rollback, vedere [rollback Installation (Windows Installer)](rollback-installation.md).

 

 



