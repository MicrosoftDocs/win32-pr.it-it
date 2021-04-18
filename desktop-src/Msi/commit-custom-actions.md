---
description: Il commit delle azioni personalizzate viene eseguito al completamento dello script di installazione.
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: Esegui commit di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174af16a84f71ff90a1fc35c76054ee503449b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309995"
---
# <a name="commit-custom-actions"></a>Esegui commit di azioni personalizzate

Il commit delle azioni personalizzate viene eseguito al completamento dello script di installazione. Se l' [azione InstallFinalize](installfinalize-action.md) ha esito positivo, il programma di installazione eseguirà tutte le azioni personalizzate di commit esistenti. L'unico parametro di modalità impostato dal programma di installazione in questo caso è MSIRUNMODE \_ commit. Per una descrizione dei parametri della modalità di esecuzione, vedere [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .

È possibile specificare un'azione personalizzata di commit aggiungendo un flag di opzione al campo Type della [tabella CustomAction](customaction-table.md). Vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md) per il flag di opzione che designa un'azione personalizzata di commit.

Un'azione personalizzata di commit è il complemento di un' [azione di rollback personalizzata](rollback-custom-actions.md) e può essere utilizzata con azioni personalizzate di rollback per annullare le azioni personalizzate che consentono di apportare modifiche direttamente al sistema.

Si noti che un'azione di rollback personalizzata potrebbe non essere in grado di rimuovere tutte le modifiche apportate dalle azioni personalizzate di commit. Sebbene il programma di installazione scriva le azioni personalizzate rollback e commit nello script rollback, le azioni personalizzate di commit vengono eseguite solo dopo che il programma di installazione ha elaborato correttamente lo script di installazione. Le azioni personalizzate di commit sono le prime azioni da eseguire nello script di rollback. Se un'azione personalizzata di commit ha esito negativo, il programma di installazione avvia il rollback ma può solo eseguire il rollback delle operazioni già scritte nello script di rollback. Ciò significa che, a seconda dell'azione personalizzata commit, un rollback potrebbe non essere in grado di annullare le modifiche apportate dall'azione. È possibile ignorare gli errori nelle azioni personalizzate di commit creando l'azione personalizzata per ignorare i codici restituiti.

Le azioni personalizzate rollback e commit non vengono eseguite quando il rollback è disabilitato. Se l'autore di un pacchetto richiede questi tipi di azioni personalizzate per l'installazione corretta, è consigliabile usare la proprietà [**RollbackDisabled**](rollbackdisabled.md) in una condizione che impedisce che l'installazione continui quando il rollback è disabilitato.

 

 



