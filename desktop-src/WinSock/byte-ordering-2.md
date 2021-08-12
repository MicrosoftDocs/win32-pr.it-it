---
description: È sempre necessario prendere in considerazione eventuali differenze tra l'ordinamento dei byte utilizzato per l'archiviazione di interi in base all'architettura host e l'ordinamento dei byte utilizzato in transito dai singoli protocolli di trasporto.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: ordine dei byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554b9f00b67fcd602daee0ed33443e228e4e3976f334506d949e3af79fef7e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560181"
---
# <a name="byte-ordering"></a>ordine dei byte

È sempre necessario prendere in considerazione eventuali differenze tra l'ordinamento dei byte utilizzato per l'archiviazione di interi in base all'architettura host e l'ordinamento dei byte utilizzato in transito dai singoli protocolli di trasporto. Qualsiasi riferimento a un indirizzo o a un numero di porta passato a o da una routine socket Windows deve essere nell'ordine di rete (big-endian) per il protocollo in uso. Nel caso di IP, questo include l'indirizzo IP e i parametri di porta di una struttura [**sockaddr**](sockaddr-2.md) (ma non il parametro *sin \_ family).*

Alcuni dei sistemi UNIX operano su CPU che rappresentano numeri interi nell'ordine dei byte di rete (big-endian). La necessità di convertire interi dall'ordine dei byte dell'host all'ordine dei byte di rete può quindi essere ignorata senza causare problemi anche se questa operazione non è consigliata per la portabilità.

Al contrario, l'ordinamento dei byte usato per rappresentare numeri interi dalla maggior parte delle CPU Intel® è little-endian. È quindi obbligatorio convertire i numeri interi dall'ordine dei byte dell'host all'ordine dei byte di rete prima di essere usati nelle funzioni e nelle strutture di Winsock Sockets.

Si consideri un'applicazione che in genere contatta un server sulla porta TCP corrispondente al servizio ora, ma fornisce all'utente un meccanismo per specificare una porta alternativa. Il numero di porta restituito da [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) è già in ordine di rete, ovvero il formato necessario per costruire un indirizzo in modo che non sia necessaria alcuna conversione. Tuttavia, se l'utente sceglie di usare una porta diversa, immessa come numero intero, l'applicazione deve convertirlo dall'host all'ordine di rete TCP/IP (usando la funzione [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) o [**WSAHtons)**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) prima di usarlo per costruire un indirizzo. Viceversa, se l'applicazione visualizza il numero della porta all'interno di un indirizzo (ad esempio restituito da [**getpeername),**](/windows/desktop/api/winsock/nf-winsock-getpeername) il numero di porta deve essere convertito dalla rete all'ordine host (usando la funzione [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) o [**WSANtohs)**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) prima di poter essere visualizzato.

Poiché gli ordini di byte Intel e Internet sono diversi, le conversioni descritte in precedenza sono inevitabili. I writer di applicazioni devono usare le funzioni di conversione standard fornite come parte di Winsock anziché scrivere il proprio codice di conversione, poiché è probabile che le implementazioni future di Winsock siano eseguite in sistemi per i quali l'ordine host è identico all'ordine dei byte di rete. È probabile che solo le applicazioni che usano le funzioni di conversione standard tra l'ordine dei byte host e di rete siano portabili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**hton**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**sockaddr**](sockaddr-2.md)
</dt> <dt>

[Considerazioni sulla programmazione winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



