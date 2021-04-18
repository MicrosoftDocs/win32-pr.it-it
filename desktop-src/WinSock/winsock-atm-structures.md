---
description: Nell'elenco seguente vengono fornite descrizioni concise di ogni struttura ATM di Winsock. Per ulteriori informazioni su qualsiasi struttura, fare clic sul nome della struttura.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Strutture ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308862"
---
# <a name="winsock-atm-structures"></a>Strutture ATM Winsock

Nell'elenco seguente vengono fornite descrizioni concise di ogni struttura ATM di Winsock. Per ulteriori informazioni su qualsiasi struttura, fare clic sul nome della struttura.



| Struttura ATM                           | Descrizione                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**\_indirizzo ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Archivia i dati dell'indirizzo ATM per i socket basati su ATM.             |
| [**\_BHLI ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Identifica le informazioni B-HLI per un socket ATM associato. |
| [**\_BLLI ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Identifica le informazioni B-LLI per un socket ATM associato. |
| [**sockaddr \_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Archivia le informazioni sull'indirizzo del socket per i socket ATM.         |



 

Per i servizi ATM nativi, usare AF \_ ATM per la famiglia di indirizzi e la struttura di indirizzi del socket [**\_ ATM sockaddr**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) . Per aprire un socket ATM nativo, passare \_ rispettivamente AF ATM, Sock \_ RAW e ATMPROTO \_ AAL5 o ATMPROTO \_ AALUSER nella funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) .

 

 



