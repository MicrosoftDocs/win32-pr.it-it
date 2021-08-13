---
description: Uno dei modi più comuni per ricevere un evento è tramite un'applicazione in esecuzione, ad esempio un'applicazione di gestione che raccoglie e visualizza gli eventi a un utente.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Ricezione di eventi per la durata dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6815c2ddd7725ccd12dd65b0047874ddce1038b2a2c07f90a40d6f87e6af3a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554219"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Ricezione di eventi per la durata dell'applicazione

Uno dei modi più comuni per ricevere un evento è tramite un'applicazione in esecuzione, ad esempio un'applicazione di gestione che raccoglie e visualizza gli eventi a un utente. Tali applicazioni vengono chiamate "temporanee" perché un consumer temporaneo non riceve notifiche di eventi all'arresto.

Un consumer temporaneo chiama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) nello script [**oIWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ per sottoscrivere eventi in uno spazio dei nomi. L'identità associata a questa sottoscrizione è il chiamante.

Un consumer di eventi temporaneo può ricevere notifiche in modo asincrono o semisincronoso sia negli script che in C++.

> [!Note]  
> Per motivi di sicurezza, è importante notare che le notifiche degli eventi asincrone non sono consigliate. Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md) I consumer di eventi hanno particolari problemi di sicurezza. Per altre informazioni, vedere [Protezione degli eventi WMI](securing-wmi-events.md).

 

Per altre informazioni sulla ricezione di notifiche di eventi asincrone e semisincrone, vedere [Ricezione](receiving-asynchronous-event-notifications.md) di notifiche degli eventi asincrone e Ricezione di notifiche di [eventi semisincroni.](receiving-synchronous-and-semisynchronous-event-notifications.md)

 

 



