---
description: Finché il sistema determina che è presente un'attività dell'utente o dell'applicazione, non entrerà in stato di sospensione.
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: Criteri di sospensione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90950b980ec1e0fa06171d7a57d76b410534f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756566"
---
# <a name="system-sleep-criteria"></a>Criteri di sospensione del sistema

Finché il sistema determina che è presente un'attività dell'utente o dell'applicazione, non entrerà in stato di sospensione. Il sistema è in grado di rilevare determinate attività, ad esempio l'input dell'utente o le comunicazioni di rete. Tuttavia, esistono altre attività che il sistema non è in grado di rilevare. Ad esempio, un'applicazione di presentazione richiede la visualizzazione della schermata. Tuttavia, potrebbe sembrare che l'applicazione sia inattiva durante la presentazione, causando la disattivazione dello schermo da parte del sistema.

Per notificare al sistema che l'applicazione è occupata, usare la funzione [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) . Questa funzione impedisce al sistema di entrare in stato di sospensione o di spegnere la visualizzazione mentre l'applicazione è in esecuzione.

Per le applicazioni di presentazione e multimediali è necessario chiamare la funzione [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) con lo **\_ schermo es \_ necessario** , in modo che il sistema sappia che non deve mettere il dispositivo di visualizzazione in sospensione. Le applicazioni per la gestione degli eventi, ad esempio gli strumenti per la gestione dei fax in ingresso, devono chiamare **SetThreadExecutionState** con **es \_ System \_ required**, gestire l'evento e quindi cancellare il flag in modo che il sistema possa tornare in sospensione. Si noti che la maggior parte delle applicazioni di produttività non deve usare **SetThreadExecutionState** perché il sistema può in genere determinare l'attività in base all'input dell'utente.

Per mantenere il tempo trascorso dall'ultimo input dell'utente, il sistema utilizza un timer di inattività di visualizzazione e un timer di inattività del sistema. Il sistema confronta i timer di inattività con i valori configurati nella combinazione per il risparmio di energia. Se il valore del timer di inattività visualizzato è maggiore del valore di timeout di visualizzazione e nessun thread ha richiesto la visualizzazione chiamando [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) con **lo \_ schermo es \_ necessario**, il sistema spegne lo schermo. Analogamente, se il timer di inattività del sistema è superiore al valore di timeout del sistema e nessuna applicazione ha richiesto il sistema chiamando **SetThreadExecutionState** con **es \_ System \_ required**, il sistema entra in stato di sospensione.

Il sistema gestisce un conteggio delle applicazioni che hanno chiamato [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate). Il sistema tiene traccia di ogni thread che chiama **SetThreadExecutionState** e modifica di conseguenza il contatore. Se il contatore raggiunge il valore zero e non è presente alcun input dell'utente, il sistema entra in stato di sospensione.

Se il risparmio di energia è basso, un'applicazione può richiedere l'intervento dell'utente o richiedere che il sistema si sospenda automaticamente. È possibile sospendere l'operazione di sistema utilizzando la funzione [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

Se il sistema viene riattivato automaticamente ([PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)), nessuno dei timer è pertinente. Per ulteriori informazioni, vedere [eventi di riattivazione del sistema](system-wake-up-events.md).

## <a name="entering-sleep"></a>Immissione di sospensione

Quando il sistema entra in stato di sospensione, lo stato dell'intero sistema e di tutte le applicazioni verrà mantenuto automaticamente. Per la maggior parte delle applicazioni, pertanto, non è necessario eseguire alcuna azione speciale. Le applicazioni che devono eseguire azioni specifiche prima della transizione del sistema possono registrarsi per gli eventi di alimentazione.

Quando il sistema invia un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) , ogni applicazione ha due secondi per eseguire le azioni necessarie prima che il sistema avvii la transizione alla modalità di sospensione. Le applicazioni devono limitare l'azione eseguita in risposta a questo evento per assicurarsi che completino tutte le operazioni nel tempo assegnato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> <dt>

[Eventi di riattivazione del sistema](system-wake-up-events.md)
</dt> </dl>

 

 



