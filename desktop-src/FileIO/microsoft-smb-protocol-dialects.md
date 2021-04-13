---
description: Per stabilire una connessione tra un client e un server utilizzando il protocollo SMB Microsoft, è necessario innanzitutto determinare il dialetto con il livello più elevato di funzionalità supportate dal client e dal server.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Dialetti del protocollo SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484732"
---
# <a name="microsoft-smb-protocol-dialects"></a><span data-ttu-id="8984c-103">Dialetti del protocollo SMB Microsoft</span><span class="sxs-lookup"><span data-stu-id="8984c-103">Microsoft SMB Protocol Dialects</span></span>

<span data-ttu-id="8984c-104">L'elenco dei pacchetti di messaggi del protocollo SMB Microsoft è cresciuto nel corso degli anni per supportare le funzionalità crescenti del protocollo SMB Microsoft e ora i numeri delle centinaia.</span><span class="sxs-lookup"><span data-stu-id="8984c-104">The list of Microsoft SMB Protocol message packets has grown over the years to accommodate the increasing functionality of Microsoft SMB Protocol, and now numbers in the hundreds.</span></span> <span data-ttu-id="8984c-105">Ogni fase della sua crescita è contrassegnata da un set di pacchetti standard o dal dialetto.</span><span class="sxs-lookup"><span data-stu-id="8984c-105">Each stage of its growth is marked by a standard packet set, or dialect.</span></span> <span data-ttu-id="8984c-106">Ogni dialetto è identificato da una stringa standard, ad esempio "PC NETWORK PROGRAM 1,0", "MICROSOFT NETWORKs 3,0", "DOS LANMAN 2,1" o "NT LM 0,12".</span><span class="sxs-lookup"><span data-stu-id="8984c-106">Each dialect is identified by a standard string such as "PC NETWORK PROGRAM 1.0", "MICROSOFT NETWORKS 3.0", "DOS LANMAN 2.1", or "NT LM 0.12".</span></span> <span data-ttu-id="8984c-107">La prima stringa identifica il primo dialetto SMB e l'ultima stringa identifica CIFS, il primo dialetto del protocollo SMB Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8984c-107">The first string identifies the first dialect of SMB, and the last string identifies CIFS, the first dialect of Microsoft SMB Protocol.</span></span>

<span data-ttu-id="8984c-108">La maggior parte dei client Windows supporta almeno sei dialetti diversi del protocollo SMB Microsoft, quindi uno dei primi passaggi per stabilire una connessione tra un client e un server tramite il protocollo SMB Microsoft consiste nel determinare il dialetto con il massimo livello di funzionalità supportato dal client e dal server.</span><span class="sxs-lookup"><span data-stu-id="8984c-108">Most Windows clients support at least six different dialects of Microsoft SMB Protocol, so one of the first steps in establishing a connection between a client and a server using Microsoft SMB Protocol is to determine the dialect with the highest level of functionality that both the client and server support.</span></span> <span data-ttu-id="8984c-109">Questo processo è noto come "negoziazione del dialetto".</span><span class="sxs-lookup"><span data-stu-id="8984c-109">This process is known as "negotiating the dialect."</span></span> <span data-ttu-id="8984c-110">Le stringhe di dialetto indicate in precedenza sono incluse nei pacchetti di richiesta e risposta di negoziazione di dialetto per questo scopo.</span><span class="sxs-lookup"><span data-stu-id="8984c-110">The dialect strings mentioned above are included in the dialect negotiation request and response packets for this purpose.</span></span>

 

 



