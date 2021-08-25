---
description: I client e gli host del profilo dispositivo per servizi Web (DPWS) comunicano in rete usando una serie di messaggi SOAP su UDP e HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Individuazione e modelli di Exchange metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b41267e86358a9d6e263f4bc8971632f1061eb1c94d1e64cc76d65020ce255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856796"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Individuazione e modelli di Exchange metadati

I client e gli host del profilo dispositivo per servizi Web (DPWS) comunicano in rete usando una serie di messaggi SOAP su UDP e HTTP.

Il diagramma seguente mostra una panoramica del traffico UDP e HTTP previsto tra un host e un client DPWS.

![Diagramma che mostra il traffico UDP e HTTP tra un host e un client DPWS.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

[I](hello-message.md)messaggi Hello , [Bye](bye-message.md), [Probe,](probe-message.md) [Resolve](resolve-message.md)e [Get](get--metadata-exchange--http-request-and-message.md) vengono tutti generati senza richieste di rete. Questi messaggi vengono usati per annunciare lo stato del dispositivo o per inviare una richiesta di ricerca. [I messaggi ProbeMatches,](probematches-message.md) [ResolveMatches](resolvematches-message.md)e [GetResponse](getresponse--metadata-exchange--message.md) vengono generati in risposta ai messaggi Probe, Resolve e Get.

[I](hello-message.md)messaggi Hello , [Bye](bye-message.md), [Resolve](resolve-message.md)e [ResolveMatches](resolvematches-message.md) verranno sempre eseguiti tramite UDP. Analogamente, i [messaggi di](get--metadata-exchange--http-request-and-message.md) metadati [Get e GetResponse](getresponse--metadata-exchange--message.md) si verificheranno sempre su HTTP o HTTPS. [I](probe-message.md) messaggi [Probe e ProbeMatches](probematches-message.md) vengono in genere trasmessi tramite UDP, ma si verificano tramite una connessione HTTP o HTTPS in uno scenario di individuazione diretta. Per altre informazioni sui modelli di messaggi di individuazione diretta, vedere [Troubleshooting Applications Using Directed Discovery](troubleshooting-applications-using-directed-discovery.md).

L'elenco seguente mostra la sequenza tipica di messaggi in transito. Non tutti i messaggi sono obbligatori.

1.  [Ciao](hello-message.md)
2.  [Probe](probe-message.md)
3.  [ProbeMatches](probematches-message.md)
4.  [Risolvi](resolve-message.md)
5.  [ResolveMatches](resolvematches-message.md)
6.  [Get](get--metadata-exchange--http-request-and-message.md) (richiesta di scambio di metadati)
7.  [Getresponse](getresponse--metadata-exchange--message.md)
8.  [Ciao](bye-message.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui servizi Web nei dispositivi](about-web-services-for-devices.md)
</dt> </dl>

 

 



