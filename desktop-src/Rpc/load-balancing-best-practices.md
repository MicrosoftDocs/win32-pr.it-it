---
title: Procedure consigliate per il bilanciamento del carico
description: Procedure consigliate per il bilanciamento del carico
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fe4af9dffe758c89d1a494d4cc2597e057c563ca8c85db87d789ae91b89698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928596"
---
# <a name="load-balancing-best-practices"></a>Procedure consigliate per il bilanciamento del carico

Quando si configura e si configura il bilanciamento del carico RPC, è consigliabile seguire diverse procedure consigliate.

In primo luogo, la sicurezza deve essere impostata sulle chiamate LBS in ingresso e in uscita. Ciò significa che entrambe le chiavi del Registro di sistema [NoSecurity](configuring-load-balancing.md) facoltative non devono essere presenti o devono essere impostate su zero.

In secondo piano, è necessario prestare attenzione alla soluzione di bilanciamento del carico front-end usata insieme alla soluzione di bilanciamento del carico RPC. Ad esempio, se il servizio di bilanciamento del carico front-end usa il bilanciamento del carico round robin semplice, nel server farm deve essere presente un numero dispari di server. Ciò consente di attenuare la possibilità che tutte le connessioni vengano inoltrate e quindi trattate dallo stesso server o server.

Per motivi di sicurezza, è in genere consigliabile avere un firewall che controlla l'accesso ai server proxy RPC. Se viene utilizzata una soluzione firewall basata su porte, gli endpoint RPC devono essere statici per limitare il numero di porte aperte nel firewall. In Windows Server 2008 e versioni successive di Windows, RPC fornisce un meccanismo per assegnare una porta statica agli endpoint dinamici. Questa operazione viene ottenuta tramite i comandi del firewall netsh RPC. Un set di comandi di esempio per impostare l'interfaccia LBS sulla porta statica di 3010 è:

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

Il comando NETSH RPC può essere usato per impostare un endpoint statico per qualsiasi interfaccia dinamica o statica. Ciò è utile quando si limita l'accesso a un computer che esegue una soluzione firewall basata su porta. Se viene Windows soluzione firewall, l'interfaccia RPC può essere bloccata o abilitata senza doverla assegnare a una porta specifica. Per altre informazioni, vedere il riferimento al comando [firewall netsh RPC](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).

 

 