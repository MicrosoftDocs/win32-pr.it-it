---
description: Un provider di eventi può dedicare molto tempo alla creazione di eventi.
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: Ottimizzazione di un provider di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70eaabfbbd462b831059b10590d7959bdef05cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318182"
---
# <a name="optimizing-an-event-provider"></a>Ottimizzazione di un provider di eventi

Un provider di eventi può dedicare molto tempo alla creazione di eventi. Se nessuna applicazione client utilizza gli eventi creati, il provider sta sprecando risorse di sistema. Inoltre, WMI impiega una quantità considerevole di risorse che analizzano e inviano query complesse al provider appropriato. Per evitare lo spreco di risorse di sistema e migliorare le prestazioni del provider di eventi, è possibile implementare l'interfaccia [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) . **IWbemEventProviderQuerySink** monitora le query che le applicazioni client registrano con WMI usando i metodi [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) e [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) . Monitorando le query client registrate, il provider può determinare cosa accade se è necessario inviare messaggi a WMI.

WMI chiama [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) su un provider di eventi quando un consumer client registra una query del filtro eventi che contiene riferimenti a eventi supportati da tale provider di eventi. Il provider di eventi responsabile degli eventi di modifica dell'istanza per la classe **EmailClass** può quindi essere configurato per generare notifiche solo per il **mittente**. Quando il provider riceve una query che richiede la notifica delle modifiche apportate alla proprietà **Subject** , il provider può iniziare a generare tali notifiche. In questo scenario non è necessario che WMI elimini le notifiche che segnalano solo le modifiche del **destinatario** .

Analogamente, WMI chiama [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) su un provider di eventi quando un consumer client Annulla la registrazione di una query del filtro eventi che contiene riferimenti a eventi supportati dal provider di eventi. Lo scopo di **CancelQuery** è che il provider di eventi aggiorni l'elenco degli eventi da inviare.

> [!Note]  
> Se il provider supporta sia [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) che [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink), assicurarsi che l'implementazione del metodo **IUnknown:: QueryInterface** restituisca i puntatori a entrambe le interfacce.

 

 

 



