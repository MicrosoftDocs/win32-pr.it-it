---
title: Configurazione dei timeout specifici dell'applicazione
description: Configurazione dei timeout specifici dell'applicazione
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configurazione di HTTP per timeout specifici dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722d44c1377a3bee22a88fe92f0f5aed272c08f0b0a6645361c4e03816f408fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950880"
---
# <a name="configuring-the-application-specific-timeouts"></a>Configurazione dei timeout specifici dell'applicazione

Le impostazioni a livello di API del server HTTP si applicano a tutte le sessioni del server e a tutti i gruppi di URL nel computer. Queste configurazioni possono essere sostituite dall'applicazione impostando i valori di timeout specifici dell'applicazione. I timeout della sessione del server sostituiscono i timeout a livello di API del server HTTP e si applicano a tutti i gruppi di URL creati al loro interno. La configurazione della proprietà timeouts in un gruppo di URL sostituisce i timeout della sessione del server per tutti gli URL nel gruppo.

Se si specifica zero per uno dei timer nella struttura [**HTTP \_ TIMEOUT LIMIT \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) per un gruppo di URL, l'API del server HTTP ripristina i timeout della sessione del server, se presenti, o le impostazioni predefinite dell'API del server HTTP se i timeout della sessione del server non esistono. Ad esempio, quando la proprietà timeout del server è presente in un gruppo di URL e il timer **EntityBody** è zero, viene usato il timeout della sessione del server. Se la proprietà timeouts non è impostata in una sessione del server, viene usata la configurazione predefinita dell'API del server HTTP. Per disabilitare un timer, impostare il valore su **MAXUSHORT**, ad eccezione del timer **MinSendRate** impostato su **MAXULONG.**

L'API del server HTTP può configurare solo i timer **HeaderWait** specifici dell'applicazione e i timer **IdleConnection** sono effettivi solo dopo la ricezione della prima richiesta. Prima della ricezione della prima richiesta, vengono applicati i valori di timeout a livello di API del server HTTP. Quando arriva la prima richiesta e viene associata a una coda di richieste, è possibile applicare i timer **HeaderWait** e **IdleConnection** specifici dell'applicazione. I timer specifici dell'applicazione vengono applicati a tutte le richieste successive che arrivano nella coda di richieste per una connessione keep-alive.

Per altre informazioni sulla configurazione dei timer, vedere gli argomenti [Configuring the URL Group](configuring-the-url-group.md) e [Configuring the Server Session.](configuring-the-server-session.md)

 

 




