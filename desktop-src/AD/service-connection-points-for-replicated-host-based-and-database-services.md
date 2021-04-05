---
title: Punti di connessione del servizio per i servizi replicati, basati su host e di database
description: Quando si pubblica un servizio usando un punto di connessione del servizio (SCP), prendere in considerazione il modo in cui i client troveranno il SCP per il servizio.
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- Punti di connessione del servizio per i servizi replicati, basati su host e database di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b69491dd84a9367f8fd05e9d23ca771551dfbb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046485"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>Punti di connessione del servizio per i servizi replicati, basati su host e di database

Quando si pubblica un servizio usando un punto di connessione del servizio (SCP), prendere in considerazione il modo in cui i client troveranno il SCP per il servizio. Se esistono più istanze del servizio, valutare il modo in cui i client distingueranno il servizio con le funzionalità desiderate da servizi simili con funzionalità diverse. Se si pubblica un servizio replicato, considerare come un client sceglierà una replica. In questo argomento vengono illustrati questi problemi per diversi tipi di servizi.

## <a name="replicable-services"></a>Servizi replicabili

Per un servizio replicabile è possibile che esistano una o più istanze o repliche del servizio e che i client non siano interessati dalla replica a cui si connettono perché ognuno fornisce lo stesso servizio. Active Directory Domain Services sono esempi di servizi replicati: tutti i controller di dominio per un determinato dominio contengono dati identici, soggetti alla latenza di replica e forniscono servizi identici.

I servizi replicabili possono archiviare convergenza e altri oggetti specifici del servizio per più repliche in un singolo contenitore. L'applicazione di installazione per la prima replica può creare il contenitore come figlio del contenitore di sistema del dominio locale. Per ulteriori informazioni, vedere [pubblicazione in un contenitore di sistema del dominio](publishing-in-a-domain-system-container.md). Verificare che il descrittore di sicurezza per il contenitore consenta ai programmi di installazione per le repliche successive di creare gli oggetti nello stesso contenitore. Concedere le autorizzazioni per l'amministratore che esegue l'installazione per specificare gli utenti o i gruppi che possono creare o modificare gli oggetti nel contenitore.

Una strategia per un servizio replicabile consiste nel creare un SCP per ogni replica. Quando un client esegue una query per il GUID del prodotto del servizio o un'altra parola chiave di identificazione, trova gli oggetti SCP per tutte le repliche e ne seleziona uno in modo casuale o usando un algoritmo di bilanciamento del carico. Un amministratore può ad esempio specificare i dati di priorità e di bilanciamento del carico per ogni replica, in modo analogo ai campi Priority e Weight di un record DNS SRV. L'applicazione di installazione del servizio può archiviare questi dati nell'attributo **serviceBindingInformation** dell'SCP di ogni replica. I client recuperano i dati da ogni SCP e li usano per selezionare una replica.

Un'altra strategia consiste nel creare un singolo SCP per tutte le repliche e impostare l'attributo SCP **serviceDNSName** sul nome di un record DNS SRV. Quindi, l'applicazione di installazione per ogni replica registra un record SRV con tale nome. Quando un client identifica l'SCP solitario del servizio, il client recupera il nome del record SRV e usa la funzione [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) per recuperare la matrice di record SRV per le repliche. Ogni record SRV contiene il nome di un computer host e i dati aggiuntivi che il client può usare per selezionare una replica.

## <a name="database-services"></a>Servizi di database

Diverse istanze di un servizio di database possono contenere dati completamente diversi, anche se sono tutti dello stesso tipo di servizio, in genere chiamato classe del servizio. Per pubblicare questo tipo di servizio, l'attributo **Keywords** dell'SCP può identificare sia la classe del servizio che il database specifico. Un client di uso generico che sa solo il GUID della classe del servizio può eseguire una query per tutti i database pubblicati da tale classe del servizio e quindi presentare un'interfaccia utente per consentire all'utente di selezionarne uno. Per un client progettato in modo specifico per il database di destinazione, è possibile impostare come hardcoded il GUID del database nel codice client.

## <a name="host-based-services"></a>Servizi basati su host

I servizi basati su host sono servizi strettamente legati a un singolo computer host. È possibile installare istanze della classe del servizio in molti computer e ogni istanza fornisce servizi identificati con il relativo computer host.

Ogni istanza di un servizio basato su host deve creare il proprio SCP nell'oggetto computer del relativo host. I client che utilizzano un GUID di prodotto per cercare l'SCP di un servizio basato su host in genere trovano molte istanze della classe del servizio nell'intera foresta aziendale. I client possono quindi utilizzare l'attributo **serviceDNSName** di convergenza per trovare il punto di SCP per l'istanza del servizio nel computer host desiderato.

 

 