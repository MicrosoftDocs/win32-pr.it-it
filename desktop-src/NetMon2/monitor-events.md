---
description: I monitoraggi sono progettati per utilizzare Strumentazione gestione Windows (WMI) per attivare eventi in computer locali o remoti.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Monitorare gli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485148"
---
# <a name="monitor-events"></a><span data-ttu-id="97a5d-103">Monitorare gli eventi</span><span class="sxs-lookup"><span data-stu-id="97a5d-103">Monitor Events</span></span>

<span data-ttu-id="97a5d-104">I monitoraggi sono progettati per utilizzare [Strumentazione gestione Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) per attivare eventi in computer locali o remoti.</span><span class="sxs-lookup"><span data-stu-id="97a5d-104">Monitors are designed to use [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to fire events to local or remote computers.</span></span>

> [!Note]  
> <span data-ttu-id="97a5d-105">Poiché i monitoraggi utilizzano un'acquisizione in tempo reale, possono solo acquisire i dati nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="97a5d-105">Because monitors use a real-time capture they can only capture data at the local computer.</span></span> <span data-ttu-id="97a5d-106">Si tratta di una limitazione dell'interfaccia **IRTC** del provider di pacchetti di rete.</span><span class="sxs-lookup"><span data-stu-id="97a5d-106">This is a limitation of the network packet provider's **IRTC** interface.</span></span> <span data-ttu-id="97a5d-107">Tuttavia, utilizzando gli eventi WMI, i dati acquisiti possono essere esaminati localmente mentre gli eventi possono essere inviati a computer locali o remoti.</span><span class="sxs-lookup"><span data-stu-id="97a5d-107">However, by using WMI events, the captured data can be examined locally while events can be sent to local or remote computers.</span></span>

 

<span data-ttu-id="97a5d-108">I monitoraggi non comunicano direttamente con WMI.</span><span class="sxs-lookup"><span data-stu-id="97a5d-108">Monitors do not communicate directly with WMI.</span></span> <span data-ttu-id="97a5d-109">Il [*servizio di controllo di monitoraggio*](m.md) (MCSVC) fornisce un'interfaccia (denominata [IMonitorEventer](imonitoreventer.md)), che può essere usata dal monitoraggio per ottenere una struttura di dati degli eventi e riempirla con le informazioni rilevanti.</span><span class="sxs-lookup"><span data-stu-id="97a5d-109">The [*Monitor Control Service*](m.md) (MCSVC) provides an interface (called [IMonitorEventer](imonitoreventer.md)), which the monitor can use to obtain an event data structure and fill it with the relevant information.</span></span> <span data-ttu-id="97a5d-110">MCSVC può quindi inviare la struttura dei dati dell'evento a WMI, che a sua volta genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="97a5d-110">The MCSVC can then send the event data structure to WMI, which in turn fires the event.</span></span>

 

 
