---
title: Rilevamento ed evitare la latenza di replica
description: La latenza di replica è un fatto di vita in un sistema distribuito a regime di controllo libero.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707720"
---
# <a name="detecting-and-avoiding-replication-latency"></a><span data-ttu-id="da0a3-103">Rilevamento ed evitare la latenza di replica</span><span class="sxs-lookup"><span data-stu-id="da0a3-103">Detecting and Avoiding Replication Latency</span></span>

<span data-ttu-id="da0a3-104">La latenza di replica è un fatto di vita in un sistema distribuito a regime di controllo libero.</span><span class="sxs-lookup"><span data-stu-id="da0a3-104">Replication latency is a fact of life in a loosely coupled distributed system.</span></span> <span data-ttu-id="da0a3-105">Le applicazioni devono soddisfare questa esigenza.</span><span class="sxs-lookup"><span data-stu-id="da0a3-105">Applications must accommodate this.</span></span> <span data-ttu-id="da0a3-106">Il modo migliore per gestire la latenza di replica consiste nel progettare le applicazioni per ridurre al minimo gli effetti.</span><span class="sxs-lookup"><span data-stu-id="da0a3-106">The best way to accommodate replication latency is to design applications to minimize the effects.</span></span> <span data-ttu-id="da0a3-107">Applicazione ideale abilitata per la directory:</span><span class="sxs-lookup"><span data-stu-id="da0a3-107">The ideal directory-enabled application:</span></span>

-   <span data-ttu-id="da0a3-108">Non è sensibile all'inclinazione della versione.</span><span class="sxs-lookup"><span data-stu-id="da0a3-108">Is insensitive to version skew.</span></span>
-   <span data-ttu-id="da0a3-109">Non dipende dalle relazioni tra più oggetti.</span><span class="sxs-lookup"><span data-stu-id="da0a3-109">Does not depend on relationships among multiple objects.</span></span>
-   <span data-ttu-id="da0a3-110">Non presenta requisiti di coerenza intra-o tra oggetti.</span><span class="sxs-lookup"><span data-stu-id="da0a3-110">Has no intra- or inter-object consistency requirements.</span></span>

<span data-ttu-id="da0a3-111">Le applicazioni e i servizi che soddisfano questo profilo non devono preoccuparsi della latenza di replica.</span><span class="sxs-lookup"><span data-stu-id="da0a3-111">Applications and services that fit this profile need not be concerned with replication latency.</span></span> <span data-ttu-id="da0a3-112">Le altre applicazioni devono essere progettate tenendo presente la latenza di replica.</span><span class="sxs-lookup"><span data-stu-id="da0a3-112">Other applications must be designed with replication latency in mind.</span></span> <span data-ttu-id="da0a3-113">La chiave per il successo nella progettazione di un'applicazione di questo tipo è la consapevolezza del processo di replica.</span><span class="sxs-lookup"><span data-stu-id="da0a3-113">The key to success in designing such an application is awareness of the replication process.</span></span> <span data-ttu-id="da0a3-114">I passaggi eseguiti in fase di progettazione per ridurre le dipendenze tra oggetti e ridurre al minimo le finestre degli aggiornamenti parziali pagheranno dividendi di grandi dimensioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="da0a3-114">Steps taken at design time to reduce inter-object dependencies and minimize partial update windows will pay large dividends at run time.</span></span> <span data-ttu-id="da0a3-115">Gli approcci alla gestione della latenza di replica sono divisi in due classi, ovvero strategie di prevenzione che riducono l'effetto delle strategie di latenza e rilevamento che consentono a un'applicazione di rilevare gli stati indotti dalla latenza.</span><span class="sxs-lookup"><span data-stu-id="da0a3-115">Approaches to dealing with replication latency are divided into two classes—avoidance strategies that reduce the impact of latency and detection strategies that allow an application to detect latency-induced states.</span></span>

 

 




