---
description: La rete atm (Asynchronous Transfer Mode) sta emergendo nel mainstream dell'elaborazione e il supporto per ILM è stato aggiunto a molte parti del sistema operativo.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Quality of Service (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131f54d69cd44799f9ea694fe83d50f28fded0ac7c8c15dabfd7a2db499b2293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761232"
---
# <a name="quality-of-service-telephony-api"></a>Quality of Service (API di telefonia)

La rete atm (Asynchronous Transfer Mode) sta emergendo nel mainstream dell'elaborazione e il supporto per ILM è stato aggiunto a molte parti del sistema operativo. TAPI supporta anche gli attributi chiave per stabilire chiamate nelle strutture del bancomat. Il più importante dal punto di vista dell'applicazione è la possibilità di richiedere, negoziare, rinegoziare e ricevere indicazioni dei parametri QOS (Quality of Service) nelle chiamate in ingresso e in uscita.

Le informazioni QOS in TAPI vengono scambiate tra applicazioni e provider di servizi in strutture [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) definite in Windows Sockets 2.0.

Le applicazioni richiedono QOS nelle chiamate in uscita impostando i valori delle informazioni sulla sessione prima di avviare una sessione di comunicazione. Il provider di servizi tenterà di fornire il QOS specificato e, in caso contrario, non riuscirà a eseguire la chiamata. L'applicazione può quindi modificare i parametri e ripetere la chiamata. Dopo aver stabilito una chiamata, un'applicazione può richiedere una modifica in QOS.

TAPI fornisce notifiche degli eventi al proprietario o al monitoraggio delle applicazioni in caso di modifiche nei livelli QOS.

Il supporto per QOS non è limitato ai trasporti dei bancomat. qualsiasi provider di servizi può implementare le funzionalità QOS.

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x: **[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize** e **dwReceivingFlowspecOffset** membri di [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

**TAPI 3.x: **[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
