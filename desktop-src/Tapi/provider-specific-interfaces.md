---
description: TAPI 3 supporta l'integrazione di interfacce specifiche del provider di servizi negli oggetti standard, consentendo alle applicazioni di sfruttare le funzionalità specifiche del provider.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Provider-Specific interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09290bf6d2ade55a9e9d2b0f51315acfc5488805b6c19b23679e00708ddaed45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060569"
---
# <a name="provider-specific-interfaces"></a>Provider-Specific interfacce

TAPI 3 supporta l'integrazione di interfacce specifiche del provider di servizi negli oggetti standard, consentendo alle applicazioni di sfruttare le funzionalità specifiche del provider. TAPI 3 consente inoltre ai provider di servizi di recapitare eventi specifici del fornitore alle applicazioni come oggetti COM tramite la stessa interfaccia in cui l'applicazione riceve eventi standard.

TAPI ottiene questa integrazione aggregando oggetti specifici del provider con gli oggetti standard ( TAPI, Address, Terminal, Call e CallHub) e inviando o delegando metodi sconosciuti a questi oggetti specifici del provider.

Ad esempio, un provider di servizi può consentire alle applicazioni di ottenere informazioni su una chiamata oltre a quanto esposto [**dall'interfaccia ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) Il fornitore deve definire un'interfaccia che consenta alle applicazioni di eseguire queste query aggiuntive e implementare tale interfaccia su un oggetto. Questo oggetto implementa anche un'interfaccia di query sulle informazioni del fornitore in modo che un'applicazione possa individuare i tipi di funzioni specifiche del provider disponibili.

Quando l'applicazione ottiene un riferimento a un oggetto chiamata, l'applicazione può usare la nuova interfaccia specifica del provider e i relativi metodi come se fossero implementati dall'oggetto chiamata stesso.

Per un elenco di tutte le interfacce MSP standard, vedere Informazioni di riferimento su [Media Service Provider Interface (MSPI).](media-service-provider-interface-mspi-reference.md)

Per un elenco di tutte le interfacce specifiche di [IPConf MSP, vedere IpConf MSP Interfaces](ipconf-msp-interfaces.md) (Interfacce MSP IPConf).

 

 



