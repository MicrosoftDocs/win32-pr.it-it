---
description: Per alcune applicazioni è necessario ricevere una notifica degli eventi di connessione, prima dell'evento, subito dopo che si è verificata o entrambi. È possibile creare una DLL per ricevere una notifica avanzata e successiva al fatto degli eventi di connessione.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Ricezione di notifiche di connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524876"
---
# <a name="receiving-connection-notifications"></a><span data-ttu-id="176ec-104">Ricezione di notifiche di connessione</span><span class="sxs-lookup"><span data-stu-id="176ec-104">Receiving Connection Notifications</span></span>

<span data-ttu-id="176ec-105">Per alcune applicazioni è necessario ricevere una notifica degli eventi di connessione, prima dell'evento, subito dopo che si è verificata o entrambi.</span><span class="sxs-lookup"><span data-stu-id="176ec-105">Some applications need to receive notification of connection events, either before the event, just after it occurs, or both.</span></span> <span data-ttu-id="176ec-106">È possibile creare una DLL per ricevere una notifica avanzata e successiva al fatto degli eventi di connessione.</span><span class="sxs-lookup"><span data-stu-id="176ec-106">You can create a DLL to receive advance and after-the-fact notification of connection events.</span></span>

<span data-ttu-id="176ec-107">Un esempio di applicazione che deve ricevere una notifica di avanzamento di un evento di connessione è il servizio di accesso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="176ec-107">An example of an application that needs to receive advance notification of a connection event is the Remote Access Service (RAS).</span></span> <span data-ttu-id="176ec-108">Prima di stabilire una connessione, è necessario informare RAS perché potrebbe essere necessario stabilire una connessione modem prima di effettuare la connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="176ec-108">RAS needs to be informed before a connection is made because it may be necessary to establish a modem connection before making the network connection.</span></span>

<span data-ttu-id="176ec-109">Analogamente, è possibile che le applicazioni debbano pulire le risorse dopo aver effettuato la connessione, richiedendo pertanto una notifica post-connessione.</span><span class="sxs-lookup"><span data-stu-id="176ec-109">Similarly, applications may need to clean up resources after the connection is made, therefore requiring a post-connection notification.</span></span>

<span data-ttu-id="176ec-110">Le applicazioni interessate a ricevere notifiche avanzate e successive al fatto degli eventi di connessione devono fornire una DLL che esporta due funzioni, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) e [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span><span class="sxs-lookup"><span data-stu-id="176ec-110">Applications interested in receiving advance and after-the-fact notification of connection events must supply a DLL that exports two functions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) and [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span></span>

<span data-ttu-id="176ec-111">Dopo aver implementato queste funzioni, è necessario registrare la DLL come descritto in [registrazione per ricevere notifiche di connessione](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="176ec-111">After you implement these functions, you must register your DLL as described in [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 



