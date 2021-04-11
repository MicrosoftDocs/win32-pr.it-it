---
description: La famiglia di indirizzi IPX definisce la struttura di indirizzamento per i protocolli che utilizzano l'indirizzamento dei socket IPX standard. Per questi trasporti, un indirizzo endpoint è costituito da un numero di rete, un indirizzo del nodo e un numero di socket.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Famiglia di indirizzi AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129227"
---
# <a name="af_ipx-address-family"></a>\_Famiglia di indirizzi IPX AF

La famiglia di indirizzi IPX definisce la struttura di indirizzamento per i protocolli che utilizzano l'indirizzamento dei socket IPX standard. Per questi trasporti, un indirizzo endpoint è costituito da un numero di rete, un indirizzo del nodo e un numero di socket.

Il numero di rete è un dominio amministrativo e in genere denomina un singolo segmento di anello Ethernet o token. Il numero del nodo è un indirizzo fisico della stazione. La combinazione di rete e nodo costituisce un indirizzo di stazione univoco che si presume sia univoco nel mondo. I numeri di nodo e NET sono rappresentati nel testo ASCII in un blocco o in una notazione tratteggiata come:' 0101a040, 00001b498765' o ' 01-01-a0-40, 00-00-1B-49-87-65'. Gli zeri iniziali non devono essere presenti.

Il numero di socket IPX è un numero di servizio di rete/trasporto molto simile a un numero di porta TCP e non deve essere confuso con il descrittore di socket Winsock. I numeri di socket IPX sono globali per la stazione finale e non possono essere associati a indirizzi net/node specifici. Ad esempio, se la stazione finale ha due schede di interfaccia di rete, un socket associato può inviare e ricevere su entrambe le schede. In particolare, i socket di datagramma riceveranno datagrammi broadcast su entrambe le schede.

> [!Caution]  
> SOCKADDR \_ IPX ha una lunghezza di 14 byte ed è più breve della struttura di [**riferimento sockaddr**](sockaddr-2.md) a 16 byte. Le implementazioni IPX/SPX possono accettare la lunghezza di 16 byte e la lunghezza vera. Se si usa SOCKADDR \_ IPX e una lunghezza hardcoded di 16 byte, l'implementazione può presumere che abbia accesso ai 2 byte che seguono la struttura.

 



| Campo           | Valore                                    |
|-----------------|------------------------------------------|
| **\_famiglia sa**  | Famiglia di indirizzi AF \_ IPX nell'ordine host.    |
| **\_Netnum SA**  | Identificatore di rete IPX in ordine di rete. |
| **\_Nodenum SA** | Indirizzo del nodo della stazione, svuotato a destra.     |
| **\_Socket SA**  | Numero di socket IPX nell'ordine di rete.      |



 

 

 



