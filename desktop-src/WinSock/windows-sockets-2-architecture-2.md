---
description: L'architettura Windows Sockets 2 (Winsock) è conforme all'architettura di Windows Open System (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Architettura di Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130415"
---
# <a name="windows-sockets-2-architecture"></a>Architettura di Windows Sockets 2

L'architettura Windows Sockets 2 è conforme all'architettura di Windows Open System (WOSA), come illustrato di seguito:

![architettura di Windows Sockets 2](images/ovrvw2-1.png)

Winsock definisce un'interfaccia del provider di servizi (SPI) standard tra il Application Programming Interface (API), con le funzioni esportate da WS2 \_32.dll e gli stack di protocolli. Di conseguenza, il supporto Winsock non è limitato agli stack di protocolli TCP/IP come nel caso di Windows Sockets 1,1.

Con l'architettura Windows Sockets 2, non è necessario o auspicabile, perché i fornitori di stack forniscano una propria implementazione di WS2 \_32.dll, dal momento che un singolo WS2 \_32.dll deve funzionare in tutti gli stack. Gli WS2 \_32.dll e gli shim di compatibilità devono essere visualizzati allo stesso modo di un componente del sistema operativo.

 

 



