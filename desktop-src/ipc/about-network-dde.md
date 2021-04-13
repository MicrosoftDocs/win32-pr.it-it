---
description: La rete DDE viene utilizzata per avviare e gestire le connessioni di rete necessarie per le conversazioni DDE tra le applicazioni in esecuzione in computer diversi in una rete.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Informazioni su DDE di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345086"
---
# <a name="about-network-dde"></a>Informazioni su DDE di rete

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

La rete DDE viene utilizzata per avviare e gestire le connessioni di rete necessarie per le conversazioni DDE tra le applicazioni in esecuzione in computer diversi in una rete. Una *conversazione* DDE è l'interazione tra applicazioni client e server. Utilizzare la rete DDE insieme a DDE e la libreria di gestione DDE (DDEML) nell'applicazione.

DDE è una forma di comunicazione interprocesso che utilizza la memoria condivisa per scambiare dati tra le applicazioni. Le applicazioni possono utilizzare DDE per i trasferimenti di dati una volta o per gli scambi in corso e per l'aggiornamento dei dati. Per ulteriori informazioni su DDE, vedere [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).

DDEML semplifica l'attività di aggiunta della funzionalità DDE a un'applicazione. Anziché inviare, inviare ed elaborare direttamente i messaggi DDE, un'applicazione utilizza le funzioni fornite da DDEML per gestire le conversazioni DDE. Per ulteriori informazioni su DDEML, vedere [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="network-dde-files"></a>File DDE di rete

Per usare gli elementi API del DDE di rete, è necessario includere il file di intestazione NDDEApi. h nei file di origine e includere il file NDDEApi. lib nella riga di collegamento. È inoltre necessario assicurarsi che il file di NDDEApi.dll venga caricato.

Per altre informazioni, vedere i seguenti argomenti:

-   [Agente DDE di rete](network-dde-agent.md)
-   [Condivisioni DDE](dde-shares.md)
-   [Condivisioni attendibili e sicurezza](trusted-shares-and-security.md)
-   [Gestione delle condivisioni DDE](managing-dde-shares.md)

 

 
