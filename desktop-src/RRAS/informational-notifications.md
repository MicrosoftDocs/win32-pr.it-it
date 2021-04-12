---
title: Notifiche informative
description: Per gli Stati di connessione noti come stati in esecuzione, non è richiesta alcuna azione del gestore di notifiche a meno che non si verifichi un errore.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2020
ms.locfileid: "104472398"
---
# <a name="informational-notifications"></a><span data-ttu-id="12b4d-103">Notifiche informative</span><span class="sxs-lookup"><span data-stu-id="12b4d-103">Informational Notifications</span></span>

<span data-ttu-id="12b4d-104">Per gli [Stati di connessione](connection-states.md) noti come stati in esecuzione, non è richiesta alcuna azione del gestore di notifiche a meno che non si verifichi un errore.</span><span class="sxs-lookup"><span data-stu-id="12b4d-104">For the [connection states](connection-states.md) known as running states, no action is required of the notification handler unless an error occurs.</span></span> <span data-ttu-id="12b4d-105">Gli Stati di esecuzione si verificano durante le parti dell'operazione di connessione gestite automaticamente da RAS, ad esempio la connessione ai dispositivi necessari, l'autenticazione dell'utente e l'attesa di un callback dal server remoto.</span><span class="sxs-lookup"><span data-stu-id="12b4d-105">Running states occur during the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="12b4d-106">La notifica è semplicemente un report sullo stato di avanzamento per il client.</span><span class="sxs-lookup"><span data-stu-id="12b4d-106">The notification is simply a progress report to the client.</span></span>

<span data-ttu-id="12b4d-107">Il client può scegliere di passare le notifiche informative all'utente.</span><span class="sxs-lookup"><span data-stu-id="12b4d-107">The client can choose to pass these informational notifications on to the user.</span></span> <span data-ttu-id="12b4d-108">In alcuni stati in esecuzione, il client potrebbe voler visualizzare informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="12b4d-108">In some running states, the client may want to display additional information.</span></span> <span data-ttu-id="12b4d-109">Ad esempio, un gestore di notifiche che riceve una \_ notifica RASCS ConnectDevice può chiamare la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere il nome e il tipo del dispositivo a cui si è connessi.</span><span class="sxs-lookup"><span data-stu-id="12b4d-109">For example, a notification handler that receives a RASCS\_ConnectDevice notification can call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the name and type of the device being connected to.</span></span> <span data-ttu-id="12b4d-110">Un altro esempio è quando il client riceve una \_ notifica RASCS proiettata.</span><span class="sxs-lookup"><span data-stu-id="12b4d-110">Another example is when the client receives a RASCS\_Projected notification.</span></span> <span data-ttu-id="12b4d-111">Questo errore si verifica quando la fase di proiezione RAS dell'operazione di connessione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="12b4d-111">This occurs when the RAS projection phase of the connection operation has been completed.</span></span> <span data-ttu-id="12b4d-112">Il client può chiamare la funzione [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) per ottenere informazioni aggiuntive sulla proiezione.</span><span class="sxs-lookup"><span data-stu-id="12b4d-112">The client can call the [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) function to get additional information about the projection.</span></span> <span data-ttu-id="12b4d-113">Il client può utilizzare queste informazioni per notificare all'utente i protocolli di rete che possono essere utilizzati da questa connessione.</span><span class="sxs-lookup"><span data-stu-id="12b4d-113">The client can use this information to notify the user as to which network protocols can be used by this connection.</span></span>

<span data-ttu-id="12b4d-114">È consigliabile evitare di scrivere codice che dipende dall'ordine o dall'occorrenza di determinati stati informativi, perché questo può variare tra le piattaforme.</span><span class="sxs-lookup"><span data-stu-id="12b4d-114">You should avoid writing code that depends on the order or occurrence of particular informational states, because this may vary between platforms.</span></span>

 

 




