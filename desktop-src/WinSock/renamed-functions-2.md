---
description: In due casi era necessario rinominare le funzioni usate nei socket Berkeley per evitare conflitti con altre funzioni dell'API Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Funzioni rinominate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880458"
---
# <a name="renamed-functions"></a>Funzioni rinominate

In due casi era necessario rinominare le funzioni usate nei socket Berkeley per evitare conflitti con altre funzioni dell'API Microsoft Windows.

## <a name="close-and-closesocket"></a>Close e chiamata closesocket

I socket sono rappresentati da descrittori di file standard nei socket Berkeley, quindi è possibile usare la funzione **Close** per chiudere i socket e i file normali. Sebbene nessun elemento in Windows Sockets impedisca a un'implementazione di utilizzare handle di file normali per identificare i socket, non è necessario alcun elemento. In Windows è necessario chiudere i socket usando la routine [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) . IN Windows, l'utilizzo della funzione **Close** per chiudere un socket non è corretto e gli effetti di tale operazione non sono definiti da questa specifica.

## <a name="ioctl-and-ioctlsocketwsaioctl"></a>IOCTL e ioctlsocket/WSAIoctl

Vari sistemi di runtime del linguaggio C utilizzano le IOCTL per scopi non correlati a Windows Sockets. Di conseguenza, la funzione [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) e la funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) sono state definite per gestire le funzioni socket eseguite da **IOCTL** e **fcntl** nella distribuzione del software Berkeley.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



