---
description: Le funzioni MultiPoint di Winsock generiche supportano il multicast IP.
ms.assetid: 32fffca8-4f13-495b-afb6-bb57a9cce553
title: Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c6b4ece06119d01e2661028f452985bb20b068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129159"
---
# <a name="multicast"></a><span data-ttu-id="0a7b4-103">Multicast</span><span class="sxs-lookup"><span data-stu-id="0a7b4-103">Multicast</span></span>

<span data-ttu-id="0a7b4-104">Le funzioni MultiPoint di Winsock generiche supportano il multicast IP.</span><span class="sxs-lookup"><span data-stu-id="0a7b4-104">Generic Winsock multipoint functions support IP multicast.</span></span> <span data-ttu-id="0a7b4-105">Tuttavia, i provider di trasporto TCP/IP che supportano il multicast devono anche fornire lo stile BSD (Berkeley Software Distribution), supportando le opzioni multicast corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="0a7b4-105">However, the TCP/IP transport providers that support multicast must also provide Berkeley Software Distribution (BSD) style–multicast support by supporting the corresponding multicast options.</span></span> <span data-ttu-id="0a7b4-106">In questo modo si semplifica il porting delle applicazioni multicast esistenti a Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="0a7b4-106">This simplifies the porting of existing multicast applications to Windows Sockets 2.</span></span>

 

 



