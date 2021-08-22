---
description: L'architettura Windows Sockets 2 (Winsock) è conforme all'architettura Windows Open System Architecture (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows Architettura dei socket 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad3dd29f692df94e1f66c13c00c75eeca36fb04d18c5f2e95e67b91773698f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569156"
---
# <a name="windows-sockets-2-architecture"></a>Windows Architettura dei socket 2

L'architettura Windows Sockets 2 è conforme all'architettura Windows Open System Architecture (WOSA), come illustrato di seguito:

![Architettura di Windows Sockets 2](images/ovrvw2-1.png)

Winsock definisce un'interfaccia SPI (Service Provider Interface) standard tra l'API (Application Programming Interface), con le relative funzioni esportate da WS232.dll e \_ dagli stack di protocolli. Di conseguenza, il supporto di Winsock non è limitato agli stack di protocolli TCP/IP, come nel caso di Windows Sockets 1.1.

Con l'architettura Windows Sockets 2, per i fornitori di stack non è necessario o auspicabile fornire la propria implementazione di WS232.dll, poiché un singolo32.dll WS2 deve funzionare in tutti gli \_ \_ stack. Gli SS232.dll e di compatibilità devono essere visualizzati nello stesso modo \_ di un componente del sistema operativo.

 

 



