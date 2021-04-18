---
title: Interfacce di Servizi Desktop remoto AudioEndpoint
description: Con l'API AudioEndpoint vengono usate le interfacce seguenti.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298031"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Interfacce di Servizi Desktop remoto AudioEndpoint

Con l'API AudioEndpoint vengono usate le interfacce seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

Inizializza un oggetto endpoint dispositivo e ottiene le funzionalità del dispositivo che rappresenta.

</dd> <dt>

[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

Fornisce informazioni al motore audio di un endpoint audio. Questa interfaccia viene implementata da un endpoint audio.

</dd> <dt>

[**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

Controlla lo stato del flusso di un endpoint.

</dd> <dt>

[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Ottiene la differenza tra le posizioni di lettura e scrittura correnti nel buffer dell'endpoint.

</dd> <dt>

[**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

Ottiene il buffer di input per ogni passaggio di elaborazione.

</dd> <dt>

[**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

Ottiene il buffer di output per ogni passaggio di elaborazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'API Servizi Desktop remoto AudioEndpoint è destinata all'uso in scenari Desktop remoto; non è per le applicazioni client.

 

 




