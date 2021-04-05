---
description: Uno dei modi più comuni per ricevere un evento è tramite un'applicazione in esecuzione, ad esempio un'applicazione di gestione che raccoglie e visualizza gli eventi di un utente.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Ricezione di eventi per la durata dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049762"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Ricezione di eventi per la durata dell'applicazione

Uno dei modi più comuni per ricevere un evento è tramite un'applicazione in esecuzione, ad esempio un'applicazione di gestione che raccoglie e visualizza gli eventi di un utente. Tali applicazioni sono denominate "temporanee" perché un consumer temporaneo non riceve le notifiche degli eventi quando viene arrestato.

Un consumer temporaneo chiama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) nello script o [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ per sottoscrivere gli eventi in uno spazio dei nomi. L'identità associata a questa sottoscrizione è il chiamante.

Un consumer di eventi temporaneo può ricevere notifiche in modo asincrono o semisincrona in entrambi gli script e C++.

> [!Note]  
> Per motivi di sicurezza, è importante notare che le notifiche degli eventi asincroni non sono consigliate. Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md). I consumer di eventi hanno particolari problemi di sicurezza. Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).

 

Per ulteriori informazioni sulla ricezione di notifiche di eventi asincroni e semisincrono, vedere [ricezione di notifiche di eventi asincroni](receiving-asynchronous-event-notifications.md) e ricezione di notifiche di eventi [semisincrono](receiving-synchronous-and-semisynchronous-event-notifications.md).

 

 



