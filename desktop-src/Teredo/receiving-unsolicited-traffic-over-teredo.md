---
title: Ricezione di traffico non richiesto su Teredo
description: Teredo connettività globale tramite funzionalità di attraversamento NAT e IPv6.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca6a4a6580200eee1f039fc87da29515db00a29f94700ff02548c38ba776f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099631"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Ricezione di traffico non richiesto su Teredo

[Teredo](about-teredo.md) connettività globale tramite funzionalità di attraversamento NAT e IPv6. Tuttavia, molte applicazioni, tra cui peer-to-peer, Teredo ricevere traffico non richiesto da Internet. Un'applicazione può essere programmata per ricevere traffico su una singola interfaccia IPv6 o su tutte le interfacce che supportano IPv6. Questa documentazione descrive i requisiti per le applicazioni che usano l'Teredo per ricevere traffico IPv6 non richiesto.

Un'applicazione riceverà traffico non richiesto sull'interfaccia Teredo solo se l'applicazione è registrata con [Windows Firewall.](/previous-versions/windows/desktop/ics/windows-firewall-start-page) Per ricevere traffico non richiesto, è necessario che si verifichi quanto segue:

-   Agli utenti deve essere richiesto di usare Microsoft Management Console (MMC) per abilitare l'opzione "Attraversamento edge" per un'applicazione. Questa opzione è disponibile nella Windows firewall Snap-In --> <application name> --> "Avanzate". L'opzione "Attraversamento edge" deve essere abilitata singolarmente per ogni applicazione.

-   L'opzione "Attraversamento edge" è abilitata dall'applicazione. È possibile che le applicazioni in grado di ricevere traffico non richiesto si registrino con Windows Firewall per "Attraversamento perimetrale" e ricevano traffico non richiesto sull'interfaccia Teredo rete. A tale scopo, un'applicazione deve chiamare l'API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con l'opzione "Edge Traversal" impostata su VARIANT \_ TRUE. Il consenso dell'utente è necessario per questa chiamata API prima che un'applicazione sia autorizzata ad ascoltare il traffico.

-   L'applicazione imposta l'opzione socket PROTECTION [ \_ \_ LEVEL di](/windows/desktop/WinSock/ipv6-protection-level) Winsock IPV6 su **PROTECTION LEVEL \_ \_ UNRESTRICTED** tramite [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt) Ciò consentirà all'applicazione di ricevere il traffico di attraversamento perimetrale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricezione di traffico richiesto su Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 