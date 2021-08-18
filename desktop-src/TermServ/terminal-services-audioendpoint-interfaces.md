---
title: Servizi Desktop remoto interfacce AudioEndpoint
description: Le interfacce seguenti vengono usate con l'API AudioEndpoint.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec12cd3d4648f3ed357e898f75850e77b3b679d59a92d9f0518f809ba52f58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000071"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Servizi Desktop remoto interfacce AudioEndpoint

Le interfacce seguenti vengono usate con l'API AudioEndpoint.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

Inizializza un oggetto endpoint del dispositivo e ottiene le funzionalità del dispositivo che rappresenta.

</dd> <dt>

[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

Fornisce informazioni al motore audio su un endpoint audio. Questa interfaccia viene implementata da un endpoint audio.

</dd> <dt>

[**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

Controlla lo stato del flusso di un endpoint.

</dd> <dt>

[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Ottiene la differenza tra le posizioni correnti di lettura e scrittura nel buffer dell'endpoint.

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

L Servizi Desktop remoto API AudioEndpoint è da usare in Desktop remoto scenari. non è per le applicazioni client.

 

 




