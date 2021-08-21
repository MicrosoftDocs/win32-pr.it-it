---
description: Un provider di eventi può dedicare molto tempo alla creazione di eventi.
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: Ottimizzazione di un provider di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613fa6b054f979d0f7d1a33a87f927df9ef129a280cf7cd1675cbe0cf9818473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923408"
---
# <a name="optimizing-an-event-provider"></a>Ottimizzazione di un provider di eventi

Un provider di eventi può dedicare molto tempo alla creazione di eventi. Se nessuna applicazione client usa gli eventi creati, il provider sta sprecando le risorse di sistema. WMI spende inoltre una notevole quantità di risorse per l'analisi e l'invio di query complesse al provider appropriato. Per evitare lo spreco di risorse di sistema e migliorare le prestazioni del provider di eventi, è possibile implementare [**l'interfaccia IWbemEventProviderQuerySink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) **IWbemEventProviderQuerySink** monitora le query registrate dalle applicazioni client con WMI usando i [**metodi NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) [**e CancelQuery.**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) Monitorando le query client registrate, il provider può determinare se è necessario inviare messaggi a WMI.

WMI chiama [**NewQuery su**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) un provider di eventi quando un consumer client registra una query di filtro eventi che contiene riferimenti agli eventi supportati da tale provider di eventi. Il provider di eventi responsabile degli eventi di modifica dell'istanza per la **classe EmailClass** può quindi essere configurato per generare notifiche solo per il **mittente.** Quando il provider riceve una query che  richiede una notifica delle modifiche alla proprietà dell'oggetto, il provider può iniziare a generare tali notifiche. In questo scenario, WMI non è necessario per rimuovere le notifiche che segnalano solo le **modifiche dei destinatari.**

Analogamente, WMI chiama [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) su un provider di eventi quando un consumer client annulla la registrazione di una query di filtro eventi che contiene riferimenti agli eventi supportati dal provider di eventi. Lo scopo di **CancelQuery** è che il provider di eventi aggiorni l'elenco degli eventi da inviare.

> [!Note]  
> Se il provider supporta [**sia IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) che [**IWbemEventProviderQuerySink,**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)assicurarsi che l'implementazione del metodo **IUnknown::QueryInterface** restituisca puntatori a entrambe le interfacce.

 

 

 



