---
description: Lo scopo di un'azione personalizzata di esecuzione posticipata consiste nel ritardare l'esecuzione di una modifica di sistema fino al momento in cui viene eseguito lo script di installazione.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Azioni personalizzate di esecuzione posticipata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09b91793f5d5bbc7be7099c92f8d8f212012d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967815"
---
# <a name="deferred-execution-custom-actions"></a>Azioni personalizzate di esecuzione posticipata

Lo scopo di un'azione personalizzata di esecuzione posticipata consiste nel ritardare l'esecuzione di una modifica di sistema fino al momento in cui viene eseguito lo script di installazione. Questo comportamento è diverso da un'azione personalizzata normale o da un'azione standard in cui il programma di installazione esegue l'azione immediatamente dopo che è stata rilevata in una tabella di sequenza o in una chiamata a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). Un'azione personalizzata di esecuzione posticipata consente a un autore di pacchetti di specificare le operazioni di sistema in un determinato punto all'interno dell'esecuzione dello script di installazione.

Il programma di installazione non esegue un'azione personalizzata di esecuzione posticipata al momento dell'elaborazione della sequenza di installazione. Il programma di installazione scrive invece l'azione personalizzata nello script di installazione. L'unico parametro di modalità impostato dal programma di installazione in questo caso è MSIRUNMODE \_ scheduled. Per una descrizione dei parametri della modalità di esecuzione, vedere [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .

È necessario pianificare un'azione personalizzata di esecuzione posticipata nella tabella Execute Sequence all'interno della sezione che esegue la generazione di script. Le azioni personalizzate di esecuzione posticipata devono essere successive a [InstallInitialize](installinitialize-action.md) e prima di [InstallFinalize](installfinalize-action.md) nella sequenza di azione.

In molti casi le azioni personalizzate che impostano le proprietà, gli Stati delle funzionalità, gli Stati dei componenti o le directory di destinazione o che pianificano le operazioni di sistema inserendo righe nelle tabelle di sequenza possono utilizzare l'esecuzione immediata in modo sicuro. Tuttavia, le azioni personalizzate che modificano direttamente il sistema o chiamano un altro servizio di sistema devono essere rinviate al momento in cui viene eseguito lo script di installazione. Per ulteriori informazioni sui potenziali conflitti tra le azioni personalizzate e il thread di installazione principale, vedere [azioni personalizzate sincrone e asincrone](synchronous-and-asynchronous-custom-actions.md) .

Poiché lo script di installazione può essere eseguito all'esterno della sessione di installazione in cui è stato scritto, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione. Ciò significa che l'handle di sessione originale e il set di dati della proprietà durante la sequenza di installazione non sono disponibili per un'azione personalizzata di esecuzione posticipata. Le azioni personalizzate posticipate che chiamano librerie a collegamento dinamico (dll) passano un handle che può essere usato solo per ottenere una quantità molto limitata di informazioni, come descritto in [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).

Si noti che le azioni personalizzate posticipate, incluse le azioni personalizzate di [rollback](rollback-custom-actions.md) e le [azioni personalizzate di commit](commit-custom-actions.md), sono gli unici tipi di azioni che possono essere eseguite all'esterno del contesto di sicurezza degli utenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Opzioni di esecuzione In-Script azione personalizzata](custom-action-in-script-execution-options.md)
</dt> <dt>

[Riferimento all'azione personalizzata](custom-action-reference.md)
</dt> </dl>

 

 



