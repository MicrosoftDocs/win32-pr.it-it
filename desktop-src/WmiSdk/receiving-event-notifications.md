---
description: Le query di eventi vengono utilizzate da consumer di eventi temporanei, consumer di eventi permanenti e provider di eventi. I consumer di eventi utilizzano query di eventi per specificare gli eventi di interesse e i provider di eventi utilizzano le query per specificare gli eventi che forniscono.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Ricezione di notifiche degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309919"
---
# <a name="receiving-event-notifications"></a>Ricezione di notifiche degli eventi

Le query di eventi vengono utilizzate da consumer di eventi temporanei, consumer di eventi permanenti e provider di eventi. I consumer di eventi utilizzano query di eventi per specificare gli eventi di interesse e i provider di eventi utilizzano le query per specificare gli eventi che forniscono.

[I consumer temporanei](receiving-events-for-the-duration-of-your-application.md) inseriscono le query nelle chiamate al metodo [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) o [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) . [I consumer di eventi permanenti](receiving-events-at-all-times.md) inseriscono query nella proprietà **query** di un'istanza della classe di sistema [**\_ \_ EventFilter**](--eventfilter.md) .

I [provider di eventi](writing-an-event-provider.md) utilizzano le query di eventi per eseguire la registrazione per supportare uno o più tipi di eventi. Inseriscono le query nella proprietà **EventQueryList** di un'istanza della classe di sistema [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) . Tutti i provider di eventi creano un'istanza di **\_ \_ EventProviderRegistration** per la registrazione con Strumentazione gestione Windows (WMI). Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di eventi](registering-an-event-provider.md).

I consumer e i provider di eventi utilizzano l' [istruzione SELECT](select-statement-for-event-queries.md) e una clausola WHERE correlata per le query di eventi, oltre a un'ampia gamma di estensioni specifiche per il WMI Query Language (WQL). Le estensioni vengono usate per proteggere gli utenti dal sovraccarico delle notifiche che si verificano troppo spesso per essere utili.

I consumer che non richiedono la notifica ogni volta che si verifica un evento possono specificare le clausole seguenti nelle query:

-   Clausola [within](within-clause.md)
-   Clausola [Group](group-clause.md)
-   Clausola [having](having-clause.md)

Le clausole with e HAVING influiscono sul tempo degli eventi e la clausola GROUP genera un evento rappresentativo da inviare al posto di un evento che si verifica di frequente.

 

 



