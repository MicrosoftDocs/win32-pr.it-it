---
title: Bluetooth e setsockopt
description: Bluetooth usa la funzione setsockopt per impostare vari parametri associati al canale server o alla connessione.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth e setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337751"
---
# <a name="bluetooth-and-setsockopt"></a>Bluetooth e setsockopt

Bluetooth usa la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per impostare vari parametri associati al canale server o alla connessione. L'uso di **setsockopt** con Bluetooth prevede i requisiti seguenti:

-   Il parametro *s* di [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere un Socket Bluetooth valido.
-   Il parametro *Level* di [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere Sol \_ rfcomm.

Per un elenco delle opzioni dei Socket Bluetooth disponibili, vedere Opzioni per il connettore [Bluetooth e il socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 