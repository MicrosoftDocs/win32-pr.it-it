---
title: Sviluppo rispetto alla distribuzione in rete
description: La maggior parte degli sviluppatori scrive e testa il software in una LAN affidabile veloce.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044590"
---
# <a name="development-vs-deployment-in-the-network"></a><span data-ttu-id="94c6d-103">Sviluppo rispetto alla distribuzione in rete</span><span class="sxs-lookup"><span data-stu-id="94c6d-103">Development vs. Deployment in the Network</span></span>

<span data-ttu-id="94c6d-104">La maggior parte degli sviluppatori scrive e testa il software in una LAN affidabile veloce.</span><span class="sxs-lookup"><span data-stu-id="94c6d-104">Most developers write and test their software on a fast reliable LAN.</span></span> <span data-ttu-id="94c6d-105">Il client e il server sono spesso nello stesso segmento di rete.</span><span class="sxs-lookup"><span data-stu-id="94c6d-105">Their client and server are often on the same network segment.</span></span> <span data-ttu-id="94c6d-106">In questi casi la rete non risponde raramente e la connettività si interrompe raramente.</span><span class="sxs-lookup"><span data-stu-id="94c6d-106">In such circumstances the network is rarely unresponsive, and connectivity rarely lost.</span></span> <span data-ttu-id="94c6d-107">Quando vengono distribuiti in un ambiente cliente, tuttavia, il client e il server si trovano spesso in segmenti di rete diversi, possibilmente geograficamente remoti, e il server viene caricato molto con altri client.</span><span class="sxs-lookup"><span data-stu-id="94c6d-107">When deployed in a customer environment however, client and server are often on different network segments, possibly geographically remote, and the server is heavily loaded with other clients.</span></span> <span data-ttu-id="94c6d-108">In altre parole, non è possibile presupporre la velocità di risposta della rete.</span><span class="sxs-lookup"><span data-stu-id="94c6d-108">In other words: network responsiveness cannot be assumed.</span></span>

<span data-ttu-id="94c6d-109">In questo articolo viene illustrato come costruire solide architetture client/server in presenza di incertezze introdotte da una rete intrinsecamente inaffidabile e da server potenzialmente non disponibili.</span><span class="sxs-lookup"><span data-stu-id="94c6d-109">This article explains how to construct robust client/server architectures in the face of uncertainty introduced by an intrinsically unreliable network and potentially unavailable servers.</span></span>

 

 




