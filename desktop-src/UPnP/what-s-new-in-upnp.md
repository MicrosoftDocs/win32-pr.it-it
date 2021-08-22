---
title: Novità delle API UPnP
description: Le API UPnP™ hanno nuove funzionalità e documentazione aggiornata per Windows XP SP2. La tabella seguente identifica la nuova documentazione.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68ab872eab498e80ec8d30f996f839c73432875d02ec8d32060595ce8d6482b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057999"
---
# <a name="whats-new-in-the-upnp-apis"></a>Novità delle API UPnP

Le API UPnP™ hanno nuove funzionalità e documentazione aggiornata per Windows XP SP2. La tabella seguente identifica la nuova documentazione.



| Funzionalità                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Questa nuova interfaccia consente a un dispositivo ospitato di ottenere informazioni su un richiedente (ovvero un punto di controllo) e sulla richiesta. Include tre metodi, ognuno dei quali fornisce un tipo diverso di informazioni.                                                                                                                                                              |
| [Implementazione del comportamento del dispositivo](implementing-device-behavior.md) | Questo argomento include una nuova sezione che illustra come ottenere informazioni sull'endpoint usando la [**nuova interfaccia IUPnPRemoteEndpointInfo.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)                                                                                                                                                                                                     |
| [Configurazione Impostazioni](configuration-settings.md)             | Questo nuovo argomento fornisce informazioni sulle impostazioni del Registro di sistema che influiscono sul comportamento delle API UPnP.                                                                                                                                                                                                                                                                    |
| [Codici di errore del dispositivo](device-error-codes.md)                     | Questo nuovo argomento illustra come un codice di errore da un dispositivo viene convertito in un valore HRESULT e viceversa. Una conoscenza di questo processo è necessaria per valutare un valore HRESULT restituito dai metodi [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**IUPnPService::QueryStateVariable.**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) |



 

 

 




