---
title: Problemi di programmazione di RTMv2
description: Le funzioni RTMv2 vengono scritte con i presupposti seguenti.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problemi di programmazione, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329844"
---
# <a name="rtmv2-programming-issues"></a><span data-ttu-id="0ff89-104">Problemi di programmazione di RTMv2</span><span class="sxs-lookup"><span data-stu-id="0ff89-104">RTMv2 Programming Issues</span></span>

<span data-ttu-id="0ff89-105">Le funzioni RTMv2 vengono scritte con i presupposti seguenti.</span><span class="sxs-lookup"><span data-stu-id="0ff89-105">RTMv2 functions are written with the following assumptions.</span></span>

-   <span data-ttu-id="0ff89-106">Le funzioni RTMv2 non allocano memoria per il client.</span><span class="sxs-lookup"><span data-stu-id="0ff89-106">RTMv2 functions do not allocate memory for the client.</span></span> <span data-ttu-id="0ff89-107">Il client deve sempre allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="0ff89-107">The client must always allocate memory.</span></span>
-   <span data-ttu-id="0ff89-108">Quando si annulla la registrazione di un client, è necessario eseguire operazioni di pulizia, ad esempio il rilascio di tutta la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="0ff89-108">When a client is unregistering, it must perform clean-up operations itself, such as releasing all memory allocated.</span></span>
-   <span data-ttu-id="0ff89-109">I client devono rilasciare gli handle correttamente; le perdite di memoria possono verificarsi se un client non osserva questa procedura.</span><span class="sxs-lookup"><span data-stu-id="0ff89-109">Clients must release handles correctly; memory leaks can occur if a client does not observe this practice.</span></span>

 

 




