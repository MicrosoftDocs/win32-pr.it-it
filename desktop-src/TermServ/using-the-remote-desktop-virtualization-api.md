---
title: Uso dell'API di virtualizzazione Desktop remoto
description: Gli sviluppatori possono utilizzare questa API per personalizzare la logica utilizzata da gestore connessione Desktop remoto per determinare la destinazione migliore per una connessione client in ingresso.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto tramite l'API di virtualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9ebfc014a2c8ec20d299bbb8be9183b25ce89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399143"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Uso dell'API di virtualizzazione Desktop remoto

Il servizio ruolo directory di sessione di Servizi terminal consente ai server terminal di archiviare le informazioni relative a utenti e sessioni in un database denominato directory di sessione. Quando un utente si connette a un server terminal in una farm, directory di sessione di Servizi terminal determina se l'utente dispone già di una sessione in esecuzione su un server terminal e, in tal caso, reindirizza l'utente a tale server terminal.

In Windows Server 2008, il servizio ruolo directory di sessione di Servizi terminal è stato espanso e rinominato gestore sessioni Servizi terminal. Oltre a gestire una directory di sessioni esistenti, broker di sessione di Servizi terminal può anche broker di connessioni in ingresso. Quando broker di sessione di Servizi terminal riceve una connessione in ingresso da un utente, controlla il relativo database per determinare se l'utente dispone di una sessione esistente in un server terminal. In tal caso, broker di sessione di Servizi terminal reindirizza la connessione allo stesso server terminal. In caso contrario, broker di sessione di Servizi terminal determina quale server terminal dispone del minor numero di connessioni e reindirizza la connessione al server.

A partire da Windows Server 2008, Microsoft ha rilasciato anche un Application Programming Interface pubblico (API) per il monitoraggio e l'interazione con le sessioni sui server terminal. Questa API è descritta in informazioni di [riferimento sul plug-in connessione Desktop remoto broker](/windows/desktop/TermServ/terminal-services-virtualization-api-reference). Utilizzando questa API, gli sviluppatori possono creare plug-in di criteri personalizzati che eseguono l'override della logica di reindirizzamento standard di broker di sessione di Servizi terminal. I plug-in personalizzati possono reindirizzare le sessioni ai server terminal, oltre a macchine virtuali, desktop virtuali, server blade e desktop fisici.

In Windows Server 2008 R2 l'architettura di Connessione Desktop remoto broker (gestore connessione Desktop remoto), precedentemente nota come broker di sessione di Servizi terminal, è stata espansa per supportare le connessioni alle macchine virtuali. La nuova architettura supporta la gestione delle sessioni per le macchine virtuali tramite l'API di virtualizzazione Desktop remoto. Gli sviluppatori possono utilizzare questa API per personalizzare la logica utilizzata da gestore connessione Desktop remoto per determinare la destinazione migliore per una connessione client in ingresso.

Desktop remoto API di virtualizzazione offre diversi vantaggi agli sviluppatori:

-   Le interfacce per l'utilizzo di server terminal fisici sono simili a quelle per l'utilizzo delle macchine virtuali.
-   Gli sviluppatori possono sostituire tutta o parte della logica di reindirizzamento standard. Gli sviluppatori possono basarsi sul codice fornito con il prodotto e non devono scrivere tutto da zero.
-   Non è necessario alcun agente di gestione aggiuntivo sul server di gestione o all'interno della sessione.
-   I plug-in di broker di sessione di Servizi terminal sviluppati per l'uso con Windows Server 2008 sono ancora supportati.
-   L'API consente inoltre agli sviluppatori di creare interfacce utente per l'amministrazione host sessione Desktop remoto di server Host sessione Desktop remoto (in precedenza noti come "server terminal") e macchine virtuali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API di virtualizzazione Desktop remoto](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[Riferimento al plug-in di Connessione Desktop remoto broker](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 