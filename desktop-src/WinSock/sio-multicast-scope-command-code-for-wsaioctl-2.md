---
description: Quando viene utilizzato il multicast, in genere è necessario specificare l'ambito sul quale deve essere eseguito il multicast.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: Codice del comando SIO_MULTICAST_SCOPE per WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049765"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a><span data-ttu-id="c371d-103">\_ \_ Codice del comando per ambito multicast Sio per WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="c371d-103">SIO\_MULTICAST\_SCOPE Command Code for WSAIoctl</span></span>

<span data-ttu-id="c371d-104">Quando viene utilizzato il multicast, in genere è necessario specificare l' *ambito* sul quale deve essere eseguito il multicast.</span><span class="sxs-lookup"><span data-stu-id="c371d-104">When multicasting is employed, it is usually necessary to specify the *scope* over which the multicast should occur.</span></span> <span data-ttu-id="c371d-105">L'ambito è definito come il numero di segmenti di rete indirizzati da coprire.</span><span class="sxs-lookup"><span data-stu-id="c371d-105">Scope is defined as the number of routed network segments to be covered.</span></span> <span data-ttu-id="c371d-106">Un ambito pari a zero indicherà che la trasmissione multicast non verrà distribuita in transito, ma potrebbe essere divulgata tra i socket all'interno dell'host locale.</span><span class="sxs-lookup"><span data-stu-id="c371d-106">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="c371d-107">Un valore di ambito pari a 1 (impostazione predefinita) indica che la trasmissione verrà posizionata in transito, ma non incrocierà alcun router.</span><span class="sxs-lookup"><span data-stu-id="c371d-107">A scope value of 1 (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="c371d-108">I valori di ambito più elevati determinano il numero di router che possono essere superati.</span><span class="sxs-lookup"><span data-stu-id="c371d-108">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="c371d-109">Si noti che corrisponde al parametro time-to-Live (TTL) in multicast IP.</span><span class="sxs-lookup"><span data-stu-id="c371d-109">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

<span data-ttu-id="c371d-110">La funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) viene usata per aggiungere un nodo foglia alla sessione multipoint.</span><span class="sxs-lookup"><span data-stu-id="c371d-110">The function [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) is used to join a leaf node into the multipoint session.</span></span> <span data-ttu-id="c371d-111">Per una discussione su come viene usata questa funzione, vedere quanto segue.</span><span class="sxs-lookup"><span data-stu-id="c371d-111">See the following for a discussion on how this function is utilized.</span></span>

 

 



