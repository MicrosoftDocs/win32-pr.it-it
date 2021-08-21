---
description: La configurazione e la rimozione di connessioni da punto a punto e da punto a multipunto ATM sono supportate in modo nativo dalla specifica Windows Sockets 2.
ms.assetid: 07e4fcb8-f7b5-450d-a2f4-ba81267ef8ca
title: Controlli atm Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed891f24c16f01025d0bd06da1ea3ec9c0cca01abdcaf3c9950229bf512f0b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051449"
---
# <a name="winsock-atm-controls"></a>Controlli atm Winsock

La configurazione e la rimozione di connessioni da punto a punto e da punto a multipunto ATM sono supportate in modo nativo dalla specifica Windows Sockets 2. In realtà, Windows specifica QoS di Sockets 2 e meccanismi multipoint/multicast indipendenti dal protocollo sono stati progettati con ATM in considerazione, insieme ad altri protocolli. Vedere la sezione 2.7 e l'appendice D della specifica dell'API Windows Sockets 2 rispettivamente per Windows Sockets 2, Quality of Service e Multipoint Support. Pertanto, non è necessario introdurre ioctls specifici di ATM in questo documento.

 

 



