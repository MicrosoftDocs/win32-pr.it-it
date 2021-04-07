---
description: La rete di modalità di trasferimento asincrona (ATM) sta emergendo nel mainstream del computer e il supporto per ATM è stato aggiunto a molte parti del sistema operativo.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Qualità del servizio (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884013"
---
# <a name="quality-of-service-telephony-api"></a>Qualità del servizio (API di telefonia)

La rete di modalità di trasferimento asincrona (ATM) sta emergendo nel mainstream del computer e il supporto per ATM è stato aggiunto a molte parti del sistema operativo. TAPI supporta anche gli attributi chiave per stabilire chiamate sulle funzionalità ATM. Il più importante di questi aspetti dal punto di vista dell'applicazione è la possibilità di richiedere, negoziare, rinegoziare e ricevere indicazioni sui parametri di qualità del servizio (QOS) sulle chiamate in ingresso e in uscita.

Le informazioni QOS in TAPI vengono scambiate tra le applicazioni e i provider di servizi in strutture [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) definite in Windows sockets 2,0.

Le applicazioni richiedono QOS per le chiamate in uscita impostando i valori delle informazioni di sessione prima di avviare una sessione di comunicazione. Il provider di servizi tenterà di fornire il QOS specificato e non riuscirà a eseguire la chiamata. L'applicazione può quindi modificare i parametri e ripetere la chiamata. Dopo che è stata stabilita una chiamata, un'applicazione può richiedere una modifica nel QOS.

TAPI fornisce notifiche degli eventi al proprietario o al monitoraggio delle applicazioni in caso di modifica dei livelli QOS.

Il supporto per QOS non è limitato ai trasporti ATM; qualsiasi provider di servizi può implementare le funzionalità QOS.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

* * TAPI 2. x: * *[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **DwSendingFlowspecOffset**, **dwReceivingFlowspecSize** e **dwReceivingFlowspecOffset** membri di [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

* * TAPI 3. x: * *[**ITBasicCallControl:: SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
