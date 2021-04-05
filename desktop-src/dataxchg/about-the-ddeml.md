---
title: Informazioni su DDEML
description: In questo argomento viene illustrato lo scambio dinamico di dati.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), informazioni
- DDE (Dynamic Data Exchange), informazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Libreria di gestione Dynamic Data Exchange (DDEML), informazioni
- DDEML (libreria di gestione Dynamic Data Exchange), informazioni
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516087"
---
# <a name="about-the-ddeml"></a>Informazioni su DDEML

Dynamic Data Exchange (DDE) differisce dal meccanismo di trasferimento dei dati degli Appunti. Una differenza consiste nel fatto che gli Appunti vengono quasi sempre usati come risposta monouso a un'azione specifica da parte dell'utente, ad esempio facendo clic su **Incolla** da un menu. Sebbene il DDE possa essere avviato anche da un utente, in genere continua senza ulteriore coinvolgimento dell'utente.

La libreria di gestione Dynamic Data Exchange (DDEML) fornisce un'interfaccia che semplifica l'attività di aggiunta della funzionalità DDE a un'applicazione. Anziché inviare, inviare ed elaborare direttamente i messaggi DDE, un'applicazione utilizza le funzioni fornite da DDEML per gestire le conversazioni DDE. Una conversazione DDE è l'interazione tra applicazioni client e server. Il DDEML fornisce anche un mezzo per gestire le stringhe e i dati condivisi tra le applicazioni DDE. Anziché utilizzare gli atomi e i puntatori agli oggetti Shared Memory, le applicazioni DDE creano e scambiano handle di stringa, che identificano le stringhe e gli handle di dati, che identificano gli oggetti DDE. DDEML fornisce una funzione ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) che consente a un'applicazione server di registrare i nomi di servizio supportati. I nomi dei servizi vengono quindi trasmessi ad altre applicazioni nel sistema, che usano i nomi per connettersi al server. Il DDEML garantisce inoltre la compatibilità tra applicazioni DDE richiedendo loro di implementare il protocollo DDE in modo coerente.

Le applicazioni esistenti che utilizzano il protocollo DDE basato su messaggi sono completamente compatibili con quelle che utilizzano DDEML; ovvero, un'applicazione che utilizza un DDE basato su messaggi può stabilire conversazioni ed eseguire transazioni con le applicazioni utilizzando DDEML. Anziché utilizzare i messaggi DDE nella nuova applicazione, sfruttare i vantaggi offerti da DDEML e dai numerosi miglioramenti offerti.

Per usare DDEML, è necessario includere il DDEML. File di intestazione H nei file di origine, collegamento con USER32. File LIB e assicurarsi che il file di DDEML.DLL si trovi nel percorso del sistema.

Ogni volta che una funzione DDEML ha esito negativo, un'applicazione può chiamare la funzione [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) per determinare la cause dell'errore. **DdeGetLastError** restituisce un valore di errore che specifica la ragione dell'errore più recente.

 

 




