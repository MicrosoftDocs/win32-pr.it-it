---
description: I personal computer che eseguono Microsoft Windows hanno spesso numerose connessioni di rete, ad esempio più schede di interfaccia di rete (NIC) connesse a reti diverse o una connessione di rete fisica e una connessione remota.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Provider del servizio di riconoscimento del percorso di rete (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129143"
---
# <a name="network-location-awareness-service-provider-nla"></a><span data-ttu-id="c023d-103">Provider del servizio di riconoscimento del percorso di rete (NLA)</span><span class="sxs-lookup"><span data-stu-id="c023d-103">Network Location Awareness Service Provider (NLA)</span></span>

<span data-ttu-id="c023d-104">I personal computer che eseguono Microsoft Windows hanno spesso numerose connessioni di rete, ad esempio più schede di interfaccia di rete (NIC) connesse a reti diverse o una connessione di rete fisica e una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="c023d-104">Personal computers running Microsoft Windows often have numerous network connections, such as multiple network interface cards (NIC) connected to different networks, or a physical network connection and a dial-up connection.</span></span> <span data-ttu-id="c023d-105">Windows Sockets è stato in grado di enumerare le interfacce di rete disponibili per un certo periodo di tempo, ma alcune informazioni critiche sulle connessioni di rete non erano disponibili in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c023d-105">Windows Sockets has been capable of enumerating available network interfaces for some time, but certain critical information about network connections was previously unavailable.</span></span> <span data-ttu-id="c023d-106">Sono incluse informazioni quali la rete logica a cui è collegato un computer Windows o se più interfacce sono connesse alla stessa rete.</span><span class="sxs-lookup"><span data-stu-id="c023d-106">This includes information such as the logical network to which a Windows computer is attached or whether multiple interfaces are connected to the same network.</span></span>

<span data-ttu-id="c023d-107">Il provider del servizio di riconoscimento del percorso di rete, comunemente noto come NLA, consente alle applicazioni Windows Sockets 2 di identificare la rete logica a cui è collegato un computer Windows.</span><span class="sxs-lookup"><span data-stu-id="c023d-107">The Network Location Awareness service provider, commonly referred to as NLA, enables Windows Sockets 2 applications to identify the logical network to which a Windows computer is attached.</span></span> <span data-ttu-id="c023d-108">Inoltre, NLA consente alle applicazioni Windows Sockets di identificare l'interfaccia di rete fisica che una determinata applicazione ha salvato informazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="c023d-108">In addition, NLA enables Windows Sockets applications to identify to which physical network interface a given application has saved specific information.</span></span> <span data-ttu-id="c023d-109">NLA viene implementato come provider di servizi di risoluzione dei nomi Windows Sockets 2 generico.</span><span class="sxs-lookup"><span data-stu-id="c023d-109">NLA is implemented as a generic Windows Sockets 2 Name Resolution service provider.</span></span>

 

 



