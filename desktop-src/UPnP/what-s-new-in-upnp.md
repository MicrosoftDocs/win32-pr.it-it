---
title: Novità delle API UPnP
description: Per le API™ UPnP sono disponibili nuove funzionalità e una documentazione aggiornata per Windows XP SP2. La tabella seguente identifica la nuova documentazione.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714350"
---
# <a name="whats-new-in-the-upnp-apis"></a>Novità delle API UPnP

Per le API™ UPnP sono disponibili nuove funzionalità e una documentazione aggiornata per Windows XP SP2. La tabella seguente identifica la nuova documentazione.



| Funzionalità                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Questa nuova interfaccia consente a un dispositivo ospitato di ottenere informazioni su un richiedente, ovvero un punto di controllo, e la richiesta. Sono inclusi tre metodi, ognuno dei quali fornisce un tipo diverso di informazioni.                                                                                                                                                              |
| [Implementazione del comportamento del dispositivo](implementing-device-behavior.md) | In questo argomento è inclusa una nuova sezione in cui viene illustrato come ottenere informazioni sugli endpoint tramite la nuova interfaccia [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .                                                                                                                                                                                                     |
| [Impostazioni di configurazione](configuration-settings.md)             | Questo nuovo argomento fornisce informazioni sulle impostazioni del registro di sistema che influiscono sul comportamento delle API UPnP.                                                                                                                                                                                                                                                                    |
| [Codici di errore del dispositivo](device-error-codes.md)                     | Questo nuovo argomento illustra come un codice di errore di un dispositivo viene convertito in un valore HRESULT e viceversa. È necessario comprendere questo processo per valutare un valore HRESULT restituito dai metodi [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**IUPnPService:: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) . |



 

 

 




