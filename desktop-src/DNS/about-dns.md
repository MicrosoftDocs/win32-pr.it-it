---
title: Informazioni su DNS
description: Domain Name System (DNS) è un protocollo standard del settore usato per individuare i computer in una rete basata su IP. Gli utenti possono ricordare i nomi visualizzati, ad esempio www.microsoft.com più semplici rispetto agli indirizzi basati su numeri, ad esempio 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Informazioni Domain Name System DNS
- Domain Name System DNS , informazioni
- Domain Name System DNS, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc286c18aa60a930a243c1500cf4707d0d42874fc9556fcb090df582334f077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084791"
---
# <a name="about-dns"></a>Informazioni su DNS

Domain Name System (DNS) è un protocollo standard del settore usato per individuare i computer in una rete basata su IP. Gli utenti possono ricordare i nomi visualizzati, ad esempio più semplici rispetto agli indirizzi basati su numeri, ad esempio `www.microsoft.com` 207.46.131.137.

Le reti IP, ad esempio Internet e Windows, si basano su indirizzi basati su numeri per trasmettere i dati in tutta la rete; Pertanto, è necessario convertire i nomi visualizzati (ad esempio ) in indirizzi numerici che la rete è in grado di riconoscere (ad esempio `www.microsoft.com` 207.46.131.137). DNS è il servizio preferito in Windows per individuare tali risorse e convertirle in indirizzi IP.

DNS è il servizio di localizzazione primario per Active Directory e pertanto può essere considerato un servizio di base sia per Windows che per Active Directory. Windows fornisce funzioni che consentono ai programmatori di applicazioni di usare funzioni DNS, ad esempio l'esecuzione di query DNS a livello di codice, il confronto dei record e la ricerca di nomi.

Molte funzioni DNS sono in realtà tipi di funzione, in quanto esiste un nome di base per la funzione, ma il suo uso dipende dalla codifica dei caratteri. Ad esempio, la funzione [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) è elencata nel riferimento alla funzione dell'API DNS come **DnsQuery,** ma il suo uso nelle applicazioni dipende dal fatto che la codifica dei caratteri sia ANSI (designata aggiungendo A al nome del tipo di funzione), Unicode (designato aggiungendo W al nome del tipo di funzione) o \_ \_ UTF-8 (definito aggiungendo UTF al nome del tipo di \_ funzione). Pertanto, la chiamata di funzione per **la funzione DnsQuery** sarebbe in effetti una delle seguenti:

DnsQuery \_ A ( A per la codifica \_ ANSI)

DnsQuery \_ W ( W per la codifica \_ Unicode)

DnsQuery \_ UTF8 \_ (UTF8 per la codifica UTF-8)

Tutte le funzioni che richiedono questa convenzione specificano chiaramente questo requisito all'interno delle prime frasi della relativa definizione di funzione. Usare il nome della funzione corretto. Ad esempio, non è possibile chiamare [**semplicemente DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) anziché DnsQuery \_ A.

 

 




