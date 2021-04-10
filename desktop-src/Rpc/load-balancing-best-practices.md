---
title: Procedure consigliate per il bilanciamento del carico
description: Procedure consigliate per il bilanciamento del carico
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963304"
---
# <a name="load-balancing-best-practices"></a>Procedure consigliate per il bilanciamento del carico

Quando si installa e si configura il bilanciamento del carico RPC, è necessario seguire alcune procedure consigliate.

Per prima cosa, è necessario impostare la sicurezza sulle chiamate in ingresso e in uscita LBS. Ciò significa che entrambe le chiavi facoltative del registro di sistema [NoSecurity](configuring-load-balancing.md) non devono essere presenti o devono essere impostate su zero.

In secondo luogo, è necessario prestare attenzione alla soluzione front-end di bilanciamento del carico usata insieme alla soluzione di bilanciamento del carico RPC. Se, ad esempio, il servizio di bilanciamento del carico front-end usa il bilanciamento del carico round robin semplice, nel server farm dovrebbe esistere un numero dispari di server. Questo consente di ridurre la possibilità che tutte le connessioni vengano trasmesse e quindi gestite dallo stesso server o server.

Per la sicurezza, è preferibile disporre di un controllo firewall per l'accesso ai server proxy RPC. Se viene utilizzata una soluzione firewall basata su porta, gli endpoint RPC devono essere statici per limitare il numero di porte aperte nel firewall. In Windows Server 2008 e versioni successive di Windows, RPC fornisce un meccanismo per assegnare una porta statica agli endpoint dinamici. Questa operazione viene eseguita tramite i comandi netsh firewall di RPC. Un set di comandi di esempio per impostare l'interfaccia LBS sulla porta statica 3010 è:

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

Il comando netsh RPC può essere utilizzato per impostare un endpoint statico per qualsiasi interfaccia dinamica o statica. Questa operazione è utile quando si limita l'accesso a un computer che esegue una soluzione firewall basata su porte. Se si utilizza la soluzione Windows Firewall, l'interfaccia RPC può essere bloccata o abilitata senza che sia necessario assegnarla a una porta specifica. Per ulteriori informazioni, vedere la Guida di [riferimento al comando RPC netsh firewall](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).

 

 