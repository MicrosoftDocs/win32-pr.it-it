---
description: DDE di rete viene usato per avviare e gestire le connessioni di rete necessarie per le conversazioni DDE tra applicazioni in esecuzione in computer diversi in una rete.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Informazioni su DDE di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb8f232dc10080a575a6afe500727435bed7913ae95364daf697844c3c65dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756457"
---
# <a name="about-network-dde"></a>Informazioni su DDE di rete

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

DDE di rete viene usato per avviare e gestire le connessioni di rete necessarie per le conversazioni DDE tra applicazioni in esecuzione in computer diversi in una rete. Una conversazione DDE *è* l'interazione tra applicazioni client e server. È possibile usare DDE di rete insieme a DDE e alla libreria di gestione DDE (DDEML) nell'applicazione.

DDE è una forma di comunicazione interprocesso che usa la memoria condivisa per lo scambio di dati tra applicazioni. Le applicazioni possono usare DDE per trasferimenti di dati una sola volta o per scambi in corso e aggiornamento dei dati. Per altre informazioni su DDE, vedere [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).

DDEML semplifica l'attività di aggiunta della funzionalità DDE a un'applicazione. Anziché inviare, pubblicare ed elaborare direttamente messaggi DDE, un'applicazione usa le funzioni fornite da DDEML per gestire le conversazioni DDE. Per altre informazioni su DDEML, vedere [Dynamic Data Exchange Management Library.](../dataxchg/dynamic-data-exchange-management-library.md)

## <a name="network-dde-files"></a>File DDE di rete

Per usare gli elementi API di DDE di rete, è necessario includere il file di intestazione NDDEApi.h nei file di origine e includere il file NDDEApi.lib nella riga di collegamento. È inoltre necessario assicurarsi che il file NDDEApi.dll sia caricato.

Per altre informazioni, vedere i seguenti argomenti:

-   [Agente DDE di rete](network-dde-agent.md)
-   [Condivisioni DDE](dde-shares.md)
-   [Condivisioni e sicurezza attendibili](trusted-shares-and-security.md)
-   [Gestione delle condivisioni DDE](managing-dde-shares.md)

 

 
