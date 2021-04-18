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
# <a name="receiving-event-notifications"></a><span data-ttu-id="2cccc-104">Ricezione di notifiche degli eventi</span><span class="sxs-lookup"><span data-stu-id="2cccc-104">Receiving Event Notifications</span></span>

<span data-ttu-id="2cccc-105">Le query di eventi vengono utilizzate da consumer di eventi temporanei, consumer di eventi permanenti e provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="2cccc-105">Event queries are used by temporary event consumers, permanent event consumers, and event providers.</span></span> <span data-ttu-id="2cccc-106">I consumer di eventi utilizzano query di eventi per specificare gli eventi di interesse e i provider di eventi utilizzano le query per specificare gli eventi che forniscono.</span><span class="sxs-lookup"><span data-stu-id="2cccc-106">Event consumers use event queries to specify events of interest, and event providers use the queries to specify the events that they provide.</span></span>

<span data-ttu-id="2cccc-107">[I consumer temporanei](receiving-events-for-the-duration-of-your-application.md) inseriscono le query nelle chiamate al metodo [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) o [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="2cccc-107">[Temporary consumers](receiving-events-for-the-duration-of-your-application.md) place queries in calls to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span> <span data-ttu-id="2cccc-108">[I consumer di eventi permanenti](receiving-events-at-all-times.md) inseriscono query nella proprietà **query** di un'istanza della classe di sistema [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="2cccc-108">[Permanent event consumers](receiving-events-at-all-times.md) place queries in the **Query** property of an instance of the [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>

<span data-ttu-id="2cccc-109">I [provider di eventi](writing-an-event-provider.md) utilizzano le query di eventi per eseguire la registrazione per supportare uno o più tipi di eventi.</span><span class="sxs-lookup"><span data-stu-id="2cccc-109">[Event providers](writing-an-event-provider.md) use event queries to register to support one or more types of events.</span></span> <span data-ttu-id="2cccc-110">Inseriscono le query nella proprietà **EventQueryList** di un'istanza della classe di sistema [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="2cccc-110">They place queries in the **EventQueryList** property of an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) system class.</span></span> <span data-ttu-id="2cccc-111">Tutti i provider di eventi creano un'istanza di **\_ \_ EventProviderRegistration** per la registrazione con Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2cccc-111">All event providers create an **\_\_EventProviderRegistration** instance to register with Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="2cccc-112">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di eventi](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2cccc-112">For more information, see [Registering an Event Provider](registering-an-event-provider.md).</span></span>

<span data-ttu-id="2cccc-113">I consumer e i provider di eventi utilizzano l' [istruzione SELECT](select-statement-for-event-queries.md) e una clausola WHERE correlata per le query di eventi, oltre a un'ampia gamma di estensioni specifiche per il WMI Query Language (WQL).</span><span class="sxs-lookup"><span data-stu-id="2cccc-113">Event consumers and providers use the [SELECT statement](select-statement-for-event-queries.md) and a related WHERE clause for event queries, plus a variety of extensions specific to the WMI Query Language (WQL).</span></span> <span data-ttu-id="2cccc-114">Le estensioni vengono usate per proteggere gli utenti dal sovraccarico delle notifiche che si verificano troppo spesso per essere utili.</span><span class="sxs-lookup"><span data-stu-id="2cccc-114">The extensions are used to protect consumers from being flooded with notifications that occur too frequently to be useful.</span></span>

<span data-ttu-id="2cccc-115">I consumer che non richiedono la notifica ogni volta che si verifica un evento possono specificare le clausole seguenti nelle query:</span><span class="sxs-lookup"><span data-stu-id="2cccc-115">Consumers that do not require notification each time an event occurs can specify the following clauses in their queries:</span></span>

-   <span data-ttu-id="2cccc-116">Clausola [within](within-clause.md)</span><span class="sxs-lookup"><span data-stu-id="2cccc-116">[WITHIN](within-clause.md) clause</span></span>
-   <span data-ttu-id="2cccc-117">Clausola [Group](group-clause.md)</span><span class="sxs-lookup"><span data-stu-id="2cccc-117">[GROUP](group-clause.md) clause</span></span>
-   <span data-ttu-id="2cccc-118">Clausola [having](having-clause.md)</span><span class="sxs-lookup"><span data-stu-id="2cccc-118">[HAVING](having-clause.md) clause</span></span>

<span data-ttu-id="2cccc-119">Le clausole with e HAVING influiscono sul tempo degli eventi e la clausola GROUP genera un evento rappresentativo da inviare al posto di un evento che si verifica di frequente.</span><span class="sxs-lookup"><span data-stu-id="2cccc-119">The WITHIN and HAVING clauses affect the timing of events, and the GROUP clause causes a representative event to be sent in place of a frequently occurring event.</span></span>

 

 



