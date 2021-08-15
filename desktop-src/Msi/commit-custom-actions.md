---
description: Commit Le azioni personalizzate vengono eseguite al completamento dello script di installazione.
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: Eseguire il commit di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a126468df400e23c8eb59885b6e5a66c96d740c0c0e0959320697da293d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380306"
---
# <a name="commit-custom-actions"></a>Eseguire il commit di azioni personalizzate

Commit Le azioni personalizzate vengono eseguite al completamento dello script di installazione. Se [l'azione InstallFinalize ha](installfinalize-action.md) esito positivo, il programma di installazione eseguirà tutte le azioni commit personalizzate esistenti. L'unico parametro mode impostato dal programma di installazione in questo caso è MSIRUNMODE \_ COMMIT. Per una descrizione dei parametri della modalità di esecuzione, vedere [**MsiGetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)

È possibile specificare un'azione personalizzata di commit aggiungendo un flag di opzione al campo Type della [tabella CustomAction](customaction-table.md). Vedere [Azioni personalizzate In-Script opzioni di esecuzione per](custom-action-in-script-execution-options.md) il flag di opzione che designa un'azione personalizzata di commit.

Un'azione personalizzata di commit è il complemento a un'azione personalizzata [di rollback](rollback-custom-actions.md) e può essere usata con azioni personalizzate di rollback per invertire le azioni personalizzate che apportano modifiche direttamente al sistema.

Si noti che un'azione personalizzata di rollback potrebbe non essere in grado di rimuovere tutte le modifiche apportate dalle azioni personalizzate di commit. Anche se il programma di installazione scrive azioni personalizzate di rollback e commit nello script di rollback, il commit delle azioni personalizzate viene eseguito solo dopo che il programma di installazione ha elaborato correttamente lo script di installazione. Le azioni personalizzate di commit sono le prime azioni da eseguire nello script di rollback. Se un'azione personalizzata di commit ha esito negativo, il programma di installazione avvia il rollback, ma può solo eseguire il rollback delle operazioni già scritte nello script di rollback. Ciò significa che, a seconda dell'azione personalizzata di commit, un rollback potrebbe non essere in grado di annullare le modifiche apportate dall'azione. È possibile ignorare gli errori nelle azioni personalizzate di commit mediante la creazione dell'azione personalizzata per ignorare i codici restituiti.

Le azioni personalizzate di rollback e commit non vengono eseguite quando il rollback è disabilitato. Se l'autore di un pacchetto richiede questi tipi di azioni personalizzate per l'installazione corretta, deve usare la proprietà [**RollbackDisabled**](rollbackdisabled.md) in una condizione che impedisce la continuazione dell'installazione quando il rollback è disabilitato.

 

 



