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
# <a name="receiving-events-for-the-duration-of-your-application"></a><span data-ttu-id="4356c-103">Ricezione di eventi per la durata dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="4356c-103">Receiving Events for the Duration of Your Application</span></span>

<span data-ttu-id="4356c-104">Uno dei modi più comuni per ricevere un evento è tramite un'applicazione in esecuzione, ad esempio un'applicazione di gestione che raccoglie e visualizza gli eventi di un utente.</span><span class="sxs-lookup"><span data-stu-id="4356c-104">One of the most common ways to receive an event is through a running application, such as a management application that collects and displays events to a user.</span></span> <span data-ttu-id="4356c-105">Tali applicazioni sono denominate "temporanee" perché un consumer temporaneo non riceve le notifiche degli eventi quando viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="4356c-105">Such applications are called "temporary" because a temporary consumer does not receive event notifications when shut down.</span></span>

<span data-ttu-id="4356c-106">Un consumer temporaneo chiama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) nello script o [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ per sottoscrivere gli eventi in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4356c-106">A temporary consumer calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in script or [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ to subscribe to events in a namespace.</span></span> <span data-ttu-id="4356c-107">L'identità associata a questa sottoscrizione è il chiamante.</span><span class="sxs-lookup"><span data-stu-id="4356c-107">The identity associated with this subscription is the caller.</span></span>

<span data-ttu-id="4356c-108">Un consumer di eventi temporaneo può ricevere notifiche in modo asincrono o semisincrona in entrambi gli script e C++.</span><span class="sxs-lookup"><span data-stu-id="4356c-108">A temporary event consumer can receive notifications either asynchronously or semisynchronously in both scripts and C++.</span></span>

> [!Note]  
> <span data-ttu-id="4356c-109">Per motivi di sicurezza, è importante notare che le notifiche degli eventi asincroni non sono consigliate.</span><span class="sxs-lookup"><span data-stu-id="4356c-109">For security reasons, it is important to note that asynchronous event notifications are not recommended.</span></span> <span data-ttu-id="4356c-110">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="4356c-110">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span> <span data-ttu-id="4356c-111">I consumer di eventi hanno particolari problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4356c-111">Event consumers have special security concerns.</span></span> <span data-ttu-id="4356c-112">Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="4356c-112">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

 

<span data-ttu-id="4356c-113">Per ulteriori informazioni sulla ricezione di notifiche di eventi asincroni e semisincrono, vedere [ricezione di notifiche di eventi asincroni](receiving-asynchronous-event-notifications.md) e ricezione di notifiche di eventi [semisincrono](receiving-synchronous-and-semisynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="4356c-113">For more information about receiving asynchronous and semisynchronous event notifications, see [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md) and [Receiving Semisynchronous Event Notifications](receiving-synchronous-and-semisynchronous-event-notifications.md).</span></span>

 

 



