---
description: L'elenco seguente fornisce descrizioni concise di ogni struttura di Winsock ATM. Per altre informazioni su qualsiasi struttura, fare clic sul nome della struttura.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Strutture di Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f45cafef8bcf628f9172f2ad7ce3323d0d5b0c3e2c3912d195615ea2471501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612801"
---
# <a name="winsock-atm-structures"></a>Strutture di Winsock ATM

L'elenco seguente fornisce descrizioni concise di ogni struttura di Winsock ATM. Per altre informazioni su qualsiasi struttura, fare clic sul nome della struttura.



| Struttura ATM                           | Descrizione                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**INDIRIZZO \_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Archivia i dati degli indirizzi ATM per i socket basati su ATM.             |
| [**ATM \_ BHLI**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Identifica le informazioni B-HLI per un socket ATM associato. |
| [**ATM \_ BLLI**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Identifica le informazioni B-LLI per un socket ATM associato. |
| [**sockaddr \_ atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Archivia le informazioni sull'indirizzo del socket per i socket ATM.         |



 

Per i servizi ATM nativi, usare AF ATM per la famiglia di indirizzi e la struttura degli indirizzi \_ del socket [**sockaddr \_ atm.**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) Per aprire un socket ATM nativo, passare rispettivamente AF \_ ATM, SOCK RAW e \_ ATMPROTO \_ AAL5 o ATMPROTO \_ AALUSER nella funzione [**socket.**](/windows/desktop/api/Winsock2/nf-winsock2-socket)

 

 



