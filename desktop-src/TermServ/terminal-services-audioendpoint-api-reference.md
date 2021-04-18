---
title: Informazioni di riferimento sull'API Servizi Desktop remoto AudioEndpoint
description: Supporta le interfacce per la registrazione di endpoint audio e il trasporto di dati.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, informazioni di riferimento sull'API AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396483"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Informazioni di riferimento sull'API Servizi Desktop remoto AudioEndpoint

Un *endpoint audio* rappresenta un dispositivo audio, un'API audio o qualsiasi altra origine o sink audio e viene usato per inviare o utilizzare dati dal motore audio. Un endpoint audio deve essere connesso al motore audio tramite una *connessione* e a ogni connessione può essere connesso un solo endpoint. Dopo la registrazione di un endpoint, il motore audio connette l'endpoint alla connessione.

Ogni oggetto endpoint deve implementare le interfacce seguenti:

-   [**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) per abilitare il motore audio per ottenere informazioni sull'endpoint.
-   [**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) per ottenere informazioni sul buffer di dati prima di eseguire un passaggio di elaborazione e inviare una notifica all'endpoint al termine del passaggio.
-   Interfaccia [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) o [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) , a seconda che l'oggetto endpoint stia acquisendo o eseguendo il rendering dell'audio.
-   [**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

Il motore audio utilizza queste interfacce per ottenere informazioni sugli endpoint collegati al motore. L'implementazione dell'endpoint deve fornire il meccanismo per il recapito o l'utilizzo di dati dal motore in base a quanto specificato da tali interfacce.

L'API Servizi Desktop remoto AudioEndpoint supporta i tipi di enumerazione, le interfacce e le strutture.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Tipi di enumerazione Servizi Desktop remoto AudioEndpoint](terminal-services-audioendpoint-enumeration-types.md)
-   [Funzioni di Servizi Desktop remoto AudioEndpoint](remote-desktop-services-audioendpoint-functions.md)
-   [Interfacce di Servizi Desktop remoto AudioEndpoint](terminal-services-audioendpoint-interfaces.md)
-   [Servizi Desktop remoto strutture AudioEndpoint](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Commenti

L'API Servizi Desktop remoto AudioEndpoint è destinata all'uso in scenari Desktop remoto; non è per le applicazioni client.

 

 




