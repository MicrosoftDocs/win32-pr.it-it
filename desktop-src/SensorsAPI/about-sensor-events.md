---
description: L'API del sensore può fornire notifiche degli eventi.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Informazioni sugli eventi dell'API del sensore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884265"
---
# <a name="about-sensor-api-events"></a><span data-ttu-id="3cc29-103">Informazioni sugli eventi dell'API del sensore</span><span class="sxs-lookup"><span data-stu-id="3cc29-103">About Sensor API Events</span></span>

<span data-ttu-id="3cc29-104">L'API del sensore può fornire notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="3cc29-104">The Sensor API can provide event notifications.</span></span>

<span data-ttu-id="3cc29-105">Quando si esegue la registrazione per ricevere eventi, tramite [**ISensor:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) o [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)è necessario fornire un puntatore a un'interfaccia di callback.</span><span class="sxs-lookup"><span data-stu-id="3cc29-105">When you register to receive events, through either [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) or [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), you must provide a pointer to a callback interface.</span></span> <span data-ttu-id="3cc29-106">È necessario implementare i metodi dell'interfaccia di callback nel codice.</span><span class="sxs-lookup"><span data-stu-id="3cc29-106">You must implement the methods of the callback interface in your code.</span></span> <span data-ttu-id="3cc29-107">L'API del sensore definisce le interfacce di callback seguenti:</span><span class="sxs-lookup"><span data-stu-id="3cc29-107">The Sensor API defines the following callback interfaces:</span></span>

-   <span data-ttu-id="3cc29-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="3cc29-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="3cc29-109">Implementare questa interfaccia per ricevere eventi dai sensori.</span><span class="sxs-lookup"><span data-stu-id="3cc29-109">Implement this interface to receive events from sensors.</span></span> <span data-ttu-id="3cc29-110">I sensori possono notificare all'applicazione i nuovi dati, le modifiche allo stato del sensore, la disconnessione del sensore e gli eventi personalizzati definiti dal produttore del sensore.</span><span class="sxs-lookup"><span data-stu-id="3cc29-110">Sensors can notify your application about new data, changes in sensor state, sensor disconnection, and custom events defined by the sensor manufacturer.</span></span>
-   <span data-ttu-id="3cc29-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="3cc29-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span> <span data-ttu-id="3cc29-112">Implementare questa interfaccia per ricevere eventi da Gestione sensori.</span><span class="sxs-lookup"><span data-stu-id="3cc29-112">Implement this interface to receive events from the sensor manager.</span></span> <span data-ttu-id="3cc29-113">Gestione sensori può inviare una notifica all'applicazione quando si connette un sensore e pertanto può essere disponibile per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="3cc29-113">The sensor manager can notify your application when a sensor connects, and therefore may be available for use.</span></span>

<span data-ttu-id="3cc29-114">È possibile annullare le notifiche degli eventi chiamando di nuovo [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) , questa volta passando un valore **null** tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="3cc29-114">You can cancel event notifications by calling [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) again, this time passing a **NULL** value through the parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cc29-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3cc29-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cc29-116">Uso degli eventi dell'API del sensore</span><span class="sxs-lookup"><span data-stu-id="3cc29-116">Using Sensor API Events</span></span>](using-sensor-api-events.md)
</dt> </dl>

 

 
