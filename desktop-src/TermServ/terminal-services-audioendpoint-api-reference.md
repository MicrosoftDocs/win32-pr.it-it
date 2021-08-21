---
title: Servizi Desktop remoto informazioni di riferimento sulle API AudioEndpoint
description: Supporta le interfacce per la registrazione dell'endpoint audio e il trasporto dati.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto , Informazioni di riferimento sulle API AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9a7aa83b519ca10128f9bea3b945492f387c0498c81f8b2959cb9830b91dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000091"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Servizi Desktop remoto informazioni di riferimento sulle API AudioEndpoint

Un *endpoint audio* rappresenta un dispositivo audio, un'API audio o qualsiasi altra origine o sink audio e viene usato per inviare o utilizzare dati dal motore audio. Un endpoint audio deve essere connesso al motore audio tramite una connessione *e* a ogni connessione può essere connesso un solo endpoint. Dopo la registrazione di un endpoint, il motore audio collega l'endpoint alla connessione.

Ogni oggetto endpoint deve implementare le interfacce seguenti:

-   [**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) per consentire al motore audio di ottenere informazioni sull'endpoint.
-   [**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) per ottenere informazioni sul buffer di dati prima di eseguire un passaggio di elaborazione e notificare all'endpoint quando il passaggio è completo.
-   Interfaccia [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) o [**IAudioOutputEndpointRT,**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) a seconda che l'oggetto endpoint acquisisca o eserciti il rendering dell'audio.
-   [**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

Il motore audio usa queste interfacce per ottenere informazioni sugli endpoint collegati al motore. L'implementazione dell'endpoint deve fornire il meccanismo per recapitare o utilizzare i dati dal motore come specificato da queste interfacce.

L Servizi Desktop remoto'API AudioEndpoint supporta tipi di enumerazione, interfacce e strutture.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Servizi Desktop remoto tipi di enumerazione AudioEndpoint](terminal-services-audioendpoint-enumeration-types.md)
-   [Servizi Desktop remoto Funzioni AudioEndpoint](remote-desktop-services-audioendpoint-functions.md)
-   [Servizi Desktop remoto interfacce AudioEndpoint](terminal-services-audioendpoint-interfaces.md)
-   [Servizi Desktop remoto strutture AudioEndpoint](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Commenti

L Servizi Desktop remoto'API AudioEndpoint è da usare in Desktop remoto scenari. non è per le applicazioni client.

 

 




