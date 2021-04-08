---
description: Quando un programma di controllo del servizio richiede l'esecuzione di un nuovo servizio, gestione controllo servizi avvia il servizio e invia una richiesta di avvio al dispatcher del controllo.
ms.assetid: e55e056f-7628-4e3d-9aea-b55c371b4287
title: Funzione ServiceMain del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed50f0f378f348415e56827a09fcf17eea7fc330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968383"
---
# <a name="service-servicemain-function"></a>Funzione ServiceMain del servizio

Quando un programma di controllo del servizio richiede l'esecuzione di un nuovo servizio, gestione controllo servizi avvia il servizio e invia una richiesta di avvio al dispatcher del controllo. Il dispatcher del controllo Crea un nuovo thread per eseguire la funzione [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) per il servizio. Per un esempio, vedere [scrittura di una funzione ServiceMain](writing-a-servicemain-function.md).

La funzione [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) deve eseguire le attività seguenti:

1.  Inizializzare tutte le variabili globali.
2.  Chiamare immediatamente la funzione [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) per registrare una funzione di [**gestione**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) per gestire le richieste di controllo per il servizio. Il valore restituito di **RegisterServiceCtrlHandler** è un *handle dello stato del servizio* che verrà utilizzato nelle chiamate per notificare al SCM lo stato del servizio.
3.  Eseguire l'inizializzazione. Se il tempo di esecuzione del codice di inizializzazione dovrebbe essere molto breve (meno di un secondo), l'inizializzazione può essere eseguita direttamente in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona).

    Se è previsto che il tempo di inizializzazione sia superiore a un secondo, il servizio deve utilizzare una delle tecniche di inizializzazione seguenti:

    -   Chiamare la funzione [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) per segnalare che il servizio \_ è in esecuzione, ma non accetta alcun controllo fino al completamento dell'inizializzazione. Il servizio esegue questa operazione chiamando **SetServiceStatus** con **DWCURRENTSTATE** impostato su Service \_ Running e **dwControlsAccepted** impostato su 0 nella struttura [**\_ dello stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) . Ciò garantisce che SCM non invierà le richieste di controllo al servizio prima che sia pronto e libera la gestione SCM per la gestione di altri servizi. Questo approccio all'inizializzazione è consigliato per le prestazioni, in particolare per i servizi di avvio automatico.
    -   Avvio del servizio report \_ \_ in sospeso, non accetta alcun controllo e specifica un hint di attesa. Se il codice di inizializzazione del servizio esegue attività che richiedono più tempo del valore iniziale del suggerimento di attesa, il codice deve chiamare periodicamente la funzione [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) (possibilmente con un hint di attesa modificato) per indicare che l'avanzamento viene eseguito. Assicurarsi di chiamare **SetServiceStatus** solo se l'inizializzazione sta procedendo. In caso contrario, SCM può attendere che il servizio entri nello \_ stato di esecuzione del servizio presumendo che il servizio stia eseguendo lo stato di avanzamento e impedisce l'avvio di altri servizi. Non chiamare **SetServiceStatus** da un thread separato a meno che non si sia certi che il thread che esegue l'inizializzazione stia effettivamente facendo progressi.

        Un servizio che utilizza questo approccio può inoltre specificare un valore del punto di controllo e incrementare il valore periodicamente durante un'inizializzazione prolungata. Il programma che ha avviato il servizio può chiamare [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) o [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) per ottenere il valore del punto di controllo più recente da SCM e usare il valore per segnalare l'avanzamento incrementale all'utente.

4.  Al termine dell'inizializzazione, chiamare [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) per impostare lo stato del servizio sul servizio \_ in esecuzione e specificare i controlli che il servizio è pronto ad accettare. Per un elenco di controlli, vedere la [**struttura \_ dello stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) .
5.  Eseguire le attività del servizio oppure, se non sono presenti attività in sospeso, restituire il controllo al chiamante. Qualsiasi modifica apportata allo stato del servizio garantisce una chiamata a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) per segnalare nuove informazioni sullo stato.
6.  Se si verifica un errore durante l'inizializzazione o l'esecuzione del servizio, il servizio deve chiamare [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) per impostare lo stato del servizio sull'arresto del servizio in \_ \_ sospeso se la pulizia sarà lunga. Al termine della pulizia, chiamare **SetServiceStatus** per impostare lo stato del servizio su servizio \_ interrotto dall'ultimo thread per terminare. Assicurarsi di impostare i membri **dwServiceSpecificExitCode** e **dwWin32ExitCode** della struttura [**\_ dello stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) per identificare l'errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di una funzione ServiceMain](writing-a-servicemain-function.md)
</dt> </dl>

 

 
