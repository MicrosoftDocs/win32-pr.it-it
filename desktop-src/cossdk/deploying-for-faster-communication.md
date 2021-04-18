---
description: Distribuzione per una comunicazione più veloce
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Distribuzione per una comunicazione più veloce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305326"
---
# <a name="deploying-for-faster-communication"></a><span data-ttu-id="10899-103">Distribuzione per una comunicazione più veloce</span><span class="sxs-lookup"><span data-stu-id="10899-103">Deploying for Faster Communication</span></span>

<span data-ttu-id="10899-104">Le prestazioni sono un fattore fondamentale quando si distribuisce un'applicazione COM+ e il percorso del componente è la chiave per ottenere le migliori prestazioni da un'applicazione progettata correttamente.</span><span class="sxs-lookup"><span data-stu-id="10899-104">Performance is a key consideration when deploying a COM+ application, and component location is the key to getting the best performance from a well-designed application.</span></span>

<span data-ttu-id="10899-105">Una volta diffusa questa situazione con le architetture di applicazioni scalabili, è possibile risolvere le prestazioni semplicemente spostando i componenti principali dell'applicazione in un hardware più rapido.</span><span class="sxs-lookup"><span data-stu-id="10899-105">It was once widely held that with scalable application architectures, performance could be addressed by simply moving primary components of the application to faster hardware.</span></span> <span data-ttu-id="10899-106">Questa operazione si è rivelata non vera.</span><span class="sxs-lookup"><span data-stu-id="10899-106">This has proven not to be true.</span></span> <span data-ttu-id="10899-107">I problemi di prestazioni non si verificano dalle prestazioni dei singoli componenti ma dai collegamenti che connettono i componenti.</span><span class="sxs-lookup"><span data-stu-id="10899-107">Performance problems arise not from individual component performance but from the links connecting components.</span></span>

<span data-ttu-id="10899-108">Il fattore principale per il successo è la posizione.</span><span class="sxs-lookup"><span data-stu-id="10899-108">The primary factor for success is location.</span></span> <span data-ttu-id="10899-109">La vicinanza o la posizione fisica, il tempo, la capacità e lo scopo sono aspetti distinti della località che si applicano alla distribuzione di un'applicazione COM+, che influiscono sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="10899-109">Proximity or physical location, time, capacity, and purpose are distinct aspects of location that apply to the deployment of a COM+ application, all of which affect performance.</span></span>

<span data-ttu-id="10899-110">Le prestazioni migliori si verificano quando i componenti e le risorse dell'applicazione vengono progettati e distribuiti in base alle richieste poste dal carico di lavoro dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="10899-110">The best performance comes when the application components and resources are designed and deployed to match the demands placed upon them by the application workload.</span></span>

<span data-ttu-id="10899-111">In generale, è consigliabile distribuire i componenti per ridurre al minimo le comunicazioni tra processi e in particolare tra computer e tra i componenti.</span><span class="sxs-lookup"><span data-stu-id="10899-111">In general, you should deploy components to minimize cross-process, and especially cross-computer, communication between components.</span></span> <span data-ttu-id="10899-112">Se la progettazione dell'applicazione è efficiente, le classi all'interno di un componente vengono raggruppate per utilizzo e funzione per ottimizzare le comunicazioni all'interno dei componenti.</span><span class="sxs-lookup"><span data-stu-id="10899-112">If your application design is efficient, classes within a component are grouped by use and function to maximize communications within components.</span></span> <span data-ttu-id="10899-113">Per la distribuzione dei componenti, è necessario assicurarsi che i componenti si trovino logicamente per utilizzare le relazioni tra i componenti e per ridurre la quantità di messaggi di messaggistica tra i componenti.</span><span class="sxs-lookup"><span data-stu-id="10899-113">In deploying components, you need to ensure that the components are logically located to make use of the relationships between the components and to reduce the amount of messaging between components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10899-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10899-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10899-115">Progettazione per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="10899-115">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> </dl>

 

 



