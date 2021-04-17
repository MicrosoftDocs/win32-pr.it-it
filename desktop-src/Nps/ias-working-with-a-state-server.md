---
title: Utilizzo di un server di stato
description: NPS esegue l'autenticazione usando un database configurato nel sito del server NPS.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299923"
---
# <a name="working-with-a-state-server"></a>Utilizzo di un server di stato

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

NPS esegue l'autenticazione usando un database configurato nel sito del server NPS. Questo database di autenticazione può essere il database utente per un dominio di Windows oppure può attingere alle informazioni utente ottenute dalla Active Directory di Windows. Il diagramma seguente illustra una configurazione tipica che mostra il modo in cui NPS interagisce con i database di autenticazione, ad esempio un database utente di dominio di Windows o Active Directory. Nel diagramma viene inoltre illustrato il modo in cui NPS può interagire con un server di stato fornito da terze parti. Lo scopo principale di un server di stato è limitare il numero di sessioni di accesso simultanee che possono essere eseguite da un singolo utente.

![NPS che interagisce con il server di stato e i database di autenticazione](images/ias02.png)

Esistono due punti di interazione tra NPS e il server di stato. Una delle interazioni si verifica quando NPS riceve una richiesta di autenticazione dal server NAS. Il server di stato fornisce informazioni dal database per determinare se accettare o rifiutare la richiesta. L'altra interazione si verifica quando NPS riceve le richieste di Accounting dal server NAS. Il server di stato utilizza le informazioni contenute in queste richieste di contabilità per aggiornare il relativo database.

Per ulteriori informazioni sui server di stato, vedere:

-   [Considerazioni sulla progettazione del server di stato](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio di autenticazione Internet e server dei criteri di rete](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticazione, autorizzazione e accounting RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registrazione con server dei criteri di rete](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 