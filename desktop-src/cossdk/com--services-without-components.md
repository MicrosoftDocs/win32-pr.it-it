---
description: Servizi COM+ senza componenti
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Servizi COM+ senza componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127042"
---
# <a name="com-services-without-components"></a><span data-ttu-id="311ee-103">Servizi COM+ senza componenti</span><span class="sxs-lookup"><span data-stu-id="311ee-103">COM+ Services Without Components</span></span>

<span data-ttu-id="311ee-104">Con COM+ 1,5, è possibile utilizzare i servizi forniti da COM+ senza che sia necessario compilare un componente che contenga i metodi che chiamano tali servizi.</span><span class="sxs-lookup"><span data-stu-id="311ee-104">With COM+ 1.5, you can use the services provided by COM+ without needing to build a component to contain the methods that call those services.</span></span> <span data-ttu-id="311ee-105">Si tratta di un vantaggio molto vantaggioso per gli sviluppatori che in genere non utilizzano componenti, ma che desiderano utilizzare servizi COM+ quali transazioni o lo strumento di rilevamento COM+.</span><span class="sxs-lookup"><span data-stu-id="311ee-105">This greatly benefits developers who do not normally use components but want to use COM+ services such as transactions or the COM+ Tracker.</span></span> <span data-ttu-id="311ee-106">Utilizzando i servizi COM+ senza componenti, gli sviluppatori possono evitare il sovraccarico dovuto alla creazione di un componente utilizzato per accedere solo ai servizi COM+ necessari.</span><span class="sxs-lookup"><span data-stu-id="311ee-106">By using COM+ services without components, developers can avoid the overhead of creating a component that is used to access only the COM+ services they need.</span></span>

<span data-ttu-id="311ee-107">Gli ambienti di script, ad esempio, sono tradizionalmente gli utenti più grandi dei servizi COM+, ma non sono mai stati in grado di utilizzare i servizi in modo efficiente perché i servizi devono essere inclusi in un componente COM+.</span><span class="sxs-lookup"><span data-stu-id="311ee-107">For example, script environments traditionally have been the largest consumers of COM+ services but they were never able to use those services efficiently because the services needed to be bundled within a COM+ component.</span></span> <span data-ttu-id="311ee-108">Questo requisito di aggregazione aumenta i costi di prestazioni a causa dell'aumento delle comunicazioni e della duplicazione dei dati necessari per l'interazione dell'ambiente di script con il componente.</span><span class="sxs-lookup"><span data-stu-id="311ee-108">This bundling requirement increased performance costs because of the increased communication and duplication of data necessary for the scripting environment to interact with the component.</span></span> <span data-ttu-id="311ee-109">Usando i servizi senza componenti, questi costi sono ridotti al minimo.</span><span class="sxs-lookup"><span data-stu-id="311ee-109">By using services without components, such costs are minimized.</span></span>

<span data-ttu-id="311ee-110">Negli argomenti descritti nella tabella seguente vengono fornite informazioni di base e attività sull'utilizzo di servizi COM+ senza componenti.</span><span class="sxs-lookup"><span data-stu-id="311ee-110">The topics described in the following table provide background and task information about using COM+ services without components.</span></span> <span data-ttu-id="311ee-111">Questa funzionalità è destinata agli sviluppatori di Visual C++ avanzati che interessano le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="311ee-111">This feature is intended for advanced Visual C++ developers who are concerned about performance.</span></span>



| <span data-ttu-id="311ee-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="311ee-112">Topic</span></span>                                                                                                 | <span data-ttu-id="311ee-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="311ee-113">Description</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="311ee-114">Concetti relativi ai servizi COM+ senza componenti</span><span class="sxs-lookup"><span data-stu-id="311ee-114">COM+ Services Without Components Concepts</span></span>](com--services-without-components-concepts.md)<br/> | <span data-ttu-id="311ee-115">Viene fornita una panoramica dell'utilizzo dei servizi COM+ senza componenti.</span><span class="sxs-lookup"><span data-stu-id="311ee-115">Provides an overview of using COM+ services without components.</span></span><br/>                     |
| [<span data-ttu-id="311ee-116">Servizi COM+ senza attività componenti</span><span class="sxs-lookup"><span data-stu-id="311ee-116">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)<br/>       | <span data-ttu-id="311ee-117">Vengono fornite istruzioni per l'utilizzo di COM+ per la creazione e l'utilizzo di servizi senza componenti.</span><span class="sxs-lookup"><span data-stu-id="311ee-117">Provides instructions for using COM+ to create and use services without components.</span></span><br/> |



 

 

 




