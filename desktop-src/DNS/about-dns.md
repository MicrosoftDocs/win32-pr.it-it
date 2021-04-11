---
title: Informazioni su DNS
description: Domain Name System (DNS) è un protocollo standard del settore usato per individuare i computer in una rete basata su IP. Gli utenti possono ricordare i nomi visualizzati, ad esempio www.microsoft.com più semplici degli indirizzi basati su numeri, ad esempio 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Informazioni sul DNS Domain Name System
- Domain Name System DNS, informazioni
- Domain Name System DNS, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234910"
---
# <a name="about-dns"></a>Informazioni su DNS

Domain Name System (DNS) è un protocollo standard del settore usato per individuare i computer in una rete basata su IP. Gli utenti possono ricordare i nomi visualizzati, ad esempio `www.microsoft.com` gli indirizzi basati sui numeri, ad esempio 207.46.131.137.

Le reti IP, ad esempio le reti Internet e Windows, si basano sugli indirizzi numerici per trasmettere i dati in tutta la rete. è pertanto necessario convertire i nomi visualizzati, ad esempio, `www.microsoft.com` in indirizzi numerici che la rete è in grado di riconoscere, ad esempio 207.46.131.137. DNS è il servizio da scegliere in Windows per individuare tali risorse e convertirle in indirizzi IP.

DNS è il servizio localizzatore primario per Active Directory e pertanto DNS può essere considerato un servizio di base per Windows e Active Directory. Windows fornisce funzioni che consentono ai programmatori di applicazioni di usare funzioni DNS quali la creazione di query DNS a livello di codice, il confronto di record e la ricerca di nomi.

Molte funzioni DNS sono in realtà tipi di funzione, in quanto è presente un nome di base per la funzione, ma il suo utilizzo dipende dalla codifica dei caratteri. La funzione [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) , ad esempio, è elencata nel riferimento alla funzione dell'API (Application Programming Interface) DNS come **DnsQuery**, tuttavia, l'uso nelle applicazioni varia a seconda che la codifica dei caratteri sia ANSI (designata mediante l'aggiunta di \_ un oggetto al nome del tipo di funzione), Unicode (designata aggiungendo \_ W al nome del tipo di funzione) o UTF-8 (designato aggiungendo \_ UTF al nome del tipo di funzione). Pertanto, la chiamata di funzione per la funzione **DnsQuery** è in realtà una delle seguenti:

DnsQuery \_ a ( \_ a per la codifica ANSI)

DnsQuery \_ w ( \_ w per codifica Unicode)

DnsQuery \_ UTF8 ( \_ UTF8 per codifica UTF-8)

Tutte le funzioni che richiedono questa convenzione indicano chiaramente questo requisito entro le prime frasi della definizione di funzione. Usare il nome della funzione appropriato. ad esempio, non è possibile chiamare semplicemente [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) anziché DnsQuery \_ A.

 

 




