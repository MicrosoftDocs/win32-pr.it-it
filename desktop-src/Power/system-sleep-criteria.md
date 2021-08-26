---
description: Finché il sistema determina che è presente un'attività dell'utente o dell'applicazione, non entra in sospensione.
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: Criteri di sospensione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b93b0eb1a55d156a9d75b51ef826c85eabd28b29789cf50bb7f0fd7b5fee90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032821"
---
# <a name="system-sleep-criteria"></a>Criteri di sospensione del sistema

Finché il sistema determina che è presente un'attività dell'utente o dell'applicazione, non entra in sospensione. Il sistema può rilevare determinate attività, ad esempio l'input dell'utente o le comunicazioni di rete. Esistono tuttavia altre attività che il sistema non è in grado di rilevare. Ad esempio, un'applicazione di presentazione richiede la visualizzazione dello schermo. Tuttavia, potrebbe sembrare che l'applicazione sia inattiva durante la presentazione, causando la disattivazione della visualizzazione da parte del sistema.

Per notificare al sistema che l'applicazione è occupata, usare la [**funzione SetThreadExecutionState.**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) Questa funzione impedisce al sistema di entrare in sospensione o di disattivare la visualizzazione mentre l'applicazione è in esecuzione.

Le applicazioni di presentazione e multimediali devono chiamare la funzione [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) con **ES \_ DISPLAY \_ REQUIRED** in modo che il sistema sappia che non deve mettere in sospensione il dispositivo di visualizzazione. Le applicazioni di gestione degli eventi, ad esempio gli strumenti per la gestione dei fax in ingresso, devono chiamare **SetThreadExecutionState** con **ES \_ SYSTEM \_ REQUIRED,** gestire l'evento e quindi cancellare il flag in modo che il sistema possa tornare in sospensione. Si noti che la maggior parte delle applicazioni di produttività non deve usare **SetThreadExecutionState** perché il sistema può in genere determinare l'attività in base all'input dell'utente.

Per mantenere il tempo dopo l'ultimo input dell'utente, il sistema usa un timer di inattività dello schermo e un timer di inattività del sistema. Il sistema confronta i timer inattivi con i valori configurati nella combinazione per il risparmio di energia. Se il valore del timer di inattività di visualizzazione è maggiore del valore di timeout della visualizzazione e nessun thread ha richiesto la visualizzazione chiamando [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) con **ES \_ DISPLAY \_ REQUIRED,** il sistema disattiva la visualizzazione. Analogamente, se il timer di inattività del sistema è maggiore del valore di timeout del sistema e nessuna applicazione ha richiesto il sistema chiamando **SetThreadExecutionState** con **ES \_ SYSTEM \_ REQUIRED,** il sistema entra in sospensione.

Il sistema gestisce un conteggio delle applicazioni che hanno chiamato [**SetThreadExecutionState.**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) Il sistema tiene traccia di ogni thread che chiama **SetThreadExecutionState** e regola il contatore di conseguenza. Se questo contatore raggiunge zero e non è stato immesso alcun input utente, il sistema entra in sospensione.

Se l'alimentazione è bassa, un'applicazione può richiedere l'intervento dell'utente o richiedere che il sistema si sospende. È possibile sospendere l'operazione di sistema usando la [**funzione SetSuspendState.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

Se il sistema viene riattivato automaticamente[(PBT \_ APMRESUMEAUTOMATIC),](pbt-apmresumeautomatic.md)nessuno dei timer è pertinente. Per altre informazioni, vedere [Eventi di riattivazione del sistema](system-wake-up-events.md).

## <a name="entering-sleep"></a>Immissione della sospensione

Quando il sistema entra in sospensione, mantiene automaticamente lo stato dell'intero sistema e di tutte le applicazioni. Pertanto, la maggior parte delle applicazioni non deve eseguire alcuna azione speciale. Applicazioni che devono eseguire azioni specifiche prima che le transizioni di sistema possano registrarsi per gli eventi di alimentazione.

Quando il sistema invia un evento [ \_ PBT APMSUSPEND,](pbt-apmsuspend.md) ogni applicazione ha due secondi per eseguire le azioni necessarie prima che il sistema inizi la transizione alla sospensione. Le applicazioni devono limitare l'azione eseguita in risposta a questo evento per assicurarsi che completino tutte le operazioni nel tempo assegnato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Risparmio energia](about-power-management.md)
</dt> <dt>

[Eventi di riattivazione del sistema](system-wake-up-events.md)
</dt> </dl>

 

 



