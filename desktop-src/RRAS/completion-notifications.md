---
title: Notifiche di completamento
description: La gestione connessione di accesso remoto continua le notifiche di stato fino al completamento dell'operazione di connessione.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044755"
---
# <a name="completion-notifications"></a><span data-ttu-id="2ee55-103">Notifiche di completamento</span><span class="sxs-lookup"><span data-stu-id="2ee55-103">Completion Notifications</span></span>

<span data-ttu-id="2ee55-104">La gestione connessione di accesso remoto continua le notifiche di stato fino al completamento dell'operazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="2ee55-104">The Remote Access Connection Manager continues progress notifications until the connection operation has been completed.</span></span> <span data-ttu-id="2ee55-105">Questo problema si verifica nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ee55-105">This occurs in the following situations:</span></span>

-   <span data-ttu-id="2ee55-106">Il gestore riceve una \_ notifica RASCS connessa o RASCS \_ disconnessa.</span><span class="sxs-lookup"><span data-stu-id="2ee55-106">The handler receives a RASCS\_Connected, or RASCS\_Disconnected notification.</span></span> <span data-ttu-id="2ee55-107">L'applicazione client RAS può uscire senza interruzioni della connessione stabilita.</span><span class="sxs-lookup"><span data-stu-id="2ee55-107">The RAS client application can exit without breaking any established connection.</span></span>
-   <span data-ttu-id="2ee55-108">Si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="2ee55-108">An error occurs.</span></span> <span data-ttu-id="2ee55-109">Il gestore riceve una notifica che indica l'errore e lo stato della connessione quando si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="2ee55-109">The handler receives a notification indicating the error and the connection state when the error occurred.</span></span> <span data-ttu-id="2ee55-110">È possibile uscire dall'applicazione client RAS.</span><span class="sxs-lookup"><span data-stu-id="2ee55-110">The RAS client application can exit.</span></span>

<span data-ttu-id="2ee55-111">L'applicazione client RAS non deve presupporre che l'operazione di connessione venga completata dopo la chiamata a [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span><span class="sxs-lookup"><span data-stu-id="2ee55-111">The RAS client application should not assume the connection operation is complete after calling [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span></span> <span data-ttu-id="2ee55-112">Deve attendere una delle condizioni precedenti prima di uscire.</span><span class="sxs-lookup"><span data-stu-id="2ee55-112">It should wait for one of the preceding conditions before exiting.</span></span>

 

 




