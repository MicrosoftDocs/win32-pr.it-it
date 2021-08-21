---
description: Lo scopo di un'azione personalizzata di esecuzione posticipata è ritardare l'esecuzione di una modifica di sistema all'ora in cui viene eseguito lo script di installazione.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Azioni personalizzate di esecuzione posticipata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cec06600fa2cdb447ace579ecf9d19be62e5f4824ecf2d34d77ed879a717d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379178"
---
# <a name="deferred-execution-custom-actions"></a>Azioni personalizzate di esecuzione posticipata

Lo scopo di un'azione personalizzata di esecuzione posticipata è ritardare l'esecuzione di una modifica di sistema all'ora in cui viene eseguito lo script di installazione. Questo comportamento è diverso da un'azione personalizzata normale o un'azione standard, in cui il programma di installazione esegue l'azione immediatamente dopo che è stata rilevata in una tabella di sequenza o in una chiamata a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). Un'azione personalizzata di esecuzione posticipata consente a un autore del pacchetto di specificare le operazioni di sistema in un determinato punto all'interno dell'esecuzione dello script di installazione.

Il programma di installazione non esegue un'azione personalizzata di esecuzione posticipata al momento dell'elaborazione della sequenza di installazione. Il programma di installazione scrive invece l'azione personalizzata nello script di installazione. L'unico parametro mode impostato dal programma di installazione in questo caso è MSIRUNMODE \_ SCHEDULED. Per una descrizione dei parametri della modalità di esecuzione, vedere [**MsiGetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)

Un'azione personalizzata di esecuzione posticipata deve essere pianificata nella tabella della sequenza di esecuzione all'interno della sezione che esegue la generazione di script. Le azioni personalizzate di esecuzione posticipata devono essere eseguite dopo [InstallInitialize](installinitialize-action.md) e devono essere eseguite prima [di InstallFinalize](installfinalize-action.md) nella sequenza di azioni.

Le azioni personalizzate che impostano proprietà, stati delle funzionalità, stati dei componenti o directory di destinazione o che pianificano le operazioni di sistema inserendo righe nelle tabelle di sequenza, possono in molti casi usare l'esecuzione immediata in modo sicuro. Tuttavia, le azioni personalizzate che modificano direttamente il sistema o chiamano un altro servizio di sistema devono essere rinviate al momento in cui viene eseguito lo script di installazione. Per [altre informazioni sui](synchronous-and-asynchronous-custom-actions.md) potenziali conflitti tra le azioni personalizzate e il thread di installazione principale, vedere Azioni personalizzate sincrone e asincrone.

Poiché lo script di installazione può essere eseguito all'esterno della sessione di installazione in cui è stato scritto, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione. Ciò significa che l'handle di sessione originale e il set di dati delle proprietà durante la sequenza di installazione non sono disponibili per un'azione personalizzata di esecuzione posticipata. Le azioni personalizzate posticipate che chiamano librerie a collegamento dinamico (DLL) passano un handle che può essere usato solo per ottenere una quantità molto limitata di informazioni, come descritto [in](obtaining-context-information-for-deferred-execution-custom-actions.md)Ottenere informazioni di contesto per le azioni personalizzate di esecuzione posticipata.

Si noti che le azioni personalizzate posticipate, tra cui il [rollback](rollback-custom-actions.md) delle azioni personalizzate e le azioni personalizzate di [commit,](commit-custom-actions.md)sono gli unici tipi di azioni che possono essere eseguite al di fuori del contesto di sicurezza degli utenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Opzioni di esecuzione In-Script azioni personalizzate](custom-action-in-script-execution-options.md)
</dt> <dt>

[Informazioni di riferimento su azioni personalizzate](custom-action-reference.md)
</dt> </dl>

 

 



