---
description: Il servizio di notifica eventi di sistema consente alle applicazioni compatibili con dispositivi mobili di ricevere notifiche dagli eventi di sistema monitorati da SENS. Quando si verifica l'evento richiesto, SENS invia una notifica all'applicazione.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notifiche (servizio di notifica eventi di sistema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316628"
---
# <a name="notifications-system-event-notification-service"></a><span data-ttu-id="33ad6-104">Notifiche (servizio di notifica eventi di sistema)</span><span class="sxs-lookup"><span data-stu-id="33ad6-104">Notifications (System Event Notification Service)</span></span>

<span data-ttu-id="33ad6-105">Il servizio di notifica eventi di sistema consente alle applicazioni compatibili con dispositivi mobili di ricevere notifiche dagli eventi di sistema monitorati da SENS.</span><span class="sxs-lookup"><span data-stu-id="33ad6-105">The System Event Notification Service enables mobile-aware applications to receive notifications from system events that SENS monitors.</span></span> <span data-ttu-id="33ad6-106">Quando si verifica l'evento richiesto, SENS invia una notifica all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="33ad6-106">When the requested event occurs, SENS notifies the application.</span></span>

<span data-ttu-id="33ad6-107">SENS può notificare alle applicazioni circa tre classi di eventi di sistema:</span><span class="sxs-lookup"><span data-stu-id="33ad6-107">SENS can notify applications about three classes of system events:</span></span>

-   <span data-ttu-id="33ad6-108">Eventi di rete TCP/IP, ad esempio lo stato di una connessione di rete TCP/IP o la qualità della connessione.</span><span class="sxs-lookup"><span data-stu-id="33ad6-108">TCP/IP network events, such as the status of a TCP/IP network connection or the quality of the connection.</span></span>
-   <span data-ttu-id="33ad6-109">Eventi di accesso utente.</span><span class="sxs-lookup"><span data-stu-id="33ad6-109">User logon events.</span></span>
-   <span data-ttu-id="33ad6-110">Eventi di alimentazione a batteria e AC.</span><span class="sxs-lookup"><span data-stu-id="33ad6-110">Battery and AC power events.</span></span>

<span data-ttu-id="33ad6-111">Ad esempio, un'applicazione può sottoscrivere uno qualsiasi degli eventi di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="33ad6-111">For example, an application can subscribe to any of the following system events:</span></span>

-   <span data-ttu-id="33ad6-112">Creazione della connettività di rete</span><span class="sxs-lookup"><span data-stu-id="33ad6-112">Establishment of network connectivity</span></span>
-   <span data-ttu-id="33ad6-113">Notifica quando è possibile raggiungere una destinazione specificata entro i parametri di qualità della connessione (QOC) specificati</span><span class="sxs-lookup"><span data-stu-id="33ad6-113">Notification when a specified destination can be reached within specified Quality of Connection (QOC) parameters</span></span>
-   <span data-ttu-id="33ad6-114">Il computer è stato alimentato a batteria</span><span class="sxs-lookup"><span data-stu-id="33ad6-114">The computer has switched to battery power</span></span>
-   <span data-ttu-id="33ad6-115">La percentuale di alimentazione della batteria rimanente rientra in un parametro specificato</span><span class="sxs-lookup"><span data-stu-id="33ad6-115">The percentage of remaining battery power is within a specified parameter</span></span>
-   <span data-ttu-id="33ad6-116">Eventi pianificati con Gestione sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="33ad6-116">Scheduled events using Synchronization Manager occur</span></span>

<span data-ttu-id="33ad6-117">**Windows Server 2008 R2 e Windows 7:** Il Sottoscrittore è costituito da un massimo di 3 minuti per rispondere a una notifica sulle interfacce [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) e [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) .</span><span class="sxs-lookup"><span data-stu-id="33ad6-117">**Windows Server 2008 R2 and Windows 7:** The subscriber has a maximum of 3 minutes to respond to a notification on the [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) and [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) interfaces.</span></span> <span data-ttu-id="33ad6-118">Dopo 3 minuti, SENS Annulla la chiamata ai sottoscrittori e sblocca il thread di notifica.</span><span class="sxs-lookup"><span data-stu-id="33ad6-118">After 3 minutes, SENS cancels the call to subscribers and unblocks the notification thread.</span></span> <span data-ttu-id="33ad6-119">Se è necessaria un'operazione di lunga durata per rispondere alla notifica, restituire da **ISensLogon** o **ISensLogon2** il più rapidamente possibile e aprire un altro thread per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="33ad6-119">If a lengthy operation is required to respond to the notification, return from **ISensLogon** or **ISensLogon2** as quickly as possible and open another thread for processing.</span></span>

 

 



