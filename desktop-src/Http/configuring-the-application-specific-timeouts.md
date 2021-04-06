---
title: Configurazione dei timeout specifici dell'applicazione
description: .
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configurazione dei timeout specifici dell'applicazione HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35827b797ad6c9f19b728064f6fe65b0d89b2a3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044653"
---
# <a name="configuring-the-application-specific-timeouts"></a>Configurazione dei timeout specifici dell'applicazione

Le impostazioni a livello di API del server HTTP si applicano a tutte le sessioni server e ai gruppi di URL nel computer. È possibile eseguire l'override di queste configurazioni da parte dell'applicazione impostando i valori di timeout specifici dell'applicazione. I timeout della sessione del server eseguono l'override dei timeout a livello di API del server HTTP e si applicano a tutti i gruppi di URL creati al suo interno. La configurazione della proprietà timeout in un gruppo di URL sostituisce i timeout della sessione del server per tutti gli URL nel gruppo.

Se si specifica zero per uno dei timer nella struttura di [**\_ informazioni sul \_ limite \_ di timeout http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) per un gruppo di URL, l'API del server http ripristinerà i timeout della sessione del server, se esistono, oppure le impostazioni predefinite dell'API del server http se i timeout della sessione del server non esistono. Ad esempio, quando la proprietà timeout server è presente in un gruppo di URL e il timer **EntityBody** è zero, viene usato il timeout della sessione del server. Se la proprietà timeouts non è impostata in una sessione del server, viene utilizzata la configurazione predefinita dell'API del server HTTP. Per disabilitare un timer, impostare il valore su **MAXUSHORT**, ad eccezione del timer **MinSendRate** impostato su **MAXULONG**.

L'API server HTTP può configurare solo **HeaderWait** specifici dell'applicazione e i timer **IdleConnection** sono validi solo dopo la ricezione della prima richiesta. Prima della ricezione della prima richiesta, vengono applicati i valori di timeout a livello di API del server HTTP. Una volta che la prima richiesta arriva ed è associata a una coda di richieste, è possibile applicare i timer **HeaderWait** e **IdleConnection** specifici dell'applicazione. I timer specifici dell'applicazione vengono applicati a tutte le richieste successive che arrivano nella coda di richieste per una connessione keep-alive.

Per ulteriori informazioni sulla configurazione dei timer, vedere gli argomenti [configurazione del gruppo di URL](configuring-the-url-group.md) e [configurazione della sessione del server](configuring-the-server-session.md) .

 

 




