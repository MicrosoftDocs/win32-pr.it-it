---
title: Informazioni su DDEML
description: In questo argomento viene illustrato lo scambio dinamico dei dati.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Windows Interfaccia utente,Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), informazioni
- DDE (Dynamic Data Exchange),about
- scambio di dati, Dynamic Data Exchange (DDE)
- Windows Interfaccia utente,Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange Management Library (DDEML), informazioni
- DDEML (Dynamic Data Exchange Management Library), informazioni
- scambio di dati, Dynamic Data Exchange Management Library (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755d4efea534918ac3fd3da46364e3cb528e4199498ea7533c1635af6780cc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545562"
---
# <a name="about-the-ddeml"></a>Informazioni su DDEML

Dynamic Data Exchange (DDE) differisce dal meccanismo di trasferimento dei dati degli Appunti. Una differenza è che gli Appunti vengono quasi sempre usati come risposta una sola volta a un'azione specifica da parte dell'utente, ad esempio facendo clic su **Incolla** da un menu. Anche se può essere avviata anche da un utente, DDE continua in genere senza un ulteriore coinvolgimento dell'utente.

La Dynamic Data Exchange Management Library (DDEML) fornisce un'interfaccia che semplifica l'attività di aggiunta della funzionalità DDE a un'applicazione. Anziché inviare, pubblicare ed elaborare direttamente messaggi DDE, un'applicazione usa le funzioni fornite da DDEML per gestire le conversazioni DDE. Una conversazione DDE è l'interazione tra applicazioni client e server. DDEML consente anche di gestire le stringhe e i dati condivisi tra le applicazioni DDE. Invece di usare atom e puntatori a oggetti di memoria condivisa, le applicazioni DDE creano e scambiano handle di stringa, che identificano stringhe e handle di dati, che identificano gli oggetti DDE. DDEML fornisce una funzione ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) che consente a un'applicazione server di registrare i nomi dei servizi supportati. I nomi dei servizi vengono quindi trasmessi ad altre applicazioni del sistema, che usano i nomi per connettersi al server. DDEML garantisce anche la compatibilità tra le applicazioni DDE richiedendole di implementare il protocollo DDE in modo coerente.

Le applicazioni esistenti che usano il protocollo DDE basato su messaggi sono completamente compatibili con quelle che usano DDEML. in altre informazioni, un'applicazione che usa DDE basata su messaggi può stabilire conversazioni ed eseguire transazioni con le applicazioni usando DDEML. Invece di usare i messaggi DDE nella nuova applicazione, sfruttare DDEML e i numerosi miglioramenti che offre.

Per usare DDEML, è necessario includere DDEML. File di intestazione H nei file di origine, collegamento con USER32. LIB e assicurarsi che il DDEML.DLL si trovi nel percorso del sistema.

Ogni volta che una funzione DDEML ha esito negativo, un'applicazione può chiamare la [**funzione DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) per determinare la causa dell'errore. **DdeGetLastError** restituisce un valore di errore che specifica la causa dell'errore più recente.

 

 




