---
title: Bluetooth e associare
description: Bluetooth usa la funzione bind per eseguire l'associazione a un socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth e associare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7e7571e8d8a2c1a6dee29dc5f4839af5f1064bc5351cd3a13937f5750dd04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588491"
---
# <a name="bluetooth-and-bind"></a>Bluetooth e associare

Bluetooth usa la [**funzione bind**](/windows/desktop/api/winsock/nf-winsock-bind) per l'associazione a un socket. Per associare un socket Bluetooth, chiamare la **funzione bind** usando la [**struttura \_ BTH SOCKADDR.**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) Usare la **struttura SOCKADDR \_ BTH** con le impostazioni seguenti:

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

Nelle applicazioni client, il membro di porta deve essere zero per consentire l'assegnazione di un endpoint locale appropriato. Nelle applicazioni server, il membro della porta deve essere un numero di porta valido o BT PORT ANY. Le porte assegnate automaticamente tramite BT PORT ANY possono essere richieste successivamente con una chiamata alla \_ \_ funzione \_ \_ [**getsockname.**](bluetooth-and-getsockname.md) L'intervallo valido per la richiesta di una porta RFCOMM specifica è compreso tra 1 e 30. I canali server sono risorse globali e solo 30 canali server sono disponibili per RFCOMM in qualsiasi dispositivo Bluetooth, che deve essere condiviso da tutti i socket Windows che appartengono alla famiglia di indirizzi Bluetooth. Se non è disponibile alcun canale server o se il canale del server specificato è già riservato, la [**chiamata di**](/windows/desktop/api/winsock/nf-winsock-bind) binding non riesce.

Al termine dell'associazione, il canale del server viene riservato fino alla chiusura del socket. Usare la [**funzione getsockname**](bluetooth-and-getsockname.md) per recuperare il numero di canale per la registrazione SDP.

Le applicazioni devono usare l'allocazione automatica per il canale del server.

La [**funzione bind**](/windows/desktop/api/winsock/nf-winsock-bind) non annuncia automaticamente l'applicazione server usando Bluetooth SDP; Le applicazioni devono chiamare [**la funzione WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) per essere trovate da applicazioni Bluetooth remote.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Associare**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 