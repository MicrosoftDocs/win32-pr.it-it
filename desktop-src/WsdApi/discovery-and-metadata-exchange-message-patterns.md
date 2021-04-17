---
description: Il profilo dispositivo per gli host dei servizi Web (DPWS) e i client comunicano in rete utilizzando una serie di messaggi SOAP su UDP e HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Modelli di messaggi di individuazione e scambio di metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104234456"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Modelli di messaggi di individuazione e scambio di metadati

Il profilo dispositivo per gli host dei servizi Web (DPWS) e i client comunicano in rete utilizzando una serie di messaggi SOAP su UDP e HTTP.

Il diagramma seguente mostra una panoramica del traffico UDP e HTTP previsto tra un host e un client di DPWS.

![Diagramma che mostra il traffico UDP e HTTP tra un host DPWS e un client.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

[Hello](hello-message.md), [bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md)e [Get](get--metadata-exchange--http-request-and-message.md) messages vengono generati senza richiesta di rete; questi messaggi vengono usati per annunciare lo stato del dispositivo o per emettere una richiesta di ricerca. I messaggi [ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md)e [GetResponse](getresponse--metadata-exchange--message.md) vengono generati in risposta a probe, Resolve e Get messages.

I messaggi [Hello](hello-message.md), [bye](bye-message.md), [Resolve](resolve-message.md)e [ResolveMatches](resolvematches-message.md) vengono sempre eseguiti su UDP. Analogamente, i messaggi di metadati [Get](get--metadata-exchange--http-request-and-message.md) e [GetResponse](getresponse--metadata-exchange--message.md) vengono sempre eseguiti su http o HTTPS. I messaggi [Probe](probe-message.md) e [ProbeMatches](probematches-message.md) vengono in genere trasmessi tramite UDP, ma avvengono tramite una connessione HTTP o HTTPS in uno scenario di individuazione diretta. Per ulteriori informazioni sui modelli di messaggi di individuazione diretta, vedere [risoluzione dei problemi relativi alle applicazioni mediante l'individuazione diretta](troubleshooting-applications-using-directed-discovery.md).

Nell'elenco seguente viene illustrata la sequenza tipica dei messaggi in transito. Non tutti i messaggi sono obbligatori.

1.  [Ciao](hello-message.md)
2.  [Probe](probe-message.md)
3.  [ProbeMatches](probematches-message.md)
4.  [Risolvi](resolve-message.md)
5.  [ResolveMatches](resolvematches-message.md)
6.  [Get](get--metadata-exchange--http-request-and-message.md) (richiesta di scambio di metadati)
7.  [GetResponse](getresponse--metadata-exchange--message.md)
8.  [Bye](bye-message.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui servizi Web nei dispositivi](about-web-services-for-devices.md)
</dt> </dl>

 

 



