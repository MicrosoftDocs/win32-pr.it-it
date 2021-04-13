---
description: È sempre necessario tenere conto di eventuali differenze tra l'ordine dei byte utilizzato per archiviare numeri interi dall'architettura host e l'ordine dei byte utilizzato in transito dai singoli protocolli di trasporto.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: ordine dei byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484956"
---
# <a name="byte-ordering"></a>ordine dei byte

È sempre necessario tenere conto di eventuali differenze tra l'ordine dei byte utilizzato per archiviare numeri interi dall'architettura host e l'ordine dei byte utilizzato in transito dai singoli protocolli di trasporto. Qualsiasi riferimento a un indirizzo o a un numero di porta passato a o da una routine di Windows Sockets deve essere nell'ordine di rete (big-endian) per il protocollo utilizzato. Nel caso di IP, sono inclusi i parametri relativi all'indirizzo IP e alla porta di una struttura [**sockaddr**](sockaddr-2.md) (ma non al parametro della *\_ famiglia sin* ).

Alcuni sistemi UNIX operano su CPU che rappresentano numeri interi in ordine byte di rete (big-endian). Pertanto la necessità di convertire numeri interi dall'ordine dei byte dell'host all'ordine dei byte di rete può essere ignorata senza causare problemi anche se questa opzione non è consigliata per la portabilità.

Al contrario, l'ordine dei byte utilizzato per rappresentare i numeri interi per la maggior parte delle CPU Intel® è Little-endian. Pertanto, è diventato obbligatorio che i numeri interi vengano convertiti da host byte order a byte di rete prima di essere utilizzati nelle funzioni e nelle strutture dei socket Winsock.

Si consideri un'applicazione che in genere Contatta un server sulla porta TCP corrispondente al servizio ora, ma fornisce un meccanismo che consente all'utente di specificare una porta alternativa. Il numero di porta restituito da [**GetServByName**](/windows/desktop/api/winsock/nf-winsock-getservbyname) è già in ordine di rete, ovvero il formato necessario per costruire un indirizzo in modo che non sia necessaria alcuna conversione. Tuttavia, se l'utente sceglie di usare una porta diversa, immessa come Integer, l'applicazione deve convertirla dall'host all'ordine di rete TCP/IP (usando la funzione [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) o [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ) prima di usarla per costruire un indirizzo. Viceversa, se l'applicazione dovesse visualizzare il numero di porta all'interno di un indirizzo (restituito da [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , ad esempio), il numero di porta deve essere convertito dalla rete all'ordine host (usando la funzione [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) o [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) prima di poter essere visualizzato.

Poiché gli ordini di byte Intel e Internet sono diversi, le conversioni descritte in precedenza sono inevitabili. Gli sviluppatori di applicazioni si avvertono che devono utilizzare le funzioni di conversione standard fornite come parte di Winsock anziché scrivere il proprio codice di conversione, in quanto le future implementazioni di Winsock probabilmente verranno eseguite su sistemi per i quali l'ordine host è identico all'ordine dei byte di rete. Sono probabilmente portabili solo le applicazioni che utilizzano le funzioni di conversione standard tra l'ordine dei byte host e rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**sockaddr**](sockaddr-2.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



