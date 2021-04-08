---
title: Bluetooth e getsockopt
description: Bluetooth usa la funzione getsockopt per eseguire una query sui diversi parametri associati al canale server o alla connessione.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth e getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728362"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth e getsockopt

Bluetooth usa la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per eseguire una query sui diversi parametri associati al canale server o alla connessione. L'uso di **getsockopt** con Bluetooth prevede i requisiti seguenti:

-   Il parametro *s* di [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve essere un Socket Bluetooth valido.
-   Il parametro *Level* di [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve essere Sol \_ rfcomm.

Per un elenco delle opzioni dei Socket Bluetooth disponibili, vedere Opzioni per il connettore [Bluetooth e il socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 