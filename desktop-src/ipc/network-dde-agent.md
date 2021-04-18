---
description: L'agente DDE di rete avvia la rete DDE se rileva l'attività DDE della rete locale.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agente DDE di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305708"
---
# <a name="network-dde-agent"></a><span data-ttu-id="2e62e-103">Agente DDE di rete</span><span class="sxs-lookup"><span data-stu-id="2e62e-103">Network DDE Agent</span></span>

<span data-ttu-id="2e62e-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="2e62e-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="2e62e-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="2e62e-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="2e62e-106">L'agente DDE di rete avvia la rete DDE se rileva l'attività DDE della rete locale.</span><span class="sxs-lookup"><span data-stu-id="2e62e-106">The network DDE agent starts network DDE if it detects local network DDE activity.</span></span> <span data-ttu-id="2e62e-107">Non rileva un client remoto che tenta di connettersi.</span><span class="sxs-lookup"><span data-stu-id="2e62e-107">It does not detect a remote client trying to connect.</span></span> <span data-ttu-id="2e62e-108">Pertanto, prima che un client possa connettersi correttamente, è necessario avviare la rete DDE sul computer server.</span><span class="sxs-lookup"><span data-stu-id="2e62e-108">Therefore, before any client can successfully connect, network DDE must be started on the server computer.</span></span> <span data-ttu-id="2e62e-109">Si noti che la rete DDE non è avviata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2e62e-109">Note that network DDE is not started by default.</span></span> <span data-ttu-id="2e62e-110">Per avviare la rete DDE, eseguire NETDDE.EXE.</span><span class="sxs-lookup"><span data-stu-id="2e62e-110">To start network DDE, run NETDDE.EXE.</span></span> <span data-ttu-id="2e62e-111">Questo file si trova nella directory di Windows.</span><span class="sxs-lookup"><span data-stu-id="2e62e-111">This file is located in your Windows directory.</span></span>

<span data-ttu-id="2e62e-112">L'agente DDE di rete avvia anche le applicazioni necessarie per la rete DDE.</span><span class="sxs-lookup"><span data-stu-id="2e62e-112">The network DDE agent also starts the applications necessary for network DDE.</span></span> <span data-ttu-id="2e62e-113">Una volta avviata la rete DDE, le conversazioni DDE vengono controllate tramite una finestra DDE di rete associata a una delle applicazioni DDE di rete.</span><span class="sxs-lookup"><span data-stu-id="2e62e-113">After network DDE is started, DDE conversations are controlled through a network DDE window associated with one of the network DDE applications.</span></span> <span data-ttu-id="2e62e-114">Questa applicazione funge da proxy.</span><span class="sxs-lookup"><span data-stu-id="2e62e-114">This application acts as a proxy.</span></span> <span data-ttu-id="2e62e-115">Comunica con tutte le applicazioni DDE locali e remote.</span><span class="sxs-lookup"><span data-stu-id="2e62e-115">It communicates with all local and remote DDE applications.</span></span>

 

 



