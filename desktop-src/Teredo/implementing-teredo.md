---
title: Implementazione di Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 'Altre informazioni su: Implementazione di Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b24f4524d6c513dc0a5cd11e7f6420eb7e546fa3bce75c830759fc38faaef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681651"
---
# <a name="implementing-teredo"></a>Implementazione di Teredo

Anche se non è necessario apportare modifiche di programmazione per Teredo [,](about-teredo.md)è consigliabile che gli sviluppatori apportare modifiche secondarie che comportano l'uso più efficiente dell'interfaccia Teredo:

-   È possibile che le applicazioni in grado di usare solo il traffico IPv6 Teredo. È tuttavia necessario prendere in considerazione l'elaborazione del traffico IPv4 e IPv6 durante lo sviluppo del protocollo dell'applicazione. L'applicazione dovrà essere associata ad AF \_ INET6 o AF \_ UNSPEC nelle opzioni socket.
-   Le applicazioni in grado di ascoltare il traffico non richiesto da Internet sono necessarie per abilitare l'opzione Attraversamento NAT (Network Address Translation) all'interno Windows Firewall. Questa operazione viene eseguita chiamando l'API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con l'opzione "Edge Traversal" impostata su VARIANT \_ TRUE. Windows Vista garantisce che l'Teredo disponibile per l'uso quando un'applicazione lo richiede. Di conseguenza, l'Teredo si stabilizza automaticamente quando viene usata l Teredo intervazione. Se un'applicazione vuole garantire che l'indirizzo Teredo sia stabile, la chiamata all'API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) Teredo la transizione a uno stato stabile.
-   Le applicazioni possono anche usare l'opzione socket Winsock [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) per impostare il livello di protezione, che consente al traffico in ingresso non richiesto di passare attraverso il firewall. Per altre informazioni, vedere Receiving [Unsolicited Traffic Over Teredo](receiving-unsolicited-traffic-over-teredo.md) (Ricezione di traffico non richiesto Teredo per altre informazioni).

L'implementazione dell'helper IP (Internet Protocol Helper) di funzioni Teredo specifiche funge da esempio di come l'indirizzo Teredo può essere verificato e reso disponibile per un'applicazione. Per altre informazioni, vedere [Using Teredo With IP Helper](using-teredo-with-ip-helper.md).

 

 
