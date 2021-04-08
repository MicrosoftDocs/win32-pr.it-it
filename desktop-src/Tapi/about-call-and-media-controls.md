---
description: I controlli della chiamata e dei supporti TAPI 3 sono un set generico di oggetti COM, interfacce e metodi per effettuare chiamate tra due o più computer.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: Informazioni sui controlli Call e media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886010"
---
# <a name="about-call-and-media-controls"></a>Informazioni sui controlli Call e media

I controlli della chiamata e dei supporti TAPI 3 sono un set generico di oggetti COM, interfacce e metodi per effettuare chiamate tra due o più computer. Nel contesto di TAPI 3, *Call* si riferisce non solo alla trasmissione vocale sulla rete PSTN (Public Switched Telephone), ma a qualsiasi meccanismo di supporto e trasporto per cui sono presenti i provider di servizi, ad esempio una conferenza multicast multimediale in esecuzione su una rete Intranet aziendale.

I cinque oggetti principali nella chiamata TAPI 3 e nell'architettura del controllo multimediale sono [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md)e [CallHub](callhub-object.md). Inoltre, è stato effettuato il provisioning per [interfacce specifiche del provider](provider-specific-interfaces.md).

Il diagramma seguente illustra il modo in cui questi oggetti interagiscono.

![interazioni tra la chiamata a TAPI 3,0 e gli oggetti di controllo multimediale](images/sdkobj2.png)

## <a name="features"></a>Funzionalità

-   Astrae sia la funzionalità chiamata che la funzionalità multimediale per consentire protocolli di comunicazione diversi e apparentemente incompatibili per esporre un'interfaccia comune alle applicazioni.
-   In base alla Component Object Model (COM), le applicazioni possono essere scritte in quasi tutti i linguaggi. Se sono necessarie ulteriori informazioni su COM, consultare Platform Software Development Kit (SDK).
-   Controllo delle chiamate fornito da provider di servizi di telefonia (TSPs), che implementano meccanismi specifici del trasporto.
-   Controllo multimediale fornito da provider di servizi multimediali (MSPs). MSPs correnti usano DirectShow. DirectShow è un sistema modulare di componenti collegabili, denominati filtri, disposti in una configurazione denominata grafico a filtro. Il gestore del grafo dei filtri controlla la connessione di questi filtri e controlla il flusso di dati del flusso. Per ulteriori informazioni su DirectShow, consultare Platform SDK.

 

 



