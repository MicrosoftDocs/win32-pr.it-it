---
title: Implementazione di Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 'Altre informazioni su: implementazione di Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffdf2859d3742bea02e240c6a26bd0e4ade85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233830"
---
# <a name="implementing-teredo"></a>Implementazione di Teredo

Sebbene non sia necessario apportare modifiche alla programmazione per [Teredo](about-teredo.md), è consigliabile che gli sviluppatori apportino modifiche minime che comportino un uso più efficiente dell'interfaccia Teredo:

-   È possibile che le applicazioni che sono in grado di utilizzare solo il traffico IPv6 possano utilizzare Teredo. Tuttavia, l'elaborazione del traffico IPv4 e IPv6 deve essere presa in considerazione durante lo sviluppo del protocollo dell'applicazione. L'applicazione dovrà essere associata a AF \_ INET6 o AF \_ UNSPEC in opzioni socket.
-   Le applicazioni in grado di restare in attesa di traffico non richiesto da Internet sono necessarie per abilitare l'opzione di attraversamento NAT (Network Address Translation) all'interno Windows Firewall. Questa operazione viene eseguita chiamando l'API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con l'opzione "attraversamento bordo" impostata su Variant \_ true. Windows Vista garantisce che l'indirizzo Teredo sia disponibile per l'uso quando richiesto da un'applicazione. Di conseguenza, l'indirizzo Teredo si stabilizza automaticamente quando si usa l'interfaccia Teredo. Se un'applicazione vuole assicurarsi che l'indirizzo Teredo sia stabile, la chiamata dell'API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) attiva Teredo per passare a uno stato stabile.
-   Le applicazioni possono inoltre utilizzare l'opzione del socket Winsock del [ \_ \_ livello di protezione IPv6](/windows/desktop/WinSock/ipv6-protection-level) per impostare il livello di protezione, consentendo al traffico in ingresso non richiesto di passare attraverso il firewall. Per ulteriori informazioni, vedere [ricezione di traffico non richiesto su Teredo](receiving-unsolicited-traffic-over-teredo.md) .

L'implementazione dell'helper protocollo Internet (helper IP) di funzioni Teredo specifiche funge da esempio di come è possibile verificare l'indirizzo Teredo e renderlo disponibile per un'applicazione. Per ulteriori informazioni, vedere l'argomento relativo [all'utilizzo di Teredo con l'helper IP](using-teredo-with-ip-helper.md).

 

 
