---
title: Più servizi directory
description: Una sfida di lavorare all'interno di un ambiente di elaborazione distribuita è l'identificazione e l'individuazione di risorse quali utenti, gruppi, code di stampa e documenti.
ms.assetid: 66929290-b830-4768-a2ae-604d1a9de5c4
ms.tgt_platform: multiple
keywords:
- ADSI per più servizi directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2e174fc1b07564f1cca6c12093a289a0c865a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328412"
---
# <a name="multiple-directory-services"></a><span data-ttu-id="94d12-104">Più servizi directory</span><span class="sxs-lookup"><span data-stu-id="94d12-104">Multiple Directory Services</span></span>

<span data-ttu-id="94d12-105">Una sfida di lavorare all'interno di un ambiente di elaborazione distribuita è l'identificazione e l'individuazione di risorse quali utenti, gruppi, code di stampa e documenti.</span><span class="sxs-lookup"><span data-stu-id="94d12-105">One challenge of working within a distributed computing environment is identifying and locating resources such as users, groups, print queues, and documents.</span></span> <span data-ttu-id="94d12-106">Un servizio directory è la parte di un ambiente di elaborazione distribuita che fornisce un modo per individuare e identificare gli utenti e le risorse disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="94d12-106">A directory service is the part of a distributed computing environment that provides a way to locate and identify the users and resources available in the system.</span></span> <span data-ttu-id="94d12-107">Un servizio directory è analogo a una directory telefonica.</span><span class="sxs-lookup"><span data-stu-id="94d12-107">A directory service is like a phone directory.</span></span> <span data-ttu-id="94d12-108">Dato un nome per una persona o una risorsa, fornisce i dati necessari per accedere a tale persona o risorsa.</span><span class="sxs-lookup"><span data-stu-id="94d12-108">Given a name for a person or a resource, it provides the data necessary to access that person or resource.</span></span> <span data-ttu-id="94d12-109">Non è necessario iniziare con i dati di binding per accedere a una risorsa nella rete.</span><span class="sxs-lookup"><span data-stu-id="94d12-109">You do not have to start with binding data to access a resource on the network.</span></span>

<span data-ttu-id="94d12-110">Per la maggior parte delle aziende sono già presenti molte directory diverse.</span><span class="sxs-lookup"><span data-stu-id="94d12-110">Most enterprises already have many different directories in place.</span></span> <span data-ttu-id="94d12-111">Ad esempio, i sistemi operativi di rete, i sistemi di posta elettronica e i prodotti "groupware" hanno tutte le proprie directory.</span><span class="sxs-lookup"><span data-stu-id="94d12-111">For example, network operating systems, electronic mail systems, and "groupware" products all have their own directories.</span></span> <span data-ttu-id="94d12-112">Molti problemi si verificano quando una singola organizzazione distribuisce più directory.</span><span class="sxs-lookup"><span data-stu-id="94d12-112">Many issues arise when a single enterprise deploys multiple directories.</span></span> <span data-ttu-id="94d12-113">Questi problemi includono l'usabilità, la coerenza dei dati, i costi di sviluppo e i costi di supporto, tra gli altri.</span><span class="sxs-lookup"><span data-stu-id="94d12-113">These issues include usability, data consistency, development cost, and support cost, among others.</span></span>

<span data-ttu-id="94d12-114">Questi problemi vengono risolti in ADSI, in quanto viene fornito un set di interfacce singolo, coerente e aperto che può essere utilizzato per la gestione e l'utilizzo di qualsiasi servizio di directory con un provider ADSI.</span><span class="sxs-lookup"><span data-stu-id="94d12-114">These issues are addressed in ADSI, in that there is provided a single, consistent, open set of interfaces that can be used for managing and using any directory service that has an ADSI provider.</span></span>

 

 




