---
description: Le query di eventi vengono usate da consumer di eventi temporanei, consumer di eventi permanenti e provider di eventi. I consumer di eventi usano query di eventi per specificare gli eventi di interesse e i provider di eventi usano le query per specificare gli eventi che forniscono.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Ricezione di notifiche degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1064fd0098ac72c6ceecbb5fcbc212fb38f6b2b25d0e61d8149bdb0fad177267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996011"
---
# <a name="receiving-event-notifications"></a>Ricezione di notifiche degli eventi

Le query di eventi vengono usate da consumer di eventi temporanei, consumer di eventi permanenti e provider di eventi. I consumer di eventi usano query di eventi per specificare gli eventi di interesse e i provider di eventi usano le query per specificare gli eventi che forniscono.

[I consumer](receiving-events-for-the-duration-of-your-application.md) temporanei posizionano le query nelle chiamate al metodo [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) o [**IWbemServices::ExecNotificationQueryAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) [I consumer di eventi](receiving-events-at-all-times.md) permanenti posizionano **le query nella proprietà Query** di un'istanza della classe di sistema [**\_ \_ EventFilter.**](--eventfilter.md)

[I provider di eventi](writing-an-event-provider.md) usano query di eventi per eseguire la registrazione per supportare uno o più tipi di eventi. Le query vengono posizionate **nella proprietà EventQueryList** di un'istanza della classe di sistema [**\_ \_ EventProviderRegistration.**](--eventproviderregistration.md) Tutti i provider di eventi creano **\_ \_ un'istanza di EventProviderRegistration** da registrare Windows Strumentazione gestione Windows (WMI). Per altre informazioni, vedere [Registrazione di un provider di eventi.](registering-an-event-provider.md)

I consumer e i provider di eventi usano l'istruzione [SELECT](select-statement-for-event-queries.md) e una clausola WHERE correlata per le query di eventi, oltre a un'ampia gamma di estensioni specifiche di WMI Query Language (WQL). Le estensioni vengono usate per proteggere i consumer dall'inondazione di notifiche che si verificano troppo frequentemente per essere utili.

I consumer che non richiedono la notifica ogni volta che si verifica un evento possono specificare le clausole seguenti nelle query:

-   [Clausola WITHIN](within-clause.md)
-   [Clausola GROUP](group-clause.md)
-   [Clausola HAVING](having-clause.md)

Le clausole WITHIN e HAVING influiscono sulla durata degli eventi e la clausola GROUP determina l'invio di un evento rappresentativo al posto di un evento che si verifica di frequente.

 

 



