---
title: Bluetooth e binding
description: Bluetooth usa la funzione di binding per eseguire il binding a un socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth e binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872909"
---
# <a name="bluetooth-and-bind"></a>Bluetooth e binding

Bluetooth usa la funzione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) per eseguire il binding a un socket. Per associare un Socket Bluetooth, chiamare la funzione **Bind** usando la [**struttura \_ BTH di SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) . Usare la **struttura \_ BTH di SOCKADDR** con le impostazioni seguenti:

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

Nelle applicazioni client, il membro della porta deve essere zero per consentire l'assegnazione di un endpoint locale appropriato. Nelle applicazioni server, il membro di porta deve essere un numero di porta valido o una \_ porta BT \_ qualsiasi; le porte assegnate automaticamente usando \_ la porta BT \_ any possono essere eseguite successivamente con una chiamata alla funzione [**getsockname**](bluetooth-and-getsockname.md) . L'intervallo valido per la richiesta di una porta RFCOMM specifica è compreso tra 1 e 30. I canali server sono risorse globali e sono disponibili solo 30 canali server per RFCOMM su qualsiasi dispositivo Bluetooth, che deve essere condiviso da tutti i socket di Windows che appartengono alla famiglia di indirizzi Bluetooth. Se non è disponibile alcun canale server o se il canale server specificato è già riservato, la chiamata di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) ha esito negativo.

Al termine della restituzione dal binding, il canale server viene riservato fino alla chiusura del socket. Usare la funzione [**getsockname**](bluetooth-and-getsockname.md) per recuperare il numero di canale per la registrazione SDP.

Le applicazioni devono utilizzare l'allocazione automatica per il canale server.

La funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) non annuncia automaticamente l'applicazione server tramite il Bluetooth SDP; le applicazioni devono chiamare la funzione [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) per trovare le applicazioni Bluetooth Remote.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**associare**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 