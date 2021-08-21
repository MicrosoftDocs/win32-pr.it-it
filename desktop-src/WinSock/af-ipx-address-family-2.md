---
description: La famiglia di indirizzi IPX definisce la struttura di indirizzamento per i protocolli che usano l'indirizzamento socket IPX standard. Per questi trasporti, un indirizzo endpoint è costituito da un numero di rete, un indirizzo di nodo e un numero di socket.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: AF_IPX Address Family
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3915eefab8e6fc6c18cf4e2b81835b8c6821d0cdd65f5683f509504d4d2c24bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112804"
---
# <a name="af_ipx-address-family"></a>Famiglia \_ di indirizzi IPX af

La famiglia di indirizzi IPX definisce la struttura di indirizzamento per i protocolli che usano l'indirizzamento socket IPX standard. Per questi trasporti, un indirizzo endpoint è costituito da un numero di rete, un indirizzo di nodo e un numero di socket.

Il numero di rete è un dominio amministrativo e in genere indica un singolo segmento Ethernet o token ring. Il numero di nodo è l'indirizzo fisico di una stazione. La combinazione di rete e nodo forma un indirizzo di stazione univoco che si presume sia univoco nel mondo. I numeri net e node sono rappresentati in testo ASCII in una notazione a blocchi o tratteggiata come: '0101a040,00001b498765' o '01-01-a0-40,00-00-1b-49-87-65'. Gli zeri iniziali non devono essere presenti.

Il numero di socket IPX è un numero di servizio di rete/trasporto molto simile a un numero di porta TCP e non deve essere confuso con il descrittore del socket Winsock. I numeri di socket IPX sono globali per la stazione finale e non possono essere associati a indirizzi net/node specifici. Ad esempio, se la stazione di fine ha due schede di interfaccia di rete, un socket associato può inviare e ricevere su entrambe le schede. In particolare, i socket di datagramma riceveranno datagrammi broadcast su entrambe le schede.

> [!Caution]  
> SOCKADDR IPX ha una lunghezza di 14 byte ed è più breve della struttura di riferimento \_ [**sockaddr**](sockaddr-2.md) a 16 byte. Le implementazioni IPX/SPX possono accettare la lunghezza di 16 byte e la lunghezza effettiva. Se si usa SOCKADDR IPX e una lunghezza hard coded di 16 byte, l'implementazione può presupporre che abbia accesso ai 2 byte che segue \_ la struttura.

 



| Campo           | Valore                                    |
|-----------------|------------------------------------------|
| **famiglia \_ sa**  | IpX af \_ famiglia di indirizzi in ordine host.    |
| **Sa \_ netnum**  | Identificatore di rete IPX in ordine di rete. |
| **Nodenum Sa \_** | Indirizzo del nodo stazione, scaricato a destra.     |
| **Socket \_ Sa**  | Numero di socket IPX in ordine di rete.      |



 

 

 



