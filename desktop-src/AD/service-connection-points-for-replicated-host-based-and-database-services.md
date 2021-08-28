---
title: Punti di connessione del servizio per i servizi replicati, basati su host e di database
description: Quando si pubblica un servizio usando un punto di connessione del servizio (SCP), valutare in che modo i client individuano il protocollo SCP per il servizio.
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- Punti di connessione del servizio per Active Directory replicati, basati su host e servizi di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7658cc60704dbfc37009272e5f14f997d213ea993054fa22c1c5e0c307794b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024899"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>Punti di connessione del servizio per i servizi replicati, basati su host e di database

Quando si pubblica un servizio usando un punto di connessione del servizio (SCP), valutare in che modo i client individuano il protocollo SCP per il servizio. Se esistono più istanze del servizio, valutare in che modo i client distingueranno il servizio con le funzionalità desiderate da servizi simili con funzionalità diverse. Se si pubblica un servizio replicato, valutare in che modo un client sceglierà una replica. Questo argomento illustra questi problemi per vari tipi di servizi.

## <a name="replicable-services"></a>Servizi replicabili

Per un servizio replicabile possono essere presenti una o più istanze o repliche del servizio e ai client non importa a quale replica si connettono perché ognuna fornisce lo stesso servizio. Active Directory Domain Services esempi di servizi replicati: tutti i controller di dominio per un determinato dominio contengono dati identici, soggetti a latenza di replica e forniscono servizi identici.

I servizi replicabili possono archiviare gli scp e altri oggetti specifici del servizio per più repliche in un singolo contenitore. L'applicazione di installazione per la prima replica può creare il contenitore come figlio del contenitore System del dominio locale. Per altre informazioni, vedere [Pubblicazione in un contenitore del sistema di dominio](publishing-in-a-domain-system-container.md). Assicurarsi che il descrittore di sicurezza per il contenitore consenta ai programmi di installazione per le repliche successive di creare gli oggetti nello stesso contenitore. Concedere all'amministratore di installazione le autorizzazioni per specificare gli utenti o i gruppi che possono creare o modificare oggetti nel contenitore.

Una strategia per un servizio replicabile consiste nel creare un SCP per ogni replica. Quando un client esegue una query per il GUID del prodotto del servizio o un'altra parola chiave di identificazione, trova gli oggetti SCP per tutte le repliche e ne seleziona uno in modo casuale o usando un algoritmo di bilanciamento del carico. Ad esempio, un amministratore può specificare i dati di priorità e bilanciamento del carico per ogni replica, in modo simile ai campi priorità e peso di un record DNS SRV. L'applicazione di installazione del servizio può archiviare questi dati **nell'attributo serviceBindingInformation** di SCP di ogni replica. I client recuperano i dati da ogni SCP e lo usano per selezionare una replica.

Un'altra strategia consiste nel creare un singolo SCP per tutte le repliche e impostare l'attributo SCP **serviceDNSName** sul nome di un record DNS SRV. L'applicazione di installazione per ogni replica registra quindi un record SRV con tale nome. Quando un client identifica la SCP solitaria del servizio, recupera il nome del record SRV e usa la funzione [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) per recuperare la matrice di record SRV per le repliche. Ogni record SRV contiene il nome di un computer host e dati aggiuntivi che il client può usare per selezionare una replica.

## <a name="database-services"></a>Servizi di database

Istanze diverse di un servizio di database possono contenere dati completamente diversi, anche se sono tutti dello stesso tipo di servizio, in genere denominato classe di servizio. Per pubblicare questo tipo di servizio, l'attributo **keywords** del SCP può identificare sia la classe del servizio che il database specifico. Un client per utilizzo generico che conosce solo il GUID della classe di servizio può eseguire una query per tutti i database pubblicati da tale classe di servizio e quindi presentare un'interfaccia utente per consentire all'utente di selezionarne uno. Per un client progettato specificamente per il database di destinazione, è possibile impostare come hard code il GUID del database nel codice client.

## <a name="host-based-services"></a>Servizi basati su host

I servizi basati su host sono servizi strettamente associati a un singolo computer host. È possibile installare istanze della classe di servizio in molti computer e ogni istanza fornisce servizi identificati con il computer host.

Ogni istanza di un servizio basato su host deve creare il proprio SCP sotto l'oggetto computer del relativo host. I client che usano un GUID di prodotto per cercare il protocollo SCP di un servizio basato su host trovano in genere molte istanze della classe di servizio in tutta la foresta aziendale. I client possono quindi usare **l'attributo serviceDNSName** degli scp per trovare il protocollo SCP per l'istanza del servizio nel computer host desiderato.

 

 