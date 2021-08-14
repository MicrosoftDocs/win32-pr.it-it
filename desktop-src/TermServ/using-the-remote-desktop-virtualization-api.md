---
title: Uso dell'API Desktop remoto Virtualization
description: Gli sviluppatori possono usare questa API per personalizzare la logica utilizzata da Gestore connessione Desktop remoto per determinare la destinazione migliore per una connessione client in ingresso.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto , usando l'API di virtualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7075c3a0cfcabc2df0dcb8438b7de5a748eb2b0340e26bf3d1e51afdb182f81e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423631"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Uso dell'API Desktop remoto Virtualization

Il servizio ruolo Directory sessione Servizi terminal consente ai server terminal di archiviare le informazioni utente e sessione in un database denominato directory di sessione. Quando un utente si connette a un server terminal in una farm, directory di sessione di Servizi terminal determina se l'utente ha già una sessione in esecuzione su un server terminal e, in tal caso, reindirizza l'utente a tale server terminal.

In Windows Server 2008, il servizio ruolo Directory sessione Servizi terminal è stato espanso e rinominato Gestore di sessione Servizi terminal . Oltre a gestire una directory di sessioni esistenti, TS Session Broker può anche gestire le connessioni in ingresso. Quando Broker sessione Servizi terminal riceve una connessione in ingresso da un utente, controlla il database per determinare se l'utente dispone di una sessione esistente in un server terminal. In tal caso, Gestore sessione Servizi terminal reindirizza la connessione allo stesso server terminal. In caso contrario, TS Session Broker determina quale server terminal dispone del numero più breve di connessioni e reindirizza la connessione a tale server.

A partire da Windows Server 2008, Microsoft ha anche rilasciato un'API (Application Programming Interface) pubblica per il monitoraggio e l'interazione con le sessioni nei server terminal. Questa API è descritta in [informazioni Connessione Desktop remoto plug-in di Broker.](/windows/desktop/TermServ/terminal-services-virtualization-api-reference) Usando questa API, gli sviluppatori possono creare plug-in di criteri personalizzati che eseguono l'override della logica di reindirizzamento standard di TS Session Broker. I plug-in personalizzati possono reindirizzare le sessioni ai server terminal, nonché alle macchine virtuali, ai desktop virtuali, ai server blade e ai desktop fisici.

In Windows Server 2008 R2, l'architettura di Connessione Desktop remoto Broker (Gestore connessione Desktop remoto) (in precedenza nota come Gestore sessione Servizi terminal) è stata espansa per supportare le connessioni alle macchine virtuali. La nuova architettura supporta la gestione delle sessioni per le macchine virtuali tramite l'API Desktop remoto Virtualization. Gli sviluppatori possono usare questa API per personalizzare la logica utilizzata da Gestore connessione Desktop remoto per determinare la destinazione migliore per una connessione client in ingresso.

Desktop remoto'API di virtualizzazione offre diversi vantaggi agli sviluppatori:

-   Le interfacce per l'uso di server terminal fisici sono simili a quelle per l'uso di macchine virtuali.
-   Gli sviluppatori possono sostituire tutta o parte della logica di reindirizzamento standard. Gli sviluppatori possono basarsi sul codice fornito con il prodotto e non devono scrivere tutto da zero.
-   Non è necessario alcun agente di gestione aggiuntivo nel server di gestione o all'interno della sessione.
-   I plug-in di TS Session Broker sviluppati per l'uso con Windows Server 2008 sono ancora supportati.
-   L'API consente inoltre agli sviluppatori di creare interfacce utente per l'amministrazione di server host sessione Desktop remoto (host sessione Desktop remoto) (precedentemente noti come "server terminal") e macchine virtuali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Desktop remoto informazioni di riferimento sulle API di virtualizzazione](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[informazioni di riferimento sul plug-in Connessione Desktop remoto Broker](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 