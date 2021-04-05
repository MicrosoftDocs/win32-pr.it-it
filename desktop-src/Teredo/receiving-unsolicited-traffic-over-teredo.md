---
title: Ricezione di traffico non richiesto su Teredo
description: Teredo fornisce connettività globale usando le funzionalità di attraversamento NAT e IPv6.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729042"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Ricezione di traffico non richiesto su Teredo

[Teredo](about-teredo.md) fornisce connettività globale usando le funzionalità di attraversamento NAT e IPv6. Tuttavia, molte applicazioni, tra cui peer-to-peer, richiedono Teredo per ricevere traffico non richiesto da Internet. Un'applicazione può essere programmata per ricevere traffico su una singola interfaccia IPv6 o su tutte le interfacce che supportano IPv6. In questa documentazione vengono descritti i requisiti per le applicazioni che utilizzano l'interfaccia Teredo per ricevere traffico IPv6 non richiesto.

Un'applicazione riceverà traffico non richiesto sull'interfaccia Teredo solo se l'applicazione è registrata con [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page). Per ricevere traffico non richiesto, è necessario che si verifichi quanto segue:

-   Agli utenti deve essere richiesto di utilizzare Microsoft Management Console (MMC) per abilitare l'opzione "attraversamento confini" per un'applicazione. Questa opzione è disponibile in Windows Firewall Snap-In--> <application name> > scheda "avanzate". L'opzione "attraversamento bordo" deve essere abilitata singolarmente per ogni applicazione.

-   L'opzione "attraversamento bordo" è abilitata dall'applicazione. È possibile che le applicazioni in grado di ricevere traffico non richiesto vengano registrate con Windows Firewall per "attraversamento del perimetro" e ricevano traffico non richiesto sull'interfaccia Teredo. A tale scopo, un'applicazione deve chiamare l'API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con l'opzione "attraversamento bordo" impostata su Variant \_ true. Il consenso dell'utente è necessario per questa chiamata API prima che un'applicazione sia autorizzata ad ascoltare il traffico.

-   L'applicazione imposta l'opzione del socket del [ \_ \_ livello di protezione IPv6](/windows/desktop/WinSock/ipv6-protection-level) Winsock sul **livello di protezione \_ \_ senza restrizioni** tramite [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt). Ciò consentirà all'applicazione di ricevere il traffico di attraversamento perimetrale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricezione di traffico richiesto su Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 