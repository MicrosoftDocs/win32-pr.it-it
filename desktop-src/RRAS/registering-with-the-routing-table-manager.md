---
title: Registrazione con gestione tabelle di routing
description: Prima che un client possa accedere alla tabella di routing, deve prima eseguire la registrazione con gestione tabelle di routing tramite la funzione RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Gestione tabelle di routing versione 2 RRAS, registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221356"
---
# <a name="registering-with-the-routing-table-manager"></a><span data-ttu-id="be142-104">Registrazione con gestione tabelle di routing</span><span class="sxs-lookup"><span data-stu-id="be142-104">Registering with the Routing Table Manager</span></span>

<span data-ttu-id="be142-105">Prima che un client possa accedere alla tabella di routing, deve prima eseguire la registrazione con gestione tabelle di routing tramite la funzione [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .</span><span class="sxs-lookup"><span data-stu-id="be142-105">Before a client can access the routing table, it first must register with the routing table manager using the [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function.</span></span>

<span data-ttu-id="be142-106">Quando un client esegue la registrazione, passa a gestione tabelle di routing una struttura di [**\_ \_ informazioni sull'entità RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) .</span><span class="sxs-lookup"><span data-stu-id="be142-106">When a client registers, it passes to the routing table manager an [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structure.</span></span> <span data-ttu-id="be142-107">Questa struttura contiene le informazioni che identificano in modo univoco un client, la famiglia di indirizzi e l'istanza di gestione tabelle di routing con cui il client sta effettuando la registrazione.</span><span class="sxs-lookup"><span data-stu-id="be142-107">This structure contains the information that uniquely identifies a client, the address family, and the instance of the routing table manager with which the client is registering.</span></span> <span data-ttu-id="be142-108">Un client può anche stabilire il callback di [**\_ \_ callback evento RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) .</span><span class="sxs-lookup"><span data-stu-id="be142-108">A client can also establish the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback.</span></span> <span data-ttu-id="be142-109">Il servizio di gestione delle tabelle di routing utilizzerà questo callback per notificare al client gli eventi, ad esempio le notifiche di modifica e le registrazioni dei client.</span><span class="sxs-lookup"><span data-stu-id="be142-109">The routing table manager will use this callback to notify the client of events such as change notifications and client registrations.</span></span>

<span data-ttu-id="be142-110">Gestione tabelle di routing completa l'elaborazione della registrazione e restituisce un handle per il client.</span><span class="sxs-lookup"><span data-stu-id="be142-110">The routing table manager completes its registration processing and returns a handle to the client.</span></span> <span data-ttu-id="be142-111">Il client deve usare questo handle per tutte le chiamate successive alle funzioni RTMv2.</span><span class="sxs-lookup"><span data-stu-id="be142-111">The client must use this handle for all subsequent calls to RTMv2 functions.</span></span>

<span data-ttu-id="be142-112">La funzione [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) utilizzata in RTMv2 è analoga alla funzione [**RtmRegisterClient**](rtmregisterclient.md) utilizzata in RTMv1.</span><span class="sxs-lookup"><span data-stu-id="be142-112">The [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function that is used in RTMv2 is analogous to the [**RtmRegisterClient**](rtmregisterclient.md) function that is used in RTMv1.</span></span> <span data-ttu-id="be142-113">La funzione **RtmRegisterClient** è obsoleta, ad eccezione dei client che utilizzano IPX.</span><span class="sxs-lookup"><span data-stu-id="be142-113">The **RtmRegisterClient** function is obsolete, except for clients using IPX.</span></span>

<span data-ttu-id="be142-114">Una volta che un client ha terminato l'interazione con gestione tabelle di routing, deve chiamare [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span><span class="sxs-lookup"><span data-stu-id="be142-114">Once a client has finished interacting with the routing table manager, it must call [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span></span> <span data-ttu-id="be142-115">Gestione tabelle di routing Elimina l'handle associato al client.</span><span class="sxs-lookup"><span data-stu-id="be142-115">The routing table manager destroys the handle associated with the client.</span></span> <span data-ttu-id="be142-116">Per evitare perdite di memoria, il client deve assicurarsi che rilasci tutti gli handle ed elimini tutte le route e gli hop successivi che possiede prima di chiamare **RtmDeregisterEntity**.</span><span class="sxs-lookup"><span data-stu-id="be142-116">To avoid memory leaks, the client must ensure that it releases all handles and deletes all the routes and next hops that it owns before calling **RtmDeregisterEntity**.</span></span>

<span data-ttu-id="be142-117">Per il codice di esempio che illustra come usare queste funzioni, vedere eseguire la [registrazione con gestione tabelle di routing](register-with-the-routing-table-manager.md) e [usare il callback di notifica degli eventi](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="be142-117">For sample code that shows how to use these functions, see [Register with the Routing Table Manager](register-with-the-routing-table-manager.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




